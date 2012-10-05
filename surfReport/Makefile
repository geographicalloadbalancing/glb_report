pdf : surfReport.tex
	pdflatex surfReport.tex
	bibtex surfReport
	pdflatex surfReport.tex
	pdflatex surfReport.tex

display : pdf
	xdg-open surfReport.pdf

presentation_pdf : presentation.tex
	pdflatex presentation.tex
	pdflatex presentation.tex

presentation_display : presentation_pdf
	xdg-open presentation.pdf