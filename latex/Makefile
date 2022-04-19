RUBBER_INSTALLED := $(shell command -v rubber 2>/dev/null)

MAIN_TEX = glt_2022_infinisim

all: $(MAIN_TEX).tex
ifdef RUBBER_INSTALLED
	rubber -d $<
else

	pdflatex $(MAIN_TEX).tex
	#bibtex $(MAIN_TEX)
	#pdflatex $(MAIN_TEX).tex
	pdflatex $(MAIN_TEX).tex
	@echo "=============================="
	@echo "= consider installing rubber ="	
	@echo "=============================="
endif

clean:
	rm -f *.aux
	rm -f *.log
	rm -f *.pdf
	rm -f *.nav
	rm -f *.out
	rm -f *.snm
	rm -f *.toc
	rm -f *.bbl
	rm -f *.blg
	rm -f *.lof
	rm -f *.idx
	rm -f *.ilg
	rm -f *.ind
	rm -f *.vrb
	rm -f *.rubbercache

.PHONY: all
.PHONY: clean
