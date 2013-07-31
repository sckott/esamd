---
title       : Reproducible Research and Collaboration
subtitle    : Markdown and knitr
author      : Scott Chamberlain & Karthik Ram
date        : 2013-08-05
job         : 
logo        : "ropensci_small.png"
biglogo     : "ropensci_main.png"
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
assets      :
  css: "http://netdna.bootstrapcdn.com/font-awesome/3.2.1/css/font-awesome.css"
---

## What you'll learn

### Markdown 
+ A stupidly simple language for writing.

### knitr
+ A simple way to write reproducible documents including R code blocks and text.

---

## What is Markdown?

> ### Markdown is a text-to-HTML conversion tool for ~~web writers~~. Markdown allows you to write using an easy-to-read, easy-to-write plain text format, then convert it to ~~structurally valid XHTML (or HTML)~~ other file formats.

<br><br><br>

from [the Markdown site](http://daringfireball.net/projects/markdown/)

---

## Markdown use cases

### Taking notes
### Blog posts
### Research papers
### Conversing on the web

---

## Throw away Word and pick up MD

| Markdown            | Word          | 
| ------------- |:-------------:|
| Super simple to learn - The syntax is dead simple      | Simple, okay, i'll give you that |
| Widely supported on the web (StackOverflow, GitHub, pandoc, static webpages, etc..)      | Not supported on the web      |
| Versioning? Can at least partly due as it's plain text | Can't version binary files  |
| Open in your favorite editor? heck yes | Sorry, only Word and OpenOffice |
| Execute code inside the document? Yep! |  Sorry, what does that mean? |
| easy | hard |
| free | nope |

--- &twocol

## Markdown - Syntax

*** =left

> + Headings (#, or put = or - under words)
  + ### This is a Heading 3
> + Blockquote (> Put your quote here after the carrot)
> + Lists
  + Create list using *, +, or -
  + Ordered list using 1., 2., etc.
  + Nested lists, and more, see the MD site
> + Code blocks
  + Indent 1 tab or 4 spaces
  
*** =right

> + Emphasis
  + __Bold__ \*\*bold\*\* or \_\_bold\_\_
  + _Italic_ *italic* or \_italic\_
  + In the middle of a world: un\*\*believe\*\*able
> + Links, like this => []() or [][] with []: url somewhere else
  + e.g., [here is a link](http://ropensci.org/)
> + You can always just write html! Here's an html table
  <table>
      <tr>
          <td>Foo</td>
          <td>Bar</td>
      </tr>
      <tr>
          <td>5</td>
          <td>6</td>
      </tr>
  </table>

---

<!-- 

Karthik - - Here, I can do a bit of live typing of MD w/ probably Marked app showing how the MD gets rendered live. Then let them jump in to trying it

-->


## <i class="icon-keyboard"></i> Markdown exercizes - your turn

<br><br><br><br>

### Create something in MD and view it.  
### Try and hit as many stylistic elements as possible.

--- &twocol

## More Markdown

*** =left

### Images

\!\[\](http://example.com/logo.png)

\!\[\](figures/img.png)

### Inline code

Wrap code to execute in backticks, so "1 + 1" is executed within this sentence

I counted 2 red trucks on the highway.

### Code blocks

<!-- Karthik - know how to escape code blocks? -->

```r
print("foo")
```

*** =right

### Strikethrough

Use double tildas \~\~strikethrough\~\~ to get ~~strikethrough~~

### Tables

```
First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell
```

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

---

## knitr - R code blocks in Markdown

Put executable code blocks in your markdown


```r
foo <- function() {
    print("bar")
}

foo()
```

```
## [1] "bar"
```


Sweet! <i class="icon-thumbs-up-alt"></i>

---

## Anatomy of a code chunk
<br>
<br>
<center>![knitslide](assets/img/codeChunk.png)</center>
<br>
Three basic components of a knitr document

1. Markdown formatted text

2. Code chunk designation and options

3. Code to execute

---

## <i class="icon-keyboard"></i> Markdown exercizes - your turn again, with code this time

<br><br><br><br>

1. Write markdown with code in code blocks without executing the code. 

2. Then, put your markdown text w/code blocks in R, and compile document using knitr, like 


```r
library(knitr)
knit("/path/to/your/file")
```


---
## Working with code chunk options

Some options

+ `eval`: T or F
  + Evaluate a chunk or just print it
+ `fig.width`, `fig.height`: numeric
  + Width and height of the plot in inches
+ `message`, `warning`, `error`: T or F
  + Whether or not to display messages, warnings or errors

RStudio has a helpful autocomplete for code chunk options

Here's a [full list of options](http://yihui.name/knitr/options)

---

## <i class="icon-keyboard"></i> Markdown exercizes - With code and options

<br><br><br><br>

1. Take your previous example and add some code chunk options.

2. Compile document using knitr

---
## Convert knitr documents to other formats

<!-- Will go through examples of some of these on the CLI, etc. -->

+ Markdown - using knitr


```r
knit("knitr_eg.Rmd")
```


+ HTML - using knitr


```r
knit2html("knitr_eg.Rmd")
```


+ PDF - You have to go to the command line for this (though you can go from LaTeX to PDF)

```bash
pandoc -o knitr_eg.pdf knitr_eg.md
pandoc -V geometry:margin=1in -o knitr_eg.pdf knitr_eg.md
```

+ LaTeX - Requires a bit of text for proper latex doc

```bash
pandoc -o knitr_eg.tex knitr_eg.md
```

---

<!-- 

Karthik - Do the live demo of working with git here?

-->

---

## Resources for Markdown

+ How do I write MD? See [here](http://daringfireball.net/projects/markdown/)
+ Has anyone used MD to write a paper? Yep, see these
  + [Ethan White et al. 2013](https://github.com/weecology/data-sharing-paper/blob/master/data_sharing_ms.md)
  + [Ram 2013](https://github.com/karthikram/smb_git/)
+ Will MD gain more features? Yep, see [here](https://github.com/scholmd/scholmd)
+ Where else can I write MD?
  + [DraftIn](https://draftin.com/) - collaborative writing on the web in MD
+ [MD cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
+ pandoc [get it here](http://johnmacfarlane.net/pandoc/)

---

## Resources for knitr

+ How do I use knitr? See [here](http://yihui.name/knitr/)
+ Can I just see some minimal examples? See [here](http://yihui.name/knitr/demo/minimal/)
+ But I want to see a video? See [here](http://yihui.name/knitr/)

---

## rOpenSci Drinkup

###  Location: Brit's Pub, 3rd floor Verandah bar. 6:30 pm.

<center>![](assets/img/drinkup.png)</center>
