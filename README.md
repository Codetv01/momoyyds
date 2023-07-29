<p align="center">
    <img src="./assets/img/logo.png" width="250" height="200">
</p>
<h1 align="center">哔哩哔哩-API收集整理</h1>
<p align="center">
    <a href="https://github.com/SocialSisterYi/bilibili-API-collect/issues" style="text-decoration:none">
        <img src="https://img.shields.io/github/issues/SocialSisterYi/bilibili-API-collect.svg" alt="GitHub issues"/>
    </a>
    <a href="https://github.com/SocialSisterYi/bilibili-API-collect/stargazers" style="text-decoration:none" >
        <img src="https://img.shields.io/github/stars/SocialSisterYi/bilibili-API-collect.svg" alt="GitHub stars"/>
    </a>
    <a href="https://github.com/SocialSisterYi/bilibili-API-collect/network" style="text-decoration:none" >
        <img src="https://img.shields.io/github/forks/SocialSisterYi/bilibili-API-collect.svg" alt="GitHub forks"/>
    </a>
    <a href="https://github.com/SocialSisterYi/bilibili-API-collect/actions">
        <img src="https://img.shields.io/github/actions/workflow/status/SocialSisterYi/bilibili-API-collect/vuepress-deploy.yml">
    </a>
    <a href="https://github.com/SocialSisterYi/bilibili-API-collect/blob/master/LICENSE" style="text-decoration:none" >
        <img src="https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg" alt="GitHub license"/>
    </a>
</p>
<h3 align="center">野生API文档</h3>
<h3 align="center">不断更新中....</h3>

本项目旨在对 B站 WEB、APP、TV 等客户端中，散落在世界各地的野生 API 进行收集整理，研究使用方法并对其进行说明，运用了黑箱法、控制变量法、代码逆向分析、拆包及反编译法、网络抓包法等研究办法

本文档探讨的对象是主站业务接口，[官方开放平台](https://openhome.bilibili.com/doc) 和 [直播开放平台](https://open-live.bilibili.com/document/) 均不属于本项目范畴，请移步

B站 API 采用 C/S 结构，大多数接口为 REST API 和 gRPC，少部分接口为 WebSocket；REST API 接口请求数据大多为 url query 表单或 JSON，返回数据大多为 JSON 或 Protobuf，强制使用 https 协议

📖阅读地址：[GithubPages](https://socialsisteryi.github.io/bilibili-API-collect/)

小小的 Demo：~~av583785685~~ [视频失效原因](https://shakaianee.top/archives/56/) ([Youtube备链](https://www.youtube.com/watch?v=nfF91Z6fqGk))

::: warning ⚠️声明

1. 本项目遵守 CC-BY-NC 4.0 协议，禁止一切商业使用，如需转载请注明作者 ID
2. **请勿滥用，本项目仅用于学习和测试！请勿滥用，本项目仅用于学习和测试！请勿滥用，本项目仅用于学习和测试！**
3. 利用本项目提供的接口、文档等造成不良影响及后果与本人无关
4. 由于本项目的特殊性，可能随时停止开发或删档
5. 本项目为开源项目，不接受任何形式的催单和索取行为，更不容许存在付费内容

:::

## 🌱参与贡献

欢迎各位 dalao 对本项目做出贡献，也希望每个使用者都能提出宝贵的意见

目前本项目存在的问题包括但不限于：

1. 文档二级目录尚未完成
2. 部分文档较旧，修改与更新没有跟进
3. 目前文档使用 markdown 语法编写，不易生成编程语言的 SDK，详见 [#604](https://github.com/SocialSisterYi/bilibili-API-collect/issues/604)

更多信息请浏览 [贡献指南](CONTRIBUTING.md)

## 🍴目录

计划整理分类 & 目录：(文档已完结请选中 checkbox) 

- [ ] [接口签名与验证](docs/misc/sign)
  - [x] [APP API 签名](docs/misc/sign/APP.md)（`appkey`与`sign`）
  - [x] [已知的 APPKey](docs/misc/sign/APPKey.md)
  - [x] [Wbi 签名](docs/misc/sign/wbi.md)（`wts`与`w_rid`）

- [x] [公共错误码](docs/misc/errcode.md)
- [x] [图片格式化](docs/misc/picture.md)
- [x] [bvid 说明](docs/misc/bvid_desc.md)
- [ ] [gRPC API 接口定义](grpc_api)
- [ ] [登录](docs/login)
  - [x] [登录操作 (人机认证)](docs/login/login_action)
    - [x] [短信登录](docs/login/login_action/SMS.md)
    - [x] [密码登录](docs/login/login_action/password.md)
    - [x] [二维码登录](docs/login/login_action/QR.md)
    - [ ] SNS 登录 (QQ & 微信 & 微博)
  - [x] [登录基本信息](docs/login/login_info.md)
  - [ ] [个人中心](docs/login/member_center.md)
  - [ ] [注销登录](docs/login/exit.md)
  - [x] [登录记录](docs/login/login_notice.md)
  - [x] [Web 端 Coookie 刷新](docs/login/cookie_refresh.md)
- [ ] [消息中心](docs/message)
  - [ ] [通知类消息](docs/message/msg.md)
  - [ ] [私信](docs/message/private_msg.md)
  - [ ] 设置
- [ ] [用户](docs/user)
  - [x] [基本信息](docs/user/info.md)
  - [x] [状态数](docs/user/status_number.md)
  - [x] [关系](docs/user/relation.md)
  - [ ] [个人空间](docs/user/space.md)
  - [x] [检查昵称是否可注册](docs/user/check_nickname.md)
  - [x] [用户注册](docs/user/register.md)
  - [x] [用户认证类型一览](docs/user/official_role.md)
- [ ] [大会员](docs/vip)
  - [ ] [大会员基本信息](docs/vip/info.md)
  - [ ] [大会员中心](docs/vip/center.md)
  - [ ] [大会员签到](docs/vip/clockin.md)
  - [ ] [大会员操作](docs/vip/action.md)
- [ ] [视频](docs/video)
  - [x] [视频分区一览 (分区代码)](docs/video/video_zone.md)
  - [x] [基本信息](docs/video/info.md)
  - [x] [状态数](docs/video/status_number.md)
  - [x] [快照](docs/video/snapshot.md)
  - [x] [点赞 & 投币 & 收藏 & 分享](docs/video/action.md)
  - [ ] [TAG](docs/video/tags.md)
  - [x] [视频推荐](docs/video/recommend.md)
  - [x] [播放&下载地址 (视频流)](docs/video/videostream_url.md)
  - [ ] [互动视频](docs/video/interact_video.md)
  - [x] [高能进度条](docs/video/pbp.md)
  - [ ] [信息上报 (心跳及记录历史)](docs/video/report.md)
  - [x] [视频属性数据](docs/video/attribute_data.md)
  - [x] [视频在线人数](docs/video/online.md)
- [ ] [剧集 (番剧、影视)](docs/bangumi)
  - [ ] [基本信息](docs/bangumi/info.md)
  - [ ] [播放&下载地址（视频流）](docs/bangumi/videostream_url.md)
  - [ ] [时间轴](docs/bangumi/timeline.md)
  - [ ] 状态数
  - [ ] 操作
- [ ] [视频弹幕](docs/danmaku)
  - [x] [protobuf 实时弹幕](docs/danmaku/danmaku_proto.md)
  - [x] [protobuf 弹幕元数据（BAS 弹幕 / 互动弹幕）](docs/danmaku/danmaku_view_proto.md)
  - [x] [xml 实时弹幕](docs/danmaku/danmaku_xml.md)
  - [x] [历史弹幕](docs/danmaku/history.md)
  - [x] [快照](docs/danmaku/snapshot.md)
  - [ ] [弹幕操作](docs/danmaku/action.md)
  - [ ] 高级弹幕
  - [ ] 屏蔽管理
  - [ ] 智
