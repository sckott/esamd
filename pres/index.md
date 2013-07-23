---
title       : Reproducible Research and Collaboration
subtitle    : Fun with markdown and git
author      : Ted Hart & Scott Chamberlain
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

## Markdown

> + Markdown, MD for short, is a markup language with a few killer attributes 
  + Super simple to learn (much easier than LaTeX)
  + Incorporate code blocks <i class="icon-code"></i>
  + Allows you to write reproducible documents (code + text)
> + Background
  + Created by [John Gruber](http://daringfireball.net/) (w/ help from [Aaron Swartz](http://www.aaronsw.com/))
  + [The canonical place to learn more](http://daringfireball.net/projects/markdown/)


---

## Markdown use cases

Why would you want to use Markdown?

> + Taking notes
> + Blog posts
> + Research paper
> + MD is used in many places (StackOverflow, Github, etc.), so good to learn it

---

## Markdown - Syntax

> + Headings (#, =, or -)
  + Heading 3 (###)
> + Blockquote (>)
> + Lists
  + Create list using *, +, or -, or ordered list using 1., 2., etc.
  + Nested lists, and more, see the MD site
> + Code blocks
  + Indent 1 tab or 4 spaces
> + Emphasis
  + __Bold__ \*\*bold\*\* or \_\_bold\_\_
  + _Italic_ *italic* or \_italic\_
  + In the middle of a world: un\*\*believe\*\*able
> + Links, like this => []() or [][] with []: url somewhere else
> + You can always just write html!

---

## Markdown - your turn

<i class="icon-exclamation-sign"></i> Exercizes

1. Write some simple markdown. View it in your favorite MD viewer.
2. Write markdown with code blocks that execute code using R. Compile the file and view.

---

## Markdown - R code blocks

Code blocks can be written and are highlighted, e.g.

```r
foo <- function(){
  print('bar')
}
```

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

## Markdown - your turn again, with code this time

<i class="icon-exclamation-sign"></i> Exercizes

1. Write markdown with code in code blocks without executing the code. View it in your favorite MD viewer.
2. Now, put your markdown text w/code blocks in R, and compile document using knitr, like 


```r
library(knitr)
knit("/path/to/your/file")
```


---

## git

> + git is a version control system
> + Use cases
  + Local version control of some files
  + Branching to try out completely new things
  + <i class="icon-group"></i> Collaboration with others
  + <i class="icon-code-fork"></i> Forking! 


---

## Why git? Who did what?

![](assets/img/contributions.png)

---

## Why git? Visualize contributions

![](assets/img/commits.png)

---

## git - your turn

> + If you have git installed:
  + Create a folder `foo <- bar(the = 5)`
  + Create a document inside that folder with some markdown text `touch mydoc.md`
  + Initiate the git repo `git init`
  + Tell git to track your file `git add .` or `git add mydoc.md`
  + Commit those changes `git commit -a -m 'initial commit, added mydoc file'`
  + Make some additional changes to your file
  + Commit those changes `git commit -a -m 'edited mydoc file'`
  + Create a branch `git branch newbranch` then `git checkout newbranch`
  + Make a few changes to the file on the new branch and commit `git commit -a -m '...'`
  + Merge the new branch into the master branch `git checkout master` & `git merge newbranch`

---

## Resources for Markdown and git, via FAQ

> + Markdown
  + How do I write Markdown? See [here](http://daringfireball.net/projects/markdown/)
  + How do I ...
> + git 
  + How do I use git? See [here](http://git-scm.com/book)
  + But, I want to watch videos! Okay, see [here](https://www.youtube.com/channel/UCP7RrmoueENv9TZts3HXXtw)
  + How do I ...
