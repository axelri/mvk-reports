LATEX?=xelatex
LATEXFLAGS+=-file-line-error

.PHONY: default force distclean clean

default: report.pdf

report.pdf: *.tex
	$(LATEX) $(LATEXFLAGS) report

force: clean
	$(LATEX) $(LATEXFLAGS) report && $(LATEX) $(LATEXFLAGS) report && $(LATEX) $(LATEXFLAGS) report

distclean: clean
	rm -f report.pdf

clean:
	rm -f *.log *.out *.aux *.toc
