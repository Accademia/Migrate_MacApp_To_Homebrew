
目的：
--------------------------------

查询 可以将哪些APP迁移到Homebrew，以便通过brew upgrade --greedy 自动更新这些APP


.

可以迁移哪些程序？
--------------------------------

仅识别非Mac App Store安装的程序。

因为通过MAS安装的程序，苹果应用商店会自动更新，没有必要通过第三方更新。第三方更新后会有弹窗提示权限请求，非常烦人。


.


BUG
--------------------------------


目前，对于那些APP识别率不能做到100% ？

 - 安装后名称有变化的APP，还不能100%识别，以待后续改进，如 ：
    + IDA Free
    + Jdownloader2
    + Adobe系列
    + MacCleaner
    等等……

 - 所有的iPad App、iPhone APP（等待Mas List支持、无需修改代码）


.

生成文件：
--------------------------------

会自动生成两个文件：

non_brew_non_mas_apps.txt	包含，非homebrew安装的app和非Mac App Store安装的APP
 
brew_install_commands.txt	包含，可迁移的APP


文件会生成在调用命令所在的文件夹（默认文件夹为当前用户的根目录）


.

授权许可：
--------------------------------

所有代码均来自于 xAI Grok DeepThink

本软件使用MIT协议进行分发。
