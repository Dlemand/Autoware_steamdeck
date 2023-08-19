# steam deck cannot install CH9120 Driver:\
That is because the origin OS don't have the **Kernel Headers**,which lead to the error:"/lib/modules/5.13.0-valve21.3-1-neptune/build: No such file or directory. Stop " \
so we need to install the header: \
```c++
sudo pacman -S linux-neptune-headers
```
if you dont have pacman in steamos, you can search on google.

# CH343
https://github.com/WCHSoftGroup/ch343ser_linux

# Change Serials ID
```shell
#search serial info
udevadm info --attribute-walk --name=/dev/ttyUSB0
#creat rules
sudo gedit /etc/udev/rules.d/xxx.rules #any name
#INPUT,accroding special serial info find the serial and change it 
KERNELS=="xxx", MODE:="0777", GROUP:="xxxxx", SYMLINK+="xxxxxxx"
#SYMLINK is another name to visit serial
```
