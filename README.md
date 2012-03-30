# Sublime-Extendscript 
#### 从 Sublime Text 2 编写及运行 Adobe ExtendScript.
A tool to execute ExtendScript from Sublime Text 2.
#### [Sublime Text 2](http://www.sublimetext.com/2)

<embed src="http://www.tudou.com/v/WXGx3VpkgtA/&amp;rpid=16122036&amp;resourceId=16122036_05_11_99/v.swf" type="application/x-shockwave-flash" allowscriptaccess="always" allowfullscreen="true" wmode="opaque" width="480" height="400"></embed>

## 安装 Installation
- `git clone https://moluapple@github.com/moluapple/Sublime-Extendscript.git`
- 或使用github .zip下载选项下载zip压缩包，解压缩并将文件夹重命名为 `Sublime-Extendscript`
- 将整个文件夹放置于 `${packages}` 目录下 `> Windows: %APPDATA%\Sublime Text 2\Packages`

## 使用 Usage
包含py2/py3两种配置，默认为py3版。假如系统安装python 2和3并存的话，可通过为其中一种 Build system 里 cmd 中使用绝对路径来实现。(请修改py27 build system中的路径为你的python27安装路径。)
_备注：目前仅限Windows系统使用_

### Build system
打开一个 jsx 文件, 从 Tools -> Build System 里选择 Indesign/Illustrator, `Ctrl+B` 或 `F7` 运行.

### 已知问题
包含汉字(路径/文件名)的脚本文件因编码问题默认无法运行。

[解决方法](http://www.sublimetext.com/forum/viewtopic.php?f=3&t=6407&start=0&hilit=UnicodeEncodeError)：
打开 `sublime_plugin.py` 文件(位于 Sublime Text 2 安装目录下)，在开头添加以下内容并保存。

	import sys 
	reload(sys) 
	sys.setdefaultencoding('gbk')

### [参考说明](http://applia.tumblr.com/post/18494845809/sublime-text-2-adobe-extendscript)

Have fun!