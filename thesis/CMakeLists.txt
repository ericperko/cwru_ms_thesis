cmake_minimum_required(VERSION 2.8.0)
project(Thesis NONE)

set(LATEX_CHAPTER_SOURCES
	title.tex
	committee_approval_sheet.tex
	acknowledgements.tex
	abstract.tex
	chapter0.tex
	chapter1.tex
	chapter2.tex
	chapter3.tex
	chapter4.tex
	chapter5.tex
	chapter6.tex
	introduction.tex
	conclusion.tex
	future_work.tex
	)

include(UseLATEX.cmake)
add_latex_document(thesis.tex
	INPUTS ${LATEX_CHAPTER_SOURCES}
	BIBFILES bibliography.bib
	IMAGE_DIRS images
	)
