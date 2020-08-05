****************************************************************************************

            
                           EFI support 10.13.6 - 10.15.x
			 
		       This EFI original source is from below

	     https://github.com/xiaoMGitHub/LEGION_Y7000Series_Hackintosh

			

****************************************************************************************

1、BIOS Configration
   Press Fn + o + D enter into BIOS Advanced Setting when reboot the computer 
   Press F9 reset to default setting then change below
   1）turn the secure boot off
   2) change Advanced>Debug settings>legacy URAT
   3）turn off CFG lock
   4）change DVMT to 64M
   5）press F10 and save
   6) reboot

2、Replace EFI after boot into macOS and execute the below command in terminal

   sudo sh -c "$(curl -fsSL https://gitee.com/xiaoMGit/Y7000Series_Hackintosh_Fix/raw/master/Script/Optimize.sh)"

3、Setting for the Numpad

  1）open terminal and execute open /usr/local/bin/    then you can see file "setleds"
  2）open "system preference > security & privacy > Assistant
  3）drag "settlers" into Assistant 



   