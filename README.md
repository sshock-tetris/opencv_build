# opencv_build

OpenCV core build for T99 margin timer auto starter

## Releases
https://github.com/sshock-tetris/opencv_build/releases

## Build requirements
* [CMake](https://cmake.org/)
* [Visual Studio 2019](https://visualstudio.microsoft.com/) (msbuild)
  * "Desktop development with C++" component must be installed.

## Build instructions for Windows

### Get repository

```
git clone --recursive https://github.com/sshock-tetris/opencv_build.git
cd opencv_build
```

### Run CMake
```
mkdir out
cd out

cmake -G "Visual Studio 16 2019" -A x64 -D CMAKE_BUILD_TYPE=Release \
-D CMAKE_INSTALL_PREFIX=install -D BUILD_JASPER=OFF -D BUILD_JAVA=OFF \
-D BUILD_JPEG=OFF -D BUILD_OPENEXR=OFF -D BUILD_OPENJPEG=OFF \
-D BUILD_PACKAGE=OFF -D BUILD_PERF_TESTS=OFF -D BUILD_PNG=OFF \
-D BUILD_PROTOBUF=OFF -D BUILD_SHARED_LIBS=OFF -D BUILD_TESTS=OFF \
-D BUILD_TIFF=OFF -D BUILD_WEBP=OFF -D BUILD_ZLIB=OFF \
-D BUILD_opencv_apps=OFF -D BUILD_opencv_calib3d=OFF -D BUILD_opencv_dnn=OFF \
-D BUILD_opencv_features2d=OFF -D BUILD_opencv_flann=OFF \
-D BUILD_opencv_gapi=OFF -D BUILD_opencv_highgui=OFF \
-D BUILD_opencv_imgcodecs=OFF -D BUILD_opencv_imgproc=OFF \
-D BUILD_opencv_java_bindings_generator=OFF \
-D BUILD_opencv_js_bindings_generator=OFF -D BUILD_opencv_ml=OFF \
-D BUILD_opencv_objc_bindings_generator=OFF -D BUILD_opencv_objdetect=OFF \
-D BUILD_opencv_photo=OFF -D BUILD_opencv_python_bindings_generator=OFF \
-D BUILD_opencv_python_tests=OFF -D BUILD_opencv_stitching=OFF \
-D BUILD_opencv_ts=OFF -D BUILD_opencv_video=OFF -D BUILD_opencv_videoio=OFF \
-D ENABLE_LTO=ON -D ENABLE_PIC=OFF -D WITH_1394=OFF -D WITH_ADE=OFF \
-D WITH_ARITH_DEC=OFF -D WITH_DIRECTX=OFF -D WITH_DSHOW=OFF \
-D WITH_EIGEN=OFF -D WITH_FFMPEG=OFF -D WITH_GSTREAMER=OFF \
-D WITH_IMGCODEC_HDR=OFF -D WITH_IMGCODEC_PFM=OFF -D WITH_IMGCODEC_PXM=OFF \
-D WITH_IMGCODEC_SUNRASTER=OFF -D WITH_IPP=ON -D WITH_ITT=OFF \
-D WITH_JASPER=OFF -D WITH_JPEG=OFF -D WITH_LAPACK=OFF -D WITH_MSMF=OFF \
-D WITH_MSMF_DXVA=OFF -D WITH_OPENCLAMDFFT=OFF -D WITH_OPENCL_D3D11_NV=OFF \
-D WITH_OPENEXR=OFF -D WITH_OPENJPEG=OFF -D WITH_PNG=OFF \
-D WITH_PROTOBUF=OFF -D WITH_QUIRC=OFF -D WITH_TIFF=OFF -D WITH_VTK=OFF \
-D WITH_WEBP=OFF -D ccitt=OFF -D logluv=OFF -D lzw=OFF -D mdi=OFF \
-D next=OFF -D thunder=OFF ..\opencv
```

### Build
```
msbuild /m /p:Configuration=Release /p:platform=x64 INSTALL.vcxproj
```

or open and build OpenCV.sln by Visual Studio.


