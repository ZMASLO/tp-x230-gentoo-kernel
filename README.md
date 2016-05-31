#Hello there!
I provide fully working gentoo linux kernel for Lenovo ThinkPad x230

Kernel version: 4.6.0

#Working:
- Chipset
- Graphic (as module)
- Graphic RC6pp (powersaving option)
- Wifi (as module)
- Memory Card
- HD Sound System
- Sound via HDMI/DisplayPort & DockStation
- Battery optimalisation
- Microphone

#Not working: 
- Camera


#Compilation guide:
- Just simply copy config to /usr/src/linux-X-X-X/.config
- You can edit configuration with make nconfig -j5
- make -j5
- make modules_install
- make install

#Installation (without compilation)
I don't recomend copy my precompiled kernel 'cause some
of features (like hibernation) may not work. But if you
know the risk and still want to copy it here u are.

- copy vmlizuz-X.X.X-gentoo to /boot/

#Turning on RC6pp
- copy gpu.conf to /etc/modprobe.d/
- reboot
