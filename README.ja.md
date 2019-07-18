# Foundation
機械学習研究のためのDockerfile

## Usage
このリポジトリで管理されているDockerfileは、Docker Hubの[hkawashima/foundation](https://hub.docker.com/r/hkawashima/foundation)からビルド済みのものを入手可能です。

### tag: core
タグ名に `core` が付いているイメージは最もシンプルな構成のDockerイメージです。
以下の `tag: lab` などはこのイメージをベースにしています。
起動には、以下のオプションを指定してください。

```sh
docker run -it hkawashima/foundation:cpu-core
```

このイメージには、以下の主要ライブラリが含まれています。

*   PyTorch
*   Torchvision
*   Scikit-Learn
*   Matplotlib
*   Seaborn
*   Pandas


### tag: lab
タグ名に `lab` が付いているイメージには `Jupyter Lab` が含まれています。
起動には、以下のオプションを指定してください。

```sh
docker run -it -p 8888:8888 hkawashima/foundation:cpu-lab
```

その後、ホストのブラウザで `localhost:8888` に接続することで `IDE` を起動することができます。



