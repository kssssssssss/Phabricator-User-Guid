``### 3.2.1 Arcanist
Arcanist 是用于Code review的命令行工具，官方安装指南:[点我](https://secure.phabricator.com/book/phabricator/article/arcanist_quick_start/)



### 3.1.1 Arcanist 安装
1. 安装依赖
    - 安装PHP （Mac OS系统自带PHP环境无需安装）
        - 下载 http://windows.php.net/download/   [5.3+ [点我下载](http://windows.php.net/downloads/releases/php-5.6.30-nts-Win32-VC11-x86.zip) ]
        - 解压缩至C:/PHP
        - 复制 **php.ini-development** 至 **php.ini **
        - 使用文本编辑器打开php.ini 定位至;extension=php_curl.dll （889行，删除;）
        -  定位至**; extension_dir = "ext"** （734行）将该行内容更改为：
        **extension_dir = "C:\PHP\ext"**
        - 配置PHP环境变量：右键我的电脑，选择[属性][高级系统设置][环境变量] 选择变量PATH,在变量值中添加**C:\PHP** (多个值之间需要使用;间隔)
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
Windows配置
Windows建议使用[Cmder](https://github.com/cmderdev/cmder/releases/download/v1.3.2/cmder.7z)作为命令行工具
将arcanist下的bin目录路径作为天津至系统环境变量中，添加方法不再赘述。

4. 安装成功后，打开Cmd或者Cmder键入以下命令,安装成功会有帮助输出



```bash
arc --help
```








