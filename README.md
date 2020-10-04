# Testing GitHub Actions

## Build Conda Package

1. Set up:
  * `mamba-version: "*"`
  * `auto-update-conda: "true"`
  * `conda-build-version: "3.20"
2. Build package based on `path/to/conda/meta.yml`:
  * `mamba build path/to/conda --R 4.0`
3. Upload package to anaconda
  * `anaconda -t ${{ secrets.ANACONDA_TOKEN }} upload ${HOME}/miniconda3/conda-bld/**/*.tar.bz2`
4. Create conda environment containing new package and pkgdown
  * `channels: "pdiakumis,conda-forge,bioconda"`
  * `mamba create -n pkgdown r-gpgr r-pkgdown`
5. Run pkgdown
