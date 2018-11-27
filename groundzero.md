# When things goes wrong.

# clean your conda environment

## Careful this is highly destructive. DO NOT RUN IF YOU ARE UNSURE OF THE CONSEQUENCES.
`conda clean --all -y`
`rm -rf /home/jobel/.condarc`
`rm -rf /home/jobel/anaconda3`
`rm -rf /home/jobel/.conda/`


# Re-install using miniconda
```
wget --quiet -O ~/miniconda.sh \
        http://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh

chmod +x ~/miniconda.sh

 ~/miniconda.sh -b -f -p ~/miniconda3 && rm ~/miniconda.sh

# Ensure added  vim .bashrc
 `export PATH="/home/username/miniconda/bin:$PATH"`

```
### Setup channels
It is important to add them in this order so that the priority is set correctly (that is, conda-forge is highest priority).

```
conda config --system --append channels IOOS && \
conda config --system --append channels bioconda && \
conda config --system --append channels r && \
conda config --system --append channels conda-forge
conda config --system --set show_channel_urls true

conda update conda --quiet --yes
```
# Create your environment

# some packages still need the python 3.6
`conda create --name amasing python=3.6 conda`


#
conda install -c conda-forge --yes --quiet --name amasing \
        crcmod \
        dask \
        dill \
        google-api-python-client \
        httplib2 \
        h5py \
        ipykernel \
        ipywidgets \
        jinja2 \
        jsonschema \
        jupyterlab \
        matplotlib \
        mock \
        nltk \
        notebook \
        numpy \
        oauth2client \
        pandas-gbq \
        pandas \
        pandocfilters \
        pillow \
        pip \
        plotly \
        psutil \
        pygments \
        python-dateutil \
        python-snappy \
        pytz \
        pyzmq \
        requests \
        scikit-image \
        scikit-learn \
        scipy \
        seaborn \
        six \
        statsmodels \
        sympy \
        tornado \
        widgetsnbextension \
        xgboost

pip install --quiet -U --upgrade-strategy only-if-needed --no-cache-dir \
bs4 \
ggplot \
google-cloud-monitoring \
lime \
protobuf \
tensorflow \
s2sphere


## if you plan to install gdal
`export GDAL_DATA="/home/username/miniconda3/share/gdal/"`
`export GEOS_DIR="/home/username/miniconda3"`




# OR USE THE Anaconda3 full distribution

`bash ~/Downloads/Anaconda3-5.3.1-Linux-x86_64.sh`
## accept the installer to initialize Anaconda3
`/home/jobel/.bashrc`
# close terminal or issue `source ~/.bashrc`


`anaconda navigator`



It is important to add them in this order so that the priority is set correctly (that is, conda-forge is highest priority).




#
# To activate this environment, use:
# > source activate amasing
#
# To deactivate an active environment, use:
# > source deactivate
#



# REQUIRED AMASING
```
conda install -c conda-forge xmltodict

conda install -c conda-forge pyproj

conda install -c conda-forge geopy

conda install -c conda-forge geopandas shapely rasterio


conda install -c conda-forge --quiet --yes \

# geopandas \  ## REQUIRES py36 not yet available for 3.7 [2018-11-27]
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
