## code
https://github.com/stephane/libmodbus.git


## linux

### 先安装工具 apt install automake autoconf libtool
### 虚拟机不能放在共享目录编译

cd libmodbus

libtoolize
aclocal
autoheader
./autogen.sh

### ubuntu
./configure --enable-static
### 安霸
env CFLAGS="-DPLAT_AMBA -fPIC -g -O2" ./configure --enable-static CC=aarch64-linux-gnu-gcc --host=aarch64-linux-gnu --prefix=/usr/local/aarch64-linux-gnu
### 海思
env CFLAGS="-DPLAT_HISI -fPIC -g -O2" ./configure --enable-static --build=x86_64-linux-gnu --host=arm-hisiv500-linux --prefix=/usr/local/arm-hisiv500-linux


## windows
项目中已生成, 不需要在执行,
执行步骤:
进入目录src\win32
双击运行configure.js文件
打开modbus-9.sln文件
编译release版本


