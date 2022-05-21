# README

## 目录

*   [IPFS上传服务](#ipfs上传服务)

    *   [简介](#简介)

        *   [Demo-img ](#demo-img-)
    *   [使用](#使用)
    *   [IF Fork](#if-fork)
        
    *   [IF Download](#if-download)
    *   [API](#api)
    *   [网关和Cid/Hash](#网关和cidhash)
           *   [介绍](#介绍)
           *   [大文件](#大文件)  
        
    *   [Attention](#attention)
    *   [IPFS项目](#ipfs项目)
    *   [IPFS客户端](#ipfs客户端)

# IPFS上传服务

## 简介

Demo：[https://ipf.ramsong.cn/](https://ipf.ramsong.cn/ "https://ipf.ramsong.cn/")

Demo-IPFS主网(官方) : [https://ipfs.io/ipfs/QmeuXBFNqKCk2MxwXG39GyMoDUUk1oKHLc5qaKqjHgYcN3](https://ipfs.io/ipfs/QmeuXBFNqKCk2MxwXG39GyMoDUUk1oKHLc5qaKqjHgYcN3 "https://ipfs.io/ipfs/QmeuXBFNqKCk2MxwXG39GyMoDUUk1oKHLc5qaKqjHgYcN3")

(由于 DNS污染 ，主网可能打不开，可以修改Hosts文件把ipfs.io指向209.94.90.1)

Demo-IPFS小龙(阿里): [https://ipfsgw.stariverpan.com/ipfs/QmeuXBFNqKCk2MxwXG39GyMoDUUk1oKHLc5qaKqjHgYcN3](https://ipfsgw.stariverpan.com/ipfs/QmeuXBFNqKCk2MxwXG39GyMoDUUk1oKHLc5qaKqjHgYcN3 "https://ipfsgw.stariverpan.com/ipfs/QmeuXBFNqKCk2MxwXG39GyMoDUUk1oKHLc5qaKqjHgYcN3")

Demo-IPFS-CloudFlare全球CDN): [https://bafybeihwe2sbuhixw6eg7f3j5gkqo4wuxu7u5lxlzdaww3g3in447dmnpa.ipfs.cf-ipfs.com/](https://bafybeihwe2sbuhixw6eg7f3j5gkqo4wuxu7u5lxlzdaww3g3in447dmnpa.ipfs.cf-ipfs.com/ "[https://tth-ipfs.com/ipfs/QmeuXBFNqKCk2MxwXG39GyMoDUUk1oKHLc5qaKqjHgYcN3](https://bafybeihwe2sbuhixw6eg7f3j5gkqo4wuxu7u5lxlzdaww3g3in447dmnpa.ipfs.cf-ipfs.com/)")

快速上传一些小文件到IPFS全球网络

### Demo-img&#x20;

![](https://cdn.jsdelivr.net/gh/RamSong/IPFS-Upload@main/Demo-4.png)

## 使用

Fork or Download 这个项目

### IF Fork

点击项目 Setting 的Code and automation 块中的 Pages

在右侧的 **Source 块** 中，点击展开 None，选择 main，点击 Save，便会出现链接

你也可以在下面的 Custom Domain 中填写你的自定义域名

![](https://cdn.jsdelivr.net/gh/RamSong/IPFS-Upload@main/Demo-2.png)

### IF Download

*   下载 [Releases](https://github.com/RamSong/IPFS-Upload/releases) 解压所有文件打开index.html就能用

*   通过  Nginx or Apache 运行在服务器or虚拟主机上，绑定域名进行访问

## API

自行修改 static/file.js 第71行的 API 上传接口（给出的接口域名 DNS 可能会被污染）(但至少现在能用)

（ API 接口可以自行搭建或反向代理）

（反向代理请自行搜索）

（搭建请看下面IPFS项目和客户端客户端，安装后运行 ipfs daemon开启节点，其中 5001端口是API，8080 端口是网关）

 目前收集到两个API
 
 https://ipfs.staging.infura.org:5001/api/v0/add?pin=true (反应快一点)
 
 https://ipfs-vvhan-com.glitch.me/api/v0/add?pin=true  （反应有点慢)

## 网关和Cid/Hash

***

### 介绍

![](https://cdn.jsdelivr.net/gh/RamSong/IPFS-Upload@main/Demo-1.png)

收集的可在国内访问的网关：

```纯文本
cf-ipfs.com      
ipfsgw.stariverpan.com
tth-ipfs.com
infura-ipfs.io
gateway.ipfs.io
```

当然你也可自行搭建代理 ipfs.io 进行使用

### 大文件

### [https://transferkit.io/](https://transferkit.io/)

![](https://cdn.jsdelivr.net/gh/RamSong/IPFS-Upload@main/Demo-5.png)

**直接使用 或 把cid替换到别的网关**

## Attention

&#x20; 网站的 *UP自建* 是本人反代的 IPFS 网关，请尽量*不要*使用，**随时跑路**

&#x20; 你可以使用 CloudFlare 的 **Workers** 自己反代  [ipfs.io](https;//ipfs.io/)

  然后在 [index.html](https://github.com/RamSong/IPFS-Upload/blob/main/index.html "index.html") 的37行左右修改链接以替换网关

![](https://cdn.jsdelivr.net/gh/RamSong/IPFS-Upload@main/Demo-3.png)

## IPFS项目

[https://github.com/ipfs/ipfs](https://github.com/ipfs/ipfs "https://github.com/ipfs/ipfs")

## IPFS客户端

推荐Go版 [https://github.com/ipfs/go-ipfs/releases](https://github.com/ipfs/go-ipfs/releases "https://github.com/ipfs/go-ipfs/releases")
