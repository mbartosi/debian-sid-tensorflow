# debian-sid-tensorflow
Debian Sid Tensorflow build howto and optimized wheels

Create required directories and links:
```

```

## Build your own optimized wheel under Debian Sid:
Install development libraries and CUDA:
```
apt install build-essential git nvidia-cuda-toolkit libcupti-dev
apt install python3-dev python3-numpy python3-wheel python3-setuptools python3-six python3-pip
apt install python3-keras-applications python3-keras-preprocessing python3-mock
```


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
