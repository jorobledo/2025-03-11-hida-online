NOTEBOOKS := $(wildcard *.ipynb)

# Replace .ipynb with .html
HTMLS := $(NOTEBOOKS:.ipynb=.html)

all: $(HTMLS)

# rule: .ipynb -> .html
%.html: %.ipynb
	jupyter nbconvert --to slides $<
	mv $*.slides.html $@

clean:
	rm -f $(HTMLS) *.slides.html

