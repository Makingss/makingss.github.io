---
title: order
date: 2017-08-07 16:15:29
tags:
---
##### 文档说明
+ version:1.0
+ url:path+'/api/'+api_name
+ platform:laravel+vue+vuex
+ method:默认
+ 接口返回值默认格式:json
+ 接口返回值默认结构:
        {
          res:true/false,
          data:{},
          msg:'错误提示或者错误代码'
        }

> update_time:'2017.08.09'

---
##### 获取订单列表
-  ** 订单列表 **
> api_name: mobileapi.order.getUserOrderList

| 参数        | 实例           | 说明  | 备注 |
| ------------- |:-------------:| -----:| -----:|
| 用户名 | member_id | 12797 | 不能为空最长255字符 |
| 类型  | type  |   1 | enum[1,2,3,4,5,6]。1:待支付，2:待发货，3:已发货，4:已收货,5:分享购买,6,全部订单(不包含分享购买的其他订单) |
| 偏移量 | limit |    10 | 取多少数量的内容 |
| 页数  | page | 1 | 取第一页数量 |

        {
        "rsp": "succ",
        "res": {
            "day": 0,
            "yesterday": 0,
            "weeks": 19610.84
        },
        "data": {
            "170727153110140": [
                {
                    "order_id": "170727153110140",
                    "pay_status": "1",
                    "ship_status": "0",
                    "received_status": "0",
                    "status": "active",
                    "total_amount": "981.00",
                    "origin_amount": "981.00",
                    "payed": "0.00",
                    "received_time": 0,
                    "sync_lijing": "0",
                    "payment": "wxpayjsapi",
                    "buy_code": "",
                    "product_id": "24792",
                    "is_starbuy": 0,
                    "name": "YINER音儿GoodLand/优雅钩花V领收腰A字蕾丝连衣裙85805507",
                    "from_time": null,
                    "to_time": null,
                    "goods_id": "5540",
                    "s_url": "public/images/bd/d8/39/cdd88e0069326366af1435da3fbe93e17efe7963.jpg",
                    "aftersale_status": "0",
                    "user_cancel_status": "0",
                    "order_rule_discount": "0.00",
                    "coupons_discount": "0.00",
                    "currency_coupons_discount": "0.00",
                    "items_bn": "808580550701540",
                    "price": "981.00",
                    "sendnum": "0",
                    "nums": "1",
                    "final_amount": "981.00",
                    "obj_id": "372136",
                    "item_id": "419468",
                    "goods_price": "981.00",
                    "product_price": "981.00",
                    "p_order_id": "0",
                    "delivery_id": null
                }
            ],
            "170727143748125": [
                {
                    "order_id": "170727143748125",
                    "pay_status": "1",
                    "ship_status": "0",
                    "received_status": "0",
                    "status": "active",
                    "ship_email": null,
                    "total_amount": "7152.00",
                    "origin_amount": "7152.00",
                    "payed": "0.00",
                    "received_time": 0,
                    "sync_lijing": "0",
                    "payment": "wxpayjsapi",
                    "buy_code": "",
                    "product_id": "7707",
                    "is_starbuy": 0,
                    "name": "YINER音儿GoodLand/2016夏装新款 橙色长款层次拼接显瘦无袖连衣裙86205626",
                    "from_time": null,
                    "to_time": null,
                    "goods_id": "1801",
                    "s_url": "public/images/1e/42/9b/07bbca328efcf8dce4f8e2e7b20f3c1c9580de94.jpg",
                    "aftersale_status": "0",
                    "user_cancel_status": "0",
                    "order_rule_discount": "0.00",
                    "coupons_discount": "0.00",
                    "currency_coupons_discount": "0.00",
                    "items_bn": "808620562606142",
                    "price": "1788.00",
                    "sendnum": "0",
                    "nums": 4,
                    "final_amount": "1788.00",
                    "obj_id": "329488",
                    "item_id": "376820",
                    "goods_price": "1788.00",
                    "product_price": "1788.00",
                    "p_order_id": "0",
                    "delivery_id": null,
                    "item_info": [
                        {
                            "item_id": "376821",
                            "aftersale_status": "0",
                            "user_cancel_status": "0",
                            "obj_id": "329489",
                            "order_rule_discount": "0.00",
                            "coupons_discount": "0.00",
                            "currency_coupons_discount": "0.00"
                        },
                        {
                            "item_id": "376822",
                            "aftersale_status": "0",
                            "user_cancel_status": "0",
                            "obj_id": "329490",
                            "order_rule_discount": "0.00",
                            "coupons_discount": "0.00",
                            "currency_coupons_discount": "0.00"
                        },
                        {
                            "item_id": "376823",
                            "aftersale_status": "0",
                            "user_cancel_status": "0",
                            "obj_id": "329491",
                            "order_rule_discount": "0.00",
                            "coupons_discount": "0.00",
                            "currency_coupons_discount": "0.00"
                        }
                    ]
                }
            ]
        },
        "total_results": 0
    }

| 字段名 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
| res | bool |  Y  | true | 返回json字符串。当type=5及分享购买时,会参数一个最近销售订单的金额 |
| day | float | N | 1.00 | 统计今天的销售的金额 |
| yesterday | float | N | 2.00 | 统计昨天的销售的金额 |
| weeks | float | N | 3.00 | 统计一周的销售的金额 |
| data |  obj | Y | - | 返回结果状态 |
| order_id | string | Y | 170727153110140 | 订单号 |
| pay_status | string | Y | "1" | 支付状态,'0':未支付;'1':已支付 |
| ship_status | string | Y | "0" | 发货状态,'0':未支付;'1':已支付 |
| received_status | string | Y | "0" | 收货状态,'0':未支付;'1':已支付 |
| status | string | Y | "active" | 订单状态,"active"：有效;"dead":作废;"";"finish":完成;"cancel":取消 |
| total_amount | string | Y | "200.00" | 优惠后订单金额 |
| origin_amount | string | Y | "500.00" | 订单未优惠金额 |
| payed | string | Y | "200.00" | 实际支付金额 |
| received_time | int |  Y| 1502095150 | 确认收货时间 |
| sync_lijing | string | Y | "0" | 是否同步丽晶 |
| payment | string | Y | "wxpayjsapi" | 支付方式 wxpayjsapi:微信支付 |
| buy_code | string | N | "12797" | 分享购买会员ID | 
| product_id | sting | Y | "24792" | 商品ID |
| is_starbuy | int | Y | 0 | 是否是活动商品 |
| from_time | int | Y | 0 | 活动开始时间 |
| to_time | int | Y | 0 | 活动截止时间 |
| goods_id | string | Y | "5540" | 商品ID |
| s_url | string | Y | "public/images/bd/d8/39/cdd88e0069326366af1435da3fbe93e17efe7963.jpg" | 缩略图图片 |
| aftersale_status | string | Y | "0" | 售后标记 1:已做过售后 |
| user_cancel_status | string | Y | "0" | 售前标记 1:已做过售前 |
| order_rule_discount | string | Y | "0" | 订单促销金额 |
| coupons_discount | string | Y | "0" | 优惠券促销金额 |
| currency_coupons_discount | string | Y | "0" | 通用券促销金额 |
| items_bn | string | Y | "808580550701540" | 商品bn |
| price | string | Y | "0" | 单件衣服价格 |
| sendnum | string | Y | "808580550701540" | 商品bn |
| nums | string | Y | "2" | 购买衣服数量 多件会生成item_info中体现同款同码商品的item_id |
| item_info | array | N | array | 同款同码商品数据 |
| item_id | string | Y | "376821" | 同上item_id |
| aftersale_status | Y | "0" | 同上 |
| user_cancel_status | Y | "0" | 同上 |
| obj_id | Y | "0" | 同上 |
| order_rule_discount | Y | "0.00" | 同上 |
| coupons_discount | Y | "0.00" | 同上 |
| currency_coupons_discount | Y | "0.00" | 同上 |
| final_amount | string | Y | "200" | 支付金额 |
| obj_id | string | Y | "0" | items表中的项目id |
| item_id | string | Y | "376820" | 项目ID |
| goods_price | string | Y | "200" | 单件商品金额 |
| product_price | string | Y | "200" | 单件产品金额 |
| p_order_id | string | Y | "0" | 父order_id |
| delivery_id | string | N | "120170703685533211" | 发货单号,订单处于待收货状态，发货单能为空 |

---
-  ** 订单详情 **
> api_name: mobileapi.order.getOrderDetails

| 参数        | 实例           | 说明  | 备注 |
| ------------- |:-------------:| -----:| -----:|
| 用户名 | member_id | 12797 | 不能为空最长255字符 |
| 类型  | type  |   1 | enum[1,2,3,4,5,6]。1:待支付，2:待发货，3:已发货，4:已收货,5:分享购买,6,全部订单(不包含分享购买的其他订单) |
| 偏移量 | limit |    10 | 取多少数量的内容 |
| 页数  | page | 1 | 取第一页数量 |

        {
        "rsp": "succ",
        "res": "success",
        "data": {
            "170727153110140": [
                {
                    "order_id": "170727153110140",
                    "pay_status": "1",
                    "ship_status": "0",
                    "received_status": "0",
                    "status": "active",
                    "ship_area": "广东省/深圳市/其它区",
                    "ship_addr": "大浪街道浪琴路8号影儿工业园商学院2楼",
                    "ship_name": "wuzaizhi",
                    "ship_time": "任意时间,任意时间段",
                    "ship_mobile": "157****8218",
                    "total_amount": "981.00",
                    "origin_amount": "981.00",
                    "payed": "0.00",
                    "received_time": 0,
                    "sync_lijing": "0",
                    "payment": "wxpayjsapi",
                    "buy_code": "",
                    "product_id": "24792",
                    "is_starbuy": 0,
                    "name": "YINER音儿GoodLand/优雅钩花V领收腰A字蕾丝连衣裙85805507",
                    "from_time": null,
                    "to_time": null,
                    "goods_id": "5540",
                    "s_url": "public/images/bd/d8/39/cdd88e0069326366af1435da3fbe93e17efe7963.jpg",
                    "aftersale_status": "0",
                    "user_cancel_status": "0",
                    "order_rule_discount": "0.00",
                    "coupons_discount": "0.00",
                    "currency_coupons_discount": "0.00",
                    "items_bn": "808580550701540",
                    "price": "981.00",
                    "sendnum": "0",
                    "nums": "1",
                    "final_amount": "981.00",
                    "obj_id": "372136",
                    "item_id": "419468",
                    "goods_price": "981.00",
                    "product_price": "981.00",
                    "p_order_id": "0",
                    "delivery_id": null
                }
            ],
            "170727143748125": [
                {
                    "order_id": "170727143748125",
                    "pay_status": "1",
                    "ship_status": "0",
                    "received_status": "0",
                    "status": "active",
                    "ship_email": null,
                    "total_amount": "7152.00",
                    "origin_amount": "7152.00",
                    "payed": "0.00",
                    "ship_area": "广东省/深圳市/其它区",
                    "ship_addr": "大浪街道浪琴路8号影儿工业园商学院2楼",
                    "ship_name": "wuzaizhi",
                    "ship_time": "任意时间,任意时间段",
                    "ship_mobile": "157****8218",
                    "received_time": 0,
                    "sync_lijing": "0",
                    "payment": "wxpayjsapi",
                    "buy_code": "",
                    "product_id": "7707",
                    "is_starbuy": 0,
                    "name": "YINER音儿GoodLand/2016夏装新款 橙色长款层次拼接显瘦无袖连衣裙86205626",
                    "from_time": null,
                    "to_time": null,
                    "goods_id": "1801",
                    "s_url": "public/images/1e/42/9b/07bbca328efcf8dce4f8e2e7b20f3c1c9580de94.jpg",
                    "aftersale_status": "0",
                    "user_cancel_status": "0",
                    "order_rule_discount": "0.00",
                    "coupons_discount": "0.00",
                    "currency_coupons_discount": "0.00",
                    "items_bn": "808620562606142",
                    "price": "1788.00",
                    "sendnum": "0",
                    "nums": 4,
                    "final_amount": "1788.00",
                    "obj_id": "329488",
                    "item_id": "376820",
                    "goods_price": "1788.00",
                    "product_price": "1788.00",
                    "p_order_id": "0",
                    "delivery_id": null,
                    "item_info": [
                        {
                            "item_id": "376821",
                            "aftersale_status": "0",
                            "user_cancel_status": "0",
                            "obj_id": "329489",
                            "order_rule_discount": "0.00",
                            "coupons_discount": "0.00",
                            "currency_coupons_discount": "0.00"
                        },
                        {
                            "item_id": "376822",
                            "aftersale_status": "0",
                            "user_cancel_status": "0",
                            "obj_id": "329490",
                            "order_rule_discount": "0.00",
                            "coupons_discount": "0.00",
                            "currency_coupons_discount": "0.00"
                        },
                        {
                            "item_id": "376823",
                            "aftersale_status": "0",
                            "user_cancel_status": "0",
                            "obj_id": "329491",
                            "order_rule_discount": "0.00",
                            "coupons_discount": "0.00",
                            "currency_coupons_discount": "0.00"
                        }
                    ]
                }
            ]
        },
        "total_results": 0
    }

| 字段名 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
| res | bool |  Y  | true | 返回json字符串 |
| data |  obj | Y | - | 返回结果状态 |
| order_id | string | Y | 170727153110140 | 订单号 |
| pay_status | string | Y | "1" | 支付状态,'0':未支付;'1':已支付 |
| ship_status | string | Y | "0" | 发货状态,'0':未支付;'1':已支付 |
| received_status | string | Y | "0" | 收货状态,'0':未支付;'1':已支付 |
| status | string | Y | "active" | 订单状态,"active"：有效;"dead":作废;"";"finish":完成;"cancel":取消 |
| ship_email | string | Y | "636154" | 收货人邮编 |
| total_amount | string | Y | "200.00" | 优惠后订单金额 |
| origin_amount | string | Y | "500.00" | 订单未优惠金额 |
| payed | string | Y | "200.00" | 实际支付金额 |
| ship_area | string | Y | "广东省/深圳市/其它区" | 收货人区域 |
| ship_addr | string | Y | "大浪街道浪琴路8号影儿工业园商学院2楼" | 收货人地址 |
| ship_name | string | Y | "200" | 收货人姓名 |
| ship_time | string | Y | "任意时间,任意时间段" | 送货时间 |
| ship_mobile | string | Y | "157****8218" | 收货人手机号 |
| received_time | int |  Y| 1502095150 | 确认收货时间 |
| sync_lijing | string | Y | "0" | 是否同步丽晶 |
| payment | string | Y | "wxpayjsapi" | 支付方式 wxpayjsapi:微信支付 |
| buy_code | string | N | "12797" | 分享购买会员ID | 
| product_id | sting | Y | "24792" | 商品ID |
| is_starbuy | int | Y | 0 | 是否是活动商品 |
| from_time | int | Y | 0 | 活动开始时间 |
| to_time | int | Y | 0 | 活动截止时间 |
| goods_id | string | Y | "5540" | 商品ID |
| s_url | string | Y | "public/images/bd/d8/39/cdd88e0069326366af1435da3fbe93e17efe7963.jpg" | 缩略图图片 |
| aftersale_status | string | Y | "0" | 售后标记 1:已做过售后 |
| user_cancel_status | string | Y | "0" | 售前标记 1:已做过售前 |
| order_rule_discount | string | Y | "0" | 订单促销金额 |
| coupons_discount | string | Y | "0" | 优惠券促销金额 |
| currency_coupons_discount | string | Y | "0" | 通用券促销金额 |
| items_bn | string | Y | "808580550701540" | 商品bn |
| price | string | Y | "0" | 单件衣服价格 |
| sendnum | string | Y | "808580550701540" | 商品bn |
| nums | string | Y | "2" | 购买衣服数量 多件会生成item_info中体现同款同码商品的item_id |
| item_info | array | N | array | 同款同码商品数据 |
| item_id | string | Y | "376821" | 同上item_id |
| aftersale_status | Y | "0" | 同上 |
| user_cancel_status | Y | "0" | 同上 |
| obj_id | Y | "0" | 同上 |
| order_rule_discount | Y | "0.00" | 同上 |
| coupons_discount | Y | "0.00" | 同上 |
| currency_coupons_discount | Y | "0.00" | 同上 |
| final_amount | string | Y | "200" | 支付金额 |
| obj_id | string | Y | "0" | items表中的项目id |
| item_id | string | Y | "376820" | 项目ID |
| goods_price | string | Y | "200" | 单件商品金额 |
| product_price | string | true | "200" | 单件产品金额 |
| p_order_id | string | true | "0" | 父order_id |
| delivery_id | string | N | "120170703685533211" | 发货单号,订单处于待收货状态，发货单能为空 |

---
-  ** 获取售后列表 **
> api_name:mobileapi.aftersales.getAfterSalesList 

| 参数        | 实例           | 说明  | 备注 |
| ------------- |:-------------:| -----:| -----:|
| 用户名 | member_id | 12797 | 不能为空最长255字符 |
| 偏移量 | limit |    10 | 取多少数量的内容 |
| 页数  | page | 1 | 取第一页数量 |

        {
        "rsp": "succ",
        "res": "success",
        "data": {
            "170727153110140": [
                {
                    "order_id": "170727153110140",
                    "pay_status": "1",
                    "ship_status": "0",
                    "received_status": "0",
                    "status": "active",
                    "ship_area": "广东省/深圳市/其它区",
                    "ship_addr": "大浪街道浪琴路8号影儿工业园商学院2楼",
                    "ship_name": "wuzaizhi",
                    "ship_time": "任意时间,任意时间段",
                    "ship_mobile": "157****8218",
                    "total_amount": "981.00",
                    "origin_amount": "981.00",
                    "payed": "0.00",
                    "received_time": 0,
                    "sync_lijing": "0",
                    "payment": "wxpayjsapi",
                    "buy_code": "",
                    "product_id": "24792",
                    "is_starbuy": 0,
                    "name": "YINER音儿GoodLand/优雅钩花V领收腰A字蕾丝连衣裙85805507",
                    "from_time": null,
                    "to_time": null,
                    "goods_id": "5540",
                    "s_url": "public/images/bd/d8/39/cdd88e0069326366af1435da3fbe93e17efe7963.jpg",
                    "aftersale_status": "0",
                    "user_cancel_status": "0",
                    "order_rule_discount": "0.00",
                    "coupons_discount": "0.00",
                    "currency_coupons_discount": "0.00",
                    "items_bn": "808580550701540",
                    "price": "981.00",
                    "sendnum": "0",
                    "nums": "1",
                    "final_amount": "981.00",
                    "obj_id": "372136",
                    "item_id": "419468",
                    "goods_price": "981.00",
                    "product_price": "981.00",
                    "p_order_id": "0",
                    "delivery_id": null
                }
            ],
            "170727143748125": [
                {
                    "order_id": "170727143748125",
                    "pay_status": "1",
                    "ship_status": "0",
                    "received_status": "0",
                    "status": "active",
                    "ship_email": null,
                    "total_amount": "7152.00",
                    "origin_amount": "7152.00",
                    "payed": "0.00",
                    "ship_area": "广东省/深圳市/其它区",
                    "ship_addr": "大浪街道浪琴路8号影儿工业园商学院2楼",
                    "ship_name": "wuzaizhi",
                    "ship_time": "任意时间,任意时间段",
                    "ship_mobile": "157****8218",
                    "received_time": 0,
                    "sync_lijing": "0",
                    "payment": "wxpayjsapi",
                    "buy_code": "",
                    "product_id": "7707",
                    "is_starbuy": 0,
                    "name": "YINER音儿GoodLand/2016夏装新款 橙色长款层次拼接显瘦无袖连衣裙86205626",
                    "from_time": null,
                    "to_time": null,
                    "goods_id": "1801",
                    "s_url": "public/images/1e/42/9b/07bbca328efcf8dce4f8e2e7b20f3c1c9580de94.jpg",
                    "aftersale_status": "0",
                    "user_cancel_status": "0",
                    "order_rule_discount": "0.00",
                    "coupons_discount": "0.00",
                    "currency_coupons_discount": "0.00",
                    "items_bn": "808620562606142",
                    "price": "1788.00",
                    "sendnum": "0",
                    "nums": 4,
                    "final_amount": "1788.00",
                    "obj_id": "329488",
                    "item_id": "376820",
                    "goods_price": "1788.00",
                    "product_price": "1788.00",
                    "p_order_id": "0",
                    "delivery_id": null,
                    "item_info": [
                        {
                            "item_id": "376821",
                            "aftersale_status": "0",
                            "user_cancel_status": "0",
                            "obj_id": "329489",
                            "order_rule_discount": "0.00",
                            "coupons_discount": "0.00",
                            "currency_coupons_discount": "0.00"
                        },
                        {
                            "item_id": "376822",
                            "aftersale_status": "0",
                            "user_cancel_status": "0",
                            "obj_id": "329490",
                            "order_rule_discount": "0.00",
                            "coupons_discount": "0.00",
                            "currency_coupons_discount": "0.00"
                        },
                        {
                            "item_id": "376823",
                            "aftersale_status": "0",
                            "user_cancel_status": "0",
                            "obj_id": "329491",
                            "order_rule_discount": "0.00",
                            "coupons_discount": "0.00",
                            "currency_coupons_discount": "0.00"
                        }
                    ]
                }
            ]
        },
        "total_results": 0
    }

| 字段名 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
| res | bool |  Y  | true | 返回json字符串 |
| data |  obj | Y | - | 返回结果状态 |
| order_id | string | Y | 170727153110140 | 订单号 |
| pay_status | string | Y | "1" | 支付状态,'0':未支付;'1':已支付 |
| ship_status | string | Y | "0" | 发货状态,'0':未支付;'1':已支付 |
| received_status | string | Y | "0" | 收货状态,'0':未支付;'1':已支付 |
| status | string | Y | "active" | 订单状态,"active"：有效;"dead":作废;"";"finish":完成;"cancel":取消 |
| ship_email | string | Y | "636154" | 收货人邮编 |
| total_amount | string | Y | "200.00" | 优惠后订单金额 |
| origin_amount | string | Y | "500.00" | 订单未优惠金额 |
| payed | string | Y | "200.00" | 实际支付金额 |
| ship_area | string | Y | "广东省/深圳市/其它区" | 收货人区域 |
| ship_addr | string | Y | "大浪街道浪琴路8号影儿工业园商学院2楼" | 收货人地址 |
| ship_name | string | Y | "200" | 收货人姓名 |
| ship_time | string | Y | "任意时间,任意时间段" | 送货时间 |
| ship_mobile | string | Y | "157****8218" | 收货人手机号 |
| received_time | int |  Y| 1502095150 | 确认收货时间 |
| sync_lijing | string | Y | "0" | 是否同步丽晶 |
| payment | string | Y | "wxpayjsapi" | 支付方式 wxpayjsapi:微信支付 |
| buy_code | string | N | "12797" | 分享购买会员ID | 
| product_id | sting | Y | "24792" | 商品ID |
| is_starbuy | int | Y | 0 | 是否是活动商品 |
| from_time | int | Y | 0 | 活动开始时间 |
| to_time | int | Y | 0 | 活动截止时间 |
| goods_id | string | Y | "5540" | 商品ID |
| s_url | string | Y | "public/images/bd/d8/39/cdd88e0069326366af1435da3fbe93e17efe7963.jpg" | 缩略图图片 |
| aftersale_status | string | Y | "0" | 售后标记 1:已做过售后 |
| user_cancel_status | string | Y | "0" | 售前标记 1:已做过售前 |
| order_rule_discount | string | Y | "0" | 订单促销金额 |
| coupons_discount | string | Y | "0" | 优惠券促销金额 |
| currency_coupons_discount | string | Y | "0" | 通用券促销金额 |
| items_bn | string | Y | "808580550701540" | 商品bn |
| price | string | Y | "0" | 单件衣服价格 |
| sendnum | string | Y | "808580550701540" | 商品bn |
| nums | string | Y | "2" | 购买衣服数量 多件会生成item_info中体现同款同码商品的item_id |
| item_info | array | N | array | 同款同码商品数据 |
| item_id | string | Y | "376821" | 同上item_id |
| aftersale_status | Y | "0" | 同上 |
| user_cancel_status | Y | "0" | 同上 |
| obj_id | Y | "0" | 同上 |
| order_rule_discount | Y | "0.00" | 同上 |
| coupons_discount | Y | "0.00" | 同上 |
| currency_coupons_discount | Y | "0.00" | 同上 |
| final_amount | string | Y | "200" | 支付金额 |
| obj_id | string | Y | "0" | items表中的项目id |
| item_id | string | Y | "376820" | 项目ID |
| goods_price | string | Y | "200" | 单件商品金额 |
| product_price | string | true | "200" | 单件产品金额 |
| p_order_id | string | true | "0" | 父order_id |
| delivery_id | string | N | "120170703685533211" | 发货单号,订单处于待收货状态，发货单能为空 |

