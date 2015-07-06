# XCodeCodeSnippets

### 1.概述
该Repo主要用于同步我的XCode Code Snippet，这里说明下，为什么我要自己维护这个XCodeCodeSnippets，原因主要有两点:

* 虽然Github已经有类似的CodeSnippets管理，但由于个人习惯不一样，所定义的快捷键就不一样，于是codesnippets也会不一样.
* 其他的CodeSnippets的Repo，无法自动同步，导致有些CodeSnippets遗失.

### 2.安装
#### 自动
* fork it
* 执行如下命令
<pre>
wget https://raw.githubusercontent.com/smallmuou/XCodeCodeSnippets/master/install.sh;/bin/bash install.sh <font color="red">您的github名</font>
</pre>

#### 手动
* fork it.
* 备份自己的codesnippet
<pre>
mv ~/Library/Developer/Xcode/UserData/CodeSnippets ~/Library/Developer/Xcode/UserData/CodeSnippets_bak
</pre>
* git clone. 
<pre>
git clone git@github.com:<font color="red">您的github名</font>/XCodeCodeSnippets ~/Library/Developer/Xcode/UserData/CodeSnippets
</pre>
如我的如下:
<pre>
git clone git@github.com:smallmuou/XCodeCodeSnippets ~/Library/Developer/Xcode/UserData/CodeSnippets
</pre>

* 同步自己的codesnippet
<pre>
cp ~/Library/Developer/Xcode/UserData/CodeSnippets_bak/* ~/Library/Developer/Xcode/UserData/CodeSnippets
rm -rf ~/Library/Developer/Xcode/UserData/CodeSnippets_bak
</pre>

### 3.同步
* crontab -e 
<pre>
* 10 * * * /Users/<font color="red">此处需修改为您的系统用户名</font>/Library/Developer/Xcode/UserData/CodeSnippets/sync.sh
</pre>
更新频度请自行斟酌，我是设置每天10点更新一次