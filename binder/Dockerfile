FROM pangeo/pangeo-notebook:2020.03.27
USER root
RUN apt-get update && apt-get install -y build-essential && rm -rf /var/lib/apt/lists/*
USER jovyan

RUN git clone https://github.com/facebook/prophet
RUN cd prophet/python && python -m pip install -e .
