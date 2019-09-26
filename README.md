[English](README.md) | [日本語](README.ja.md)

# Foundation

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/08c1f2f2f2994da098439e4c3614b8e2)](https://app.codacy.com/app/KawashimaHirotaka/foundation?utm_source=github.com&utm_medium=referral&utm_content=KawashimaHirotaka/foundation&utm_campaign=Badge_Grade_Dashboard)

Dockerfiles for research of machine learning.

## Usage
Those images are hosted on [Docker Hub](https://hub.docker.com/r/hkawashima/foundation).
So please pull image and run it.

These container images have the following libraries and applications installed by default.

* Python 3.6.8
* PyTorch >= 1.1.0
* Torchvision
* Comet-ML
* Scikit-Learn
* Pandas
* matplotlib
* Seaborn

### tag: core
the most simple container images. 
these container images tagged `lab` are based on `core`.

```sh
docker run -it hkawashima/foundation:core-forCPU
```

if you want to run container on your GPU, you should use `core-forCUDA`.

```sh
docker run -it --runtime=nvidia hkawashima/foundation:core-forCUDA
```

### tag: lab
these container images contain `Jupyter Lab`.


```sh
docker run -it -p 8888:8888 hkawashima/foundation:lab-forCPU
```

and access `localhost:8888` on your web browser.
