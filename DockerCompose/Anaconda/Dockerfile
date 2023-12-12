FROM continuumio/anaconda3

ADD ./conf/requirements.txt /

RUN conda install -c conda-forge gcc
RUN pip install --upgrade setuptools && pip install -r requirements.txt
RUN mkdir -p /root/.jupyter
COPY ./conf/jupyter_notebook_config.json /root/.jupyter/jupyter_notebook_config.json

EXPOSE 8888
