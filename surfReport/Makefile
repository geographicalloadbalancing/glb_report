pdf : surfReport.tex
	pdflatex surfReport.tex
	bibtex surfReport
	pdflatex surfReport.tex
	pdflatex surfReport.tex

display : pdf
	xdg-open surfReport.pdf

presentation_pdf : presentation.tex svg/nearestrouting.pdf svg/glbrouting.pdf
	pdflatex presentation.tex
	pdflatex presentation.tex

presentation_display : presentation_pdf
	xdg-open presentation.pdf

svg/%.pdf: svg/%.svg
	inkscape $< --export-pdf=$@
