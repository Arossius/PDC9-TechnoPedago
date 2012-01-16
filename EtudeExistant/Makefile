TARGET=Existant.pdf
INCLUDES=Introduction.tex Analyse.tex
ASSETS=
TEXFILE=Existant.tex
CC=pdflatex -halt-on-error

all: $(TARGET)

clean: cleantmp
	rm -f $(TARGET) *.toc *.ind *.dvi

cleantmp:
	rm -f *.log *.out *.aux *.ilg

$(TARGET): $(TEXFILE) $(INCLUDES) $(ASSETS)
#Once for toc, hyper-refs, etc, and once for good
	$(CC) $(TEXFILE)
	$(CC) $(TEXFILE)
