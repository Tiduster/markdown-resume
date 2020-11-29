# markdown-resume
The simplest possible resume workflow from markdown source.

Changing the content or styling of a resume or CV is a relatively common event that can be a frustrating, time-consuming hassle. This repo contains starter files for the simplest possible workflow where resume *content* is maintained in a simple markdown file and generating `.html`, `.pdf` and `.docx` output formats can be automated with two tools: `pandoc` and `wkhtmltopdf`. 

```
pandoc -s -o resume.html -c resume-css-stylesheet.css resume.md
sed -i '19 a<img src=\"picture.jpg\"/>' resume.html
wkhtmltopdf --enable-local-file-access resume.html resume.pdf
```
