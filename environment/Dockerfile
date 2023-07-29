# hash:sha256:0923a0dc5a17796c3f291e2dd462575d695b825267f784d0cd5c14ab5df04049
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

COPY postInstall /
RUN /postInstall
