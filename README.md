# aamixsh.github.io

Personal site of Aayush Mishra. Plain static HTML: no build step. The only JavaScript is the light/dark toggle and the footer's "last updated" date, which comes from the deploy time GitHub Pages reports.

- `index.html`: the whole site (styles are inline in `<style>`)
- `files/cv.tex`: CV source → `files/CV.pdf`
- `files/`: CV and the degree/transcript PDFs it links to
- `images/`: photo, publication thumbnails, and organization logos
- Older files and the previous Jekyll site live on the `legacy` branch

## Update the CV

```bash
cd files && pdflatex cv.tex && rm -f cv.aux cv.log cv.out
```

Use `\job[logo]{Org}{Role}{Location}{Dates}` for an experience entry and `\pub{Title}{Authors}{Venue}{Year}` for a publication. Organization logos come from `images/logos/` (via `\graphicspath{{../images/logos/}}`), so build from `files/` or keep that folder layout on Overleaf. The font is IBM Plex Sans (`plex-sans`), which ships with Overleaf and full TeX Live; on BasicTeX, install it with `tlmgr --usermode install plex fontaxes mweights xkeyval`.

## Preview locally

```bash
python3 -m http.server 8000
```
