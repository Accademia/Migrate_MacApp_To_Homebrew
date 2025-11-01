
目的：
--------------------------------

查询 可以将哪些APP迁移到Homebrew，以便通过brew管理这些APP（升级、卸载、安装）


.

可以迁移哪些程序？
--------------------------------

仅识别非Mac App Store安装的程序。

因为通过MAS安装的程序，苹果应用商店会自动更新，没有必要通过第三方更新。第三方更新后会有弹窗提示权限请求，非常烦人。



.

命令 1 ：
--------------------------------

- 检查：哪些APP可以迁移到Homebrew安装
    
-   统计：本地安装的APP中，那些是 “非 HomeBrew APP” + 非 Mac AppStore APP“
-   统计：本地安装的APP中，上述哪些APP可以迁移到Homebrew 
    注意：Mac AppStore APP 不参与迁移 ⚠️
    ~~~
    ./usercmd_migrate_macapp_to_homebrew
    ~~~
    
    生成如下文件 (文件会生成在调用命令所在的文件夹)
    
    ~~~
    ./brew_install_commands.txt	# ✅ 此文件为 可以迁移的软件列表
    ./non_brew_non_mas_apps.txt	
    ./ambiguous_matches.txt
    ~~~

    brew_install_commands.txt 内含了所有迁移所需的命令，直接多行一起整体拷贝，粘贴到命令行执行。此过程会触发多次密码请求。

    建议手工排查，因为很多用户会使用非正版软件，直接覆盖，会导致目前安装版本实效。

.

命令 2 ：
--------------------------------

- 检查：通过 homebrew 下载安装的APP，是否有问题，如果有问题将自动重装。

    ~~~
    ./usercmd_check_InstallByHomebrew
    ~~~
    
- 生成如下文件

    ~~~
    ./brew_installation_check.log	
    ~~~




.

授权许可：
--------------------------------

第二版，代码来自于 OpenAI ChatGPT5 Pro + Agnet

第一版，代码来自于 xAI Grok DeepThink

本软件使用MIT协议进行分发。
