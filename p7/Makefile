.PHONY: report.pdf all clean

all: report.pdf

report.pdf: report.tex
	latexmk -pdf -pdflatex="pdflatex -interaction=nonstopmode" -use-make report.tex
	cp report.tex /var/www/html/dumped/udacity-p7
	cp report.pdf /var/www/html/dumped/udacity-p7

clean:
	latexmk -CA
