FROM jupyterhub/jupyterhub:latest
LABEL maintainer="jason.chong2@gmail.com"

RUN apt-get update && \
    apt-get install build-essential software-properties-common -y

RUN pip install --upgrade pip
RUN pip install npm
RUN pip install jupyterlab

RUN jupyter serverextension enable --py jupyterlab
RUN jupyter labextension install @jupyterlab/hub-extension
RUN jupyter labextension install @jupyterlab/google-drive
RUN jupyter labextension install @jupyterlab/git
RUN pip install jupyterlab-git
RUN jupyter serverextension enable --py jupyterlab_git

EXPOSE 8888