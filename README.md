# install_ubuntu-16.04_tensorflow-gpu
These instructions are intended to set up a deep learning environment for GPU-powered tensorflow.

After following these instructions you'll have:
1. CUDA 9.0
2. cnDNN 7.0.5
3. Tensorflow-gpu 1.8.0

---

## Sewoony's Install Env<br>

| OS | GPU | PYTHON |
|:---:|:---:|:---:|
| Ubuntu 16.04 | NVIDIA GIX 1080 | 3.5 |

---

## CUDA & cuDNN<br>
There are two different versions of Tensorflow : CPU / GPU<br>
To use the Tensorflow-gpu version you need to install CUDA and cuDNN.<br>
There is a different version to install for each TF version.<br>
Starting with version 1.5, CUDA 9 and cuDNN 7 are required.<br>

| TF version | CUDA | cuDNN |
|:---:|:---:|:---:|
|TF 1.8|9|7|
|~|9|7|
|TF 1.5|9|7|
|TF 1.4|8|6|

Also, the version of CUDA and cuDNN that can be installed for each graphics card may be different.<br>
You should check your graphic card and check the version of TF that matches your graphics card.<br>

---

## Install CUDA 9.0<br>
There is a minimum version of the graphics driver required when installing CUDA.<br>

|   CUDA version   | Driver |
|:---:|:---:|
|CUDA 9.2|396.xx|
|CUDA 9.1|387.xx|
|CUDA 9.0|384.xx|
|CUDA 8.0(GA2)|375.xx|
|CUDA 8.0|367.4x|
|CUDA 7.5|352.xx|
|CUDA 7.0|346.xx|

Check the nvidia-smi command for the currently installed graphics driver.<br>
If it does not work, just go to CUDA download.

```bash
$ nvidia-smi
```

![nvidia-smi](https://user-images.githubusercontent.com/43063889/46713909-d7f1b180-cc93-11e8-8ffc-b675a83de3c3.png)
If your graphics driver version is low or high, you may not be able to install CUDA.
The CUDA installation file contains the minimum required graphics drivers.
Therefore, it is safe to delete and install existing drivers.

```bash
$ sudo apt-get purge nvidia-*
```

If you install CUDA with a driver already installed, you can downgrade if your graphics driver is up to date.

[CUDA DOWNLOAD LINK](https://developer.nvidia.com/cuda-90-download-archive?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1604&target_type=deblocal)
