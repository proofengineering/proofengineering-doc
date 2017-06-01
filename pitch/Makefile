PAPER=main
PANDOC=pandoc
BIBLIOGRAPHY=references.bib

${PAPER}.pdf: ${PAPER}.tex
	pdflatex ${PAPER}.tex
	bibtex ${PAPER}
	pdflatex ${PAPER}.tex

${PAPER}.tex: ${PAPER}.md
	${PANDOC} -s -S ${PAPER}.md -o ${PAPER}.tex --bibliography ${BIBLIOGRAPHY} --natbib 

