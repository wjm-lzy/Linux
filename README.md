# Linux
<h6>Linux内核负责两个功能：管理计算机硬件资源，为上层应用程序提供运行环境</h6>
<h6>系统调用：内核给上层应用程序提供的接口</h6>
<h6>库函数：把系统调用封装为函数，方便移植和使用</h6>
<h6>shell:命令行解释器，经常使用的为bash，位于/bin/bash</h6>
<h6></h6>

<h2>vim编辑器</h2>
<h3>设计理念</h3>
<h6>vim的设计理念为组合，如：vim中d表示删除，j表示移动到下一行，那么dj就表示删除该行和下一行</h6>
<h6>一般为Action + motion</h6>
<h6>在最前面加上数字n，表示要重复命令多少次</h6>
<h3>模式切换</h3>
<h6>vim是一种多模式编辑器 包含三种模式，相同按键在不同模式下有不同功能</h6>
<h6>分为普通模式，插入模式，视图模式</h6>
<h6>其余两个模式按esc可以退出到普通模式</h6>
<h6>ctrl+V，普通模式进入到视图模式</h6>
<h6>从普通模式进入插入模式有多种选择：</h6>
<h6>
<li>i:在光标前面插入</li>
<li>I:在行首插入</li>
<li>a:在光标后面插入</li>
<li>A:在行尾部插入</li>
</h6>
<h6>在vim中普通模式还有一些光标移动快捷键使用</h6>
<h5>动作（action）快捷方式</h5>
<h6>删除文本:dd删除一行，ndd删除n行，d^删除到行首，d$删除到行尾</h6>
<h6>p粘贴，u撤销，ctrl+r恢复，yy复制一行，nyy复制n行</h6>

<h2>常用命令</h2>
<h6>与window不一致的是，Linux是使用数的结构来管理文件系统的，我们把树的根节点称为根目录，用/表示</h6>
<h6>man 卷数 命令 查阅某个命令</h6>
<h6>shutdown now 挂起，关机，或者重启，常用选项 -H挂起，-P重启，-r重启</h6>
<h4>与目录相关的一些命令</h4>
<h6>pwd：查看当前目录</h6>
<h6>cd:修改当前工作目录,常用方式:cd /usr/lib,cd /,cd ~,cd .,cd ..,cd -跳到上一级目录<br>~代表家目录。/代表根目录</h6>
<h6>环境变量：/user/bin/env</h6>
<h6>创建目录:mkdir,选项为-p，递归创建</h6>
<h6>sudo apt install tree安装树，可以显示目录的树状结构</h6>
<h6>删除目录:rmdir,选项为-p，递归</h6>
<h6>通配符：*匹配多个字符，?匹配任意一个字符，集合匹配集合内任意一个字符[characters]</h6>
<h6>通过inode（物理文件的唯一标识）将物理文件系统和虚拟文件系统联系到一起</h6>
<h6>ls命令：选项-a显示所有内容，-i显示inode号，-l显示长格式，-h以可读形式显示文件大小</h6>
<h6>cp命令：cp 1，2可以用来复制路径1到路径2，路径可以是文件，也可以是目录，选项-n 不覆盖，-i文件存在给出用户提示信息，表示是否覆盖，-R递归复制</h6>
<h6>mv命令：移动文件，把一个文件移动到另一个位置，可以修改名称，-n表示不覆盖，-i给出提示信息，实现原理就是更改虚拟文件系统和物理文件系统之间的映射</h6>
<h6>rm命令：删除文件，-f强制删除，-r递归删除，-i提示删除</h6>
<h6>别名：有些命令比较长，我们就为其起一个别名，方便以后使用，alias命令：alias 名称='命令'，使用alias文件只会在一次开机中起作用</h6>
<h6>如果配置别名，需要在.bashrc文件中配置</h6>
<h6>source使用bash重新执行某个计算机文件</h6>