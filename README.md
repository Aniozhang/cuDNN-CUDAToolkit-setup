# cuDNN-CUDAToolkit-setup
✅ CUDA Toolkit → General GPU computing, required for PyTorch/TensorFlow. \
✅ cuDNN → Optimized deep learning kernels for CNNs, RNNs, etc. \
✅ Both are required for deep learning frameworks to use the GPU effectively.

# cuDNN Setup
Operating System: Linux \
Architecture: x86_64 \
Distribution: Ubuntu \
Version: 24.04 \
Installer Type: deb(local)
## Base Installer
Installation Instructions: 
```sh
$ wget https://developer.download.nvidia.com/compute/cudnn/9.8.0/local_installers/cudnn-local-repo-ubuntu2404-9.8.0_1.0-1_amd64.debsudo
$ dpkg -i cudnn-local-repo-ubuntu2404-9.8.0_1.0-1_amd64.debsudo
$ cp /var/cudnn-local-repo-ubuntu2404-9.8.0/cudnn-*-keyring.gpg /usr/share/keyrings/
$ sudo apt-get update
$ sudo apt-get -y install cudnn

```
To install for CUDA 11, perform the above configuration but install the CUDA 11 specific package:
```sh
$ sudo apt-get -y install cudnn-cuda-11

```
To install for CUDA 12, perform the above configuration but install the CUDA 12 specific package:
```sh
$ sudo apt-get -y install cudnn-cuda-12

```
# CUDA Toolkit 12.8 Update 1 Downloads
Operating System: Linux \
Architecture: x86_64 \
Distribution: Ubuntu \
Version: 24.04 \
Installer Type: deb(local)

## CUDA Toolkit Installer
Installation Instructions:
```sh
$ wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2404/x86_64/cuda-ubuntu2404.pin
$ sudo mv cuda-ubuntu2404.pin /etc/apt/preferences.d/cuda-repository-pin-600
$ wget https://developer.download.nvidia.com/compute/cuda/12.8.1/local_installers/cuda-repo-ubuntu2404-12-8-local_12.8.1-570.124.06-1_amd64.deb
$ sudo dpkg -i cuda-repo-ubuntu2404-12-8-local_12.8.1-570.124.06-1_amd64.deb
$ sudo cp /var/cuda-repo-ubuntu2404-12-8-local/cuda-*-keyring.gpg /usr/share/keyrings/
$ sudo apt-get update
$ sudo apt-get -y install cuda-toolkit-12-8

```
## Driver Installer
NVIDIA Driver Instructions (choose one option) \
To install the open kernel module flavor:
```sh
sudo apt-get install -y nvidia-open

```
To install the proprietary kernel module flavor:
```sh
sudo apt-get install -y cuda-drivers

```
### Conditional usage

| **Use Case**  | **Recommended Module**  |
|--------------|---------------------|
| Gaming (GeForce, RTX) | **Proprietary (PKM)** |
| AI/Deep Learning (CUDA, cuDNN) | **Proprietary (PKM)** |
| Datacenter GPUs (A100, Tesla, etc.) | **Open Kernel Module (OKM)** |
| Open-source development | **OKM (if your GPU supports it)** |
| Running the latest Linux kernel | **OKM (fewer compatibility issues)** |

### References
- 📌 [cuDNN 9.8.0 Downloads](https://developer.nvidia.com/cudnn-downloads?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=24.04&target_type=deb_local)
- 📌 [CUDA Toolkit 12.8 Update 1 Downloads](https://developer.nvidia.com/cuda-downloads?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=24.04&target_type=deb_local)



