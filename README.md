Synaptics touchpad driver for X.Org
===================================

This project is forked from: [https://github.com/dieghen89/xserver-xorg-input-synaptics](https://github.com/dieghen89/xserver-xorg-input-synaptics)

which is alredy based on: [https://github.com/felipejfc/xserver-xorg-input-synaptics](https://github.com/felipejfc/xserver-xorg-input-synaptics)

And fixes this issue [https://github.com/felipejfc/xserver-xorg-input-synaptics/issues/1](https://github.com/felipejfc/xserver-xorg-input-synaptics/issues/1)

This driver has been tested on Ubuntu 15.04 with a Dell Inspiron 15 5000 series.

Below is the original README from [felipejfc](https://github.com/felipejfc)



ABOUT
-----

In this fork I've put back SynapticsSHM into the driver to be able to use synclient monitor mode, so that the user can use xSwipe again for example.
This also add support to 4 and 5 finger click on some more trackpads, It worked on my XPS14.

HOW TO COMPILE AND INSTALL
--------------------------

**First run**

```
./autogen.sh
```

And the script will tell you all the dependencies you'll have to install in order to make.
Run the command again and again until you've resolved all the dependencies and can run ./autogen.sh without errors.

**Uninstall current installed synaptics driver from the system**

```
sudo apt-get remove xserver-xorg-input-synaptics
```

**The compile and install**

```
./configure --exec_prefix=/usr 
make
sudo make install
```

Reboot and you're done!
