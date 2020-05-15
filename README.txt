# Infrastructure for reproducibility

## Building the container

Assuming `docker` installed, open a terminal and navigate to this folder:

```
cd /path/to/this/folder
```

Then run the following to build the container:

```
docker build -t region_satellites .
```

This might take a little bit, depending on your previous set-up and your connection but, once it finishes, you should be able to see `region_satellites` on the list that comes up when you run `docker image list`.

## Running the container

Since it is built on the same platform, the container can be executed in almost the same way you would run the [`gds_env`](https://github.com/darribas/gds_env). From the folder that you want to use as the base, run:

```
docker run --rm -ti -p 8888:8888 -v ${PWD}:/home/jovyan/work region_satellites
```

This will spin up a local JupyterLab instance that you can access through your browser on the `localhost:8888` address. You will be asked for a token that you can copy from the initial log printed after launching the container. The message should look something like:

```
Executing the command: jupyter notebook
[I 19:56:55.586 NotebookApp] Writing notebook server cookie secret to /home/jovyan/.local/share/jupyter/runtime/notebook_cookie_secret
[I 19:56:56.329 NotebookApp] Loading IPython parallel extension
[I 19:56:56.593 NotebookApp] JupyterLab extension loaded from /opt/conda/lib/python3.7/site-packages/jupyterlab
[I 19:56:56.594 NotebookApp] JupyterLab application directory is /opt/conda/share/jupyter/lab
[I 19:56:57.657 NotebookApp] Serving notebooks from local directory: /home/jovyan
[I 19:56:57.657 NotebookApp] The Jupyter Notebook is running at:
[I 19:56:57.657 NotebookApp] http://4c877fd2f09d:8888/?token=445ea1d4e64ad6fd12151805133e07126265182a3a4d3734
[I 19:56:57.657 NotebookApp]  or http://127.0.0.1:8888/?token=445ea1d4e64ad6fd12151805133e07126265182a3a4d3734
[I 19:56:57.662 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[C 19:56:57.669 NotebookApp]

    To access the notebook, open this file in a browser:
        file:///home/jovyan/.local/share/jupyter/runtime/nbserver-6-open.html
    Or copy and paste one of these URLs:
        http://4c877fd2f09d:8888/?token=445ea1d4e64ad6fd12151805133e07126265182a3a4d3734
     or http://127.0.0.1:8888/?token=445ea1d4e64ad6fd12151805133e07126265182a3a4d3734
```

In this case, the token would be `445ea1d4e64ad6fd12151805133e07126265182a3a4d3734`. Copy it from the terminal and paste it on your browser where it is asked for. You are good to go to reproduce the paper!