# XCodeCodeSnippets

### 1.概述
该Repo主要用于同步我的XCode Code Snippet，这里说明下，为什么我要自己维护这个XCodeCodeSnippets，原因主要有两点:

* 虽然Github已经有类似的CodeSnippets Repo，但由于个人习惯不一样，所定义的快捷键就不一样，于是codesnippets文件也会不一样.
* 其他CodeSnippets的Repo，无法自动同步，导致有些CodeSnippets遗失.

### 2.安装
* fork XCodeCodeSnippets
* 执行如下命令
<pre>
wget https://raw.githubusercontent.com/smallmuou/XCodeCodeSnippets/master/install.sh;/bin/bash install.sh <font color="red">您的github名</font>
</pre>
* 重启XCode

### 3.自动同步
* crontab -e 
<pre>
* 10 * * * /Users/<font color="red">此处需修改为您的系统用户名</font>/Library/Developer/Xcode/UserData/CodeSnippets/sync.sh
</pre>
更新频度请自行斟酌，我是设置每天10点同步一次

### 4.快捷键

|快捷键|描述|备注|
|:--|:--|:--|
|pa|property assign|assign属性|
|ps|property strong|strong属性|
|pc|property copy|copy属性|
|pi|property IBOutlet|IBOutlet属性|
|pr|property readonly|只读属性|
|pw|property weak|weak属性|
|bg|GCD Background|后台进程|
|fb|GCD Foreground|主进程|
|cp|Copyright|我的版权信息|

### 5.许可
The repo follow MIT license.