PAPER=2015-tip-face-spoofing-temporal-cubes-copyright-notice

all: pdflatex reduce

pdflatex:
	pdflatex $(PAPER)

reduce:
	gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.5 -dNOPAUSE -dBATCH -sOutputFile=$(PAPER)-lite.pdf $(PAPER).pdf
	mv $(PAPER)-lite.pdf $(PAPER).pdf

clean: 
	rm -f *.dvi *.log *.toc *.aux *.bbl *.blg *.loa *.los *.out *.cb  *.synctex.gz

cleanall: clean
	rm -f $(PAPER).pdf
	rm -f $(PAPER)-lite.pdf

