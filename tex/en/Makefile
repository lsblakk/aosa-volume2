LATEX = pdflatex
BIBTEX = bibtex

CHAPTERS = \
	intro \
	aderby \
	gdb \
	ghc \
	gpsd \
	inkscape \
	ironlang \
	itk \
	jquery \
	k9mail \
	mailman \
	openmpi \
	parrot \
	pjs \
	pypy \
	sqlalchemy \
	yesod \
	colophon

SRC=$(foreach name,${CHAPTERS},${name}.tex)

all : aosa2.pdf

aosa2.pdf : aosa2.tex aosa2.bib ${SRC}
	${LATEX} aosa2
	${BIBTEX} aosa2
	${LATEX} aosa2
	${LATEX} aosa2

questions:
	@(for i in *.tex; do echo `fgrep aosaquestion $$i | wc -l` $$i; done) | sort -n -r

clean:
	@rm -f *.aux *.bak *.bbl *.blg *.log *.toc *~
