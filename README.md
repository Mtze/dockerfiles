# latex-minted 

With this container latex files that include minted listings can be build.


Example for gitlab ci:

```yaml
compile_pdf:
  image: mtze/latex-minted
  script:
    - pdflatex -shell-escape thesis.tex
    - bibtex thesis
    - pdflatex -shell-escape thesis.tex
    - pdflatex -shell-escape thesis.tex
  artifacts:
    paths:
      - thesis.pdf
```





This project is basend on [aergus][gh].
[gh]: https://github.com/aergus/dockerfiles

