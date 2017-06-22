# Minimal makefile for Doxygen documentation
#

## HINT: use make bg

# User variables
DOXYGENOPTS      =
DOXYGENFILE      = Doxyfile
DOXYGENBUILD     = doxygen
DOXYGENLOGFILE   = doxygen_output.log

# Put it first so that "make" without argument is like "make help".
help:
	@$(DOXYGENBUILD) --help

bg: 
	@$(DOXYGENBUILD) $(DOXYGENOPTS) $(O) > $(DOXYGENLOGFILE) 2>&1

.PHONY: help Makefile

# Catch-all target: route all unknown targets to Sphinx using the new
# "make mode" option.  $(O) is meant as a shortcut for $(SPHINXOPTS).
%: Makefile
	@$(DOXYGENBUILD) $@ $(DOXYGENOPTS) $(O)

