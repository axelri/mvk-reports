LATEX?=xelatex
LATEXFLAGS+=-file-line-error

.PHONY: default latex distclean clean

default: report.pdf

report.pdf: report.tex config.tex title.tex
	rm -f *.aux # have to clean in order to switch engine
	$(LATEX) $(LATEXFLAGS) report

distclean: clean
	rm -f report.pdf

clean:
	rm -f *.log *.out *.aux *.toc
