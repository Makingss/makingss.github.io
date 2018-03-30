---
title: member_center
date: 2018-03-08 10:40:29
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

##### 会员中心

** 会员基础信息 **

> api_name: api/pc/member
> type:GET

```json
    {
    "status": "success",
    "code": 200,
    "message": null,
    "modul": "Message",
    "data": {
        "uuid": "bff35b19-6faf-4adc-9037-372b38c16ea2",
        "nickname": "13981872077",
        "member_level": [
            {
                "name": "普通会员",
                "logo_path": null,
                "pivot": {
                    "member_id": 5,
                    "memberlevelable_id": 1,
                    "created_at": "2018-01-04 15:38:41",
                    "updated_at": "2018-01-04 15:38:42"
                }
            }
        ],
        "avatar": null,
        "point": null,
        "advance": "0.00",
        "unreadmsg": 0,
        "sign_in_logs": [
            {
                "id": 191,
                "ip": "127.0.0.1",
                "device": "PC",
                "addon": {
                    "device": {
                        "address": [
                            "XX",
                            "XX",
                            "内网IP",
                            "内网IP"
                        ],
                        "client": "Windows 10---Chrome(64.0.3282.186)",
                        "ip": "127.0.0.1"
                    }
                }
            },
            {
                "id": 190,
                "ip": "127.0.0.1",
                "device": "PC",
                "addon": {
                    "device": {
                        "address": [
                            "XX",
                            "XX",
                            "内网IP",
                            "内网IP"
                        ],
                        "client": "Windows 10---Chrome(64.0.3282.186)",
                        "ip": "127.0.0.1"
                    }
                }
            },
            {
                "id": 189,
                "ip": "127.0.0.1",
                "device": "PC",
                "addon": {
                    "device": {
                        "address": [
                            "XX",
                            "XX",
                            "内网IP",
                            "内网IP"
                        ],
                        "client": "Windows 10---Chrome(64.0.3282.186)",
                        "ip": "127.0.0.1"
                    }
                }
            }
        ],
        "order": {
            "pendingPayment": 1,
            "pendingShip": 0,
            "pendingReceived": 0,
            "pendingEvaluation": 0,
            "afterSale": 0
        },
        "member": {
            "goods": 0,
            "content": 0,
            "history": 78
        }
    }
}
```

| 字段名 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
| status | string |  Y  | success | 接口返回状态 |
| code |  int | Y | - | 返回状态码 |
| message | string | Y | null | 接口反馈信息 |
| modul | string | Y | "Message" | 模型信息 |
| data | array | Y | - | 接口数据 |
| uuid | string | Y | bff35b19-6faf-4adc-9037-372b38c16ea2 | 会员UUID |
| nickname | string | Y | "13981872077" | 用户昵称 |
| member_level | string | Y | - | 会员等级 |
| member_level.*.name | string | Y | "普通会员" | 会员等级名称 |
| member_level.*.logo_path | string | Y | "dev.app.com" | 会员等级logo地址 |
| avatar | string | Y | dev.app.com | 会员头像路径 |
| point | string | Y | 10 | 会员积分 |
| advance | string | Y | 100.00 | 会员预存款余额 |
| unreadmsg | int | Y | 0 | 未读消息数量 |
| sign_in_logs | array | Y | - | 登录记录日志 |
| sign_in_logs.*.addon | array | Y | - | 登录日志扩展字段 |
| sign_in_logs.*.addon.device | array | Y | - | 设备信息 |
| sign_in_logs.*.addon.device.address | array | Y | - | 设备地址信息；包含国家、省、市、区、宽带运营商 |
| sign_in_logs.*.addon.device.client | string | Y | "Windows 10---Chrome(64.0.3282.186)" | 用户访问的设备名称以及版本号 |
| sign_in_logs.*.addon.device.ip | string | Y | "127.0.0.1" | IP地址 |
| order | array | Y | - | 订单信息 |
| pendingPayment | int | Y | 0 | 待付款 |
| pendingShip | int | Y | 0 | 待发货 |
| pendingReceived | int | Y | 0 | 待收货 |
| pendingEvaluation | int | Y | 0 | 待评价 |
| afterSale | string | Y | "0" | 售后 |
| member | array | Y | - | 会员收藏记录信息 |
| goods | int | Y | 0 | 收藏商品数量 |
| content | int | Y | 0 | 收藏文章数量 |
| history | int | Y | 0 | 浏览商品数量 |

** 订单和足迹信息 **

> api_name: api/pc/member_order_list
> type:GET

```json
{
    "status": "success",
    "code": 200,
    "message": null,
    "modul": "Message",
    "data": {
        "order": [
            {
                "id": 19,
                "order_no": "180307114343399",
                "total_amount": "0.00",
                "pay_status": 0,
                "ship_status": 0,
                "ship_name": "彭勃",
                "created_at": "2018-03-07 11:43:43",
                "payed": null,
                "status": "active",
                "received_status": null,
                "order_cycle": {
                    "id": 67,
                    "order_id": 46,
                    "content": "订单创建成功",
                    "title": "提交订单",
                    "status": "finish"
                },
                "order_items": [
                    {
                        "goods_id": 1,
                        "obj_id": 60,
                        "name": "YINER音儿2017冬新款中长款纯羊毛双面呢大衣女8C57580330",
                        "order_id": 19,
                        "order_item_no": "180307114344366",
                        "is_aftersale": null,
                        "send_status": 0,
                        "is_sync": 0,
                        "addon": [
                            {
                                "product_id": 9,
                                "spec_id": 1,
                                "spec_name": "颜色",
                                "spec_value_id": 10,
                                "spec_value": "绿色",
                                "spec_image": "1111",
                                "alias": "green"
                            },
                            {
                                "product_id": 9,
                                "spec_id": 2,
                                "spec_name": "尺码",
                                "spec_value_id": 2,
                                "spec_value": "36",
                                "spec_image": "1111",
                                "alias": "36"
                            }
                        ],
                        "order_objects": {
                            "img_url": "/storage/images/goods/list/2P36RtQDVgpAuJIa0Z5xj1itEyqF5DRXUvCySGYU.jpeg",
                            "goods_id": 1,
                            "order_id": 19
                        }
                    }
                ]
            }
        ],
        "foot_print": [
            {
                "id": 1,
                "image_default_id": 17,
                "bn": "8C57580330",
                "name": "YINER音儿2017冬新款中长款纯羊毛双面呢大衣女8C57580330--",
                "default_images": {
                    "storage": "image",
                    "url": "/storage/images/goods/list/2P36RtQDVgpAuJIa0Z5xj1itEyqF5DRXUvCySGYU.jpeg",
                    "watermark": 0,
                    "build_size": "235806",
                    "created_at": "2018-02-08 13:38:20",
                    "updated_at": "2018-02-08 13:38:20",
                    "extension": "jpeg"
                }
            }
        ]
    }
}
```

| 字段名 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
| status | string |  Y  | success | 接口返回状态 |
| code |  int | Y | - | 返回状态码 |
| message | string | Y | null | 接口反馈信息 |
| modul | string | Y | "Message" | 模型信息 |
| data | array | Y | - | 接口数据 |
| id | intger | Y | 1 | 订单ID |
| order_no | string | Y | 180307114612257 | 订单编号 |
| total_amount | string | Y | 10.03 | 订单支付金额 |
| pay_status| int | Y | 0 | 支付状态 0：未支付 1 已支付 |
| ship_status | int | Y | 0 | 发货状态 0:为发货 |
| ship_name | string | Y | 小伙子 | 收货人名称 |
| created_at | string | Y | 2018-03-07 11:46:12 | 创建订单时间 |
| payed | string | Y | 100.00 | 实际支付金额 |
| status | string | Y | "active" | 订单状态 active:有效 dead：作废 |
| received_status | int | Y | 0 | 收货状态 0:未收货 1:已收货 |
| order_items | array | Y | - | 订单明细数据 |
| goods_id | int | Y | 1 | 商品ID |
| name | string | Y | YINER音儿2017冬新款中长款纯羊毛双面呢大衣女8C57580330 | 商品名称 |
| order_id | int | Y | 21 | 订单ID |
| order_item_no | int | Y | 180307114638960 | 订单明细编号 |
| is_aftersale | int | Y | 0 | 是否申请售后，0:未申请售后 1:已申请售后 |
| send_status | int | Y | 0 | 是否发货，0:未发货 1:已发货 |
| is_sync | int | Y | 0 | 是否同步第三方平台，0:未同步 1:已同步 |
| addon | array | Y | - | 扩展字段 |
| product_id | int | Y | 9 | 产品ID |
| spec_id | int | Y | 0 | 规格ID |
| spec_name | string | Y | 颜色 | 规格名称 |
| spec_value_id | int | Y | 10 | 规格值ID |
| spec_value | string | Y | 0 | 规格值 |
| spec_image | string | Y | dev.app.com | 规格图片 |
| alias | string | Y | green | 规格别名 |
| spec_image | array | Y | - | 扩展字段 |
| order_objects | array | Y | - | 订单对象 |
| img_url | int | Y | 9 | 商品的快照图 |
| goods_id | int | Y | 1 | 商品ID |
| order_id | int | Y | 21 | 订单ID |
| foot_print | array | Y | - | 用户足迹数据 |
| id | int | Y | 1 | 足迹数据ID |
| image_default_id | int | Y | 21 | 图片ID |
| bn | string | Y | 8C57580330 | 图片ID |
| name | string | Y | YINER音儿2017冬新款中长款纯羊毛双面呢大衣女8C57580330 | 商品名称 |
| default_images | array | Y | - | 图片数据 |
| storage | string | image | Y | 图片存储引擎 |
| url | string | dev.app.com | Y | 图片路径 |
| extension | string | jpeg | Y | 图片格式 |
| order_cycle | array | - | Y | 订单状态 |
| order_cycle.order_id | string | 45 | Y | 订单ID |
| content | string | 订单创建成功 | Y | 订单状态描述 |
| title | string | 提交订单 | Y | 周期抬头 |
| status | string | finish | Y | 状态,值为wait、process、finish、error |
** 会员中心订单详情 **

> api_name: api/pc/member/order/{order_no}
> type:GET

| 字段名 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
|order_no| int(11) | Y | 180307114612257 | 订单 |

```json
    {
    "status": "success",
    "code": 200,
    "message": null,
    "modul": "Message",
    "data": {
        "order_no": "180321043846459",
        "tax_id": 14,
        "total_amount": "3000.80",
        "origin_amount": "3873.00",
        "itemnum": 1,
        "order_items": [
            {
                "price": "2988.80",
                "amount": "3861.00",
                "nums": 1,
                "order_addrs": {
                    "id": 172,
                    "ship_area": "天津/天津市/和平区",
                    "ship_name": "",
                    "ship_mobile": "13981872077",
                    "ship_addr": "街道"
                },
                "objects": {
                    "obj_type": "",
                    "bn": "9C3814035011023",
                    "name": "INSUN恩裳金标通勤时尚OL条纹收腰修身中长款风衣马甲外套9C3814035011023",
                    "price": "3861.00",
                    "nums": 1,
                    "weight": null,
                    "score": 0,
                    "activeprice": "0.00",
                    "params": "",
                    "img_url": "/storage/images/goods/list/hboFk95rniRnVlHEb92MbHFXqW2V7zMOXZvkPwCh.jpeg"
                }
            }
        ],
        "taxs": {
            "id": 14,
            "tax_title_id": 4,
            "tax_type": 1,
            "tax_content": "明细",
            "created_at": "2018-03-17 09:30:48",
            "tax_titles": {
                "id": 4,
                "tax_type": 1,
                "tax_name": "深圳前海港影商业智能有限公司",
                "tax_no": "3434321fd334214324",
                "address": "深圳市龙华新区大浪街道办",
                "telephone_number": "072323",
                "bank_name": "32321",
                "bank_no": "322232",
                "is_default": true
            }
        },
        "rule_use_records": [
            {
                "rule_name": "订单总价满1000订单8折优惠",
                "rule_type_id": 1
            },
            {
                "rule_name": "100通用券",
                "rule_type_id": 3
            }
        ],
        "order_cycles": [
            {
                "title": "提交订单",
                "is_show": true,
                "status": "finish",
                "current": 1
            },
            {
                "title": "验证订单",
                "is_show": true,
                "status": "finish",
                "current": 2
            },
            {
                "title": "等待支付",
                "is_show": true,
                "status": "wait",
                "current": 3
            },
            {
                "title": "提交订单",
                "is_show": true,
                "status": "finish",
                "current": 4
            },
            {
                "title": "订单支付",
                "is_show": true,
                "status": "finish",
                "current": 5
            }
        ]
    }
}
```

| 字段名 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
| status | string |  Y  | success | 接口返回状态 |
| code |  intger | Y | - | 返回状态码 |
| message | string | Y | null | 接口反馈信息 |
| modul | string | Y | "Message" | 模型信息 |
| data | array | Y | - | 接口数据 |
| order_no | intger | Y | 180321043846459 | 订单编号 |
| tax_id | intger | Y | 14 | 发票ID |
| total_amount | decimal | Y | 3000.80 | 商品实付金额 |
| origin_amount | decimal | Y | 3000.80 | 未参数活动原价 |3
| itemnum | tinyint | Y | 3000.80 | 未参数活动原价 |
| order_items | array | Y | - | 订单数据 |
| price | decimal | Y | 2988.80 | 订单数据 |
| amount | decimal | Y | 3861.00 | 商品原价 |
| nums | intger | Y | 1 | 商品数量 |
| order_addrs | array | Y | - | 收货地址 考虑到换货修改地址问题，一个订单会存在多个收货地址 |
| id | intger | Y | 1 | 地址ID |
| ship_area | string | Y | 天津/天津市/和平区 | 区域 |
| ship_name | string | Y | 小伙子 |收货人名称 |
| ship_mobile | string | Y | 13981872077 | 收货人手机号 |
| ship_addr | string | Y | "大浪商业中心" | 收货街道地址 |
| objects | array | Y | - | 订单明细快照信息 |
| obj_type | string | Y | "" | 对象类型 |
| bn | string | Y | 9C3814035011023 | 产品唯一ID |
| name | string | Y | INSUN恩裳金标通勤时尚OL条纹收腰修身中长款风衣马甲外套9C3814035011023 | 商品名称 |
| price | decimal | Y | 3861.00 | 商品原价 |
| nums | intger | Y |  1 | 商品数量 |
| weight | string | Y | null | 商品重量 |
| score | intger | Y | 0 | 购买该商品产生的积分 |
| activeprice | decimal | 0.00 | 活动价格 |
| params | array | Y | "" | 规格参数 |
| img_url | string | Y | /storge/image/ | 图片路径 |
| taxs | array | N | - | 发票信息 |
| id | intger | Y | 14 | 发票ID |
| tax_type| intger |Y | 1 | 发片类型0:个人，1:公司 |
| tax_content| string | Y | 明细 | 发票内容 |
| created_at| datetime |Y | 2018-03-17 09:30:48 | 创建时间 |
| tax_titles | array | Y | - | 发票明细 |
| id | intger | Y | 4 | 明细ID |
| tax_type | intger | Y | 1 | 发票类型: 0:个人 1:公司 |
| tax_name | string | Y | 深圳前海港影商业智能有限公司 | 公司抬头 |
| tax_no | string | Y | 3434321fd334214324 | 税号 |
| address | string | Y | 深圳市龙华新区大浪街道办 | 公司地址 |
| telephone_number | string | Y | 072323 | 电话号码 |
| bank_name| string | Y | 中国银行 | 银行名称 |
| bank_no| string | Y | 123456789 | 银行卡号 |
| is_default| bool | Y | true | 是否为默认 |
| rule_use_records | array | Y | - | 该订单参与的优惠活动 |
| rule_name| string | Y | 订单总价满1000订单8折优惠 | 活动名称 |
| rule_type_id | intger | Y | 1 | 1：订单促销 2：商品促销 3:优惠券 |
| order_cycles | array | Y | - | 订单流程 |
| title | string | Y | 提交订单 | 流程标题 |
| is_show | bool | Y | true | 是否显示 |
| status | enum['wait','process','finish','error'] | Y | finish | 流程状态 wait:等待;process:过程中;finish:完成;error:异常 |
| current | intger | Y | 1 | 流程ID，最大值为最状态 |