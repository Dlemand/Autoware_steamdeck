steam deck cannot install CH9120 Driver:\
That is because the origin OS don't have the **Kernel Headers**,which lead to the error:"/lib/modules/5.13.0-valve21.3-1-neptune/build: No such file or directory. Stop " \
so we need to install the header: \
```c++
sudo pacman -S linux-neptune-headers
```
if you dont have pacman in steamos, you can search on google.
