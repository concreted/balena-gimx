
http://gimx.fr/wiki/index.php?title=DIY_USB_adapter_for_dummies

## Reference
https://blog.gimx.fr/

https://gimx.fr/wiki/index.php?title=Guide&platform=ps4&connectiontype=BT&ostype=linux&device=SteeringWheel

https://gimx.fr/wiki/index.php?title=Command_line#Linux_.2B_bluetooth_.2B_PS4

https://github.com/matlo/GIMX-tools/blob/master/PS4/gimx-ps4-helper.sh
https://raw.githubusercontent.com/matlo/GIMX-tools/master/PS4/gimx-ps4-helper.sh


## Building

libgusb-dev <- probably don't need this one?
libglib2.0-dev

gcc -v -I /usr/include/gusb-1 ds4tool.c

get all files and unzip+rename => move to /usr/local/include
```bash
wget https://github.com/matlo/gimxusb/archive/master.zip
wget https://github.com/matlo/gimxpoll/archive/master.zip
wget https://github.com/matlo/gimxcommon/archive/master.zip
wget https://github.com/matlo/gimxlog/archive/master.zip
```

This command works after getting all libs into /usr/local/include:
```bash
gcc -v -I /usr/include/glib-2.0/ -I /usr/lib/arm-linux-gnueabihf/glib-2.0/include/ -I /usr/local/include/gimxusb/include ds4tool.c -lgimxusb -lgimxpoll -lgimxlog
```
