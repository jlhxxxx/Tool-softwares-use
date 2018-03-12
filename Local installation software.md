1. [cmder](https://github.com/cmderdev/cmder) 内置 git

    [Cmder--Windows下命令行利器](https://www.cnblogs.com/zqzjs/archive/2016/12/19/6188605.html)

    `ls`不显示中文：在Settings > Startup > Environment里添加：set LANG=zh_CN.UTF8

    修改`λ`为`$`：将`cmder\vendor\clink.lua`中第41行中{lamb}修改为$ 
    即，将`local cmder_prompt = "\x1b[1;32;40m{cwd} {git}{hg} \n\x1b[1;30;40m{lamb} \x1b[0m"`修改为`local cmder_prompt = "\x1b[1;32;40m{cwd} {git}{hg} \n\x1b[1;30;40m$ \x1b[0m"`

    [参考](http://blog.csdn.net/qq_22186119/article/details/77453227)

2. android相关
    * [android_sdk](http://tools.android-studio.org/index.php/sdk)
    
      教程：[安装 Android SDK](http://www.testclass.net/appium/appium-base-sdk/)
    * [adb 驱动](adbshell.com)

3. [apache-jmeter](http://jmeter.apache.org/download_jmeter.cgi)
    * [plugins](http://www.testclass.net/jmeter/install-plugins/)
    * [apache-ant](http://ant.apache.org/bindownload.cgi)

      [基于 Ant 的 JMeter 性能自动化测试](http://blog.csdn.net/wetest_tencent/article/details/51154419)
    * [badboy](http://www.badboy.com.au/)

4. [apache-tomcat](https://tomcat.apache.org/index.html)

5. [driver](http://www.testclass.net/selenium_python/selenium3-browser-driver/)
    * [chrome](https://sites.google.com/a/chromium.org/chromedriver/home)
    * [firefox](https://github.com/mozilla/geckodriver/releases)
    * [IE](http://selenium-release.storage.googleapis.com/index.html)
    * [edge](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/)

      系统设置–>高级–>环境变量–>系统变量–>Path

6. [eclipse](https://www.eclipse.org)
    * [汉化包](www.eclipse.org/babel/downloads.php)

7. [git](https://git-scm.com/download/win)

8. [java](http://www.testclass.net/selenium_java/install-java/)

9. [jenkins](http://www.testclass.net/jenkins/install/)

10. jsunit

11. MyEclipse

12. [nodejs](https://nodejs.org/en/)
    * [cnpm](https://npm.taobao.org/)

        `npm install -g cnpm --registry=https://registry.npm.taobao.org`

13. [python](https://www.python.org/downloads/windows/)
    * selenium

        `pip install selenium`

    * Locust 负载测试

        `pip install locustio`
    
    * 配置 notepad++
        * 制表符款宽度 4，替换为空格

14. [vscode](https://code.visualstudio.com/)

    1. 同步：安装setting sync

       vscode setting sync

       Gist: 448d5bfcb9c48f5e07f97af7c8f636a7

15. [postman](https://www.getpostman.com/)

16. Jenkins

    admin/123456	jlhxxxx/jlhxxxx@gmail.com

17. [TortoiseSVN](https://tortoisesvn.net/downloads.zh.html)