This directory contains the usful tools.


## build_android.sh
This script is to build PyTorch/Caffe2 library for Android. Take following steps to start the build:

- set ANDROID_NDK to the location of ndk

```bash
export ANDROID_NDK=YOUR_NDK_PATH
```

- run build_android.sh
```bash
#in your PyTorch root directory
bash scripts/build_android.sh
```
If succeeded, the libraries and headers would be generated to build_android/install directory. You can then copy these files from build_android/install to your Android project for further usage. 

You can also override the cmake flags via command line, e.g., following command will also compile the executable binary files:
```bash
bash scripts/build_android.sh -DBUILD_BINARY=ON
```