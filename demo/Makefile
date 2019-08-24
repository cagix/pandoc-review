
## Path to pandoc templates/includes

PREFIX    = ../



## Source file
## either defined here or given at cmd line like `make SRC=coolreview.md`

SRC   ?= review.md

PDF    = $(SRC:%.md=%.pdf)
TMP1   = __title.filled.tex
TMP2   = __grading.filled.tex



## Review options

PDFOPTIONS  = -f markdown --pdf-engine=pdflatex
PDFOPTIONS += -V documentclass=scrartcl
PDFOPTIONS += -V fontsize=11pt -V papersize=a4
PDFOPTIONS += -V geometry:left=2cm -V geometry:right=2cm -V geometry:top=2cm -V geometry:bottom=2.5cm
PDFOPTIONS += --include-in-header=${TMP1}
PDFOPTIONS += --include-after-body=${TMP2}



## Targets

all:	$(PDF)
pdf:	clean $(PDF)


$(PDF): $(SRC) ${PREFIX}/review_title.tex ${PREFIX}/review_grading.tex
	pandoc --standalone --template=${PREFIX}/review_title.tex -o ${TMP1} $<
	pandoc --standalone --template=${PREFIX}/review_grading.tex -o ${TMP2} $<
	pandoc ${PDFOPTIONS} -o $@ $<
	rm -f ${TMP1} ${TMP2}


clean:
	rm -f $(PDF) ${TMP1} ${TMP2}


.PHONY: all pdf clean




