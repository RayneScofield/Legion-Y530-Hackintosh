# EFI support macOS 10.13.6 - 11.1
The purpose of this repo is for installing macOS (High Sierra and above) on the Lenoveo Legion Y530/Y7000P 2018 laptop
# Computer Specification
- Chipset HM370
- Intel® Core™ i7-8750H (Coffee-Lake)
- 16GB RAM DDR4 2666Mhz
- Intel® UHD Graphics 630
- Nvidia GTX 1060 6GB (disabled)
- SATA Sumsang 860 Evo 512GB 
- Realtek ALC3240 Audio Controller
- RTL8168H Gigabit Ethernet
- Display 15.6" 16:9, 1920 × 1080 pixels FHD, 60Hz
- Intel WiFi AC9260 (disabled)
- Trackpad ELAN 061B
- BIOS : 8JCN54WW 6/15/2020

# BIOS Settings - Paramount Important
Power on then press and hold Fn+O+D until it enters into BIOS advanced mode.
F9 reset to bios default setting if messed up. Following options need to change to then F10 save and reboot:<br>
1. Secure Boot : Disabled
2. Kernel Debug Serial Port : Legacy UART <br>
    Advanced -> Debug settings -> Legacy UART
3. CFG Lock (MSR_E2) : Disabled<br>
    Advanced -> Power & Performance -> CPU - Power Management -> View/Configure CPU Lock Options -> CFG Lock
4. DVMT Pre-Allocated Memory : 64MB<br>
    Advanced -> System Agent (SA) Configuration -> Graphics Configuration -> DVMT Pre-Allocated Memory
5. Trackpad GPIO: Enabled<br>
    Advanced -> PCH-IO config -> BIOS lock -> Security Config -> Enabled
# Pre-installation
Tools needed: 
1. [MountEFI](https://github.com/corpnewt/MountEFI) to mount EFI
2. [ProperTree](https://github.com/corpnewt/ProperTree) to edit config plist

Here just simplified, refer to [Dortania installation guide](https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html#prerequisites) or [gibMacos](https://github.com/corpnewt/gibMacOS)
# Post-installation
1.  Mount system EFI partition, and copy EFI folder to root of system EFI partition
2.  Execute the below optimise script in terminal to fix Audio headphone, Numpad and Win/Mac system time. 

```sh
sudo sh -c "$(curl -fsSL https://gitee.com/xiaoMGit/Y7000Series_Hackintosh_Fix/raw/master/Script/Optimize.sh)"
``` 
and Extra setting for numpad to work:<br>
1. go to folder /usr/local/bin/  where 'setleds' is located<br>
2. open "system preference > security & privacy > Assistant<br>
3. drag "settlers" into Assistant<br>

Optional: go to system settings and set the display resolution to 1600 ✕ 900, which give a good user experience. It's fine tuned by Display-9e5-6fb.kext in the EFI.

# Credit
- [Acidanthera](https://github.com/acidanthera)
- [xiaoM](https://github.com/xiaoMGitHub)
- etc

