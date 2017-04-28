# docker-texlive-full
used for xelatex build with french greek and arabic lang (and probably others)

Thanks for inspiration to :
- https://github.com/thomasWeise/docker-texlive
- https://github.com/tianon/dockerfiles/tree/master/latex
- https://github.com/mattmahn/docker-latex

## Usage

### GitLab

Add a build job similar to the following to your `.gitlab-ci.yml`:
```yaml
compile_pdf:
  image: 1twitif/texlive-full
  script:
    - make report.pdf
  artifacts:
    paths:
      - report.pdf
```
of course, you have to write your latex makefile to automate your building sequence

`Makefile` exemples :
- http://geekographie.maieul.net/206
- https://danielkaes.wordpress.com/2009/03/14/compiling-latex-documents-using-makefiles/
- https://github.com/JasonHiebel/latex.makefile
- https://drewsilcock.co.uk/using-make-and-latexmk
- https://tex.stackexchange.com/questions/122241/makefile-that-prevents-tex-directory-from-being-cluttered-with-build-output
- https://tex.stackexchange.com/questions/40738/how-to-properly-make-a-latex-project
- http://geekographie.maieul.net/58
- http://geekographie.maieul.net/79
