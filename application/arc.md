``### 3.2.1 Arcanist
Arcanist 是用于Code review的命令行工具，官方安装指南:[点我](https://secure.phabricator.com/book/phabricator/article/arcanist_quick_start/)



### 3.1.1 Arcanist 安装
1. 安装依赖
    - 安装PHP 
        - 下载 http://windows.php.net/download/   [5.3+ [点我下载](http://windows.php.net/downloads/releases/php-5.6.30-nts-Win32-VC11-x86.zip) ]
        - 解压缩至C:/PHP
        - 复制 **php.ini-development** 至 **php.ini **
        - 
    - 安装Git https://git-scm.com/downloads
2. clone Arcanist 仓库
  https://github.com/phacility/arcanist.git
  https://github.com/phacility/libphutil.git
  可以替换成国内地址：
  https://git.oschina.net/signit/arcanist.git
  https://git.oschina.net/signit/libphutil.git  
    
    ```bash
    git clone https://github.com/phacility/libphutil.git
    git clone https://github.com/phacility/arcanist.git
    ```
3. 配置环境变量
Mac，Linux配置
在系统的profile或者是bash的配置文件末尾加上下面这一句

    ```bash
    export PATH=$PATH:/somewhere/arcanist/bin/
    ```
Windows安装
Windows建议使用Git Bash作为命令行工具







