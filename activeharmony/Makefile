all_subsystems = build example/client_api example/constraint example/code_generation example/synth

.PHONY: all install clean distclean

all install clean distclean:
	+@for subsystem in $(all_subsystems); do \
	    $(MAKE) -C $$subsystem $@;           \
	    RETVAL=$$?;                          \
	    if [ $$RETVAL != 0 ]; then           \
		exit $$RETVAL;                   \
	    fi;                                  \
	done
