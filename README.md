# My master's thesis at Charles University

## Build

For building, just go into `text/` subfolder and run `make`
command there. The main outcomes are `text/thesis.pdf` and
`text/abstract.pdf`.

The build depends on TeXLive and GNU Make system. With both
dependencies installed the build can trivially be performed
on any Linux-based system as well as on Windows Linux
Subsystem.

The electronic version of the thesis must conform to the
PDF/A-1a or PDF/A-2u standard (noted alongside requirements
on formatting of master theses amid Dean's directives
4/2019, 1/2015, and 7/2016, and the Rector's directive
72/2017). This project produces PDF/A-2u using the [pdfx
LaTeX package](https://www.ctan.org/tex-archive/macros/latex/contrib/pdfx).
Please note that many installations of TeX have this package
either obsolete or broken. So an advise is to download
the current version of the package and unpack it to
`./tex_deps/pdfx/`.


## Acknowledgements

The authors of the initial template on which this text
is based are

 - Martin Mareš <mj@ucw.cz> -- the current maintainer,
 - Arnošt Komárek <komarek@karlin.mff.cuni.cz>,
 - Michal Kulich <kulich@karlin.mff.cuni.cz>.
