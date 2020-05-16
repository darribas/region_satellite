# Infrastructure for reproducibility

## Build a Docker image of our repository

Go to :https://mybinder.org/, then enter: https://github.com/meixuchen/region_satellite as Github, Click launch. 

It will take about 20mins to build a Docker image at the first time. If an image has already been built for the given repository, it will not be rebuilt next time. 

## Interacting with the notebooks

Since it is built, A JupyterHub server will host you to our repository's content. You can open the notebook and start reproducing the results. 

You are good to go to reproduce the paper!

NOTE: SIMSUN is a font file used for showing chinese character, it cannot be suppported in Binder, but if you downloaded this file to your own machine, and run the notebook in your conda environment, it will work.
