# Sources of inspiration:

[Installing the R kernel in Jupyter Lab
Posted on May 16, 2018 by Karlijn Willems, November 30th, 2016](https://richpauloo.github.io/2018-05-16-Installing-the-R-kernel-in-Jupyter-Lab/)

[Jupyter And R Markdown: Notebooks With R](https://www.datacamp.com/community/blog/jupyter-notebook-r#gs.z0gxLNc)


# Installing Anaconda and R for an offline computer

1) Download from a computer with internet access

**Install miniconda** *(optional- but choose wheter you want a full distribution or a mini)*

*Windows*: `https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe`

*Linux*: `https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh`

or 

**Install anaconda dstribution** (optional- but choose wheter you want a full distribution or a mini)

*Windows*: `https://repo.continuum.io/archive/Anaconda3-2018.12-Windows-x86_64.exe`

*Linux*: `https://repo.continuum.io/archive/Anaconda3-2018.12-Linux-x86_64.sh`


### The following steps are for a Linux machine (Ubuntu 18.04) with internet access. From there we will replicate our environment to a windows-based offline machine.

`conda create -n my-r-env -c conda-forge anaconda python=3.6.7 jupyter_client`

`conda activate my-r-env`

**Note** as we have already activated `my-r-env` we don't need to use the parameter `-n my-r-env` when installing the `r-essentials` package. Also, note that I have used the conda-forge instead of the channel r for my r enviroment.

`conda install -n my-r-env  -c conda-forge r-essentials`  

---
The following NEW packages will be INSTALLED:

    _r-mutex:               1.0.0-anacondar_1                       
    attrs:                  18.2.0-py_0                  conda-forge
    backcall:               0.1.0-py_0                   conda-forge
    binutils_impl_linux-64: 2.31.1-h6176602_1            conda-forge
    binutils_linux-64:      2.31.1-h6176602_3            conda-forge
    bleach:                 3.1.0-py_0                   conda-forge
    bwidget:                1.9.11-1                                
    bzip2:                  1.0.6-h14c3975_1002          conda-forge
    cairo:                  1.14.12-h8948797_3                      
    curl:                   7.63.0-hbc83047_1000                    
    entrypoints:            0.3-py36_1000                conda-forge
    fontconfig:             2.13.0-h9420a91_0                       
    freetype:               2.9.1-h94bbf69_1005          conda-forge
    fribidi:                1.0.5-h14c3975_1000          conda-forge
    gcc_impl_linux-64:      7.3.0-habb00fd_1             conda-forge
    gcc_linux-64:           7.3.0-h553295d_3             conda-forge
    gettext:                0.19.8.1-h9745a5d_1001       conda-forge
    gfortran_impl_linux-64: 7.3.0-hdf63c60_1             conda-forge
    gfortran_linux-64:      7.3.0-h553295d_3             conda-forge
    glib:                   2.56.2-had28632_1001         conda-forge
    gmp:                    6.1.2-hf484d3e_1000          conda-forge
    graphite2:              1.3.13-hf484d3e_1000         conda-forge
    gsl:                    2.4-h14c3975_4                          
    gxx_impl_linux-64:      7.3.0-hdf63c60_1             conda-forge
    gxx_linux-64:           7.3.0-h553295d_3             conda-forge
    harfbuzz:               1.9.0-he243708_1001          conda-forge
    icu:                    58.2-hf484d3e_1000           conda-forge
    ipykernel:              5.1.0-py36h24bf2e0_1002      conda-forge
    ipython:                7.2.0-py36h24bf2e0_1000      conda-forge
    jedi:                   0.13.2-py36_1000             conda-forge
    jinja2:                 2.10-py_1                    conda-forge
    jpeg:                   9c-h14c3975_1001             conda-forge
    jsonschema:             3.0.0a3-py36_1000            conda-forge
    krb5:                   1.16.1-h173b8e3_7                       
    libcurl:                7.63.0-h20c2e04_1000                    
    libedit:                3.1.20170329-hf8c457e_1001   conda-forge
    libgfortran-ng:         7.3.0-hdf63c60_0                        
    libiconv:               1.15-h14c3975_1004           conda-forge
    libpng:                 1.6.36-h84994c4_1000         conda-forge
    libssh2:                1.8.0-1                      conda-forge
    libtiff:                4.0.10-h648cc4a_1001         conda-forge
    libuuid:                1.0.3-1                      conda-forge
    libxcb:                 1.13-h14c3975_1002           conda-forge
    libxml2:                2.9.8-h143f9aa_1005          conda-forge
    make:                   4.2.1-h14c3975_2004          conda-forge
    markupsafe:             1.1.0-py36h14c3975_1000      conda-forge
    mistune:                0.8.4-py36h14c3975_1000      conda-forge
    nbconvert:              5.3.1-py_1                   conda-forge
    nbformat:               4.4.0-py_1                   conda-forge
    notebook:               5.7.4-py36_1000              conda-forge
    pandoc:                 2.5-1                        conda-forge
    pandocfilters:          1.4.2-py_1                   conda-forge
    pango:                  1.42.4-h049681c_0                       
    parso:                  0.3.2-py_0                   conda-forge
    pcre:                   8.42-h439df22_0                         
    pexpect:                4.6.0-py36_1000              conda-forge
    pickleshare:            0.7.5-py36_1000              conda-forge
    pixman:                 0.34.0-h14c3975_1003         conda-forge
    prometheus_client:      0.5.0-py_0                   conda-forge
    prompt_toolkit:         2.0.8-py_0                   conda-forge
    pthread-stubs:          0.4-h14c3975_1001            conda-forge
    ptyprocess:             0.6.0-py36_1000              conda-forge
    pygments:               2.3.1-py_0                   conda-forge
    pyrsistent:             0.14.9-py36h14c3975_1000     conda-forge
    r-assertthat:           0.2.0-r351h6115d3f_1001      conda-forge
    r-backports:            1.1.3-r351h96ca727_1000      conda-forge
    r-base:                 3.5.1-h1e0a451_2                        
    r-base64enc:            0.1_3-r351h96ca727_1002      conda-forge
    r-bh:                   1.69.0_1-r351h6115d3f_0      conda-forge
    r-bindr:                0.1.1-r351h6115d3f_1001      conda-forge
    r-bindrcpp:             0.2.2-r351h29659fb_1001      conda-forge
    r-boot:                 1.3_20-r351_1000             conda-forge
    r-broom:                0.5.1-r351h6115d3f_1000      conda-forge
    r-callr:                3.1.1-r351h6115d3f_1000      conda-forge
    r-caret:                6.0_81-r351h96ca727_1000     conda-forge
    r-cellranger:           1.1.0-r351h6115d3f_1001      conda-forge
    r-class:                7.3_15-r351h96ca727_1000     conda-forge
    r-cli:                  1.0.1-r351h6115d3f_1000      conda-forge
    r-clipr:                0.5.0-r351h6115d3f_0         conda-forge
    r-cluster:              2.0.7_1-r351ha65eedd_1000    conda-forge
    r-codetools:            0.2_16-r351h6115d3f_1000     conda-forge
    r-colorspace:           1.4_0-r351h96ca727_0         conda-forge
    r-crayon:               1.3.4-r351h6115d3f_1001      conda-forge
    r-curl:                 3.3-r351h96ca727_0           conda-forge
    r-data.table:           1.12.0-r351h96ca727_0        conda-forge
    r-dbi:                  1.0.0-r351h6115d3f_1001      conda-forge
    r-dbplyr:               1.3.0-r351h6115d3f_1000      conda-forge
    r-digest:               0.6.18-r351h96ca727_1000     conda-forge
    r-dplyr:                0.7.8-r351h29659fb_1000      conda-forge
    r-essentials:           3.5.1-r351_2000              conda-forge
    r-evaluate:             0.12-r351h6115d3f_1000       conda-forge
    r-fansi:                0.4.0-r351h96ca727_1000      conda-forge
    r-forcats:              0.3.0-r351h6115d3f_1001      conda-forge
    r-foreach:              1.4.4-r351h6115d3f_1001      conda-forge
    r-foreign:              0.8_71-r351h96ca727_1002     conda-forge
    r-formatr:              1.5-r351h6115d3f_1001        conda-forge
    r-fs:                   1.2.6-r351h29659fb_1000      conda-forge
    r-generics:             0.0.2-r351h6115d3f_1001      conda-forge
    r-ggplot2:              3.1.0-r351h6115d3f_1000      conda-forge
    r-gistr:                0.4.2-r351h6115d3f_1001      conda-forge
    r-glmnet:               2.0_16-r351ha65eedd_1001     conda-forge
    r-glue:                 1.3.0-r351h14c3975_1002      conda-forge
    r-gower:                0.1.2-r351h96ca727_1002      conda-forge
    r-gtable:               0.2.0-r351h6115d3f_1001      conda-forge
    r-haven:                2.0.0-r351h29659fb_1000      conda-forge
    r-hexbin:               1.27.2-r351ha65eedd_1002     conda-forge
    r-highr:                0.7-r351h6115d3f_1001        conda-forge
    r-hms:                  0.4.2-r351h6115d3f_1000      conda-forge
    r-htmltools:            0.3.6-r351hf484d3e_1002      conda-forge
    r-htmlwidgets:          1.3-r351h6115d3f_1000        conda-forge
    r-httpuv:               1.4.5.1-r351hf484d3e_1000    conda-forge
    r-httr:                 1.4.0-r351h6115d3f_1000      conda-forge
    r-ipred:                0.9_8-r351h96ca727_1000      conda-forge
    r-irdisplay:            0.7-r351_1000                conda-forge
    r-irkernel:             0.8.15-r351h6115d3f_1001     conda-forge
    r-iterators:            1.0.10-r351h6115d3f_1001     conda-forge
    r-jsonlite:             1.6-r351h96ca727_1000        conda-forge
    r-kernsmooth:           2.23_15-r351ha65eedd_1002    conda-forge
    r-knitr:                1.21-r351h6115d3f_1000       conda-forge
    r-labeling:             0.3-r351h6115d3f_1001        conda-forge
    r-later:                0.7.5-r351h29659fb_1000      conda-forge
    r-lattice:              0.20_38-r351h96ca727_1000    conda-forge
    r-lava:                 1.6.4-r351h6115d3f_1000      conda-forge
    r-lazyeval:             0.2.1-r351h96ca727_1002      conda-forge
    r-lubridate:            1.7.4-r351h29659fb_1001      conda-forge
    r-magrittr:             1.5-r351h6115d3f_1001        conda-forge
    r-maps:                 3.3.0-r351h96ca727_1002      conda-forge
    r-markdown:             0.9-r351h96ca727_1000        conda-forge
    r-mass:                 7.3_51.1-r351h96ca727_1000   conda-forge
    r-matrix:               1.2_15-r351h96ca727_1000     conda-forge
    r-mgcv:                 1.8_26-r351h96ca727_1000     conda-forge
    r-mime:                 0.6-r351h96ca727_1000        conda-forge
    r-modelmetrics:         1.1.0-r351h29659fb_1002      conda-forge
    r-modelr:               0.1.2-r351h6115d3f_1001      conda-forge
    r-munsell:              0.5.0-r351h6115d3f_1001      conda-forge
    r-nlme:                 3.1_137-r351ha65eedd_1000    conda-forge
    r-nnet:                 7.3_12-r351h96ca727_1002     conda-forge
    r-numderiv:             2016.8_1-r351h6115d3f_1001   conda-forge
    r-openssl:              1.0.2-r351h96ca727_1                    
    r-pbdzmq:               0.3_3-r351h193a840_1000      conda-forge
    r-pillar:               1.3.1-r351h6115d3f_1000      conda-forge
    r-pkgconfig:            2.0.2-r351h6115d3f_1001      conda-forge
    r-plogr:                0.2.0-r351h6115d3f_1001      conda-forge
    r-plyr:                 1.8.4-r351h29659fb_1002      conda-forge
    r-prettyunits:          1.0.2-r351h6115d3f_1001      conda-forge
    r-processx:             3.2.1-r351h96ca727_1000      conda-forge
    r-prodlim:              2018.04.18-r351h29659fb_1002 conda-forge
    r-progress:             1.2.0-r351h6115d3f_1002      conda-forge
    r-promises:             1.0.1-r351h29659fb_1000      conda-forge
    r-pryr:                 0.1.4-r351h29659fb_1002      conda-forge
    r-ps:                   1.3.0-r351h96ca727_1000      conda-forge
    r-purrr:                0.2.5-r351h96ca727_1002      conda-forge
    r-quantmod:             0.4_13-r351h6115d3f_1000     conda-forge
    r-r6:                   2.3.0-r351h6115d3f_1000      conda-forge
    r-randomforest:         4.6_14-r351ha65eedd_1000     conda-forge
    r-rbokeh:               0.5.0-r351h6115d3f_1001      conda-forge
    r-rcolorbrewer:         1.1_2-r351h6115d3f_1001      conda-forge
    r-rcpp:                 1.0.0-r351h29659fb_1000      conda-forge
    r-rcpproll:             0.3.0-r351h29659fb_1000      conda-forge
    r-readr:                1.3.1-r351h29659fb_1000      conda-forge
    r-readxl:               1.2.0-r351h29659fb_1000      conda-forge
    r-recipes:              0.1.4-r351h6115d3f_1000      conda-forge
    r-recommended:          3.5.1-r351_1001              conda-forge
    r-rematch:              1.0.1-r351h6115d3f_1001      conda-forge
    r-repr:                 0.19.1-r351h6115d3f_1000     conda-forge
    r-reprex:               0.2.1-r351h6115d3f_1000      conda-forge
    r-reshape2:             1.4.3-r351h29659fb_1003      conda-forge
    r-rlang:                0.3.1-r351h96ca727_0         conda-forge
    r-rmarkdown:            1.11-r351h6115d3f_1000       conda-forge
    r-rpart:                4.1_13-r351h96ca727_1002     conda-forge
    r-rprojroot:            1.3_2-r351h6115d3f_1001      conda-forge
    r-rstudioapi:           0.9.0-r351h6115d3f_0         conda-forge
    r-rvest:                0.3.2-r351h6115d3f_1001      conda-forge
    r-scales:               1.0.0-r351h29659fb_1001      conda-forge
    r-selectr:              0.4_1-r351h6115d3f_1000      conda-forge
    r-shiny:                1.2.0-r351_1000              conda-forge
    r-sourcetools:          0.1.7-r351hf484d3e_1000      conda-forge
    r-spatial:              7.3_11-r351h96ca727_1002     conda-forge
    r-squarem:              2017.10_1-r351h6115d3f_1001  conda-forge
    r-stringi:              1.2.4-r351h29659fb_1001      conda-forge
    r-stringr:              1.3.1-r351h6115d3f_1001      conda-forge
    r-survival:             2.43_3-r351h96ca727_1000     conda-forge
    r-tibble:               2.0.1-r351h96ca727_0         conda-forge
    r-tidyr:                0.8.2-r351h29659fb_1002      conda-forge
    r-tidyselect:           0.2.5-r351h29659fb_1000      conda-forge
    r-tidyverse:            1.2.1-r351h6115d3f_1001      conda-forge
    r-timedate:             3043.102-r351h6115d3f_1000   conda-forge
    r-tinytex:              0.10-r351h6115d3f_0          conda-forge
    r-ttr:                  0.23_4-r351ha65eedd_1000     conda-forge
    r-utf8:                 1.1.4-r351h96ca727_1000      conda-forge
    r-uuid:                 0.1_2-r351h96ca727_1001      conda-forge
    r-viridislite:          0.3.0-r351h6115d3f_1001      conda-forge
    r-whisker:              0.3_2-r351h6115d3f_1001      conda-forge
    r-withr:                2.1.2-r351h6115d3f_1000      conda-forge
    r-xfun:                 0.4-r351h6115d3f_1000        conda-forge
    r-xml2:                 1.2.0-r351h29659fb_1002      conda-forge
    r-xtable:               1.8_3-r351_2000              conda-forge
    r-xts:                  0.11_1-r351h96ca727_1000     conda-forge
    r-yaml:                 2.2.0-r351h96ca727_1001      conda-forge
    r-zoo:                  1.8_4-r351h96ca727_1000      conda-forge
    send2trash:             1.5.0-py_0                   conda-forge
    terminado:              0.8.1-py36_1001              conda-forge
    testpath:               0.4.2-py36_1000              conda-forge
    tktable:                2.10-h14c3975_0                         
    wcwidth:                0.1.7-py_1                   conda-forge
    webencodings:           0.5.1-py_1                   conda-forge
    xorg-kbproto:           1.0.7-h14c3975_1002          conda-forge
    xorg-libice:            1.0.9-h14c3975_1004          conda-forge
    xorg-libsm:             1.2.2-h470a237_5             conda-forge
    xorg-libx11:            1.6.6-h14c3975_1000          conda-forge
    xorg-libxau:            1.0.8-h14c3975_1006          conda-forge
    xorg-libxdmcp:          1.1.2-h14c3975_1007          conda-forge
    xorg-libxext:           1.3.3-h14c3975_1004          conda-forge
    xorg-libxrender:        0.9.10-h14c3975_1002         conda-forge
    xorg-renderproto:       0.11.1-h14c3975_1002         conda-forge
    xorg-xextproto:         7.3.0-h14c3975_1002          conda-forge
    xorg-xproto:            7.0.31-h14c3975_1007         conda-forge



---


Then, open an R session on a terminal:
`$ R`

You will get something similar to:

```
R version 3.5.1 (2018-07-02) -- "Feather Spray"
Copyright (C) 2018 The R Foundation for Statistical Computing
Platform: x86_64-conda_cos6-linux-gnu (64-bit)

>
```
Using the R prompt of oyr `my-r-env`
```
> install.packages("devtools" )  # using Sweden Repo 
> IRkernel::installspec()   #  IRkernel::installspec(user = FALSE) # install system-wide

> install.packages(c('DT', 'ROCR', 'caTools', 'lubridate', 'rjson', 'littler', 'docopt', 'formatR', 'remotes', 'selectr'), dependencies=TRUE)

...
> quit()
```

`conda install r-rgdal r-raster -c conda-forge`
`conda install r-bookdown r-PKI -c conda-forge`   

**note** install gdal after in the environment to update also the previous package for r-rgdal

`conda install gdal -c conda-forge`

To comunicate between python and R, it is recommended to use `rpy2` package

`conda install rpy2`

Adding geospatial packages(Note this will downgrade several packages):

`conda install r-RColorBrewer r-RandomFields r-classInt r-deldir r-gstat r-mapdata r-maptools r-mapview r-ncdf4 r-rgeos r-rlas r-sf r-sp r-spacetime r-spatstat r-spdep r-geoR r-geosphere -c conda-forge`












