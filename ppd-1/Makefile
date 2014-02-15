LATEX?=pdflatex
BIBTEX?=biber
LATEXFLAGS+=-file-line-error
FORCEFLAGS?=-halt-on-error

.PHONY: default force distclean clean

default: report.pdf

report.pdf: *.tex catalog.pdf metafam.pdf
	$(LATEX) $(LATEXFLAGS) report

force: clean
	$(LATEX) $(FORCEFLAGS) report && $(BIBTEX) report && $(LATEX) $(FORCEFLAGS) report && $(LATEX) $(FORCEFLAGS) report

distclean: clean
	rm -f report.pdf

clean:
	rm -f *.log *.out *.aux *.toc
