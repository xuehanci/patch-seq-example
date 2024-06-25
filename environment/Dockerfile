# hash:sha256:a4b9a494d309cb442576e3cdce0f090456267a00b1997af5263346a9a1757e4c
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/jupyterlab:3.6.1-miniconda4.12.0-python3.9-ubuntu20.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN pip install -U --no-cache-dir \
    pyarrow==16.1.0 \
    umap==0.1.1 \
    -e git+https://github.com/AllenInstitute/ipfx@622b8ffbb631c272b5281c5eebf1e73acfc65833#egg=ipfx
