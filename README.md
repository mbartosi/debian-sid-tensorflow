# debian-sid-tensorflow
Debian Sid Tensorflow build howto and optimized wheels:

Create required directories and links: copy 'cuda' link directory contents to '/usr/local/cuda' and chown to root. 

```
```

## Build your own optimized wheel under Debian Sid:
Install development libraries and CUDA 9.2 from Debian Sid repository:
```
apt install build-essential git nvidia-cuda-toolkit libcupti-dev
apt install python3-dev python3-numpy python3-wheel python3-setuptools python3-six python3-pip
apt install python3-keras-applications python3-keras-preprocessing python3-mock
```
Download form NVIDIA and install cuDNN v7.5.0 for CUDA 9.2 and NCCL v2.4.2 for CUDA 9.2.

Instal bazel 0.21.0 from https://github.com/bazelbuild/bazel/releases/tag/0.21.0 (use https://github.com/bazelbuild/bazel/releases/download/0.21.0/bazel-0.21.0-installer-linux-x86_64.sh under jour user account and add to PATH).


Checkout tensorflow from https://github.com/tensorflow/tensorflow (select a release, for example v2.0.0-alpha0).
Configure and build GPU version using instructions from https://www.tensorflow.org/install/source

## Verify the installation:

```
python3
Python 3.7.3 (default, Mar 26 2019, 07:25:18) 
[GCC 8.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import tensorflow as tf
>>> tf.__version__
'2.0.0-alpha0'
```

## Available wheels:
|TensorFlow|CUDA|CuDNN|TensorRT|Python|NCCL|Compute Capability|OS|Link|
|---:|---:|---:|---:|---:|---:|---:|:---:|:---:|
|2.0.0a0|9.2|7.5|-|3.7|2.4|6.1|Linux|[](https://github.com/)|
