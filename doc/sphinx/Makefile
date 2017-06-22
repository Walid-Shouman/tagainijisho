# Minimal makefile for Sphinx documentation
#

## HINT: use make bg

# You can set these variables from the command line.
SPHINXOPTS    =
SPHINXBUILD   = sphinx-build
SPHINXPROJ    = tagaini-jisho
SOURCEDIR     = source
BUILDDIR      = build
SPHINXLOGFILE = sphinx_output.log

# Put it first so that "make" without argument is like "make help".
help:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

bg: 
	@$(SPHINXBUILD) "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O) > $(SPHINXLOGFILE) 2>&1

.PHONY: help Makefile

# Catch-all target: route all unknown targets to Sphinx using the new
# "make mode" option.  $(O) is meant as a shortcut for $(SPHINXOPTS).
# 'TODO: sanity check if ../doxygen/xml dir is found or not. ie: docs got generated previously or not'
%: Makefile
	echo $(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)
	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)
