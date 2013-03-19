all : report presentation

report : surfReport.tex $(patsubst %.eps,%.pdf,$(wildcard eps/*.eps))
	pdflatex surfReport.tex
	bibtex surfReport
	pdflatex surfReport.tex
	pdflatex surfReport.tex
	bash -c 'rm --force --verbose -- surfReport{.aux,.bbl,.blg,.log,-blx.bib,.bcf,.run.xml,.out}'


report_display : report
	xdg-open surfReport.pdf

presentation : presentation.tex svg/nearestrouting.pdf svg/glbrouting.pdf
	pdflatex presentation.tex
	pdflatex presentation.tex

presentation_display : presentation
	xdg-open presentation.pdf

# Convert images to PDF so that pdflatex can use them
svg/%.pdf : svg/%.svg
	inkscape $< --export-pdf=$@
eps/%.pdf : eps/%.eps
	epstopdf $< --outfile=$@
