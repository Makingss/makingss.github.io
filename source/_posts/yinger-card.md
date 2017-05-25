---
title: yinger_card
date: 2017-05-25 14:58:32
tags:
---
##### 文档说明
-  ** 用户表 **
> user

| 字段名 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
| res | bool |  Y  | true | 返回json字符串 |
| rsp |  obj | Y | - | 返回结果状态 |
| cpns_id | int | Y | 6 | 优惠ID是该类型卡的号码 |
| prefix | string | Y | "Baaaa" | 优惠码前缀 |
| coupon_total_number | int | Y | "10" | 优惠库存 |
| cpns_name | string  | Y | "满100减10元" | 优惠券名称 |
| description | string | Y | "卡券优惠活动描述" | 优惠券描述 |
| start_time | time | Y | 1495382400 | 优惠券开始时间(时间戳) |
| end_time | time | Y | 1498233600 | 优惠券截止时间(时间戳) |
| brands | array | Y | "1","2","3" | 品牌 1:音儿2:恩裳3:诗篇4:歌中歌5:奥丽嘉朵6:十二篮7:诗篇蓝标8:音儿蓝标9:恩裳蓝标|
| is_allow_aftersale | bool | Y | "0" | 是否允许售后 |
| activity_start_allow | bool | N | "" | 允许售后(活动开始后) 0表示不允许该售后方式 |
| activity_finish_allow | bool | N | "" | 允许售后(活动结束后) 0表示不允许该售后方式 |
| condition | array | Y | - | 活动条件 |
| operator | sting | Y | ">=" | 符号 |
| value | string | Y | "100" | 当订单总额满100时，将享受优惠方案。当value为0时对所有订单给予优惠 |
| action_solution | array | Y | - | 优惠方案 |
| action_total_amount | array | Y | 10 | 该订单享有10元优惠 |
| percent | array | Y | 50 | 订单优惠享有50%优惠 |

> update_time:'2017.04.14'