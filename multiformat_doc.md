Dual formatting for R markdown output
================
Mik Black
22/06/2020

<!-- Run line below in R to render multiple documents: -->

<!-- rmarkdown::render("multiformat_doc.Rmd", output_format="all") -->

<!-- Run line below in R to render multiple documents: -->

<!-- rmarkdown::render("multiformat_doc.Rmd", output_format=c("html_document","word_document")) -->

<!-- rmarkdown::render("multiformat.Rmd", output_format=c("html_document", "github_document")) -->

<!-- NB: Knit just does first one (HTML), which overwrites the md file, and  -->

<!--     deletes the directory of plots etc -->

<!--     Also, using HTML as the output format, and choosing keep_md = true -->

<!--     generates markdown that doesn't render the YAML header properly on GitHub -->

## R Markdown

This is an R Markdown document. Markdown is a simple formatting syntax
for authoring HTML, PDF, and MS Word documents. For more details on
using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that
includes both content as well as the output of any embedded R code
chunks within the document. You can embed an R code chunk like this:

``` r
summary(cars)
```

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

## Including Plots

You can also embed plots, for example:

![](multiformat_doc_files/figure-gfm/pressure-1.png)<!-- -->

Note that the `echo = FALSE` parameter was added to the code chunk to
prevent printing of the R code that generated the plot.
