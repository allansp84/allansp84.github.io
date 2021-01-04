PAPER=2018-crcpress-deep-learning-biometrics-copyright-notice

all: pdflatex reduce

pdflatex:
	pdftk 2018-crcpress-deep-learning-biometrics.pdf 2018-crcpress-deep-learning-biometrics-copyright-permission.pdf cat output 2018-crcpress-deep-learning-biometrics-copyright-notice.pdf

reduce:
	gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.5 -dNOPAUSE -dBATCH -sOutputFile=$(PAPER)-lite.pdf $(PAPER).pdf
	mv $(PAPER)-lite.pdf $(PAPER).pdf

cleanall: clean
	rm -f $(PAPER).pdf
	rm -f $(PAPER)-lite.pdf

