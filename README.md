# MiniBaz2020 - HackMD / R Markdown

**Monday 22 June 2020 - 2-4pm**<BR>
**Mik Black, Department of Biochemsitry**

## Overview

This session will focus on the use of Markdown-based document creation.

We will start by introducing Markdown (a basic text-based document-creation language) 
in the context of creating reproducible research documents in R.

But first, let's take a look at a simple document written in markdown:

 * [markdownFile.md](https://github.com/mikblack/MiniBaz2020-HackMD/blob/master/markdownFile.md)

On GitHub, this file is "rendered" as a formated file.

If you click on the "Raw" button, you will see that it is just a text file,
written in Markdown.

## Part One: R Markdown

To learn about using R markdown, we're going to use part of the Software Carpentry 
*R for Reproducible Scientific Analysis* workshop - "Producing Reports With knitr":

https://swcarpentry.github.io/r-novice-gapminder/15-knitr-markdown/index.html

### Some other cool things

#### Output formats

 - The default output for R markdown is HTML (`html_document`) 
 - This can be altered in the header by altering the `output:` setting.  
   Other formats include:
    - `word_document`
    - `github_document` (docuemnts that renders on the github website)
    - `pdf_document` (requires LaTeX installed...)

Examples:

 - `github_document`
    - R markdown file: [github_doc_format.Rmd](https://github.com/mikblack/MiniBaz2020-HackMD/blob/master/github_doc_format.Rmd)
    - Output (on GitHub): [github_doc_format.md](https://github.com/mikblack/MiniBaz2020-HackMD/blob/master/github_doc_format.md)
 - `html_document` (same as default)
     - R markdown file: [github_html.Rmd](https://github.com/mikblack/MiniBaz2020-HackMD/blob/master/github_html.Rmd)
     - Output (on GitHub): [github_html.html](https://github.com/mikblack/MiniBaz2020-HackMD/blob/master/github_html.html)
 - Note the difference in how the output is rendered on GitHub
     - Github markdown format is great for displaying online
     - HTML is great for sending to collaborators

> #### Challenge
> - Use your R markdown file to create a Word document

#### Multiple output formats
 
 - The same `.Rmd` file can be used to generate multiple output formats
 - Specified in the YAML header:
```
title: "Multiple formatting for R markdown output"
author: "Mik Black"
date: "22/06/2020"
output: 
  html_document: default
  github_document: default
  word_document: default
```
 - To generate all of the specified formats, use the `render` command from the `knitr` package:
```
rmarkdown::render("multiformat_doc.Rmd", output_format="all")
```
 - You can also just generate a subset of documents (e.g., HTML and Word):
```
rmarkdown::render("multiformat_doc.Rmd", output_format=c("html_document","word_document")) 
```
 - Multiformat R markdown file: [multiformat_doc.Rmd](https://github.com/mikblack/MiniBaz2020-HackMD/blob/master/multiformat_doc.Rmd)

> #### Challenge
> - Alter your R markdown file so that it produces multiple output formats

#### Presentations

 - It is also possible to create presentations using R markdown
 - Rendered as HTML5 (allows browser-based presentation)
 - Each heading (#'s) creates a new slide

> #### Challenge
> - Create a new R markdown document in R Studio, and choose "Presentation" (just use the defailt ioslides format).
> - Knit the document, and step through the slides
> - Add some extra slides to the presentation

### A few other thoughts:

Benefits of (R) markdown: 

 - text-based format (and easy to read)
 - easy to create nicely formatted documents
 - allows you to focus on content, rather than formatting
 - highly portable (e.g., cross-platform)
 - easy for version control (can see exactly which text has changed)

## Part Two: HackMD

While R markdown (or even just straight markdown - you can use "Preview HTML" in RStudio
to render a Markdown document to HTML - it doesn't have to contain R code) is awesome for
creating great looking documents, it doesn't solve the need for *collaborative document editing*.
For this, many people use something like Google Docs or Office 365.

HackMD provides a markdown-based platform for collaboration document editing:

https://hackmd.io/

It is a commercial platform, but provides a free access tier (a subscription provides
additional benefits):

https://hackmd.io/pricing#

### Some important points

 - HackMD provides the ability to edit markdown-based documents collaboratively
 - These documents can be public (open access) or private (restricted access)
 - Edit and access permissions can be different for different people (similar to Google Docs)
 - This is a commercial cloud-based service provider: there will be some things that shouldn't be stored on here (e.g., patient information from clinical studies).

### Signing up for HackMD

Signin via:

 - create account on HackMD
 - GitHub 
 - Dropbox 
 - Facebook
 - Twitter
 - Google


