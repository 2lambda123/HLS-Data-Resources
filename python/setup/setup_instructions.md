# Repository Setup Instructions

The tutorials in this repository require a compatible Python Environment, an installation of [Git](https://git-scm.com/downloads). To setup the environment follow the steps in sections 1. To access or download HLS granules, a `.netrc` file with your NASA Earthdata Login information is needed.`earthaccess.login(persist=True)` function uses an existing `.netrc` file for authentication purposes. If one does not exist, it will prompt for your NASA Earthdata username and password. If you do not have a NASA Earthdata account, please register [here](https://urs.earthdata.nasa.gov/users/new).

+ If you do not have an Environment Manager installed, we recommend  [Anaconda](https://www.anaconda.com/products/distribution) or [miniconda](https://docs.conda.io/en/latest/miniconda.html). When installing, Anaconda or Miniconda be sure to check the box to "Add Anaconda to my PATH environment variable" to enable use of conda directly from your command line interface.
+ We also recommend using [mamba](https://mamba.readthedocs.io/en/latest/) with conda to manage packages. It typically offers higher speed and more reliable environment solutions. To install mamba, use your preferred command line interface (command prompt, terminal, cmder, etc.) and type the following:

    > `conda install mamba -n base -c conda-forge`  

+ If you do not have Git, you can download it [here](https://git-scm.com/downloads).  

## 1. Python Environment Setup  

This Python Environment will work for all tutorials within this repository. Using your preferred command line interface (command prompt, terminal, cmder, etc.) navigate to your local copy of the repository, then type the following to create a compatible Python environment:

> `mamba create -n hls_tutorial -c conda-forge --yes  python=3.9 gdal=3.7.0 hvplot=0.8.4 geoviews=1.9.6 rioxarray rasterio jupyter geopandas earthaccess jupyter_bokeh`

Activate the environment:

> `conda activate hls_tutorial`

Then use pip to install the scikit-image library and its dependencies (version 0.21.0 is not on a conda channel yet)

> `pip install scikit-image`

Note: you can also use the included `.yml` file if on Windows:  

> `mamba env create -f python/setup/hls_tutorial_windows.yml`  

## 2. Opening the notebooks

If you did the above and already have your environment activated, you can simply launch Jupyter Notebook by typing the following in command line:

> `jupyter notebook`

If returning to an already created but inactive environment, using your preferred command line interface (command prompt, terminal, cmder, etc.) navigate to your local copy of the repository, then type the following to activate the Python Environment:

> `conda activate hls_tutorial`  

Now you can launch Jupyter Notebook to open the notebooks included.

> `jupyter notebook`  

[Additional information](https://conda.io/docs/user-guide/tasks/manage-environments.html) on setting up and managing Conda environments.  

**Still having trouble getting a compatible Python environment set up? Contact [LP DAAC User Services](https://lpdaac.usgs.gov/lpdaac-contact-us/).**  

## Contact Info  

Email: <LPDAAC@usgs.gov>  
Voice: +1-866-573-3222  
Organization: Land Processes Distributed Active Archive Center (LP DAAC)¹  
Website: <https://lpdaac.usgs.gov/>  
Date last modified: 06-22-2023  

¹Work performed under USGS contract G15PD00467 for NASA contract NNG14HH33I.  
