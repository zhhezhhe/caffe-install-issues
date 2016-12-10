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
