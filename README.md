# Esp8266-nodemcu-start

### step 1: 构建固件(Cloud service)
> 在[nodemcu-build](https://nodemcu-build.com/) 在线构建固件,几分钟后会发送到邮箱

### step 2: 烧录固件
1. windows:
> 解压flash_download_tools_v3.6.2.2_1.zip, 双击exe, 选择上面构建的固件,起始地址为0x0

2. Linux:
> 执行 **```pip install esptool```** 安装esptool.py

> 执行 **```esptool.py --port [端口] write_flash 0x0000 固件名称.bin```** 下载固件

> 执行 **```esptool.py erase_flash```** 可以擦除flash内容

> 端口可以使用[USB-Serial-tool-Kitty](https://github.com/SenseAge/USB-Serial-tool-Kitty)下的shell脚本快速查看

### step 3: 上传Lua代码(Cross plat-form)
> 执行 **```java -jar ESPlorer.jar```** 波特率选择115200
