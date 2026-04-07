#####################################
#   Makefile for a LaTeX document   #
#####################################

# Name of the file can be overrided, e.g. "make DOC=proposal"

DOC =genesis21b

# Rules

.SUFFIXES: .tex .pdf
.tex.pdf:
	latexmk -pdf $<
#       /Users/karlin1/Library/TeXShop/bin/tslatexmk/latexmk -pdf $<

# Targets

default: pdf

pdf: ${DOC}.pdf
${DOC}.pdf: ${DOC}.tex *.tex

ar: ${DOC}.pdf
	acroread ${DOC}.pdf &

clean:
	rm -f *.log *.aux *.bak *.bbl *.blg *.brf *.toc *.out
	rm -f *.fls *.fdb_latexmk

distclean veryclean: clean
	rm -f *~ ${DOC}.pdf
