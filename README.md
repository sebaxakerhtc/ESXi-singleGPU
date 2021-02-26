# ESXi-singleGPU
GPU passthrough ESXi with a single GPU, integrated graphics or another situation, when you want ESXi to not use Graphics card

<p> Step 1: Install and configure ESXi
<p> Step 2: Toggle passthrough for GPU to Active
<p> Step 3: Create VM with GPU passthrough (and if we want, configure autostart)
<p> Step 4: Enable SSH or Console
<p> Step 5: Enter commands below
 
```
esxcfg-advcfg --set-kernel "TRUE" ignoreHeadless
esxcli system settings kernel set -s vga -v FALSE
```
<p> Step 6: Reboot
  
From now you will no longer see ESXi yellow/black bootscreen. Just a text like
 
```
Shutting down firmware services...
Relocating modules and starting up the kernel...
```
Enjoy!
