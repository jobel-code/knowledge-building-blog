# Anaconda python distribution
## [bioconda](https://bioconda.github.io/).

**Bioconda supports only 64-bit Linux and Mac OSX.**

When using Bioconda please cite the article [Grüning, Björn, Ryan Dale, Andreas Sjödin, Brad A. Chapman, Jillian Rowe, Christopher H. Tomkins-Tinch, Renan Valieris, the Bioconda Team, and Johannes Köster. 2018. “Bioconda: Sustainable and Comprehensive Software Distribution for the Life Sciences”. Nature Methods, 2018.](https://doi.org/10.1038/s41592-018-0046-7).

Each package added to Bioconda also has a corresponding Docker [BioContainer](https://biocontainers.pro/) automatically created and uploaded to Quay.io.

### Setup channels

It is important to add them in this order so that the priority is set correctly (that is, conda-forge is highest priority).

```
conda config --add channels defaults
conda config --add channels bioconda
conda config --add channels r
conda config --add channels conda-forge
```


# (Optional) Install the jupyter notebook jupyter notebook extensions.
[See](https://ndres.me/post/best-jupyter-notebook-extensions/)

```
conda install -c conda-forge jupyter_contrib_nbextensions
conda install -c conda-forge jupyter_nbextensions_configurator
```



# Make sure conda install -c conda-forge gdal #is installed


# Set environment variables(optional???)
(for conda only) export GDAL_DATA="/home/jobel/anaconda3/share/gdal/"
(for conda only) export GEOS_DIR="/home/jobel/anaconda3"

# Only if the later fails
[https://gis.stackexchange.com/questions/193814/installing-gdal2-1/193828#193828](https://gis.stackexchange.com/questions/193814/installing-gdal2-1/193828#193828)
```
sudo add-apt-repository -y ppa:ubuntugis/ubuntugis-unstable
sudo apt update
sudo apt upgrade # if you already have gdal 1.11 installed
sudo apt install gdal-bin python-gdal python3-gdal # if you don't have gdal 1.11 already installed

```
# REQUIRED AMASING
`conda install -c conda-forge xmltodict`

`conda install -c conda-forge pyproj`

`conda install -c conda-forge geopy`

`conda install -c conda-forge geopandas shapely rasterio`

```
conda install -c conda-forge --quiet --yes \
# blaze is used in SHARK data
blaze \  
geopandas \
scipy-sugar \
tinydb \
bcrypt \
passlib \
libgdal \
geopy \
folium \
rasterio \
ipyleaflet \
bqplot \
cmocean \
cartopy \
iris \
shapely \
pyproj \
fiona \
xmltodict
```


# Install jupyter widgets
[http://jupyter.org/widgets](http://jupyter.org/widgets)

# (Optional) Install beakerx widgets

Useful for tables, plotting and forms
`conda install -c conda-forge beakerx ipywidgets`

# (Optional) Install ipyleaflet

[conda install -c conda-forge ipyleaflet](conda install -c conda-forge ipyleaflet)


# Python stats
[See https://www.marsja.se/repeated-measures-anova-using-python/](https://www.marsja.se/repeated-measures-anova-using-python/)

`pip install pyvttbl`

**notes** `Pyvttbl` enables you to create multidimensional pivot tables, process data and carry out statistical tests.


# Google SDK
sudo pip install firebase-admin
