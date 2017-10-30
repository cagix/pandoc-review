Pandoc Markdown review template
===============================

This project defines a skeleton repo for creating reviews for bachelor thesis
or master thesis out of [Pandoc Markdown](http://pandoc.org/MANUAL.html) using
a single source approach.


History
-------

Like in he [pandoc lecture project](https://github.com/cagix/pandoc-lecture),
the [pandoc homework project](https://github.com/cagix/pandoc-homework), and
the [pandoc exam project](https://github.com/cagix/pandoc-exam) the
task of creating reviews for bachelor and master thesis can be simplified as
well using [Pandoc Markdown](http://pandoc.org/MANUAL.html).

Since LaTeX is still used as back end, all TeX macros could be used.


Installing and running
----------------------

1.  If you have not already done so, install:

    *   [git](https://git-scm.com/)
    *   [make](https://www.gnu.org/software/make/)
    *   [pandoc](http://pandoc.org/installing.html) 1.17.2 (or newer)
    *   [pandoc templates](https://github.com/jgm/pandoc-templates) 1.17.2 (or newer)
    *   [TeX Live](http://www.tug.org/texlive/)

2.  Create a working directory for your project and change into it.

3.  Clone the pandoc templates repo using `git clone https://github.com/jgm/pandoc-templates templates`.

4.  Clone this repo using `git clone https://github.com/cagix/pandoc-review review`.

5.  Change to the `review/` subdirectory. Adapt the `DATADIR` variable in the
    makefile: It should point to the working directory of the project, i.e. to
    the folder containing the two subfolders `templates` and `review`.

    Build the demo using `make`.

    Have a look at the example `review/demo/review.md`. In the yaml header of
    this document you have to define the title and the author of the thesis as
    well as the kind of theses (bachelor, master) and the grade.

    The definitions and includes of TeX packages are done in `review_title.tex`.
    The "title page" is also defined in this file, thus you should replace the
    line `\centerline{UNIVERSITY, DEPARTMENT, REVIEWER}` using your address.

    In `review_grading.tex` you will find the closing remark using the grade
    as defined in the yaml header. You need to change the lines
    `LOCATION, $date$\newline REVIEWER\newline` to your needs.


Notes and Versions
------------------

This project is supposed to be used with pandoc 1.19.x.


---

License
-------

Copyright (c) 2016-2017, Carsten Gips

[MIT licensed](http://opensource.org/licenses/MIT)


