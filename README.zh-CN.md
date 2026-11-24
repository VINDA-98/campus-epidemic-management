# 校园疫情管理系统

[English](README.md)

校园疫情监测毕业设计。管理端维护校园人员和组织信息，记录师生体温与行程，并提供市、省和全国维度的疫情统计。

## 项目结构

| 路径 | 职责 |
| --- | --- |
| [`service/service_main/`](service/service_main/) | 学院、专业、班级和人员信息，体温和行程接口，以及 Excel 处理。 |
| [`service/service_yiqing/`](service/service_yiqing/) | 市、省和全国维度的疫情统计接口。 |
| [`service/service_msm/`](service/service_msm/) 和 [`service/service_oss/`](service/service_oss/) | 邮件和对象存储服务。 |
| [`common/`](common/) | 共用的 API 响应类型和服务工具。 |
| [`graduation_front_publish/`](graduation_front_publish/) | Vue 管理端，包含校园信息、体温、行程和疫情统计页面。 |

后端的 [Maven 工程](pom.xml) 以 Java 8 为目标版本，使用 Spring Boot 2.2、Spring Cloud、MyBatis-Plus 和 MySQL。前端基于 PanJiaChen 的 Vue Admin Template，目录内保留了[原 README](graduation_front_publish/README.md) 和[许可证](graduation_front_publish/LICENSE)。

当前代码保留了毕业设计的实现。可以从[管理端页面](graduation_front_publish/src/views/edu/)追踪到对应的[后端控制器](service/service_main/src/main/java/top/weidaboy/servicemain/controller/)。本地部署需要准备自己的数据和外部服务配置。
