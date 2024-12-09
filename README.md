# iCoursera产品设计文档

> 第三组
>
> 项目成员： 李安鑫 卞卡 干凯洁 崔彦 吴霁航 李雅琪 李思琪 朱俊哲（排名不分先后）
>
> 产品名：iCoursera在线课堂平台

## 一、项目介绍

**iCoursera** 是一个面向教育领域的在线学习平台，旨在通过整合丰富的课程资源和高效的管理系统，为学生、讲师和管理员提供便捷且全面的学习与教学体验。平台设计注重用户需求，分为学生端、讲师端和管理员端三大模块，各自具备针对性功能，确保不同角色的需求得到满足，实现教育资源的高效流通与管理。

**iCoursera** 基于**SpringBoot+Vue**前后端分离的在线教育平台项目，单体应用服务架构。系统共设计三种角色：管理员、讲师和学员，三个角色分别对应一个操作端。也就是本系统1个后台项目，三个前端项目。管理员端没有引入角色和权限管理，只有一个角色。

已实现的功能列表展示：

**管理员端：**

- 数据统计
- 轮播图管理
- 课程管理
  - 课程列表
  - 课程审核
  - 分类管理
- 讲师管理
  - 讲师列表
  - 讲师审核
- 学员管理
- 用户管理
- 订单管理

**讲师端：**

- 发布课程
- 课程管理
- 评论管理
- 消息接收

**学员端（网站首页）：**

- 登录注册
- 分类与轮播图展示
- 课程列表展示
- 课程搜索（关键词、分类、讲师）
- 课程详情（播放器、课程介绍、评论、讲师简介、订阅）
- 订阅订单
- 讲师入驻

## 二、需求整理

### 二、用户需求分析

随着互联网技术的飞速发展，在线教育已成为现代教育的重要模式。生活节奏的加快使用户的时间日益碎片化，他们迫切需要一个能够随时随地学习的平台，以满足不同场景下的学习需求。同时，系统化的学习进度跟踪与提醒功能，能够帮助用户全面了解学习情况，从而提升效率并优化学习路径。

在数字化学习环境中，个性化体验已成为用户关注的重点。用户不仅希望能够收藏感兴趣的课程，方便回顾，还期待通过学习数据生成个性化报告，以掌握学习节奏、评估，成果，进而调整学习计划。与此同时，内容生产者（讲师）也渴望拥有便捷的平台，用于发布和管理课程，并通过数据分析优化教学内容。

在平台管理层面，确保课程内容质量与合规性、维护平台秩序、提升优质内容的曝光率，是在线教育平台持续发展的关键。通过优化平台运营与用户体验，构建一个内容丰富、管理规范的生态系统，将满足多样化的学习需求，推动在线教育迈向更高水平。

### 2.用户定位

1. 学生端用户：学习需求；个性化学习体验；学习进度提醒；互动与交流功能
2. 讲师端用户：课程创建与管理；教学效果反馈；互动与答疑功能；内容发布与审核
3. 管理员端用户：课程质量与审核；用户管理；平台管理；内容优化；数据分析与运营

## 三、技术选型

**开发环境**

- 工具：IntelliJ IDEA
- JDK 1.8
- 数据库：MySQL 8.0.15
- 项目构建：后端Maven、前端 webpack

**后端**

- Web框架：Spring Boot

- 字段校验：Spring Validation

- 持久层：[MyBatis-Plus](https://mybatis.plus/)

- 接口文档：Swagger2

- 缓存：Redis

- 工具：[Hutool](https://www.hutool.cn/)

- 资源存储：阿里云对象存储OSS

- 课程视频点播：阿里云视频点播VoD

- Lombok：请确保您的 IDE 安装了此插件 

**前端**

- Vue.js2 全家桶

- Element-UI

- [vue-admin-template](https://github.com/PanJiaChen/vue-admin-template) 后台模板

- axios

- 图表：v-charts（ECharts）

- 富文本编辑器：[wangEditor](https://github.com/wangeditor-team/wangEditor/)