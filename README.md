# NodeMCU Based Esp8266 Start
### step 0: Note
> 该文档目的在于项目内人员熟悉NodeMCU开发流程，不负责NodeMCU部分开发的人员可以暂时不需要了解除本仓库外其它仓库。当然想了解一下也请随意。有任何问题随时与我沟通 

> 协控硬件开发人员设计电路图时，可参考NodeMCU官方参考电路板设计[**v0.0**](https://github.com/nodemcu/nodemcu-devkit)   [**v0.1**](https://github.com/nodemcu/nodemcu-devkit-v1.0)

> @author: ZHANG Te

### step 1: 构建固件(Online service)
> 在[nodemcu-build](https://nodemcu-build.com/) 选择固件模块,点击在线构建固件,几分钟后固件会发送到邮箱

> IoT Button 目前使用的固件模块有: file, gpio, http, net, node, pwm, sjson, tmr, uart, wifi

### step 2: 烧录固件
1. windows:
> 解压本仓库flash_download_tools_v3.6.2.2_1.zip, 双击exe, 选择上面构建的固件,起始地址为0x0

2. Linux:
> 执行 **```pip install esptool```** 安装esptool.py

> 如果上面命令安装速度慢,可使用国内镜像代理, **``` pip install -i https://pypi.tuna.tsinghua.edu.cn/simple esptool ```**

> 执行 **```esptool.py --port [端口] write_flash 0x0000 固件名称```** 下载固件

> 执行 **```esptool.py erase_flash```** 可以擦除flash内容

> 端口可以使用[USB-Serial-tool-Kitty](https://github.com/SenseAge/USB-Serial-tool-Kitty)下的shell脚本快速查看

### step 3: 上传Lua代码(Cross platform)
> 执行本仓库java包 **```java -jar ESPlorer.jar```** 波特率选择115200

NodeMCU启动时总是从init.lua开始执行
