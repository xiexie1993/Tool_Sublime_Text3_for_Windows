# Sublime_Text3_Stable_Build_3143_x64_Chs 免安装版 使用说明

## 一、概述

###  1、 编写目的

+  为软件的使用安装及配置升级作指导与记录。
+  为修改、维护提供条件；

### 2、 读者对象

+  项目开发人员，特别是编程人员；
+  本软件使用人员；


### 3、 注意事项

+  权限审查：公开
+  保存备份：允许修改，允许本地备份。
+  该文档采用 markdown 编写规范，建议使用markdownPad或相关编辑工具查看和修改。


## 二、 文档说明

**文档修改纪录**

| **日期**   | **作者**     | **版本** | **备注说明**                   |
|------------|------------  |----------|------------------------------|
| 2018/6/20  | xiexie1993   | V1.1     | 新建                         |
| 2018/8/22  | xiexie1993   | V1.2     | 修订                         |

## 三、目录结构

~~~

./                    根目录（Tool_Sublime_Text3_for_Windows）
├─ SublimeText3_3176.rar 版本为3176的Sublime_Text3免安装版Windows版本（基础无安装插件）
├─ SublimeText3_3176     版本为3176的Sublime_Text3免安装版Windows版本（安装了插件）
│  ├─ Backup             Sublime的备份文件，可定期删除
│  ├─ Cache              Sublime的缓存文件，可定期删除
│  ├─ Local
│  │  ├─ License.sublime_license   证书文件
│  │  ├─ Session.sublime_session   会话记录文件，可删除
│  │  └─ ... 
│  ├─ Data             Sublime的数据文件夹
│  │  ├─ Packages      Sublime的插件包目录【手动离线安装插件，只需将插件包解压到本目录下即可】
│  │  └─ ... 
│  └─ ...              
├─ README.md          自述文件
└─ ...

~~~

## 四、使用说明

### 安装步骤


+ 基础版安装
    + 1、本软件包，为windows绿色免安装版（SublimeText3_3176.rar ），
    	* a、解压 SublimeText3_3176.rar到软件安装目录（随便一个目录，不会被随意删除的路径下，例如：C:\Software下）
    	* b、【本步骤可不执行】进入 软件安装位置目录/SublimeText3_3176.rar ,点击 “添加∕删除右键菜单.bat” 文件，根据提示操作
    	* c、此时已可以使用，点击 软件安装位置目录里的sublime_text.exe 即可启动

    注：非基础版，直接复制SublimeText3_3176即可使用
    + 2、【本步骤可不执行，不执行则无法使用函数追踪功能】安装与配置第三方软件ctags插件依赖
    	* a、下载安装ctags
    	* b、将安装的ctags路径 配置到 系统变量 里，使得命令行能使用ctags的相关命令
    	* c、进入打开 首选项 --> 插件设置 --> Ctags --> Settings-Default修改第32行附近，将ctags安装位置修改为ctags的安装位置 如： "command": "C:/Software/ctags58/ctags.exe",

    + 3、破解注册【本步骤可不执行，但可能会出现注册失效，时不时提示要注册】（执行后可能导致在线安装其他插件无法安装成功）
    	* a、本软件已破解注册，但注册码和注册方式后来更新（所以采用断网方式）
    	* b、在C:\Windows\System32\drivers\etc\hosts文件添加
    	~~~
    	  ## sublime 破解
          127.0.0.1 license.sublimehq.com 
          127.0.0.1 45.55.255.55 
          127.0.0.1 45.55.41.223 
    	~~~
        * c、启用windows的系统防火墙，设置程序断网
    	    + 进入 控制面板-->系统和安全-->Windows Defender 防火墙 --> 高级设置 --> 入站规则 --> 新建规则 --> 程序 -->  选择安装位置下的sublime_text.exe --> 设置为阻止连接
            + 进入 控制面板-->系统和安全-->Windows Defender 防火墙 --> 高级设置 --> 入站规则 --> 新建规则 --> 程序 -->  选择安装位置下的subl.exe --> 设置为阻止连接	
            + 进入 控制面板-->系统和安全-->Windows Defender 防火墙 --> 高级设置 --> 出站规则 --> 新建规则 --> 程序 -->  选择安装位置下的sublime_text.exe --> 设置为阻止连接	
    		+ 进入 控制面板-->系统和安全-->Windows Defender 防火墙 --> 高级设置 --> 出站规则 --> 新建规则 --> 程序 -->  选择安装位置下的subl.exe --> 设置为阻止连接	
    	



## 五、使用技巧

### 1、清除本地使用记录
    + 1、关闭软件
    + 2、删除软件安装位置目录/Sublime_Text3_Stable_Build_3143_x64_Chs/Sublime Text/Data/Local/Session.sublime_session 文件
    
### 2、开启vim模式
    + 1、在菜单栏中： Preferences -> Setting - User 即可打开配置文件进行编辑，将 ignored_packages 项的["Vintage"]里面内容清空,变为："ignored_packages": [],再按 Esc 退出编辑模式，即进入了 Vim 模式。
    + 参考资料：
        + [sublime开启vim模式](https://blog.csdn.net/gb4215287/article/details/78999787)

### 3、配置列编辑快捷键
    + 1、在菜单栏中 首选项 -> 按键绑定-用户
    ~~~
    [
        { 
            "keys": ["ctrl+Alt+shift+1"], "command": "move_to_group", "args": { "group": 0 } 
        },
        { 
            "keys": ["ctrl+Alt+shift+2"], "command": "move_to_group", "args": { "group": 1 } 
        }, 
        { 
            "keys": ["ctrl+Alt+shift+3"], "command": "move_to_group", "args": { "group": 2 } 
        }, 
        { 
            "keys": ["ctrl+Alt+shift+4"], "command": "move_to_group", "args": { "group": 3 } 
        },
        { "keys": ["ctrl+shift+;"], "command": "insert_datetime", "args": {"format": "ymdhms"} },
        { "keys": ["ctrl+alt+k"], "command": "select_lines", "args": {"forward": false} },
        { "keys": ["ctrl+alt+j"], "command": "select_lines", "args": {"forward": true} },
        { "keys":["alt+shift+ctrl+up"],"command":"select_lines", "args": {"forward": false} },
        { "keys":["alt+shift+ctrl+down"],"command":"select_lines","args": { "forward": true} },
        { "keys": ["alt+m"], "command": "markdown_preview", "args": {"target": "browser", "parser":"markdown"} }
    ]
    ~~~


## 六、插件安装记录

### IMESupport-master 时间：2018年6月20日23:16:30
+ 解决问题
	* 输入光标位置不对
+ 参考资料
    * [SublimeText中输入法光标位置不对的解决方法](https://blog.csdn.net/zk673820543/article/details/51242196)

### 文件对比插件 Sublimerge 3.sublime-package 时间：2018-10-01 22:36:41

+ 安装步骤：
    + 下载安装包: Sublimerge 3.sublime-package（https://www.sublimerge.com/packages/ST3/latest/Sublimerge%203.sublime-package）
    + Go to Preferences > Browse Packages... 或直接放在该安装包的Data\Installed Packages下
    + Go one folder up
    + Go to Installed Packages
    + Copy the package to that directory
    + Restart Sublime Text
+ 参考资料：
    + [sublimerge插件下载地址](http://www.sublimerge.com)
    + [sublime非常好用的文件对比插件--sublimerge](https://blog.csdn.net/a0405221/article/details/78769672)