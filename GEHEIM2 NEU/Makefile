all: build/vortrag.pdf

texoptions = \
	     --lualatex \
	     --interaction=nonstopmode \
	     --halt-on-error \
	     --output-directory=build \

build/vortrag.pdf: FORCE | build
	latexmk $(texoptions) vortrag.tex

preview: FORCE | build
	latexmk $(texoptions) vortrag.tex

FORCE:

build:
	mkdir -p build

clean:
	rm -r build
