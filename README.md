# Highway Protocol

[![License: CC BY-SA4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

Highway is a [correct-by-construction (CBC) Casper](https://github.com/cbc-casper/cbc-casper-paper)-based
consensus protocol. This paper contains the mathematical description of the protocol,
including its safety and liveness proofs.

## Generating PDF

A pre-generated version of the PDF can be found on the
[GitHub releases page](https://github.com/CasperLabs/highway/releases).
To generate the PDf yourself you must have
[LaTeX](https://www.latex-project.org/get/#tex-distributions) and
BibTex installed on your platform then run

```shell
pdflatex -halt-on-error highway && \
  bibtex highway && \
  pdflatex -halt-on-error highway && \
  pdflatex -halt-on-error highway
```

The output will be `highway.pdf`.

### Troubleshooting

If you see

```
! LaTeX Error: File `stix.sty' not found.
```

You may need to install additional parts of your LaTeX distribution (beyond the
base / recommended). E.g. if you are using `texlive` on Linux then you can try

```shell
sudo apt install texlive-fonts-extra
```
