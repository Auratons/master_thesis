OUTS = *.log *.dvi *.aux *.toc *.lof *.lot *.out *.bbl *.blg *.xmpi
OUTS_DIR = outs
# Into this folder, other packages can be downloaded.
export TEXINPUTS = ../tex_deps//:

all: restore_outs thesis.pdf abstract_en.pdf abstract_cs.pdf hide_outs

# Exit 0 here is for case when nothing is present in OUTS_DIR,
# which makes `mv` fail and `make` then as well.
restore_outs:
	mkdir --parents $(OUTS_DIR)
	mv $(OUTS_DIR)/* . 2>/dev/null || exit 0

# LaTeX must be run multiple times to get references right.
thesis.pdf: thesis.tex $(wildcard *.tex) bibliography.bib thesis.xmpdata
	pdflatex $<
	bibtex thesis
	pdflatex $<
	pdflatex $<

abstract_en.pdf: abstract_en.tex abstract_en.xmpdata
	pdflatex $<
	pdflatex $<

abstract_cs.pdf: abstract_cs.tex abstract_cs.xmpdata
	pdflatex $<
	pdflatex $<

# Exit 0 here is for case when some file type is not present,
# which makes `mv` fail and `make` then as well.
hide_outs:
	mv $(OUTS) $(OUTS_DIR) 2>/dev/null || exit 0

clean:
	rm -f  $(OUTS)
	rm -fr $(OUTS_DIR)
	rm -f  thesis.pdf abstract_en.pdf abstract_cs.pdf
