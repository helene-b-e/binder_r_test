
# Testing Binder for R with some esd examples


RStudio:[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/helene-b-e/binder_r_test.git/master?urlpath=rstudio)

Press the above image to launch an Rstudio session loading [**_esd_**](https://github.com/metno/esd/wiki)



Jupyter+R [![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/helene-b-e/binder_r_test.git/master?filepath=ESD_binder_test.ipynb) 
(Jupyter running on the [IRkernel](https://github.com/IRkernel/IRkernel) )

As of now the nbviewer preview does not show, but press "show build logs" or something and you will se that the instance is loading. It might take a minute.

https://mybinder.org/v2/gh/helene-b-e/binder_r_test.git/master


To replicate: have files specifing the build in the main repo or in a folder called binder. I have 

binder/apt.txt : \
libnetcdf-dev

binder/install.R :  \
install.packages("ncdf4") \
install.packages("zoo") \
install.packages("devtools") \
install.packages("knitr") \
install.packages("RgoogleMaps") \
devtools::install_github("metno/esd")\

binder/requirements.txt : \
jupytext

binder/runtime.txt : \
r-2018-07-10


requirements.txt with Jupytext is to be able to run Rmarkdown in Jupyter. For this one also  [needs](https://github.com/mwouts/jupytext/blob/master/.jupyter/jupyter_notebook_config.py) : 
.jupytext/jupyter_notebook_config.py :
c.NotebookApp.contents_manager_class = 'jupytext.TextFileContentsManager' 

Afterwards copy your github repository name and add the information here:
https://mybinder.org/#

You can recieve an url-link to RStudio by choosing URL where it says "Path to a notebook file (optional)" and then writing 'rstudio': 
https://mybinder.org/v2/gh/helene-b-e/binder_r_test.git/master?urlpath=rstudio


