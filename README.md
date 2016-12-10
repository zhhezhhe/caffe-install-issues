# caffe-install-issues
caffe
#cmake 安装
将
//vecLib include directory 
vecLib_INCLUDE_DIR:PATH=/System/Library/Frameworks/vecLib.framework/Headers
替换为
vecLib_INCLUDE_DIR:PATH=/System/Library/Frameworks/Accelerate.framework/Versions/Current/Frameworks/vecLib.framework/Versions/Current/Headers
#make 安装
cblas.h problem has been solved. I just edited two lines in makefile.config:
BLAS_INCLUDE := /usr/local/Cellar/openblas/0.2.9-rc2/include
BLAS_LIB := /usr/local/Cellar/openblas/0.2.9-rc2/lib注意上边的版本号改成自己电脑openblas版本同时替换配置文件中altas 换成 open
#python路径修改
PYTHON_INCLUDE := /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk/System/Library/Frameworks/Python.framework/Versions/2.7/include/python2.7 \
		/usr/local/Cellar/numpy/1.11.2/lib/python2.7/site-packages/numpy/core/include
