SOURCE = presentation.md
HTML = presentation.html
PDF = presentation.pdf

all: $(HTML) $(PDF)

$(HTML): $(SOURCE)
	quarto render "$(SOURCE)" --to revealjs
	cp _output/$(HTML) "$(HTML)"

$(PDF): $(SOURCE)
	quarto render "$(SOURCE)" --to typst --output "$(PDF)"
	cp _output/$(PDF) "$(PDF)"

clean:
	rm -f $(HTML) $(PDF)
	rm -rf _output

cleanall: clean
	rm -rf .quarto