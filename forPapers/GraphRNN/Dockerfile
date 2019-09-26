FROM pytorch/pytorch:0.4_cuda9_cudnn7

# Dockerfile for GraphRNN: Generating Realistic Graphs with Deep Auto-regressive Model
# You need the NVIDIA GPU if you want to run the container which was built from this Dockerfile.

RUN git clone https://github.com/JiaxuanYou/graph-generation && \
    cd graph-generation && \
    pip install --upgrade \
    pip \
    setuptools \
    numpy==1.14.5 \
    matplotlib \
    edward \
    observations \
    scikit-learn \
    python-louvain &&\
    pip install -r requirements.txt

