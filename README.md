# Campus Epidemic Management System

[简体中文](README.zh-CN.md)

A graduation project for campus epidemic management. The admin console brings together campus records, student and teacher temperature monitoring, travel records, and regional epidemic statistics.

## Project layout

| Path | Responsibility |
| --- | --- |
| [`service/service_main/`](service/service_main/) | Campus organization and user records, temperature and travel APIs, and Excel handling. |
| [`service/service_yiqing/`](service/service_yiqing/) | City, province, and national epidemic statistics APIs. |
| [`service/service_msm/`](service/service_msm/) and [`service/service_oss/`](service/service_oss/) | Email and object-storage services. |
| [`common/`](common/) | Shared API response types and service utilities. |
| [`graduation_front_publish/`](graduation_front_publish/) | Vue admin console with campus, temperature, travel, and epidemic statistics views. |

The backend [Maven build](pom.xml) targets Java 8 and uses Spring Boot 2.2, Spring Cloud, MyBatis-Plus, and MySQL. The frontend is based on PanJiaChen's Vue Admin Template. Its [original README](graduation_front_publish/README.md) and [license](graduation_front_publish/LICENSE) are included with the frontend.

This checkout is a graduation-project snapshot. You can trace a workflow from the [admin views](graduation_front_publish/src/views/edu/) to the [backend controllers](service/service_main/src/main/java/top/weidaboy/servicemain/controller/). A local deployment would need its own data and external service configuration.
