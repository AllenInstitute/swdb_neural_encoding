# hash:sha256:139a29d4a535bab10c78220d0b8a84fcf921dc50b402120d16df325d6a1dd624
FROM registry.codeocean.allenneuraldynamics.org/codeocean/jupyterlab:3.0.9-miniconda4.9.2-python3.8-ubuntu20.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN conda install -y --channel=conda-forge \
        matplotlib==3.3.2 \
        numpy==1.24.3 \
        pandas==1.4.2 \
        scikit-learn==1.1.1 \
    && conda clean -ya
