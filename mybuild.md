1. GCC

```
gcc --version

(base) s42sdamm@photolab96:~/Documents/thesis/Photo-SLAM$ gcc --version
gcc (Ubuntu 9.4.0-1ubuntu1~20.04.2) 9.4.0
Copyright (C) 2019 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```

2. CMake

```
cmake --version

(base) s42sdamm@photolab96:~/Documents/thesis/Photo-SLAM$ cmake --version
cmake version 3.16.3

CMake suite maintained and supported by Kitware (kitware.com/cmake).
```

3. Conda
```
conda create -n photoslam python==3.10
conda activate photoslam
```

4. NVCC by default
```
nvcc -V

(photoslam) s42sdamm@photolab96:~/Documents/thesis/Photo-SLAM$ nvcc -V
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2019 NVIDIA Corporation
Built on Sun_Jul_28_19:07:16_PDT_2019
Cuda compilation tools, release 10.1, V10.1.243
```

5. Nvidia Driver
```
nvidia-smi

(photoslam) s42sdamm@photolab96:~/Documents/thesis/Photo-SLAM$ nvidia-smi
Sat Jun  1 20:16:32 2024       
+-----------------------------------------------------------------------------------------+
| NVIDIA-SMI 550.54.14              Driver Version: 550.54.14      CUDA Version: 12.4     |
|-----------------------------------------+------------------------+----------------------+
| GPU  Name                 Persistence-M | Bus-Id          Disp.A | Volatile Uncorr. ECC |
| Fan  Temp   Perf          Pwr:Usage/Cap |           Memory-Usage | GPU-Util  Compute M. |
|                                         |                        |               MIG M. |
|=========================================+========================+======================|
|   0  NVIDIA GeForce RTX 2080 ...    Off |   00000000:01:00.0  On |                  N/A |
| 18%   37C    P8              5W /  250W |    1294MiB /   8192MiB |      2%      Default |
|                                         |                        |                  N/A |
+-----------------------------------------+------------------------+----------------------+
                                                                                         
+-----------------------------------------------------------------------------------------+
| Processes:                                                                              |
|  GPU   GI   CI        PID   Type   Process name                              GPU Memory |
|        ID   ID                                                               Usage      |
|=========================================================================================|
|    0   N/A  N/A      2001      G   /usr/lib/xorg/Xorg                            102MiB |
|    0   N/A  N/A      2265      G   /usr/lib/xorg/Xorg                            486MiB |
|    0   N/A  N/A      2395      G   /usr/bin/gnome-shell                          151MiB |
|    0   N/A  N/A     11914      G   /usr/lib/firefox/firefox                      435MiB |
|    0   N/A  N/A    121585      G   ...sion,SpareRendererForSitePerProcess        103MiB |
+-----------------------------------------------------------------------------------------+

```

6. CUDA Toolkit install using conda

URL: https://anaconda.org/nvidia/cuda-toolkit
```
conda install nvidia/label/cuda-11.8.0::cuda-toolkit
Description: Meta-package containing all toolkit packages for CUDA development
```

7. NVCC after CUDA Toolkit installation
```
nvcc -V

(photoslam) s42sdamm@photolab96:~/Documents/thesis/Photo-SLAM$ nvcc -V
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2024 NVIDIA Corporation
Built on Thu_Mar_28_02:18:24_PDT_2024
Cuda compilation tools, release 12.4, V12.4.131
Build cuda_12.4.r12.4/compiler.34097967_0


conda list | grep cuda
** To determine the version of CUDA installed, you typically look for the version associated with the cuda-toolkit package

(photoslam) s42sdamm@photolab96:~/Documents/thesis/Photo-SLAM$ conda list | grep cuda
cuda-cccl                 12.4.127             h06a4308_2  
cuda-cccl_linux-64        12.4.127             h06a4308_2  
cuda-command-line-tools   12.4.1               h06a4308_1  
cuda-compiler             12.4.1               h6a678d5_1  
cuda-crt-dev_linux-64     12.4.131             h06a4308_0  
cuda-crt-tools            12.4.131             h06a4308_0  
cuda-cudart               12.4.127             h99ab3db_0  
cuda-cudart-dev           12.4.127             h99ab3db_0  
cuda-cudart-dev_linux-64  12.4.127             hd681fbe_0  
cuda-cudart-static        12.4.127             h99ab3db_0  
cuda-cudart-static_linux-64 12.4.127             hd681fbe_0  
cuda-cudart_linux-64      12.4.127             hd681fbe_0  
cuda-cuobjdump            12.4.127             h6a678d5_1  
cuda-cupti                12.4.127             h6a678d5_1  
cuda-cupti-dev            12.4.127             h6a678d5_1  
cuda-cuxxfilt             12.4.127             h6a678d5_1  
cuda-documentation        11.8.86                       0    nvidia/label/cuda-11.8.0
cuda-driver-dev           12.4.127             h99ab3db_0  
cuda-driver-dev_linux-64  12.4.127             hd681fbe_0  
cuda-gdb                  12.4.127             h122497a_1  
cuda-libraries            12.4.1               h06a4308_1  
cuda-libraries-dev        12.4.1               h06a4308_1  
cuda-nsight               12.4.127             h06a4308_1  
cuda-nvcc                 12.4.131             h02f8991_0  
cuda-nvcc-dev_linux-64    12.4.131             h4ee8466_0  
cuda-nvcc-impl            12.4.131             h99ab3db_0  
cuda-nvcc-tools           12.4.131             h99ab3db_0  
cuda-nvcc_linux-64        12.4.131             he92618c_0  
cuda-nvdisasm             12.4.127             h6a678d5_1  
cuda-nvml-dev             12.4.127             h6a678d5_1  
cuda-nvprof               12.4.127             h6a678d5_1  
cuda-nvprune              12.4.127             h6a678d5_1  
cuda-nvrtc                12.4.127             h99ab3db_1  
cuda-nvrtc-dev            12.4.127             h99ab3db_1  
cuda-nvtx                 12.4.127             h6a678d5_1  
cuda-nvvm-dev_linux-64    12.4.131             h06a4308_0  
cuda-nvvm-impl            12.4.131             h6a678d5_0  
cuda-nvvm-tools           12.4.131             h6a678d5_0  
cuda-nvvp                 12.4.127             h6a678d5_1  
cuda-opencl               12.4.127             h6a678d5_0  
cuda-opencl-dev           12.4.127             h6a678d5_0  
cuda-profiler-api         12.4.127             h06a4308_1  
cuda-sanitizer-api        12.4.127             h99ab3db_1  
cuda-toolkit              11.8.0                        0    nvidia/label/cuda-11.8.0
cuda-tools                12.4.1               h06a4308_1  
cuda-version              12.4                 hbda6634_3  
cuda-visual-tools         12.4.1               h06a4308_1 

```

8. Installing CuDNN (Available version:  cudnn 8.9.7.29 using conda-forge)
```
URL: https://anaconda.org/conda-forge/cudnn

conda install conda-forge::cudnn

(photoslam) s42sdamm@photolab96:~/Documents/thesis/Photo-SLAM$ conda list | grep cudnn
cudnn                     8.9.7.29             h092f7fd_3    conda-forge

```
