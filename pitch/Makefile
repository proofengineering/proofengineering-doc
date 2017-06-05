PAPER=main
PANDOC=pandoc
BIBLIOGRAPHY=references.bib

${PAPER}.pdf: ${PAPER}.tex
	latex ${PAPER}
	bibtex ${PAPER}
	latex ${PAPER}
	pdflatex ${PAPER}

${PAPER}.tex: ${PAPER}.md
	${PANDOC} -s -S ${PAPER}.md -o ${PAPER}.tex --bibliography ${BIBLIOGRAPHY} --natbib 

