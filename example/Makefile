TEX = .
LATEXMK_ARGS = -synctex=1 -interaction=nonstopmode -file-line-error -pdf --shell-escape -outdir=build
MAIN_TEX_FILE = main # without extension!

default: $(TEX)
	latexmk $(LATEXMK_ARGS) ${MAIN_TEX_FILE}.tex

force: $(TEX)
	latexmk $(LATEXMK_ARGS) ${MAIN_TEX_FILE}.tex -f

clean:
	latexmk -pdf -C -outdir=build
	rm build -rf
	find . -name "*.drawio.pdf" -delete
interactive: $(TEX)
	latexmk $(LATEXMK_ARGS) -pvc thesis.tex

glossaries:
	makeglossaries -d build ${MAIN_TEX_FILE}
