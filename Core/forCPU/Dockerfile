FROM continuumio/miniconda3:4.6.14

ENV CONDA_DIR="/opt/conda"
ENV PATH="$CONDA_DIR/bin:$PATH"

RUN apt-get update && apt-get install -y vim
RUN conda update -y -n base conda \
    && conda install -y pytorch-cpu torchvision-cpu -c pytorch \
    && conda install -y scikit-learn \
    && conda install -y matplotlib \
    && conda install -y seaborn \
    && conda install -y pandas

RUN useradd -m user
USER user
WORKDIR /home/user
