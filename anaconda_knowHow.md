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
conda config --add channels conda-forge
```
