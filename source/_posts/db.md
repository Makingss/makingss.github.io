---
title: db
date: 2017-04-14 13:20:30
tags:
---
##### 文档说明
-  ** 用户表 **
> user

| 字段名 | 类型/长度 | 备注 |
| -----|:-------|:--------|
| id | int(10) | user表主键 |
| name | varchar(50) | 用户名称 |
| password | varchar(50) | 用户密码 |
> update_time:'2017.04.14'

---
-  ** 用户基本信息表 **
> member_datas

| 字段名 | 类型/长度 | 备注 |
| -----|:-------|:--------|
| member_id | int(10) | 主键 |
| member_lv_id | int(10) | 用户等级关联字段 |
| point | int(11) | 用户积分 |
| firstname | varchar(50) | 名字 |
| lastname | varchar(50) | 姓氏 |
| area | varchar(255) | 区域 |
| addr | varchar(255) | 地址 |
| mobile | varchar(200) | 电子邮箱 |
| b_year | smallint(5) | 年 |
| b_month | tinyint(1) | 月 |
| b_day | tinyint(1) | 天 |
| sex | enum('0','1','2') | 性别 0、保密1、男,2、女|
| advance | decimal(20) | 会员账户余额 |
| experience | int(11) | 经验值 |
| created_at | timestamp | 创建 |
| updated_at | timestamp | 更新 |

> update_time:'2017.04.14'

