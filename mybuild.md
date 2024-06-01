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
