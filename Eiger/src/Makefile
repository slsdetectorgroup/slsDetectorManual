DESTDIR?=../
TEX=latex


MAINTEXS= Eiger_short.tex

PDFS = $(MAINTEXS:.tex=.pdf)

all: pdf 

pdf: $(PDFS)
	mv $(PDFS) $(DESTDIR)	
	

%.dvi : %.tex
	latex $<
	latex $<

%.ps : %.dvi
	dvips -o $@  $< 


%.pdf : %.ps
	ps2pdf  $<  $@


clean:
	echo "cleaning for manual-client"
	rm -rf *.aux *.log *.toc *.out $(DVIS) $(PSS) $(PDFS) 

