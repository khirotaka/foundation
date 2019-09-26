FROM continuumio/miniconda3:4.6.14

RUN pip install --upgrade pip setuptools && \
    pip install networkx pandas tqdm texttable PyGSP numpy

WORKDIR /workspace
RUN chmod -R a+w .

RUN git clone https://github.com/benedekrozemberczki/GraphWaveMachine

WORKDIR /workspace/GraphWaveMachine

