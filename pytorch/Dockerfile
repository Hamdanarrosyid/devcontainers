FROM nvidia/cuda:12.6.2-cudnn-devel-ubuntu22.04

RUN apt-get update && \
    apt-get install -y python3 python3-pip git wget curl || \
    (cat /var/log/apt/term.log && exit 1)

RUN pip install --no-cache-dir \
    supervision \
    numpy \
    matplotlib \
    pandas \
    ipykernel \
    scikit-learn

RUN pip install --no-cache-dir \
    torch \
    torchvision \
    torchaudio \
    --index-url https://download.pytorch.org/whl/cu126

    
ENV DEBIAN_FRONTEND=noninteractive
ENV CUDA_HOME=/usr/local/cuda
ENV PATH=${CUDA_HOME}/bin:${PATH}
ENV LD_LIBRARY_PATH=${CUDA_HOME}/lib64:${LD_LIBRARY_PATH}
