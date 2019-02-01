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


### The following steps are for a Linux machine (Ubuntu 18.04) with internet access. Note, the OS of the machines that will replicate the enviroment must match. Windows 10 to Windows 10, Ubuntu 18.04 to Ubuntu 18.+, etc...

To comunicate between python and R, it is recommended to use `rpy2` package, and if you use biomod2 and geospatial r functions do not forget to install the gdal and raster packages.

`conda create -n my-r-env -c conda-forge anaconda python=3.6.7 jupyter_client r-base=3.5.1 r-essentials r-rgdal r-raster r-bookdown r-PKI gdal rpy2`

`conda activate my-r-env`

**Note** as we have already activated `my-r-env` we don't need to use the parameter `-n my-r-env` when installing the `r-essentials` package. Also, note that I have used the conda-forge instead of the channel r for my r enviroment.


---


The following NEW packages will be INSTALLED:

    _r-mutex:               1.0.0-anacondar_1                       
    anaconda:               custom-py36hbbc8b67_0                   
    attrs:                  18.2.0-py_0                  conda-forge
    backcall:               0.1.0-py_0                   conda-forge
    binutils_impl_linux-64: 2.31.1-h6176602_1            conda-forge
    binutils_linux-64:      2.31.1-h6176602_3            conda-forge
    bleach:                 3.1.0-py_0                   conda-forge
    bwidget:                1.9.11-1                                
    bzip2:                  1.0.6-h14c3975_1002          conda-forge
    ca-certificates:        2018.11.29-ha4d7672_0        conda-forge
    cairo:                  1.14.12-h80bd089_1005        conda-forge
    certifi:                2018.11.29-py36_1000         conda-forge
    curl:                   7.63.0-h646f8bb_1000         conda-forge
    decorator:              4.3.2-py_0                   conda-forge
    entrypoints:            0.3-py36_1000                conda-forge
    fontconfig:             2.13.1-h2176d3f_1000         conda-forge
    freetype:               2.9.1-h94bbf69_1005          conda-forge
    gcc_impl_linux-64:      7.3.0-habb00fd_1             conda-forge
    gcc_linux-64:           7.3.0-h553295d_3             conda-forge
    gettext:                0.19.8.1-h9745a5d_1001       conda-forge
    gfortran_impl_linux-64: 7.3.0-hdf63c60_1             conda-forge
    gfortran_linux-64:      7.3.0-h553295d_3             conda-forge
    glib:                   2.56.2-had28632_1001         conda-forge
    gmp:                    6.1.2-hf484d3e_1000          conda-forge
    graphite2:              1.3.13-hf484d3e_1000         conda-forge
    gxx_impl_linux-64:      7.3.0-hdf63c60_1             conda-forge
    gxx_linux-64:           7.3.0-h553295d_3             conda-forge
    harfbuzz:               1.9.0-he243708_1001          conda-forge
    icu:                    58.2-hf484d3e_1000           conda-forge
    ipykernel:              5.1.0-py36h24bf2e0_1002      conda-forge
    ipython:                7.2.0-py36h24bf2e0_1000      conda-forge
    ipython_genutils:       0.2.0-py_1                   conda-forge
    jedi:                   0.13.2-py36_1000             conda-forge
    jinja2:                 2.10-py_1                    conda-forge
    jpeg:                   9c-h14c3975_1001             conda-forge
    jsonschema:             3.0.0a3-py36_1000            conda-forge
    jupyter_client:         5.2.4-py_1                   conda-forge
    jupyter_core:           4.4.0-py_0                   conda-forge
    krb5:                   1.16.3-hc83ff2d_1000         conda-forge
    libcurl:                7.63.0-h01ee5af_1000         conda-forge
    libedit:                3.1.20170329-hf8c457e_1001   conda-forge
    libffi:                 3.2.1-hf484d3e_1005          conda-forge
    libgcc-ng:              7.3.0-hdf63c60_0             conda-forge
    libgfortran-ng:         7.3.0-hdf63c60_0                        
    libiconv:               1.15-h14c3975_1004           conda-forge
    libpng:                 1.6.36-h84994c4_1000         conda-forge
    libsodium:              1.0.16-h14c3975_1001         conda-forge
    libssh2:                1.8.0-h1ad7b7a_1003          conda-forge
    libstdcxx-ng:           7.3.0-hdf63c60_0             conda-forge
    libtiff:                4.0.10-h648cc4a_1001         conda-forge
    libuuid:                2.32.1-h14c3975_1000         conda-forge
    libxcb:                 1.13-h14c3975_1002           conda-forge
    libxml2:                2.9.8-h143f9aa_1005          conda-forge
    make:                   4.2.1-h14c3975_2004          conda-forge
    markupsafe:             1.1.0-py36h14c3975_1000      conda-forge
    mistune:                0.8.4-py36h14c3975_1000      conda-forge
    nbconvert:              5.3.1-py_1                   conda-forge
    nbformat:               4.4.0-py_1                   conda-forge
    ncurses:                6.1-hf484d3e_1002            conda-forge
    notebook:               5.7.4-py36_1000              conda-forge
    openssl:                1.0.2p-h14c3975_1002         conda-forge
    pandoc:                 2.5-1                        conda-forge
    pandocfilters:          1.4.2-py_1                   conda-forge
    pango:                  1.40.14-hf0c64fd_1003        conda-forge
    parso:                  0.3.2-py_0                   conda-forge
    pcre:                   8.41-hf484d3e_1003           conda-forge
    pexpect:                4.6.0-py36_1000              conda-forge
    pickleshare:            0.7.5-py36_1000              conda-forge
    pip:                    19.0.1-py36_0                conda-forge
    pixman:                 0.34.0-h14c3975_1003         conda-forge
    prometheus_client:      0.5.0-py_0                   conda-forge
    prompt_toolkit:         2.0.8-py_0                   conda-forge
    pthread-stubs:          0.4-h14c3975_1001            conda-forge
    ptyprocess:             0.6.0-py36_1000              conda-forge
    pygments:               2.3.1-py_0                   conda-forge
    pyrsistent:             0.14.9-py36h14c3975_1000     conda-forge
    python:                 3.6.7-hd21baee_1001          conda-forge
    python-dateutil:        2.7.5-py_0                   conda-forge
    pyzmq:                  17.1.2-py36h6afc9c9_1001     conda-forge
    r-assertthat:           0.2.0-r351h6115d3f_1001      conda-forge
    r-backports:            1.1.3-r351h96ca727_1000      conda-forge
    r-base:                 3.5.1-he45234b_1005          conda-forge
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
    r-openssl:              1.1-r351hff1dc39_1000        conda-forge
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
    readline:               7.0-hf8c457e_1001            conda-forge
    send2trash:             1.5.0-py_0                   conda-forge
    setuptools:             40.7.1-py36_0                conda-forge
    six:                    1.12.0-py36_1000             conda-forge
    sqlite:                 3.26.0-h67949de_1000         conda-forge
    terminado:              0.8.1-py36_1001              conda-forge
    testpath:               0.4.2-py36_1000              conda-forge
    tk:                     8.6.9-h84994c4_1000          conda-forge
    tktable:                2.10-h14c3975_0                         
    tornado:                5.1.1-py36h14c3975_1000      conda-forge
    traitlets:              4.3.2-py36_1000              conda-forge
    wcwidth:                0.1.7-py_1                   conda-forge
    webencodings:           0.5.1-py_1                   conda-forge
    wheel:                  0.32.3-py36_0                conda-forge
    xorg-kbproto:           1.0.7-h14c3975_1002          conda-forge
    xorg-libice:            1.0.9-h14c3975_1004          conda-forge
    xorg-libsm:             1.2.3-h4937e3b_1000          conda-forge
    xorg-libx11:            1.6.6-h14c3975_1000          conda-forge
    xorg-libxau:            1.0.8-h14c3975_1006          conda-forge
    xorg-libxdmcp:          1.1.2-h14c3975_1007          conda-forge
    xorg-libxext:           1.3.3-h14c3975_1004          conda-forge
    xorg-libxrender:        0.9.10-h14c3975_1002         conda-forge
    xorg-renderproto:       0.11.1-h14c3975_1002         conda-forge
    xorg-xextproto:         7.3.0-h14c3975_1002          conda-forge
    xorg-xproto:            7.0.31-h14c3975_1007         conda-forge
    xz:                     5.2.4-h14c3975_1001          conda-forge
    zeromq:                 4.2.5-hf484d3e_1006          conda-forge
    zlib:                   1.2.11-h14c3975_1004         conda-forge
    
    
    + 
    The following NEW packages will be INSTALLED:

    blas:          1.0-mkl                               
    boost-cpp:     1.68.0-h11c811c_1000       conda-forge
    expat:         2.2.5-hf484d3e_1002        conda-forge
    freexl:        1.0.5-h14c3975_1002        conda-forge
    gdal:          2.3.3-py36h1c6dbfb_1001    conda-forge
    geos:          3.7.1-hf484d3e_1000        conda-forge
    geotiff:       1.4.3-h1105359_1000        conda-forge
    giflib:        5.1.4-h14c3975_1001        conda-forge
    hdf4:          4.2.13-h9a582f1_1002       conda-forge
    hdf5:          1.10.4-nompi_h11e915b_1105 conda-forge
    intel-openmp:  2019.1-144                            
    json-c:        0.13.1-h14c3975_1001       conda-forge
    kealib:        1.4.10-he7154bc_1002       conda-forge
    libdap4:       3.19.1-hd48c02d_1000       conda-forge
    libgdal:       2.3.3-h982c1cc_1001        conda-forge
    libkml:        1.3.0-h328b03d_1009        conda-forge
    libnetcdf:     4.6.2-hbdf4f91_1001        conda-forge
    libpq:         10.6-h13b8bad_1000         conda-forge
    libspatialite: 4.3.0a-hb5ec416_1026       conda-forge
    mkl:           2019.1-144                            
    mkl_fft:       1.0.10-py36h14c3975_1      conda-forge
    mkl_random:    1.0.2-py36h637b7d7_2       conda-forge
    numpy:         1.15.4-py36h7e9f1db_0                 
    numpy-base:    1.15.4-py36hde5b4d6_0                 
    openjpeg:      2.3.0-hf38bd82_1003        conda-forge
    poppler:       0.67.0-h2fc8fa2_1002       conda-forge
    poppler-data:  0.4.9-1                    conda-forge
    postgresql:    10.6-h66cca7a_1000         conda-forge
    proj4:         5.2.0-h14c3975_1001        conda-forge
    pytz:          2018.9-py_0                conda-forge
    r-bit:         1.1_12-r351h14c3975_1002   conda-forge
    r-bit64:       0.9_7-r351h96ca727_1000    conda-forge
    r-blob:        1.1.1-r351_1001            conda-forge
    r-bookdown:    0.9-r351h6115d3f_1000      conda-forge
    r-memoise:     1.1.0-r351h6115d3f_1001    conda-forge
    r-pki:         0.1_5.1-r351h96ca727_1001  conda-forge
    r-raster:      2.6_7-r351h29659fb_1002    conda-forge
    r-rgdal:       1.3_6-r351h285a78d_1       conda-forge
    r-rsqlite:     2.1.1-r351h29659fb_1000    conda-forge
    r-sp:          1.3_1-r351h96ca727_1000    conda-forge
    rpy2:          2.9.4-py36r351h941a26a_1   conda-forge
    tzcode:        2018g-h14c3975_1001        conda-forge
    tzlocal:       1.5.1-py_0                 conda-forge
    xerces-c:      3.2.2-hac72e42_1001        conda-forge

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

> install.packages(c('DT', 'ROCR', 'caTools', 'lubridate', 'rjson', 'littler', 'docopt', 'formatR', 'remotes', 'selectr'), )   # dependencies=TRUE

...
> quit()
```

# Modelling packages: 

```
# Run in R prompt 
> install.packages(c("biomod2"), dependencies=TRUE )


# Adding geospatial packages
> install.packages(c("RColorBrewer", "deldir", "gstat", "maptools", "mapdata", "rgeos", "geoR", "geosphere", "spdep","sp"))
```

```
# NOTE
Warning messages:
1: packages ‘r-spacetime’, ‘r-spatstat’ are not available (for R version 3.5.1) 
2: In install.packages(c("RColorBrewer", "RandomFields", "classInt",  :
  installation of package ‘units’ had non-zero exit status
3: In install.packages(c("RColorBrewer", "RandomFields", "classInt",  :
  installation of package ‘sf’ had non-zero exit status

```
```
Warning messages:
1: package ‘earth’ is not available (for R version 3.4.1) 
2: In install.packages(c("earth", "dismo", "biomod2")) :
  installation of package ‘biomod2’ had non-zero exit status
``` 










