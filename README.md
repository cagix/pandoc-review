Pandoc Markdown review template
===============================

This project defines a skeleton repo for creating reviews for bachelor thesis
or master thesis out of [Pandoc Markdown](https://pandoc.org/MANUAL.html) using
a single source approach.


History
-------

Like in the [pandoc lecture project](https://github.com/cagix/pandoc-lecture),
the task of creating reviews for bachelor and master thesis can be simplified
by using [Pandoc Markdown](https://pandoc.org/MANUAL.html).

Since LaTeX is currently used as back end, all TeX macros can be used.


Installing and running
----------------------

1.  If you have not already done so, install:

    *   [git](https://git-scm.com/)
    *   [make](https://www.gnu.org/software/make/)
    *   [pandoc](https://pandoc.org/installing.html) 2.7.3 (or newer)
    *   [TeX Live](https://www.tug.org/texlive/)

2.  Create a working directory for your project and change into it.

3.  Clone this repo using `git clone https://github.com/cagix/pandoc-review review`.

5.  Change to the `demo/` subdirectory. Adapt the `DATADIR` variable in the
    makefile: It should point to the working directory of the project, i.e. to
    the folder containing the two templates `review_title.tex` and
    `review_grading.tex`.

    Build the demo using `make`.

    Have a look at the example `demo/review.md`. In the yaml header of this
    document you can define title and author of the thesis as well as the kind
    (bachelor, master) and the grading. You also need to adapt your (the
    reviewers) name and affiliation.


Notes and Versions
------------------

This project is supposed to be used with pandoc 2.7.3.


---

License
-------

Copyright (c) 2016-2021, Carsten Gips

[MIT licensed](http://opensource.org/licenses/MIT)

