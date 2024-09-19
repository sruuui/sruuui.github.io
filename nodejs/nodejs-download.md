官网：https://nodejs.org/zh-cn

安装时记录安装目录（环境配置时需要），默认为 C:\Program Files\nodejs

测试安装是否成功
node -v
npm -v

环境配置
(1) 找到安装目录，在目录下创建两个文件夹【node_global】和【node_cache】
(2) 用管理员身份打开cmd命令窗口，在窗口输入以下命令
npm config set prefix “你的路径\node_global” （复制你刚刚创建的“node_global”文件夹路径）
npm config set prefix "C:\Program Files\nodejs\node_global"
npm config set cache “你的路径\node_cache” （复制你刚刚创建的“node_cache”文件夹路径）
npm config set cache "C:\Program Files\nodejs\node_cache"

环境变量
【此电脑】-单击右键-【属性】-【高级系统设置】-【环境变量】
变量名：NODE_PATH
变量值：C:\Program Files\nodejs\node_global\node_modules
Tips: 如果输入变量值之后没有自动创建【node_modules】文件夹，就在【node_global】下手动创建一个【node_modules】文件夹，再复制你创建的【node_modules】文件夹的路径地址到变量值

更换国内镜像源
淘宝镜像
npm config set registry http://registry.npm.taobao.org
华为镜像
npm confg set registry https://mirrors.huaweicloud.com/repository/npm/
恢复npm默认镜像，输入以下命令
npm config set registry https://registry.npmjs.org

安装yarn
配置yarn的环境变量
修改yarn的下载镜像
yarn config set registry https://registry.npm.taobao.org -g 
yarn config set sass_binary_site http://cdn.npm.taobao.org/dist/node-sass -g