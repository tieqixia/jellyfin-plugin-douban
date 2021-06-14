# 中文版

## 1. 背景

[Jellyfin](https://github.com/jellyfin/jellyfin) 是一个免费的多媒体数据管理软件。
详情请见[官网](https://jellyfin.media/)

[Douban](https://www.douban.com/)  豆瓣就不用介绍了吧:-)

这个插件是一个 Jellyfin 的元数据提取插件，能够从豆瓣抓取电影和电视剧的元数据，包括评分、简介、
演员等相关信息。

## 2. 使用方式

对于 v10.6.0 以及更新的 Jellyfin 版本，可以通过添加插件仓库的方式安装。

插件仓库地址：https://raw.githubusercontent.com/Libitum/jellyfin-plugin-douban/master/manifest.json


对于 v10.5.x 及之前的版本，请参考以下方式进行安装：

1. 从 Release 页面下载最新的版本，或者自行编译。
2. 把下载的文件解压，然后将 Douban 文件夹放到 Jellyfin 的 "plugins" 目录下。
   * 对于 Linux, plugins 目录在 "$HOME/.local/jellyfin/config/plugins"
   * 对于 Mac 系统, 在 "~/.local/share/jellyfin/plugins"
   * 对于 Docker, 在 Docker 中的 "/config/plugins" 目录下。 相应的宿主机目录请查阅自己
     的目录映射配置
   * 对于 Windows 10, 如果使用管理员权限启动的话，在 "C:\ProgramData\Jellyfin\Server\plugins" 目录下。
   * 对于其他系统，如果你找不到位置，请提 issue 或者与我联系。
3. 重启 Jellyfin Service

## 3. 功能

1. 支持获取电影和电视剧类型的元数据；
2. 支持获取部分电影的背景图片，会在豆瓣海报中尝试寻找合适的图片；
3. 支持延迟请求，避免被豆瓣官方封禁；
4. 不支持把多季的电视剧合并成一个。比如：权力的游戏每一季都是分开的，不支持合并在一起。

## 4. 配置

1. 进入 控制台/媒体库，管理需要使用豆瓣挂削的媒体库，勾选豆瓣相关的元数据下载器即可。
