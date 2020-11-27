Install packages
================

# Configuration machine virtuelle mise à jour

``` bash
sudo apt-get update -y 
sudo apt-get install -y libbz2-dev
sudo apt-get install -y liblzma-dev
```

    ## sudo: unable to resolve host 484e593b34a0: Name or service not known
    ## Get:1 http://security.ubuntu.com/ubuntu focal-security InRelease [109 kB]
    ## Hit:2 http://archive.ubuntu.com/ubuntu focal InRelease
    ## Get:3 http://archive.ubuntu.com/ubuntu focal-updates InRelease [114 kB]
    ## Get:4 http://archive.ubuntu.com/ubuntu focal-backports InRelease [101 kB]
    ## Get:5 http://archive.ubuntu.com/ubuntu focal-updates/universe amd64 Packages [871 kB]
    ## Get:6 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 Packages [850 kB]
    ## Fetched 2,045 kB in 1s (2,402 kB/s)
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

    ## Old packages: 'BiocStyle'

## Installation phangorn

``` r
BiocManager::install("phangorn")
```

    ## Bioconductor version 3.12 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'phangorn'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

    ## Old packages: 'BiocStyle'

## Installation decipher

``` r
BiocManager::install("DECIPHER")
```

    ## Bioconductor version 3.12 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'DECIPHER'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

    ## Old packages: 'BiocStyle'

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

    ## Old packages: 'BiocStyle'

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

    ## Old packages: 'BiocStyle'

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

    ## Error : Could not copy `./structSSI_1.1.1.tar.gz` to `/tmp/RtmpPgkVL2/file7ae45bbdff18`

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

    ## Old packages: 'BiocStyle'

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

    ## Old packages: 'BiocStyle'

## Installation BiocStyle

``` r
BiocManager::install("BiocStyle")
```

    ## Bioconductor version 3.12 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'BiocStyle'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme
