## win bluescreen analysis

* [系统蓝屏日志DMP文件分析工具WinDbg及教程](https://www.yeboyzq.com/zhuomianweihu/xitongyingyongjiqiao/520.html)
* [windbg蓝屏dmp文件分析](http://blog.csdn.net/greless/article/details/71440505)

## software

* [windows环境下wampserver的配置教程——超级详细](http://blog.csdn.net/wuguandi/article/details/53561253)

* [Directory Opus 查看器窗格的中文乱码问题如何解决](https://www.zhihu.com/question/50458466/answer/124012007)

* 将 chrome 安装在非系统盘

  chrome默认安装路径为C:\Program Files (x86)\Google\Chrome，这时要确定 C:\Program Files (x86)\Google\ 下面没有chrome这个文件夹，因为这个要由mklink来创建。而文件夹 D:\Program Files\Google\Chrome 要先建立好。
  windows7系统在cmd命令行中输入：

  ```
  mklink /d "C:\Program Files (x86)\Google\Chrome" "D:\Program Files\Google\Chrome"
  ```

  符号链接制作完毕，开始安装chrome，安装完后进入 D:\Chrome 文件夹，这个是chrome真正的文件夹，而 C:\Program Files (x86)\Google\Chrome 只是一个映射，不占用c盘空间。

  chrome 插件安装目录：C:\Users\Administrator\AppData\Local\Google\Chrome\User Data\Default\Extensions

* [如何把本地项目上传到GitHub](https://jingyan.baidu.com/article/36d6ed1f9ba2bb1bce488368.html)


* [github 遇到Permanently added the RSA host key for IP address '192.30.252.128' to the list of known hosts问题解决](http://www.cnblogs.com/xiangyangzhu/p/5316041.html)

* github 每次 push 都要输用户名和密码解决方法

  在 github.com 上建立了一个小项目，可是在每次 push 的时候，都要输入用户名和密码，很是麻烦，原因是使用了 https 方式 push，在 bash 里边输入 `git remote -v` 可以看到形如下面的返回结果：

  ```
  origin https://github.com/yuquan0821/demo.git (fetch)
  origin https://github.com/yuquan0821/demo.git (push)
  ```

  下面把它换成ssh方式的：

  ```
  git remote rm origin
  git remote add origin git@github.com:yuquan0821/demo.git
  git push origin 
  ```

* [VSCode tasks.json中的各种替换变量的意思 ${workspaceFolder} ${file} ${fileBasename} ${fileDirname}等](http://blog.csdn.net/bat67/article/details/78302870)

## windows

*  [有线网卡与无线网卡同时使用](http://www.cnblogs.com/lovemo1314/archive/2010/10/08/1846057.html)
* [在家轻轻松松上IPv6站点之Teredo篇](http://bbs.pcbeta.com/viewthread-1580771-1-1.html)

## linux

* [linux下杀死进程（kill）的N种方法](http://blog.csdn.net/andy572633/article/details/7211546)
* [修改 ubuntu 默认启动项](https://jingyan.baidu.com/article/afd8f4de58959134e386e969.html)

