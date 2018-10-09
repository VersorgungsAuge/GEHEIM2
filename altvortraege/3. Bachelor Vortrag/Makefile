all: build/Presentation.pdf

texoptions = \
	     --lualatex \
	     --interaction=nonstopmode \
	     --halt-on-error \
	     --output-directory=build

build/Presentation.pdf: FORCE | build
	latexmk $(texoptions) Presentation.tex

preview: FORCE | build
	latexmk $(texoptions) -pvc Presentation.tex

FORCE:

build:
	mkdir -p build

clean:
	rm -r build
