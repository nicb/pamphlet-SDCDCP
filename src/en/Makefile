TARGET=sdcdcp-text.pdf
LATEX=pdflatex
BIBTEX=bibtex8

all: $(TARGET)

clean:
	$(RM) $(TARGET) *.aux *.out *.log *.bbl *.blg

.PHONY: clean

.SUFFIXES: .pdf .tex

%.pdf: %.tex
	$(LATEX) $<
	$(RM) $(TARGET)
	-$(BIBTEX) $*
	$(LATEX) $<
	$(RM) $(TARGET)
	$(LATEX) $<
