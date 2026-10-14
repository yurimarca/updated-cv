# Yuri Pereira Marca — CV

LaTeX source for my curriculum vitae, maintained in English and Portuguese.

| Language   | Source            | PDF               |
|------------|-------------------|-------------------|
| English    | `en/CV-en.tex`    | [`en/CV-en.pdf`](en/CV-en.pdf) |
| Portuguese | `pt/CV-pt.tex`    | [`pt/CV-pt.pdf`](pt/CV-pt.pdf) |

## Building

Requires a TeX distribution with `pdflatex` (e.g. TeX Live). Packages used: `titlesec`, `marvosym`, `enumitem`, `hyperref`, `fancyhdr`, `needspace`, `ragged2e`, `setspace`, `fullpage`, `color`, `verbatim`, `latexsym`.

```bash
cd en && pdflatex CV-en.tex
cd pt && pdflatex CV-pt.tex
```

Run `pdflatex` a second time if links or layout look off after the first pass. Auxiliary files (`*.aux`, `*.out`, `*.log`, `*.gz`) are gitignored.

## Structure

Each `.tex` file is self-contained: the preamble defines all custom commands, followed by these sections:

1. Presentation Letter
2. Professional Experience
3. Education
4. Technical Expertise
5. Languages
6. Projects
7. Publications

### Custom commands

| Command | Purpose |
|---|---|
| `\resumeSubheading{org}{loc}{role}{dates}` | Job or education entry |
| `\resumeSubheadingAlt{org}{loc}{r1}{d1}{r2}{d2}` | Two roles at the same organization |
| `\resumeProject{name}{url}` | Project entry with a link |
| `\resumeItem{title}{desc}` | Bullet with bold title and colon |
| `\resumeItemAlt{title}{desc}` | Bullet with bold title, no colon (publications) |

## Updating

The two versions share the same layout and commands, so content or formatting changes should be mirrored in both `en/` and `pt/`. Rebuild and commit the PDFs alongside the `.tex` changes.
