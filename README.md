# install_ubuntu-16.04_tensorflow-gpu
These instructions are intended to set up a deep learning environment for GPU-powered tensorflow.

After following these instructions you'll have:
1. CUDA 9.0
2. cnDNN 7.0.5
3. Tensorflow-gpu 1.8.0

---

__Install Env__

| OS | GPU | PYTHON |
|:---:|:---:|:---:|
| Ubuntu 16.04 | NVIDIA GIX 1080 | 3.5 |

__CUDA & cuDNN__
There are two different versions of Tensorflow : CPU / GPU<br>
To use the Tensorflow-gpu version you need to install CUDA and cuDNN.<br>
There is a different version to install for each TF version. <br>
Starting with version 1.5, CUDA 9 and cuDNN 7 are required.

| TF version | CUDA | cuDNN |
|:---:|:---:|:---:|
|TF 1.8|9|7|
|~|9|7|
|TF 1.5|9|7|
|TF 1.4|8|6|

Also, the version of CUDA and cuDNN that can be installed for each graphics card may be different. <br>
You should check your graphic card and check the version of TF that matches your graphics card.
