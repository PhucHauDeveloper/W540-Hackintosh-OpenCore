# **W540-Hackintosh-OpenCore
EFI for Lenovo W540 Hackintosh OpenCore**

*Please check Releases to select EFI according to your version of MacOS.*


**Laptop configuration:**

  CPU: Core i7-4900MQ
  
  RAM: 8GB 1600
  
  Disk: 120Gb SSD Samsung evo
  
  Wireless: Intel Wireless 7260
  
  Sound: Realtek ALC292
  
  dGPU: Nvidia Quadro K1100m
  
  iGPU: Intel HD 4600
  


**Working:**

  CPU (get all kernels and threads)
  
  iGPU (with acceleration, not full color depth and need to replace screen with higher bit)
  
  Screen Brightness, NightShift (works fine)
  
  Trackpoint/Trackpad/Keyboard (get gesture, works fine)
  (includes volume function (Fn + F1/F2 key) Brightness (Fn key + F5/F6) and Mission Control (Fn + F11))
  
  Wi-Fi (works fine, get both 2.4GHz and 5GHz, 802.11 a/b/g/n/ac)
  
  Ethernet, USB tethering (works fine)
  
  Audio (works fine but does not automatically switch speakers)
  
  Bluetooth ~~(poor connection turn off wifi to solve and sometimes doesn't work, reboot solves)~~(Works fine, 4~5m if open wifi, turn off wifi and using tethering to be able to connect further)(not recommended but or you can use itlwm.kext + HeliPort.app to replace AirportItlwm.kext)
  
  Battery level (works fine)
  
  iSevice, iMess, Facetime,...
  
  Camera, usb, etc...
  
   ***Optimize***
    To fix aliasing you should open HiDPI with the command below:
  ```
      sudo defaults write /Library/Preferences/com.apple.windowserver.plist DisplayResolutionEnabled -bool true
  ```
    or(recommended)
  ```
      bash -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/master/hidpi.sh)"
  ```
   ***Secure boot***
      You can use if you fixEDID, fix tearing if CSM is off and open custom secure boot option. If you know how to fix it please contact me to fix it !
  
  
  
**Not tested:**

  Video OUT
  
  Airplay, Sidecar, Handoff, AirDrop, Universal Clipboard, and I do not try connect Apple Bluetooth peripherals (I'm poor so I don't have money to buy it 😂 ) and Hidden Networks.
  

**Not working:**

  dGPU(I'm trying so hard to fix it)
  
  Wake(after sleep can not be woken, hold the power button off and restart solved)
  
