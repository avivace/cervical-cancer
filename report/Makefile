SVGFILES := $(shell find . -name '*.svg')

pdf: svg
	bibtex report
	pdflatex report
	bibtex report
	pdflatex report
	bibtex report

.PHONY: ${SVGFILES}
${SVGFILES}: ; inkscape $@ --export-type=pdf

.PHONY: svg
svg: ${SVGFILES}
	echo SVG converted