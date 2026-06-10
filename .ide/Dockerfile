FROM continuumio/miniconda3:latest

ENV DEBIAN_FRONTEND=noninteractive
ENV PYTHONUNBUFFERED=1

WORKDIR /workspace

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        bash \
        build-essential \
        ca-certificates \
        curl \
        git \
        wget \
    && rm -rf /var/lib/apt/lists/*

COPY environment.yml /tmp/environment.yml

RUN conda env create -f /tmp/environment.yml \
    && conda clean -afy

SHELL ["bash", "-lc"]

RUN source /opt/conda/etc/profile.d/conda.sh \
    && conda activate llm_algo_cnb \
    && python -m pip install --upgrade pip

ENV PATH="/opt/conda/envs/llm_algo_cnb/bin:${PATH}"
