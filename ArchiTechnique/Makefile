TARGET=ArchiTech.pdf
INCLUDES=Introduction.tex Objectifs.tex Logiciel.tex Materiel.tex
ASSETS=archi_materiel.png
TEXFILE=ArchiTech.tex
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
