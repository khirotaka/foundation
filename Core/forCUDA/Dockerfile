FROM nvidia/cuda:10.0-cudnn7-runtime-ubuntu18.04

ENV PATH $PATH:/root/.local/bin

WORKDIR /tmp/python
RUN apt update && apt install -y --no-install-recommends \
        build-essential \
        cmake \
        git \
        curl \
        vim \
        ca-certificates \
        libjpeg-dev \
        libpng-dev \
        python3-pip \
        python3-setuptools && \
    rm -rf /var/lib/apt/lists/* && \
    pip3 install -U pip

RUN pip3 install --user \
    torch \
    torchvision \
    comet-ml \
    pandas \
    tqdm \
    scikit-learn \
    seaborn \
    pipenv

WORKDIR /workspace
RUN chmod -R a+w .

