# aamixsh.github.io

Personal site of Aayush Mishra. Plain static HTML: no build step, no JavaScript.

- `index.html`: the whole site (styles are inline in `<style>`)
- `files/cv.tex`: CV source → `files/CV.pdf`
- `files/`: CV, transcripts, and reports linked from the site and CV

## Update the CV

```bash
cd files && pdflatex cv.tex && rm -f cv.aux cv.log cv.out
```

Use `\job{Org}{Role}{Location}{Dates}` for an experience entry and `\pub{Title}{Authors}{Venue}{Year}` for a publication. The file uses Source Sans (`sourcesanspro`), which ships with Overleaf and full TeX Live. On BasicTeX, install it with `tlmgr --usermode install sourcesans ly1 fontaxes mweights`.

## Preview locally

```bash
python3 -m http.server 8000
```
