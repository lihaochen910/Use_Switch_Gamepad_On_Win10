# 在win10系统上连接Pro Controller / Joycon手柄教程

#### 测试系统: Win10 1903
#### 测试PC: Mac Pro 2013 Late

## 往下看

* 先到这里下载 [BetterJoyForCemu](https://github.com/Davidobot/BetterJoyForCemu/releases "BetterJoyForCemu")，根据你的系统架构选择x86或者x64版本
* 然后再到这里下载 [ViGEmBus](https://github.com/ViGEm/ViGEmBus/releases "ViGEmBus")，我当前使用的版本是ViGEmBus Setup 1.16.112
* 打开ViGEmBus_Setup_1.16.115.exe并安装
* 安装并配置BetterJoyForCemu
   * 然后解压下载的BetterJoyForCemu_v5_x64.zip放到一个位置，我这里是放到D盘根目录下
   * 使用管理员打开命令提示符，
   * 输入命令 `D:` (切换当前工作盘符)
   * 输入命令 `cd D:\ButterJoyForCemu` (定位到BetterJoyForCemu路径)
   * 输入命令 `cd Drivers` (定位到BetterJoyForCemu\Drivers路径)
   * 输入命令 `devcon.exe install .\HidGuardian\HidGuardian.inf Root\HidGuardian` (安装HidGuardian驱动)
   * 输入命令 `devcon.exe classfilter HIDClass upper -HidGuardian` (配置HidGuardian)
   * 输入命令 `cd .\HidCerberus.Srv` (定位到BetterJoyForCemu\Drivers\HidCerberus.Srv路径)
    * 输入命令 `HidCerberus.Srv.exe install` (安装HidCerberus服务)
    * 输入命令 `net start "HidCerberus Service"` (启用HidCerberus服务)
* 现在可以打开BetterJoyForCemu目录下的BetterJoyForCemu.exe

* ![BetterJoyForCemu.exe](https://github.com/lihaochen910/Use_Switch_Gamepad_On_Win10/blob/master/res/%E6%97%A0%E6%A0%87%E9%A2%98_1.png?raw=true)
* 如果程序没有报任何错误，则说明驱动已经安装成功了
* 打开电脑的蓝牙，此时长按switch手柄上的Sync键(很小的那个按键)(Pro Controller在数据线接口的旁边，Joycon在侧面)，观察手柄上的指示灯开始闪
* ![PC端开始搜索蓝牙设备](https://github.com/lihaochen910/Use_Switch_Gamepad_On_Win10/blob/master/res/%E6%97%A0%E6%A0%87%E9%A2%98_2.png?raw=true)
* ![搜索到手柄](https://github.com/lihaochen910/Use_Switch_Gamepad_On_Win10/blob/master/res/%E6%97%A0%E6%A0%87%E9%A2%98_3.png?raw=true)
* 与手柄配对成功后回到BetterJoyForCemu界面后可以看到
* ![连接成功](https://github.com/lihaochen910/Use_Switch_Gamepad_On_Win10/blob/master/res/%E6%97%A0%E6%A0%87%E9%A2%98_4.png?raw=true)
* 注意手柄的电量，现在可以进入游戏玩耍了

### 如果你觉得这篇文章有帮助，请多多支持我们的游戏
![SeedHunter](https://media.st.dl.bscstorage.net/steam/apps/1078490/header_schinese.jpg?t=1563433211)