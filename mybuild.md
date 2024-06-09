1. GCC

```
gcc --version

(base) s42sdamm@photolab96:~/Documents/thesis/Photo-SLAM$ gcc --version
gcc (Ubuntu 9.4.0-1ubuntu1~20.04.2) 9.4.0
Copyright (C) 2019 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

which gcc
(photoslam) s42sdamm@photolab97:~/Documents/thesis/opencv/opencv-4.7.0/build$ which gcc
/usr/bin/gcc

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

7.1. CUDA Path
```
which nvcc

(photoslam) s42sdamm@photolab96:~/Documents/thesis/Photo-SLAM$ which nvcc
/home_domuser/s42sdamm/miniconda3/envs/photoslam/bin/nvcc
```

8. Installing CuDNN (Available version:  cudnn 8.9.7.29 using conda-forge)
```
URL: https://anaconda.org/conda-forge/cudnn

conda install conda-forge::cudnn

(photoslam) s42sdamm@photolab96:~/Documents/thesis/Photo-SLAM$ conda list | grep cudnn
cudnn                     8.9.7.29             h092f7fd_3    conda-forge

```

9. I have two different things to test. While installing opencv as mentioned in the README.md, I encountered this issue
```
(photoslam) s42sdamm@photolab97:~/Documents/thesis/opencv/opencv-4.7.0/build$ make -j8
[  0%] Built target opencv_videoio_plugins
[  0%] Built target opencv_highgui_plugins
[  0%] Built target opencv_dnn_plugins
[  0%] Built target ittnotify
[  1%] Built target zlib
[  2%] Built target libopenjp2
[  2%] Built target quirc
[  3%] Built target ippiw
[  4%] Built target jsimd
[  6%] Built target opencv_cudev
[  6%] Built target libtiff
[  7%] Built target ade
[  7%] Building NVCC (Device) object modules/core/CMakeFiles/cuda_compile_1.dir/src/cuda/cuda_compile_1_generated_gpu_mat.cu.o
[  7%] Building NVCC (Device) object modules/core/CMakeFiles/cuda_compile_1.dir/src/cuda/cuda_compile_1_generated_gpu_mat_nd.cu.o
[  8%] Built target libprotobuf
[ 10%] Built target libjpeg-turbo
nvcc warning : incompatible redefinition for option 'compiler-bindir', the last value of this option was used
nvcc warning : incompatible redefinition for option 'compiler-bindir', the last value of this option was used
[ 14%] Built target libwebp
[ 17%] Built target IlmImf
In file included from /usr/include/ctype.h:39,
                 from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/crt/host_defines.h:64,
                 from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/device_types.h:59,
                 from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/builtin_types.h:56,
                 from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/cuda_runtime.h:90,
                 from <command-line>:
/ipb245/home_domuser/s42sdamm/miniconda3/envs/photoslam/x86_64-conda-linux-gnu/sysroot/usr/include/bits/endian.h:4:3: error: #error "Never use <bits/endian.h> directly; include <endian.h> instead."
    4 | # error "Never use <bits/endian.h> directly; include <endian.h> instead."
      |   ^~~~~
In file included from /usr/include/ctype.h:39,
                 from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/crt/host_defines.h:64,
                 from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/device_types.h:59,
                 from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/builtin_types.h:56,
                 from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/cuda_runtime.h:90,
                 from <command-line>:
/ipb245/home_domuser/s42sdamm/miniconda3/envs/photoslam/x86_64-conda-linux-gnu/sysroot/usr/include/bits/endian.h:4:3: error: #error "Never use <bits/endian.h> directly; include <endian.h> instead."
    4 | # error "Never use <bits/endian.h> directly; include <endian.h> instead."
      |   ^~~~~
In file included from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/crt/host_defines.h:64,
                 from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/device_types.h:59,
                 from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/builtin_types.h:56,
                 from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/cuda_runtime.h:90,
                 from <command-line>:
/usr/include/ctype.h:237:11: fatal error: bits/types/locale_t.h: No such file or directory
  237 | # include <bits/types/locale_t.h>
      |           ^~~~~~~~~~~~~~~~~~~~~~~
compilation terminated.
In file included from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/crt/host_defines.h:64,
                 from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/device_types.h:59,
                 from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/builtin_types.h:56,
                 from /home_domuser/s42sdamm/miniconda3/envs/photoslam/targets/x86_64-linux/include/cuda_runtime.h:90,
                 from <command-line>:
/usr/include/ctype.h:237:11: fatal error: bits/types/locale_t.h: No such file or directory
  237 | # include <bits/types/locale_t.h>
      |           ^~~~~~~~~~~~~~~~~~~~~~~
compilation terminated.
CMake Error at cuda_compile_1_generated_gpu_mat.cu.o.RELEASE.cmake:222 (message):
  Error generating
  /home_domuser/s42sdamm/Documents/thesis/opencv/opencv-4.7.0/build/modules/core/CMakeFiles/cuda_compile_1.dir/src/cuda/./cuda_compile_1_generated_gpu_mat.cu.o


CMake Error at cuda_compile_1_generated_gpu_mat_nd.cu.o.RELEASE.cmake:222 (message):
  Error generating
  /home_domuser/s42sdamm/Documents/thesis/opencv/opencv-4.7.0/build/modules/core/CMakeFiles/cuda_compile_1.dir/src/cuda/./cuda_compile_1_generated_gpu_mat_nd.cu.o


make[2]: *** [modules/core/CMakeFiles/opencv_core.dir/build.make:65: modules/core/CMakeFiles/cuda_compile_1.dir/src/cuda/cuda_compile_1_generated_gpu_mat.cu.o] Error 1
make[2]: *** Waiting for unfinished jobs....
make[2]: *** [modules/core/CMakeFiles/opencv_core.dir/build.make:72: modules/core/CMakeFiles/cuda_compile_1.dir/src/cuda/cuda_compile_1_generated_gpu_mat_nd.cu.o] Error 1
make[1]: *** [CMakeFiles/Makefile2:4972: modules/core/CMakeFiles/opencv_core.dir/all] Error 2
make: *** [Makefile:163: all] Error 2

```

I could find a way to fix this missing locale_t.h problem. Internet suggests to install build-essentials along with few other packages. But I dont have the sudo 
access and I couldn't find a way to install all the build-essential packages from source - no git repo. 
```
A. I would like to first investigate where this <bits/types/local_t.h> can be found. Is it fundamental to C language and so on. 
B. Try to change nvcc version from 12.X to 11.8 
C. Try to change the GCC version
D. Try giving a host compiler flag while building OpenCV. 
E. Write down the learnings from the above tasks.
```

10. I had clock skew error while building opencv. Tried downloading source from the official tags from git hub instead of click to download link mentioned in the documentation. 

11. I installed opencv-contrib using pip into my conda env, just for trying. Running cv2.__file__ gives path /home_domuser/s42sdamm/miniconda3/envs/photoslam/lib/python3.10/site-packages/cv2/__init__.py
    which I can maybe use to edit CMakeLists as they explain to build photoslam, lets see


