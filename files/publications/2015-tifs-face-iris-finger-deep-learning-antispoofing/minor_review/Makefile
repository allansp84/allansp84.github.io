PAPER=2014-TIFS-dl-spoofing
FILES=$(shell find . -name '*.tex' -o -name '*.bib')

$(PAPER).pdf: $(FILES)
	pdflatex $(PAPER)

all: $(FILES)
	pdflatex $(PAPER)
	pdflatex $(PAPER)
	bibtex $(PAPER)
	bibtex $(PAPER)
	pdflatex $(PAPER)
	pdflatex $(PAPER)

view: $(PAPER).pdf
	open $^

clean:
	rm -vf *.{aux,log,blg,bbl,fls,synctex.gz,fdb_latexmk,dvi}
