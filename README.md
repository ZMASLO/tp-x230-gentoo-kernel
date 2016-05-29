#Hello there!
I provide fully working gentoo linux kernel for Lenovo ThinkPad x230

Kernel version: 4.6.0
Working:
- Chipset
- Wifi (as module)
- Memory Card
- HD Sound System
- Sound via HDMI/DisplayPort
- Battery optimalisation
- Microphone

Not working: 
- Sound via DockStation
- Camera

Installation guide:
- Just simply copy .configuration to /usr/src/linux-X-X-X/
- make -j5
- make modules_install
- make install
