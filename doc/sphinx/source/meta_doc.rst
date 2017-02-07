Meta Documentation
==================
This is a meta documentation document, where different trials are described, for documenting this project.

Generic Docs
------------
Docs that could be applied to any project, 
this is a direct copy from this `gist <https://gist.github.com/Walid-Shouman/6a214cdf2e4ce14dae9240079fe13e66>`__, and could be removed later.

Restructured Text Understanding
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Following are different ways that I used to get along with the restructured text formatting. 

* Use markdown to restructured text *converter*, like `pandoc <https://pandoc.org/try/>`__.
* Use a reference `restructured text file <https://docs.python.org/2.7/whatsnew/2.7.html>`__, alongside with it's `source file <https://docs.python.org/2.7/_sources/whatsnew/2.7.txt>`__.
* Use a formal restructured text *documentation*, like `docutils <http://docutils.sourceforge.net/FAQ.html>`__

Code Block Usage Notes
~~~~~~~~~~~~~~~~~~~~~~
Notes: If you are looking at the source code now

::

   Using double colons, 2 newlines, and an indented block means reserve the indented block,
   to copy this block from the rawfile, don't forget un-indenting it B-)

::

  Indentation when using double colons(::) separated from it's previous line with 2 newlines
  is much more cleaner than using the :: compactly just at the end of line

Tips
~~~~
* toctree: needs filenames after it, no need for the extension to be mentioned.
  I think it gets guessed based on the ``source_suffix`` in ``conf.py``.

TagainiJisho Docs
-----------------
Docs that target this specific project

Reusable Elements
~~~~~~~~~~~~~~~~~
* De-block the following directive to get the full documentation of AsyncQuery.h at once::

  .. doxygenfile:: ASyncQuery.h


Investigation TODOs
~~~~~~~~~~~~~~~~~~~
* This one doesn't work If I correctly remember::

   .. automodule:: tagainijisho
      :members:
      :undoc-members:
      :show-inheritance:

* autodoxygenfile - Does Not Work: due to an error in: retrieve_project_info_for_auto

::

  .. autodoxygenfile:: ASyncQuery.h

* doxygenindex - Almost Works: *tagainijisho* is found in the breathe projects dictionary, 
  however doxygenindex wouldn't work automatically, due to an error in sphinxrenderer. 
  We workaround that error by modifying sphinxrenderer.py:line935 and use [0][0] instead of [1][0]

::

  .. doxygenindex::
    :project: tagainijisho
    :path: .
    :outline:
    :no-link:
