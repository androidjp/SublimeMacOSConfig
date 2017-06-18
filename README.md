# SublimeMacOSConfig
Sublime configure on MacOS
关于更加详细的配置，可以参考[此网址](http://c.haoduoshipin.com/happysublime/)

## 一、配置相关
1. Sublime 用户配置信息存放目录: ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/User/
2. 可以将自己的配置保存到github中，必要时拉取到此目录：
  * cd ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/
  * ls
  * rm -rf User
  * git clone xxxxxxxx
  * mv xxxxx User

## 二、快捷键相关
1. cmd+shift+p : 打开命令查找面板
  * 然后，redin。。。 可以得到调整代码格式的命令
2. 要定义快捷键，需要到key Binding 的 User 配置中写入
3. 得到相关命令的命令名
  * `control + 反引号`进入命令行界面
  * 输入`sublime.log_commands(True)`设置为显示日志
  * `cmd+shift+p` 并输入相关命令，就可以查看对应的完整命令名

## 三、扩展包管理（Package Control）
1. 在目录`/Applications/Sublime\ Text.app/Contents/MacOS/Packages/`下，就自带了很多包。
2. 在网站https://packagecontrol.io/ 上，可以知道各种包的下载方式，也可以知道package control的安装方式
3. 包的安装卸载：
  * 安装：查找`install package`
  * 卸载：查找`remove package`
  * 查看安装的包：`list package`

## 四、更改图标
0. 注意！！要先关闭编辑器
1. 终端输入：`open /Applications/Sublime\ Text.app/Contents/Resources/`，将内部的Sublime Text.icns 替换为你想要替换的图标。
2. 刷新图标：
  * `touch /Applications/Sublime\ Text.app/`
  * `touch /Applications/Sublime\ Text.app/Contents/Info.plist`
3. 完成刷新

## 五、如何在命令行中使用sublime去打开某些文件？
* 做法一：
  1. 终端输入：`sudo rm /usr/local/bin/subl`
  2. 终端输入：`sudo ln -s /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl`
  3. 详细命令可看：[这里](https://www.sublimetext.com/docs/3/osx_command_line.html)
  4. 详细解决方法：[参考这个](http://stackoverflow.com/questions/32915464/sublime-symlink-disappeared-after-upgrading-to-el-capitan)

## 六、Sublime Test3 调试运行 JS
1. Tools -> Build System -> New Build System
2. Edit  the file：
  ```
  {  
    "cmd": ["/usr/local/bin/node", "--use-strict", "--harmony", "$file"],  
    "selector": "source.js"  
  }  
  ```
3. 命名为js.xxx并保存
4. `Cmd + B`执行即可

## 五、如何在命令行中使用sublime去打开某些文件？
