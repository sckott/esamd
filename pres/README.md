Reproducible Research and Collaboration
=====

The main file for the prsentation is index.Rmd 

Compile the file to slides:

+ install R packge slidify: `install_github("slidify", "ramnathv", ref="dev")`
+ install R packge slidifyLibraries: `install_github("slidifyLibraries", "ramnathv", ref="dev")`
+ Then load the two packages `library(slidify); library(slidifyLibraries)`
+ Go to the directory on your machine where this is
+ run slidify("index.Rmd"), and it will output a file "index.html" that you can open in browser and examine
+ edit stuff, commit changes, push

notes:

+ custom css is in the file `assets/css/esamd.css`
+ images in `assets/img/`