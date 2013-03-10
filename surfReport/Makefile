all : report presentation

report : surfReport.tex
	pdflatex surfReport.tex
	bibtex surfReport
	pdflatex surfReport.tex
	pdflatex surfReport.tex
	bash -c 'rm surfReport{.aux,.bbl,.blg,.log,-blx.bib,.bcf,.run.xml}'


report_display : report
	xdg-open surfReport.pdf

presentation : presentation.tex svg/nearestrouting.pdf svg/glbrouting.pdf
	pdflatex presentation.tex
	pdflatex presentation.tex

presentation_display : presentation
	xdg-open presentation.pdf

# Convert SVGs to PDF so that pdflatex can use them
svg/%.pdf: svg/%.svg
	inkscape $< --export-pdf=$@
