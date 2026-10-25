#!/usr/bin/make -f
#
# make -h
# man make
# info make
# /usr/share/doc/make-doc/make.pdf.gz
# file:///usr/share/doc/make-doc/make.html/index.html
# file:///usr/share/doc/make-doc/make.html/Functions.html#File-Name-Functions
# file:///usr/share/doc/make-doc/make.html/Functions.html#Text-Functions
#
# http://ctan.org
# http://latex-project.org
# http://wikibooks.org/wiki/LaTeX
# http://wikibooks.org/wiki/LaTeX/Bibliography_Management
# http://wikibooks.org/wiki/LaTeX/Bibliographies_with_biblatex_and_biber
# http://www.ctan.org/tex-archive/info/bibtex/tamethebeast/ttb_en.pdf
# http://mirrors.ctan.org/macros/latex/contrib/biblatex/doc/biblatex.pdf
# http://mirrors.ctan.org/macros/latex/contrib/jurabib/docs/english/jbendoc.pdf
# http://mirrors.ctan.org/macros/latex/contrib/natbib/natbib.pdf
# http://wikipedia.org/wiki/Comparison_of_graphics_file_formats
# http://wikipedia.org/wiki/List_of_file_formats#Font_file
# http://ftp.math.utah.edu/pub/tex/doc/luamult.pdf
# http://wikipedia.org/wiki/PostScript_fonts
# http://wikipedia.org/wiki/Linux_Libertine
# http://wikipedia.org/wiki/GNU_FreeFont
# http://wikipedia.org/wiki/Unicode_font # This include license information
# http://wikipedia.org/wiki/GNU_Unifont
# http://wikipedia.org/wiki/Noto_fonts
# http://wikipedia.org/wiki/Typeface
# http://wikipedia.org/wiki/Unicode
# http://wikipedia.org/wiki/UTF-8
# http://wikipedia.org/wiki/List_of_CJK_fonts # Include license information
# http://wikipedia.org/wiki/List_of_typefaces
# http://wikipedia.org/wiki/Open-source_Unicode_typefaces # License information
# http://tex.stackexchange.com/questions/7770/file-extensions-related-to-latex-etc
# https://tug.org/FontCatalogue/mathfonts.html # Fonts with math support
#
# aux	AUXliary file for temporary data
# bcf	Biber Control File
# blg	Bibtex LoG file
# bbl	Bibtex BibLiography
# bbx	Biblatex Bibliography style eXtension?
# bib	BIBliography database file
# bst	Bibliography STyle file
# cbx	Citation style BibteX
# cfg	latex ConFiGuration file
# dvi	DeVice Independent file
# lbx	Language definition file BibteX
# idx	InDeX entrys
# ilg	makeIndex LoG
# ind	INDex file
# lat	spreadscheet calculator default extension for LATex export or csv2lat export file
# lof	List Of Figures
# log	latex LOG file
# out	Bookmark file
# pdf	Postscript Document File
# pfb	Postscript Font Binary
# run.xml logreq request file /usr/share/doc/texlive-doc/latex/logreq/README
# sc	Spreadsheet Calculator % \input(table)
# tex	TeX, LaTeX TEXt file
# toc	babel Table Of Content
# vf	tex Virtual Font data

# FontForge (fontforge) etc.
# abf   Adobe Binary screen Font
# afm   Adobe Font Metrics (afm2afm, afm2tfm)
# base	? TeX/Metafont/MetaPost file
# bdf   Bitmap Distribution Format
# bmf   ByteMap Font
# bin   Mac resource font
# brfnt Binary Revolution FoNT format
# cff	Compact Font Format container
# cfg   ConFiGuration ? (hbf2gf)
# cid   Collection/Character IDentifier - postscipt font
# cjk   Chinese Japanese Korean bitmap font
# dfont Mac resource font
# fond	FONt Description resource Mac 
# eps   Encapsulated PostScript
# fmt	Font MeTric
# fon   bitmepped FONt
# fontspec	
# gf    Generic Font (hbf2gf)
# hbf   Hanzi Bitmap Font/File (hbf2gf)
# hqx   Mac resource font
# mem	? tex/MEtafont/MEtapost Metrics? file
# mf    MetaFont (mktexmf)
# mgf   MicroGrafx Font
# ocp	Omega Compiled Process file
# ofm	Omega Font Metric
# otb	Open Type Bitmap font
# otc	Open Type Collection
# otf   Open Type Font (fontforge) http://wikipedia.org/wiki/OpenType
# pcf   Portable Compiled Font/Format (X11) bitmap 
# pfa   Printer Font Ascii adobe type 1
# pfb   Printer Font Binary adobe type 1
# pfm   Printer Font Metrics adobe type 1
# pgf	Portable Graphics Format
# pk    PacKed tex bitmap font (mktexpk, ttf2pk)
# pl    Property List (afm2pl)
# ps    PostScript
# pst	PostScript Trik macro file
# px	PC-Axis File Format file, Paradox
# sfd   Spline Font Database (fontforge)
# snf   Server Normal Font
# svg   Scaled Vector Graphics
# t1	adobe postscript font Type 1 http://wikipedia.org/wiki/PostScript_fonts#Type_1
# tdf	TheDraw Font
# tfm   Tex Font Metrics (mktextfm, afm2tfm)
# ttf   True Type Font (ttf2pk) http://wikipedia.org/wiki/TrueType
# ttc   True Type Collection http://wikipedia.org/wiki/TrueType
# ufo	Unified Font Object
# woff	Web Open Font Format
#
# Serching and using fonts:
# fc-list
# kpsewhich --help-formats --show-path=FMT
# info dvips
#   -bitmapfontenc strict
#   -j*  Download fonts partially
#   -V*  Send downloadable PS fonts as PK
#   -d32
# more /etc/texmf/web2c/texmf.cnf
# update-texmf
# Find out what original source "src" or s* files you have on directory and
# create needed temporary tmp or tm* files for typesetting program.
srtex = $(wildcard *.tex)
sjson = $(wildcard *.json)
srcsv = $(wildcard *.csv)
srcsc = $(wildcard *.sc)
tmcsv = $(patsubst %.json,%.csv,$(sjson))
tmpsc = $(patsubst %.csv,%.sc,$(tmcsv))
tmlat = $(patsubst %.sc,%.lat,$(tmpsc)$(srcsc))
tmtex = $(patsubst %.lat,%.tex,$(tmlat))

# Definitions:
DOC = fldbera
SUBM = fig
#LATEX = latex
#LATEX = xelatex
LATEX = lualatex
#LATEX = lualatex -output-format=dvi
#INTENT = latexintent
CURL = curl
#WGET = wget
#SSCONVERT = ssconvert
#SSCONVERT = ssconvert -I Gnumeric_stf:stf_csvtab -T Gnumeric_html:latex
#SSCSVTEX = $(SSCONVERT) -I Gnumeric_stf:stf_csvtab -T Gnumeric_html:latex
#STATFIFI = https://pxdata.stat.fi/PxWeb/api/v1/fi/StatFin/[pra,vaerak,...,]
#STATFIEN = https://pxdata.stat.fi/PxWeb/api/v1/en/StatFin/[pra,vaerak,...,]
STATFI = https://pxdata.stat.fi/PxWeb/api/v1/en/StatFin/
#jq
#mlr --j2c verb
CSV2SC = psc -k -d,
SC2LAT = echo "set tblstyle=latex\ntbl \"\"" | sc -q
CSV2LAT = csv2latex -n -p X
DOS2UNIX = dos2unix
SEDTABX = sed -e 's/{tabular}/{tabularx}/g' | sed -e 's/{tabularx}{/{tabularx}{\\textwidth}{/'
EDTABX = (echo ',s/{tabular}/{tabularx}/' && echo ',s/{tabularx}{/{tabularx}{\\textwidth}{/' && echo 'wq') | ed -s
#SEDTABX = sed -e 's/{tabular}/{tabularx}/g' | sed -e 's/{tabularx}{/{tabularx}{\\textwidth}{/' | sed -e 's/|[[:alpha:]]/|X/g'
#EDTABX = (echo ',s/{tabular}/{tabularx}/' && echo ',s/{tabularx}{/{tabularx}{\\textwidth}{/' && echo ',s/|[:alpha:]/|X/g' && echo 'wq') | ed -s
#BIBTEX = bibtex # nbibtex, bibtexu aux->bbl
BIBER = biber # bcf->bbl
CLEAN = lintex -o -k -v && rm -f clean all $(tmpsc) $(tmlat) $(tmtex) *.xml
DISTCLEAN = $(CLEAN) $(tmpcsv) *.blg
MAKEINDEX = makeindex
#LATEXMK = latexmk
#DVIPS = dvips -d-1 -bitmapfontenc strict -q -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -o
#/usr/share/texlive/texmf-dist
#/usr/share/texlive/texmf-dist/fonts/TYPE/MODE/SUPPLIER/TYPEFACE/dpiNNN
# ls -la ~/texmf ~/.texlive*
# info kpathsea
# man fmtutil.cnf
# man update-texmf
# man luaotfload-tool
#/etc/texmf/web2c/texmf.cnf
#/etc/texmf/web2c/mktex.cnf
#/usr/share/texmf/web2c/texmf.cnf
#/usr/share/texmf/web2c/fmtutil.cnf
#/usr/share/texlive/texmf-dist/web2c/texmf.cnf
#/usr/share/texlive/texmf-dist/web2c/fmtutil.cnf
#updmap -sys || updmap -user
#/var/lib/texmf/fonts/map/dvips/updmap/psfonts.map
#/var/lib/texmf/fonts/map/pdftex/updmap/pdftex.map
#https://library.psfc.mit.edu/publishing/fonts_epub/tex.html
#DVIPS = dvips -d32 -sDEVICE=pdfwrite -o
#DVIPS = dvips -d32 -bitmapfontenc strict -sDEVICE=pdfwrite -o
#PS2PDF = gs -q -P- -dSAFER -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -dPDFSETTINGS=/prepress -dEmbedAllFonts=true -sstdout=%stderr -sOutputFile=
#PS2PDF = gs -q -dSAFER -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -dPDFSETTINGS=/prepress -dEmbedAllFonts=true -sstdout=%stderr -sOutputFile=

# Clear suffixlist
.SUFFIXES:
# Add suffixrule supported suffix to suffixes list.
#.SUFFIXES: .sc .lat .pdf
.SUFFIXES: .json .csv .sc .lat
# Avoid implicit rule automatic temporary file deletion and next build reload.
#.SECONDARY:
#.INTERMEDIATE:
.PRECIOUS: %.csv %.tex
# Define implicit rule for added suffix:
#%.pdf: %.tex $(srtex) $(tmtex)
#	make -C $(SUBM)
#	$(LATEXMK) $< $@
%.csv: %.json
	echo "Query stat.fi data over the network!"
	#$(WGET) --post-file=$< -O $@ $(STATFI)$(subst _,/,$*)
	$(CURL) -d @$< -o $@ $(STATFI)$(subst _,/,$*)
	#$(WGET) --post-file=$< -O $@ $(STATFI)$*
	#$(CURL) -d @$< -o $@ $(STATFI)$*
	$(DOS2UNIX) $@
%.tex: %.csv
	$(CSV2LAT) $< | $(SEDTABX) > $@
	#$(CSV2LAT) $< > $@
	#$(EDTABX) $@
#%.sc: %.csv
#	cat $< | $(CSV2SC) > $@
#%.lat: %.sc
#	$(SC2LAT) $<
#%.tex: %.lat
#	cp $< $@

 Targets:
.PHONY: all
all: $(DOC).pdf

$(DOC).aux $(DOC).bcf $(DOC).idx : $(DOC).tex $(srtex) $(tmtex)
	make -C $(SUBM)
	$(LATEX) $(DOC).tex

#$(DOC).bbl : $(DOC).aux ; $(BIBTEX) $(DOC).aux

$(DOC).bbl : $(DOC).bcf ; $(BIBER) $(DOC).bcf

$(DOC).ind : $(DOC).idx ; $(MAKEINDEX) $(DOC).idx

$(DOC).pdf : $(DOC).bbl $(DOC).ind $(DOC).tex ; $(LATEX) $(DOC).tex

#$(DOC).dvi : $(DOC).bbl $(DOC).ind $(DOC).tex ; $(LATEX) $(DOC).tex

#$(DOC).ps : $(DOC).dvi ; $(DVIPS) $(DOC).ps $(DOC).dvi

#$(DOC).pdf : $(DOC).ps ; $(PS2PDF)$(DOC).pdf $(DOC).ps

# Clean : Remove temporary files.
.PHONY : clean distclean
clean :
	touch $(DOC).pdf
	mv -f $(DOC).pdf ..
	$(CLEAN)
	make -C $(SUBM) clean

distclean:
	$(DISTCLEAN)
	make -C $(SUBM) clean

