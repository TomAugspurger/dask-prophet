FROM pangeo/pangeo-notebook:2020.04.22
USER root
RUN apt-get update && apt-get install -y build-essential && rm -rf /var/lib/apt/lists/*
USER jovyan

RUN git clone https://github.com/TomAugspurger/prophet
RUN cd prophet/python && \
  git checkout parallel && \
  conda uninstall -n notebook python-dateutil --force -y && \
  conda run -n notebook python -m pip install -e .
