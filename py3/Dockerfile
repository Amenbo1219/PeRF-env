FROM pytorch/pytorch:2.0.1-cuda11.7-cudnn8-devel
RUN ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime
ARG CUDA_ARCHITECTURES=90;89;86;80;75;70;61;52;37
ENV TCNN_CUDA_ARCHITECTURES=${CUDA_ARCHITECTURES}
# パッケージの追加とタイムゾーンの設定
# 必要に応じてインストールするパッケージを追加してください
RUN apt-get update && apt-get install -y \ 
    tzdata \
    git \ 
    wget \
    libglib2.0-0 \
    libsm6  \ 
    libxrender1  \ 
    libxext6 \
    libgl1-mesa-dev \
&&  apt-get clean \
&&  rm -rf /var/lib/apt/lists/*
# JupyterLab関連のパッケージ（いくつかの拡張機能を含む）
# 必要に応じて、JupyterLabの拡張機能などを追加してください


# 研究室用追加パッケージ
RUN pip install --no-cache-dir \
    pip install praat-parselmouth

#　追加パッケージのインストール
RUN pip3 install --upgrade pip
RUN pip3 install tensorboard ninja git+https://github.com/NVlabs/tiny-cuda-nn/#subdirectory=bindings/torch
