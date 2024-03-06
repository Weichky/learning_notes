## Linux基本操作
### 通用

`-i`表示问讯
#### 元字符通配符
- ？代表任意单个字符
- \*代表零个或多个字符
- \[ay]表示a或y
- \[a-i]表示a至i

### 文件操作
`touch` 创建文件
`mkdir/rmdir` 创建/删除目录

`ls` 显示文件和目录
- `-F`在目录后添加/，在可执行文件后添加\*
- `-a`显示隐藏文件
- `-R`递归显示
- `-l`显示长列表
	- d表示目录
	- -表示文件
	- l表示链接文件

`mv`移动
- 不写目录可以改名

`rm`删除
- `-f`不问询
- `-i`问询
- `-r`递归删除目录下所有文件，最后删除该目录

### 进程管理
`ps` 静态显示进程
`top`动态显示进程

`kill` 使用PID发送信号（默认TEARM）

Linux进程信号

| 信号  |  名称  |        描述        |
| :-: | :--: | :--------------: |
|  1  | HUP  |        挂起        |
|  2  | INT  |        中断        |
|  3  | QUIT |       结束运行       |
|  9  | KILL |      无条件终止       |
| 15  | TERM |      尽可能终止       |
| 17  | STOP |   无条件停止运行，但不终止   |
| 18  | TSTP |  停止或暂停，但继续在后台运行  |
| 19  | CONT | 在STOP或TSTP之后恢复执行 |

`pkill`使用程序名代替PID*使用通配符杀死系列进程*

### 其他工具
`file`显示文件类型

`cat`显示文本内容
- `-n`给所有行加上行号
- `-b`给有文本的行加上行号

`more`按页显示文本内容

`less` *less is more*

`tail`显示文件尾部（默认10行）*用于log等需要读最新文本的*
- `-n`修改显示行数
- `-f`同步显示修改

`head`显示文件头部（默认10行）*用法同tail，但无法同步显示*

`nautilus` 文件管理

`gedit` 文本编辑器
#### apt&apt-get
`aptitude`自动处理依赖关系
`apt/apt-get autoremove/autoclear`自动卸载和清理缓存

#### 解压`.tgz`文件
`tar zxvf 'file'.tgz -C '/dir'`*解压到指定目录*
## docker 相关
#### docker 基本操作
`docker pull [IMAGE]`*下载Linux发行版*

`docker run [OPTIONS] IMAGE` *创建并进入一个容器*
- `-i`以交互模式运行容器通常与`-t`同时使用
- `-t`为容器重新分配一个伪输入终端
- `--name="name"`为容器指定一个名称

`docker create IMAGE`*与run相同，但是创建后不运行*

`docker rm CONTAINER`*删除一个容器*

`docker rmi IMAGE`*删除Linux镜像*

`docker start/stop/restart id/name` *启动/停止/重启一个容器*

`docker attach id/name`*进入某容器*
`docker ps -a`*显示所有容器以及信息*

`docker cp [OPTIONS] SRC_1 SRC_2`*将SRC_1拷贝至SRC_2*

#### 容器内操作
输入`exit`彻底关闭退出.
输入按键`CTRL+P`和`CTRL+Q`暂时退出容器，容器仍在运行

#### 关于图形化
参考知乎：<a href=https://zhuanlan.zhihu.com/p/460494660>docker容器图形化界面显示</a>

首先要安装X11界面服务
`sudo apt-get install x11-xserver-utils`

要在创建容器时添加参数
- `-v /tmp/.x11-unix:/tmp/.x11-unix`共享本地UNIX端口
- `-e DISPLAY=unix$DISPLAY`修改环境变量DISPLAY
- `-e GDK_SCALE`以整倍数缩放UI元素
- `--net=host` 进入host模式
测试可以使用`xarclock`*一个显示时钟的小程序*

每次vi要输入`xhost +`开放权限，允许所有用户（包括docker）访问X11的显示接口.

## 系统相关
systemctl
- `start/stop`启动/结束服务
- `status`检查状态
- `reload/restart`重载/重启
- `kill`
- `enable/disable`引导时启用/禁用