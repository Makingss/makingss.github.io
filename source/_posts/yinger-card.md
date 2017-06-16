---
title: yinger_card
date: 2017-05-25 14:58:32
tags:
---
##### 文档说明
-  ** 获取所有优惠券基础信息 **
- 请求类型 POST
> wap2.card.getCardList

| 字段名 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
| res | bool |  Y  | true | 返回json字符串 |
| data |  obj | Y | - | 返回结果状态 |
| cpns_id | int | Y | 6 | 优惠ID是该类型卡的号码 |
|  cpns_type_name | string  | Y | 全场满100立即1 | 卡券类型名称 |
| prefix | string | Y | "Baaaa" | 优惠码前缀 |
| coupon_total_number | int | Y | "10" | 优惠库存 |
| cpns_name | string  | Y | "满100减10元" | 优惠券名称 |
| description | string | Y | "卡券优惠活动描述" | 优惠券描述 |
| start_time | time | Y | 1495382400 | 优惠券开始时间(时间戳) |
| end_time | time | Y | 1498233600 | 优惠券截止时间(时间戳) |
| brands | array | Y | "1","2","3" | 品牌 1:音儿2:恩裳3:诗篇4:歌中歌5:奥丽嘉朵6:十二篮7:诗篇蓝标8:音儿蓝标9:恩裳蓝标|
| is_allow_aftersale | bool | Y | "0" | 是否允许售后 |
| is_currency | enum | Y | "0" | 0为普通券 1为通用券 |
| activity_start_allow | bool | N | "" | 允许售后(活动开始后) 0表示不允许该售后方式 |
| activity_finish_allow | bool | N | "" | 允许售后(活动结束后) 0表示不允许该售后方式 |
| condition | array | Y | - | 活动条件 |
| operator | sting | Y | ">=" | 符号 |
| value | string | Y | "100" | 当订单总额满100时，将享受优惠方案。当value为0时对所有订单给予优惠 |
| action_solution | array | Y | - | 优惠方案 |
| total_amount | array | Y | 10 | 该订单享有10元优惠 |
| percent | array | Y | 50 | 订单优惠享有50%优惠 |
| condition_type | string | Y | 1 | 0为指定商品有效 1为全场有效 |
| status | string | N | 1 | 1为当前用户已领取，0为尚未领取
| type | enum | Y | "2" | 0为打折券，1为优惠券，2为通用券 |
> 参数 

| 参数 | 类型/长度   |备注 |
| -----|:-------|:--------|
| member_id | string | 会员ID |
| pageStart | string | 起始值 默认0 |
| pageEnd | string | 结束值 默认10 |

> 接口返回值
     
    {
        "rsp": "succ",
        "data": [
            {
                "cpns_id": "31",
                "prefix": "A23",
                "coupon_total_number": "10",
                "cpns_name": "卡券1",
                "cpns_type_name": "卡券1",
                "description": "我是描述",
                "start_time": 1496160000,
                "end_time": 1496332800,
                "brands": [
                    "2"
                ],
                "is_allow_aftersale": "0",
                "activity_start_allow": "0",
                "activity_finish_allow": "0",
                "condition": {
                    "type": "b2c_sales_order_item_order",
                    "attribute": "order_subtotal",
                    "operator": ">=",
                    "value": "100"
                },
                "availableInventory": 10,
                "isUseCount": 0,
                "type": 0,
                "action_solution": {
                    "type": "order",
                    "percent": "80"
                },
                "condition_type": "0",
                "status": "1"
            },
            {
                "cpns_id": "32",
                "prefix": "A22",
                "coupon_total_number": "10",
                "cpns_name": "我是新增2",
                "cpns_type_name": "我是名称",
                "description": "我是规则",
                "start_time": 1496246400,
                "end_time": 1496307600,
                "brands": [
                    "2"
                ],
                "is_allow_aftersale": "0",
                "is_currency":"1",
                "activity_start_allow": "0",
                "activity_finish_allow": "0",
                "condition": {
                    "type": "b2c_sales_order_item_order",
                    "attribute": "order_subtotal",
                    "operator": ">=",
                    "value": "0"
                },
                "availableInventory": 10,
                "isUseCount": 0,
                "type": 1,
                "action_solution": {
                    "type": "order",
                    "total_amount": "100"
                },
                "condition_type": "1",
                "status": "1"
            }
        ],
        "res": ""
    }
    
> update_time:'2017.04.14'

-  ** 获取领取优惠券 **
- 请求类型 POST
> wap2.card.getCard

| 参数 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
| member_id | string | Y | 12797 | 会员ID |
| openid | string | N | oNZ6WxA--3fCcTHzQs1KUrk-QMM4 | 微信OPENID |
| scene | int | Y | 0 | 领取场景0:活动广场1:微信定向推送  |
| cpns_id | int | Y | 6 | 优惠券ID | 

> 结果
  
    {
        "rsp": "succ",
        "data": {
            "msg": "当前有 980 张卡券可领取，已有 35 张卡券已领取",
            "availableInventory": 980,
            "isUseCount": 35,
            "cardNo": "Baaaa5CBF000LHY"
        },
        "res": ""
    }
    
| 参数 | 类型/长度   |备注 |
| -----|:-------|:--------|
| res | string | 返回状态 |
| data | string | 返回消息 |
| availableInventory | int | 当前库存 |
| isUseCount | int | 当前已领取 |
| cardNo | string | 当前领取到的卡券 |


> update_time:'2017.04.14'

-  ** 获取用户的所有可用卡券 **
- 请求类型 POST
> wap2.card.getMyCard

| 参数 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
| member_id | string | Y | 12797 | 会员ID |
| type | array | N | 1 | 获取已使用 |
> 结果
  
    {
        "rsp": "succ",
        "data": [
            {
                "cardNo": "A228009A0001O",
                "status": 1,
                "cpns_id": "32",
                "cardInfo": {
                    "cpns_id": "32",
                    "prefix": "A22",
                    "coupon_total_number": "10",
                    "cpns_name": "我是新增2",
                    "cpns_type_name": "我是名称",
                    "description": "我是规则",
                    "start_time": 1496246400,
                    "end_time": 1496307600,
                    "brands": [
                        "2"
                    ],
                    "is_allow_aftersale": "0",
                    "activity_start_allow": "0",
                    "activity_finish_allow": "0",
                    "condition": {
                        "type": "b2c_sales_order_item_order",
                        "attribute": "order_subtotal",
                        "operator": ">=",
                        "value": "0"
                    },
                    "availableInventory": 10,
                    "isUseCount": 0,
                    "type": 1,
                    "action_solution": {
                        "type": "order",
                        "total_amount": "100"
                    },
                    "condition_type": "1"
                }
            },
            {
                "cardNo": "A2347F2A0001E",
                "status": 1,
                "cpns_id": "31",
                "cardInfo": {
                    "cpns_id": "31",
                    "prefix": "A23",
                    "coupon_total_number": "10",
                    "cpns_name": "卡券1",
                    "cpns_type_name": "卡券1",
                    "description": "我是描述",
                    "start_time": 1496160000,
                    "end_time": 1496332800,
                    "brands": [
                        "2"
                    ],
                    "is_allow_aftersale": "0",
                    "activity_start_allow": "0",
                    "activity_finish_allow": "0",
                    "condition": {
                        "type": "b2c_sales_order_item_order",
                        "attribute": "order_subtotal",
                        "operator": ">=",
                        "value": "100"
                    },
                    "availableInventory": 10,
                    "isUseCount": 0,
                    "type": 0,
                    "action_solution": {
                        "type": "order",
                        "percent": "80"
                    },
                    "condition_type": "0"
                }
            }
        ],
        "res": ""
    }
    
| 参数 | 类型/长度   |备注 |
| -----|:-------|:--------|
| res | string | 返回状态 |
| data | string | 返回消息 |
| cardNo | string | 卡券码 |
| status | string | 卡券状态1为待使用 |
| cardInfo | string | 卡券的基础信息 |
| cpns_id | string | 卡券ID |

> update_time:'2017.06.1'

-  ** 商城卡券微信推送展示页接口 **
- 请求类型 GET
> wap2.card.firstGetCardShow

> 结果
  
    {
        "rsp": "fail",
        "res": "succ",
        "data": {
            "goodInfo": {
                "goods_id": "2644",
                "name": "YINER音儿2016秋款/优雅浅蓝色长款H型桑蚕丝女衬衫86330080",
                "price": "3312.00",
                "s_url": "public/images/b9/d7/8a/8132f82eb0df6fcbbed7ceeffc23c0662b8029f5.jpg"
            },
            "cardInfo": {
                "cpns_id": "2",
                "rule_id": "1",
                "prefix": "ACC",
                "coupon_total_number": "10",
                "cpns_name": "满1000减100",
                "cpns_type_name": "满1000减100",
                "description": "满1000减100",
                "start_time": 1497456000,
                "end_time": 1497715200,
                "brands": null,
                "grant_start_time": 1497283200,
                "grant_end_time": 1497715200,
                "is_allow_aftersale": "0",
                "activity_start_allow": "0",
                "activity_finish_allow": "0",
                "condition": {
                    "type": "b2c_sales_order_item_order",
                    "attribute": "order_subtotal",
                    "operator": ">=",
                    "value": "1000"
                },
                "is_currency": 0,
                "availableInventory": 10,
                "type": 1,
                "action_solution": {
                    "type": "order",
                    "total_amount": "100"
                },
                "condition_type": "0"
            }
        }
    }
    
| 参数 | 类型/长度   |备注 |
| -----|:-------|:--------|
| res | string | 返回状态 |
| data | string | 返回消息 |
| goodInfo | obj | 商品信息 |
| name | string | 商品名称 |
| price | decimal | 商品默认金额 |
| s_url | url | 商品图片路径 |
| cardInfo | obj | 卡券信息 可参照获取卡券列表参数 |


> update_time:'2017.06.16'