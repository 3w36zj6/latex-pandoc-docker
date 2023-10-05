# latex-pandoc-docker

[![Publish Docker image](https://github.com/3w36zj6/latex-pandoc-docker/actions/workflows/publish-docker-image.yml/badge.svg)](https://github.com/3w36zj6/latex-pandoc-docker/actions/workflows/publish-docker-image.yml)
[![Docker Image Size](https://badgen.net/docker/size/3w36zj6/pandoc?icon=docker&label=image%20size)](https://hub.docker.com/r/3w36zj6/pandoc/)

Docker image for LaTeX and Pandoc

## Installation

### From Docker Hub

```sh
docker pull 3w36zj6/pandoc
docker tag 3w36zj6/pandoc pandoc
```

### From GitHub Packages

```sh
docker pull ghcr.io/3w36zj6/pandoc
docker tag ghcr.io/3w36zj6/pandoc pandoc
```

## Usage

実行例を以下に示します。

```sh
docker run -it --rm -v $(pwd):/workdir pandoc [OPTIONS] [FILES]
```
