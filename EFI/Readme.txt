****************************************************************************************

            
                           本EFI支持10.13.6 - 10.15.x
			 
		       如果你参考了本EFI制作了新的EFI，请标明出处

	     https://github.com/xiaoMGitHub/LEGION_Y7000Series_Hackintosh

			 Y7000系列黑苹果QQ群：1014806625


****************************************************************************************

1、使用前准备
   1）从群里下载 Y7000系列一键修改BIOS_Beta_v1.8.zip
   2) 解压后，双击批处理脚本
   3）依次执行 5、7、8
   4）如果是八代处理器则需要额外多执行 4
   5）重启

2、替换EFI，成功进入MacOS后，打开终端执行下面的命令

   sudo sh -c "$(curl -fsSL https://gitee.com/xiaoMGit/Y7000Series_Hackintosh_Fix/raw/master/Script/Optimize.sh)"

3、小键盘相关设置

  0）已经执行了上面的步骤
  1）打开终端执行 open /usr/local/bin/
  2）打开 系统偏好设置 > 安全性与隐私 > 隐私 > 辅助功能
  3）将 setleds 添加到辅助功能

4、屏蔽PM981、PM981a、2019款自带镁光固态

   1) 打开 EFI/OC/config.plist
   2) 搜索 SSDT-DNVMe.aml
   3）将上方的 <key>Enabled</key> 修改为 <key>Enabled</key>
	     <false/>                 <true/>
	     


   