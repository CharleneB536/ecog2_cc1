Install packages
================

# Configuration machine virtuelle mise à jour

``` bash
sudo apt-get update -y 
sudo apt-get install -y libbz2-dev
sudo apt-get install -y liblzma-dev
```

    ## sudo: unable to resolve host 484e593b34a0: Name or service not known
    ## Hit:1 http://archive.ubuntu.com/ubuntu focal InRelease
    ## Hit:2 http://security.ubuntu.com/ubuntu focal-security InRelease
    ## Hit:3 http://archive.ubuntu.com/ubuntu focal-updates InRelease
    ## Hit:4 http://archive.ubuntu.com/ubuntu focal-backports InRelease
    ## Reading package lists...
    ## sudo: unable to resolve host 484e593b34a0: Name or service not known
    ## Reading package lists...
    ## Building dependency tree...
    ## Reading state information...
    ## libbz2-dev is already the newest version (1.0.8-2).
    ## 0 upgraded, 0 newly installed, 0 to remove and 39 not upgraded.
    ## sudo: unable to resolve host 484e593b34a0: Name or service not known
    ## Reading package lists...
    ## Building dependency tree...
    ## Reading state information...
    ## liblzma-dev is already the newest version (5.2.4-1ubuntu1).
    ## 0 upgraded, 0 newly installed, 0 to remove and 39 not upgraded.

# Installation des packages

Following instruction on
<https://benjjneb.github.io/dada2/dada-installation.html>

## Installation Dada2

``` r
BiocManager::install("dada2")
```

    ## Bioconductor version 3.12 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'dada2'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

    ## Old packages: 'rlang'

## Installation phangorn

``` r
BiocManager::install("phangorn")
```

    ## Bioconductor version 3.12 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'phangorn'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

    ## Old packages: 'rlang'

## Installation decipher

``` r
BiocManager::install("DECIPHER")
```

    ## Bioconductor version 3.12 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'DECIPHER'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

    ## Old packages: 'rlang'

## Installation ggplot2

``` r
install.packages('ggplot2')
```

    ## Installing package into '/usr/local/lib/R/site-library'
    ## (as 'lib' is unspecified)

``` r
BiocManager::install("ggplot2")
```

    ## Bioconductor version 3.12 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'ggplot2'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

    ## Old packages: 'rlang'

``` r
library(ggplot2); packageVersion("ggplot2")
```

    ## [1] '3.3.2'

## Installation gridExtra

``` r
install.packages("gridExtra")
```

    ## Installing package into '/usr/local/lib/R/site-library'
    ## (as 'lib' is unspecified)

## Installation cran-packages

``` r
.cran_packages <- c( "shiny","miniUI", "caret", "pls", "e1071", "ggplot2", "randomForest", "dplyr", "ggrepel", "nlme", "devtools",
                  "reshape2", "PMA", "structSSI", "ade4",
                  "ggnetwork", "intergraph", "scales")
.github_packages <- c("jfukuyama/phyloseqGraphTest")
.bioc_packages <- c("genefilter", "impute")
# Install CRAN packages (if not already installed)
.inst <- .cran_packages %in% installed.packages()
if (any(!.inst)){
  install.packages(.cran_packages[!.inst],repos = "http://cran.rstudio.com/")
}
.inst <- .github_packages %in% installed.packages()
if (any(!.inst)){
  devtools::install_github(.github_packages[!.inst])
}
```

    ## Skipping install of 'phyloseqGraphTest' from a github remote, the SHA1 (3fb6c274) has not changed since last install.
    ##   Use `force = TRUE` to force installation

``` r
.inst <- .bioc_packages %in% installed.packages()
if(any(!.inst)){
  Biocmanager::install(.bioc_packages[!.inst])
}
```

## Installation DESeq2

``` r
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("DESeq2")
```

    ## Bioconductor version 3.12 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'DESeq2'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

    ## Old packages: 'rlang'

## Installation structSSI

``` r
library(devtools)
```

    ## Loading required package: usethis

``` r
install_local("./structSSI_1.1.1.tar.gz")
```

    ## Warning in normalizePath(path): path[1]="./structSSI_1.1.1.tar.gz": No such file
    ## or directory

    ## Error : Could not copy `./structSSI_1.1.1.tar.gz` to `/tmp/RtmpD3ncDz/file1b91183211d`

## Installation Cran-packages

``` r
install.packages("ade4")      # Calcul de l'ACP
```

    ## Installing package into '/usr/local/lib/R/site-library'
    ## (as 'lib' is unspecified)

``` r
install.packages("factoextra")# Visualisation  de l'ACP
```

    ## Installing package into '/usr/local/lib/R/site-library'
    ## (as 'lib' is unspecified)

## Installation rmarkdown

``` r
install.packages("rmarkdown")
```

    ## Installing package into '/usr/local/lib/R/site-library'
    ## (as 'lib' is unspecified)

``` bash
sudo apt-get install -y libglpk-dev
```

    ## sudo: unable to resolve host 484e593b34a0: Name or service not known
    ## Reading package lists...
    ## Building dependency tree...
    ## Reading state information...
    ## libglpk-dev is already the newest version (4.65-2).
    ## 0 upgraded, 0 newly installed, 0 to remove and 39 not upgraded.

## Installation phyloseq

``` r
BiocManager::install("phyloseq")
```

    ## Bioconductor version 3.12 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'phyloseq'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

    ## Old packages: 'rlang'

``` r
library(phyloseq); packageVersion("phyloseq")
```

    ## [1] '1.34.0'

## Installation Biostrings

``` r
BiocManager::install("Biostrings")
```

    ## Bioconductor version 3.12 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'Biostrings'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

    ## Old packages: 'rlang'

## Installation BiocStyle

``` r
BiocManager::install("BiocStyle")
```

    ## Bioconductor version 3.12 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'BiocStyle'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

    ## Old packages: 'rlang'

## Installation des packages pour Phyloseq

``` r
library("knitr")
library("BiocStyle")
.cran_packages <- c("ggplot2", "gridExtra")
.bioc_packages <- c("dada2", "phyloseq", "DECIPHER", "phangorn")
.inst <- .cran_packages %in% installed.packages()
if(any(!.inst)) {
   install.packages(.cran_packages[!.inst])
}
.inst <- .bioc_packages %in% installed.packages()
if(any(!.inst)) {
   source("http://bioconductor.org/biocLite.R")
   biocLite(.bioc_packages[!.inst], ask = F)
}
# Load packages into session, and print package version
sapply(c(.cran_packages, .bioc_packages), require, character.only = TRUE)
```

    ## Loading required package: gridExtra

    ## Loading required package: dada2

    ## Loading required package: Rcpp

    ## Loading required package: DECIPHER

    ## Loading required package: Biostrings

    ## Loading required package: BiocGenerics

    ## Loading required package: parallel

    ## 
    ## Attaching package: 'BiocGenerics'

    ## The following objects are masked from 'package:parallel':
    ## 
    ##     clusterApply, clusterApplyLB, clusterCall, clusterEvalQ,
    ##     clusterExport, clusterMap, parApply, parCapply, parLapply,
    ##     parLapplyLB, parRapply, parSapply, parSapplyLB

    ## The following object is masked from 'package:gridExtra':
    ## 
    ##     combine

    ## The following objects are masked from 'package:stats':
    ## 
    ##     IQR, mad, sd, var, xtabs

    ## The following objects are masked from 'package:base':
    ## 
    ##     anyDuplicated, append, as.data.frame, basename, cbind, colnames,
    ##     dirname, do.call, duplicated, eval, evalq, Filter, Find, get, grep,
    ##     grepl, intersect, is.unsorted, lapply, Map, mapply, match, mget,
    ##     order, paste, pmax, pmax.int, pmin, pmin.int, Position, rank,
    ##     rbind, Reduce, rownames, sapply, setdiff, sort, table, tapply,
    ##     union, unique, unsplit, which.max, which.min

    ## Loading required package: S4Vectors

    ## Loading required package: stats4

    ## 
    ## Attaching package: 'S4Vectors'

    ## The following object is masked from 'package:base':
    ## 
    ##     expand.grid

    ## Loading required package: IRanges

    ## 
    ## Attaching package: 'IRanges'

    ## The following object is masked from 'package:phyloseq':
    ## 
    ##     distance

    ## Loading required package: XVector

    ## 
    ## Attaching package: 'Biostrings'

    ## The following object is masked from 'package:base':
    ## 
    ##     strsplit

    ## Loading required package: RSQLite

    ## Loading required package: phangorn

    ## Loading required package: ape

    ## 
    ## Attaching package: 'ape'

    ## The following object is masked from 'package:Biostrings':
    ## 
    ##     complement

    ##   ggplot2 gridExtra     dada2  phyloseq  DECIPHER  phangorn 
    ##      TRUE      TRUE      TRUE      TRUE      TRUE      TRUE

``` r
##   ggplot2 gridExtra     dada2  phyloseq  DECIPHER  phangorn 
##      TRUE      TRUE      TRUE      TRUE      TRUE      TRUE
set.seed(100)
```
