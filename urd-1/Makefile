LATEX?=pdflatex
BIBTEX?=biber
LATEXFLAGS+=-file-line-error
FORCEFLAGS?=-halt-on-error

.PHONY: default distclean clean

default: report.pdf

report.pdf: *.tex clean
	$(LATEX) $(FORCEFLAGS) report && $(BIBTEX) report && $(LATEX) $(FORCEFLAGS) report

distclean: clean
	rm -f report.pdf

clean:
	rm -f *.log *.out *.aux *.toc *.bbl *.bcf *.blg *.xml
