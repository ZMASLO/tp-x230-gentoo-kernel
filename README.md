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
- Battery
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

#Turning on RC6pp and other poversaving features
Intel-ring sync, enabled deepest RC6 states, enabled frame buffer compression and enabled lvds downclock
- copy gpu.conf to /etc/modprobe.d/
- reboot

#If it doesn't work try this out:
- edit /etc/default/grub
- Find GRUB_CMDLINE_LINUX_DEFAULT
- Example look like this: GRUB_CMDLINE_LINUX_DEFAULT="i915.enable_rc6=7 i915.enable_fbc=1 i915.lvds_downclock=1 i915.semaphores=1"
- grub-mkconfig -o /boot/grub/grub.cfg
- reboot


