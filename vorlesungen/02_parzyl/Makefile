#
# Makefile -- parzyl
#
# (c) 2017 Prof Dr Andreas Müller, Hochschule Rapperswil
#
all:	parzyl-handout.pdf MathSem-02-parzyl.pdf

include ../slides/Makefile.inc

SOURCES = common.tex slides.tex $(slides)

MathSem-02-parzyl.pdf:	MathSem-02-parzyl.tex $(SOURCES)
	pdflatex MathSem-02-parzyl.tex

parzyl-handout.pdf:	parzyl-handout.tex $(SOURCES)
	pdflatex parzyl-handout.tex

thumbnail:	thumbnail.jpg # fix1.jpg

thumbnail.pdf:	MathSem-02-parzyl.pdf
	pdfjam --outfile thumbnail.pdf --papersize '{16cm,9cm}' \
		MathSem-02-parzyl.pdf 1
thumbnail.jpg:	thumbnail.pdf
	convert -density 300 thumbnail.pdf \
                -resize 1920x1080 -units PixelsPerInch thumbnail.jpg

fix1.pdf:	MathSem-02-parzyl.pdf
	pdfjam --outfile fix1.pdf --papersize '{16cm,9cm}' \
		MathSem-02-parzyl.pdf 1
fix1.jpg:	fix1.pdf
	convert -density 300 fix1.pdf \
                -resize 1920x1080 -units PixelsPerInch fix1.jpg

