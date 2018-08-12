# rtl8723de
REALTEK devices wifi problem is fixed for rtl8723de for ubuntu 16.04
* Finally after a lot of reserch i found asolution for my ubuntu 16.04 wifi problem in HP laptops
here is the detailed description
Realtek RTL8723DE module for Linux kernel version >= 4.15

Install:

git clone https://github.com/smlinux/rtl8723de.git -b 4.15-up
dkms add ./rtl8723de
dkms install rtl8723de/5.1.1.8_21285.20171026_COEX20170111-1414
depmod -a
reboot
*then wifi start working 
any problem remove it using following method and re-proced for the above procedure

Uninstall:

rmmod -f 8723de
dkms uninstall rtl8723de/5.1.1.8_21285.20171026_COEX20170111-1414
dkms remove rtl8723de/5.1.1.8_21285.20171026_COEX20170111-1414 --all
depmod -a
reboot
