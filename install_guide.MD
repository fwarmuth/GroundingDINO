# System Requirements
```
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2204/x86_64/cuda-keyring_1.0-1_all.deb \
    && dpkg -i cuda-keyring_1.0-1_all.deb \
    && rm cuda-keyring_1.0-1_all.deb \
    && apt-get update \
    && apt-get install -y --no-install-recommends libnccl2 libnccl-dev
```
# Install modules in venv
```
python3 -m venv .venv
```
# Install dependencies manually to fix cuda and torch versions
```
./.venv/bin/activate
pip3 install -r requirements_mod.txt
```
# Build groundingDINO
```
export CUDA_HOME=/usr/local/cuda-11.7
./.venv/bin/activate
pip3 install -e .
```

