FROM nvcr.io/nvidia/pytorch:22.07-py3

# install additional runtime dependencies
RUN apt-get update && apt-get install -y \
    git \
    curl \
    && rm -rf /var/lib/apt/lists/*

# Install Python packages
RUN pip install --no-cache-dir \
    supervision \
    numpy \
    matplotlib \
    pandas 

