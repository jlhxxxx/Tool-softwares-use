# FAQ

## software

* [Directory Opus 查看器窗格的中文乱码问题如何解决](https://www.zhihu.com/question/50458466/answer/124012007)


### Chrome

* 将 chrome 安装在非系统盘

  chrome默认安装路径为C:\Program Files (x86)\Google\Chrome，这时要确定 C:\Program Files (x86)\Google\ 下面没有chrome这个文件夹，因为这个要由mklink来创建。而文件夹 D:\Program Files\Google\Chrome 要先建立好。
  windows7系统在cmd命令行中输入：

  ```powershell
  mklink /d "C:\Program Files (x86)\Google\Chrome" "D:\Program Files\Google\Chrome"
  ```

  符号链接制作完毕，开始安装chrome，安装完后进入 D:\Chrome 文件夹，这个是chrome真正的文件夹，而 C:\Program Files (x86)\Google\Chrome 只是一个映射，不占用c盘空间。

  chrome 插件安装目录：C:\Users\Administrator\AppData\Local\Google\Chrome\User Data\Default\Extensions


### cmder

- 基本设置[Cmder--Windows下命令行利器](https://www.cnblogs.com/zqzjs/archive/2016/12/19/6188605.html)

- [参考](http://blog.csdn.net/qq_22186119/article/details/77453227)

- 修改`λ`为`$`

  将`cmder\vendor\clink.lua`中第41行中{lamb}修改为$ 
  即，将`local cmder_prompt = "\x1b[1;32;40m{cwd} {git}{hg} \n\x1b[1;30;40m{lamb} \x1b[0m"`修改为`local cmder_prompt = "\x1b[1;32;40m{cwd} {git}{hg} \n\x1b[1;30;40m$ \x1b[0m"`

- `ls`不显示中文

  在Settings > Startup > Environment里添加：set LANG=zh_CN.UTF8

- cmder右键`cmder here`打开命令窗口不在当前目录解决方法

  在**setting - startup - Command line**设置成如下：

  - 以cmd启动：

    `cmd /k "%ConEmuDir%\..\init.bat" -new_console:%__CD__%`


  - 以bash启动：

    `*cmd /c "%ConEmuDir%\..\git-for-windows\bin\bash" --login -i -new_console:d:%CMDER_START%`

### MyEclipse10

* SVN

  * 下载SVN插件subclipse：[site-1.6.18](http://subclipse.tigris.org/servlets/ProjectDocumentList?folderID=2240) （MyEclipse10最高使用1.6.18版本）
  * 在**MyEclipse——MyEclipse 10——dropins——SVN**（没有就新建）下，复制刚才下载的site-1.6.18解压后的**features**和**plugins**文件夹
  * 重启MyEclipse，此时选择**窗口——打开透视图——其他**即可看到**SVN资源库研究**，**右键——新建资源库位置**开始连接远程资源库

* 反编译插件

  * 下载 [JadClipse](http://prdownloads.sourceforge.net/jadclipse/net.sf.jadclipse_3.3.0.jar?download) ，将 net.sf.jadclipse_3.3.0.jar 拷贝到 MyEclipse 的 plugins 目录下（可以自己建个文件夹）

  * 下载 [jad.exe](https://varaneckas.com/jad/) ，解压到 jdk 目录 `..\MyEclipse\Common\binary\com.sun.java.jdk.win32.x86_64_1.6.0.013`

  * 设置 MyEclipse 英文启动并重启（中文会报错）

    在 MyEclipse.ini 最后一行，修改`-Duser.language=zh`为`-Duser.language=en`

  * 在 MyEclipse 窗口下，选择 Window > Preferences > Java > JadClipse ，配置 `Path to Decompiler` 为刚才解压的 jad.exe 完整路径

  * （可选）修改临时文件夹：`Directory for temporary files`

  * （可选）将`Use Eclipse code formatter(overrides Jad formatting instructions)`选项打勾，这样可以与Ctrl+Shif+F格式化出来的代码样式一致

  * (不确定)解决中文反编译的问题，在 MyEclipse窗口下，点击 Window > Preferences > Java > JadClipse > Misc，将`Convert Unicode strings into ANSI strings`选项打勾

  * （可能用到）设置 *.class 文件类型默认打开方式：在 Window > Preferences > General > Editors > File Assoiciatior 下，点击 Associate editors 栏下Add增加按钮，添加 JadClipse Class File Viewer 并设置成默认

### GitHub

* [如何把本地项目上传到GitHub](https://jingyan.baidu.com/article/36d6ed1f9ba2bb1bce488368.html)


* [github 遇到Permanently added the RSA host key for IP address '192.30.252.128' to the list of known hosts问题解决](http://www.cnblogs.com/xiangyangzhu/p/5316041.html)

* github 每次 push 都要输用户名和密码解决方法

  在 github.com 上建立了一个小项目，可是在每次 push 的时候，都要输入用户名和密码，很是麻烦，原因是使用了 https 方式 push，在 bash 里边输入 `git remote -v` 可以看到形如下面的返回结果：

  ```bash
  origin https://github.com/yuquan0821/demo.git (fetch)
  origin https://github.com/yuquan0821/demo.git (push)
  ```

  下面把它换成ssh方式的：

  ```bash
  git remote rm origin
  git remote add origin git@github.com:yuquan0821/demo.git
  git push origin 
  ```

### IE

* 卸载IE11

  * 先卸载更新

  * 在cmd中输入

    ```powershell
    FORFILES /P %WINDIR%\servicing\Packages /M Microsoft-Windows-InternetExplorer-11..mum /c "cmd /c echo Uninstalling package @fname && start /w pkgmgr /up:@fname /norestart"
    ```


### Java

* 设置环境变量（在系统命令提示符中输入`java`和`javac`检验）

  新建 系统变量名：`JAVA_HOME` 变量值：`JDK安装路径（不是JRE）`   

  修改 系统变量名：`PATH` 变量值(在起始位置添加)：`%JAVA_HOME%\bin；`  

  变量名：`CLASSPATH` 变量值：`.;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;`

### Total Commander

* [用Total Commander替换windos默认资源管理器的方法](https://blog.csdn.net/u010528745/article/details/41759463)


* [TC 插件中文主页](http://xbeta.info/tc/addons.htm)

### VS Code

* [预定义变量](https://code.visualstudio.com/docs/editor/variables-reference#_predefined-variables)
  * `${workspaceRoot}` =`${workspaceFolder}` VS Code当前打开的文件夹
  * `${workspaceFolderBasename} ` VS Code中打开文件夹的路径, 但不包含"/"
  * `${file}` 当前打开的文件
  * `${relativeFile} `相对于workspaceRoot的相对路径
  * `${fileBasename} `当前打开文件的文件名
  * `${fileBasenameNoExtension}` 当前打开文件的文件名，不含扩展名
  * `${fileDirname} `当前打开文件的目录名，是绝对路径
  * `${fileExtname}` 当前打开文件的拓展名，如`.json`
  * ``${cwd}` the task runner's current working directory on startup
  * `${lineNumber}`  the current selected line number in the active file
* 环境变量
  * 环境变量`${env.Name}` (e.g. `${env.PATH}`)
* 参考[变量替代](https://code.visualstudio.com/docs/editor/tasks#_variable-substitution)

### WAMP

* [windows环境下wampserver的配置教程——超级详细](http://blog.csdn.net/wuguandi/article/details/53561253)

* 提示语言默认是法语，修改成英文

  找到my.ini，将`lc-messages=fr_FR`改成`lc-messages=en_US`

## windows

* [有线网卡与无线网卡同时使用](http://www.cnblogs.com/lovemo1314/archive/2010/10/08/1846057.html)

* [在家轻轻松松上IPv6站点之Teredo篇](http://bbs.pcbeta.com/viewthread-1580771-1-1.html)

* 关闭 ie 安全检查

  运行：gpedit.msc
  本地计算机策略>计算机配置>管理模块>Windows组件>Internet Explorer
  右边找到“关闭安全设置检查功能”设置为“已启用”

### win bluescreen analysis

- [系统蓝屏日志DMP文件分析工具WinDbg及教程](https://www.yeboyzq.com/zhuomianweihu/xitongyingyongjiqiao/520.html)
- [windbg蓝屏dmp文件分析](http://blog.csdn.net/greless/article/details/71440505)

### win10

* 应用商店卸载后重新安装，管理员权限运行`powershell`

  ```powershell
  Get-AppXPackage *WindowsStore* -AllUsers | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)\AppXManifest.xml"}
  ```

* 关闭“更新并关机”

  regedit--HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU

  新建SWORD 32位值，名称：`NoAutoRebootWithLoggedOnUsers`，值：`1`。

## linux

* [linux下杀死进程（kill）的N种方法](http://blog.csdn.net/andy572633/article/details/7211546)