---
title: store_center
date: 2018-01-29 16:15:29
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
##### 微店数据
-  ** 微店个人中心 **
> api_name: api/pc/store
> type: GET

```json
{
    "status": "success",
    "code": 200,
    "message": null,
    "modul": "Message",
    "data": {
        "store_info": {
            "uuid": "bff35b19-6faf-4adc-9037-372b38c16ea2",
            "conversions_num": 0,
            "member_num": 1,
            "store_name": "Prof. Bernie Legros",
            "level_name": "普通店铺",
            "level_logo_path": null,
            "avatar": "ea",
            "qr_code": "tenetur",
            "fans_num":10,
            "looks": 0
        },
        "the_month": {
            "order_num": 7527,
            "refund_num": 6547,
            "my_member_num": 1,
            "order_amount": -431233.34,
            "refund_amount": -367244.05,
            "profit": -63989.29
        },
        "badge": {
            "pending_payment": 0,
            "pending_ship": 0,
            "pending_received": 0,
            "after_sale": 0,
            "fans_num": 0,
            "order_num": 0,
            "refund_num": 0,
            "order_amount": 0,
            "refund_amount": 0,
            "profit": 0
        },
        "fans": [
            {
                "fans_type": 0,
                "type": 4,
                "member": {
                    "uuid": "3644ca43-4e55-48d5-a5d8-2f250ec7f87c",
                    "nickname": "13981872066",
                    "avatar": null
                }
            }
        ],
        "chart": {
            "today": {
                "2018-01-29-00": {
                    "hours": "2018-01-29-00",
                    "amount": "0.00"
                },
                "2018-01-29-01": {
                    "hours": "2018-01-29-01",
                    "amount": "0.00"
                },
                "2018-01-29-02": {
                    "hours": "2018-01-29-02",
                    "amount": "0.00"
                },
                "2018-01-29-03": {
                    "hours": "2018-01-29-03",
                    "amount": "0.00"
                },
                "2018-01-29-04": {
                    "hours": "2018-01-29-04",
                    "amount": "0.00"
                },
                "2018-01-29-05": {
                    "hours": "2018-01-29-05",
                    "amount": "0.00"
                },
                "2018-01-29-06": {
                    "hours": "2018-01-29-06",
                    "amount": "0.00"
                },
                "2018-01-29-07": {
                    "hours": "2018-01-29-07",
                    "amount": "0.00"
                },
                "2018-01-29-08": {
                    "hours": "2018-01-29-08",
                    "amount": "0.00"
                },
                "2018-01-29-09": {
                    "hours": "2018-01-29-09",
                    "amount": "0.00"
                },
                "2018-01-29-10": {
                    "hours": "2018-01-29-10",
                    "amount": "0.00"
                }
            },
            "yesterday": {
                "2018-01-28-00": {
                    "hours": "2018-01-28-00",
                    "amount": "0.00"
                },
                "2018-01-28-01": {
                    "hours": "2018-01-28-01",
                    "amount": "0.00"
                },
                "2018-01-28-02": {
                    "hours": "2018-01-28-02",
                    "amount": "0.00"
                },
                "2018-01-28-03": {
                    "hours": "2018-01-28-03",
                    "amount": "0.00"
                },
                "2018-01-28-04": {
                    "hours": "2018-01-28-04",
                    "amount": "0.00"
                },
                "2018-01-28-05": {
                    "hours": "2018-01-28-05",
                    "amount": "0.00"
                },
                "2018-01-28-06": {
                    "hours": "2018-01-28-06",
                    "amount": "0.00"
                },
                "2018-01-28-07": {
                    "hours": "2018-01-28-07",
                    "amount": "0.00"
                },
                "2018-01-28-08": {
                    "hours": "2018-01-28-08",
                    "amount": "0.00"
                },
                "2018-01-28-09": {
                    "hours": "2018-01-28-09",
                    "amount": "0.00"
                },
                "2018-01-28-10": {
                    "hours": "2018-01-28-10",
                    "amount": "0.00"
                },
                "2018-01-28-11": {
                    "hours": "2018-01-28-11",
                    "amount": "0.00"
                },
                "2018-01-28-12": {
                    "hours": "2018-01-28-12",
                    "amount": "0.00"
                },
                "2018-01-28-13": {
                    "hours": "2018-01-28-13",
                    "amount": "0.00"
                },
                "2018-01-28-14": {
                    "hours": "2018-01-28-14",
                    "amount": "0.00"
                },
                "2018-01-28-15": {
                    "hours": "2018-01-28-15",
                    "amount": "0.00"
                },
                "2018-01-28-16": {
                    "hours": "2018-01-28-16",
                    "amount": "0.00"
                },
                "2018-01-28-17": {
                    "hours": "2018-01-28-17",
                    "amount": "0.00"
                },
                "2018-01-28-18": {
                    "hours": "2018-01-28-18",
                    "amount": "0.00"
                },
                "2018-01-28-19": {
                    "hours": "2018-01-28-19",
                    "amount": "0.00"
                },
                "2018-01-28-20": {
                    "hours": "2018-01-28-20",
                    "amount": "0.00"
                },
                "2018-01-28-21": {
                    "hours": "2018-01-28-21",
                    "amount": "0.00"
                },
                "2018-01-28-22": {
                    "hours": "2018-01-28-22",
                    "amount": "0.00"
                },
                "2018-01-28-23": {
                    "hours": "2018-01-28-23",
                    "amount": "0.00"
                }
            },
             "config": {
                "min_time": 1514770090,
                "max_time": 1517534890
            }
        }
    }
}
```
| 字段名 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
| store_info | array |  Y  | - | 微店基础信息
| uuid | string | Y | bff35b19-6faf-4adc-9037-372b38c16ea2 | UUID |
| conversions_num | float | N | 2.00 | 转粉总数 |
| member_num | int | Y | 1 | 会员总数 |
| store_name | string | Y | 测试店铺 | 店铺名称 |
| level_name | string | Y | V1店铺 | 店铺等级  |
| level_logo_path | string | Y | http://app.com/avatar.png | 等级logo |
| avatar | string | Y | http://app.com/avatar.png | 店铺头像  |
| qr_code | string | Y | http://app.com/avatar.png | 店铺二维码 |
| fans_num | int | Y | 90 | 粉丝数量,注意该粉丝数仅仅代表该微店用户做为普通用户时的粉丝，区别与会员数和转粉数 |
| looks | int | Y | 100 | 店铺浏览量 |
| the_month | array | Y | - | 本月数据 |
| order_num | int | Y | 1 | 本月销售订单数量 |
| refund_num | int | Y | 1 | 本月退款订单数量 |
| my_member_num | int | Y | 2 | 本月会员数 |
| order_amount | float | Y | 200.00 | 本月订单销售额 |
| refund_amount | float | Y | 210.00 | 本月退款额 |
| profit | float| Y | -10.00 | 本月营业额 |
| badge | array | Y | - | 角标 |
| pending_payment | int | Y | 0 | 等待支付的数量 |
| pending_ship | int | Y | 0 | 等待发货的数量 |
| pending_received | int | Y | 0 | 等待收货的数量 |
| after_sale | int | Y | 0 | 售后需要处理数量 |
| fans_num | int | Y | 0 | 当日粉丝的数量 |
| order_num | int | Y | 0 | 当日订单数量的数量 |
| refund_num | int | Y | 0 | 当日退款数量 |
| order_amount | int | Y | 0 | 当日销售额 |
| refund_amount | int | Y | 0 | 当日退款额 |
| profit | int | Y | 0 | 当日营业额 |
| fans | array | Y | - | 会员数和转粉数会员的动态信息 |
| created_at | datetime | Y | 2018-01-23 14:56:39 | 操作记录时间 |
| fans_type | enum[0,1] | Y | 0 | 0:会员数1:转粉数 |
| type | enum[0,1,2] | Y | 0 | 会员动态类型,0:该会员登录过,1:该会员浏览过商品,2:购买过商品 |
| member | array | Y | - | 会员数或者转粉数的基础信息 |
| uuid | string | Y | 3644ca43-4e55-48d5-a5d8-2f250ec7f87c | 会员ID |
| nickname | string | Y | 昵称 | 会员昵称 |
| avatar | string | Y | http://app.com/avatar.png | 会员头像 |
| chart | array | Y | - | 图表,today：今日销售额 yesterday：昨日销售额 |
| today.* | array | Y | 2018-01-29-00 | 时间段的末尾固定两位长度00-23，b表示每1小时中的数据 |
| today.*.amount | float | Y | 200.00 | 该小时段的是销售额 |
| yestoday.* | array | Y | 2018-01-29-00 | 同上 |
| yestoday.*.amount | float | Y | 200.00 | 同上 |
| config.*.min | int | Y | 1514770090 | 图表查询的时间范围最小值 |
| config.*.max | int | Y | 1517534890 | 图表查询的时间范围最大值 |


-  ** 微店个人中心图表数据查询 **
> api_name: api/pc/store_chart
> type: POST

| 字段名 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
|start_time| int | Y | 1517270400 | 开始时间,start_time和end_time存在可不用传递length字段 |
|end_time | int | Y | 1517534541 | 截止时间，start_time和end_time存在可不用传递length字段 |
|type | enum['hour','day','month'] | Y | "day" | 截止时间 |
|length | int | Y | -1 | 查询范围 -1,-7,-30 分别代表前1天，前7天，前30天。注意如果该值存在 可以不用传递start_time和end_time字段 |

```json
{
    "chart": {
        "2018-01-30": {
            "day": "2018-01-30",
            "amount": "0.00"
        },
        "2018-01-31": {
            "day": "2018-01-31",
            "amount": "3258.65"
        },
        "2018-02-01": {
            "day": "2018-02-01",
            "amount": "2571.69"
        },
        "2018-02-02": {
            "day": "2018-02-02",
            "amount": "0.00"
        }
    },
    "panel": {
        "fans": 1,
        "order_num": 200,
        "refund_num": 1,
        "order_amount": "491502.64",
        "refund_amount": "-23780.42",
        "profit": "467722.22"
    }
}
```

- ** 微店个人中心销售额和销售量数据 **
> api_name: api/pc/store_sale_info
> type: POST

| 字段名 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
|start_time| int | Y | 1518220800 | 查询开始时间 |
|end_time | int | Y | 1518307200 | 查询截止时间 |

```json
{
        "status": "success",
    "code": 200,
    "message": null,
    "modul": "Message",
    "data": {
    "sale_amount": [
        {
            "amount": "3887231.11",
            "goods_id": 8,
            "goods": {
                "id": 8,
                "name": "Mrs. Kyla Harris",
                "price": "78.64",
                "mktprice": "20.43",
                "brand_id": 624,
                "goods_brands": null
            }
        },
    ],
    "sale_num": [
        {
            "num": 15424,
            "goods_id": 2,
            "goods": {
                "id": 2,
                "name": "Ms. Florine Franecki Jr.",
                "price": "85.50",
                "mktprice": "54.67",
                "brand_id": 2,
                "goods_brands": {
                    "id": 2,
                    "brand_name": "aut"
                }
            }
        }
        ]
    }
}
```

| 字段名 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
|sale_amount| array | Y | - | 销售额数据 |
|amount | string | Y | 3887231.00 | 单件商品最大销售金额 |
|goods_id| intger | Y | 8 | 商品ID |
|goods| array | Y | - | 商品信息数据 |
|name| string | Y |连衣裙 | 商品名称 |
|price | string | Y | 100.00 | 商品下单金额 |
|mktprice | string | Y | 100.00 | 商品市场金额 |
|brand_id| array | Y | 2 | 品牌ID |
|brand_name| string | Y | 恩裳 | 品牌名称 |
|sale_num| array | Y | - | 销售数量数据|
|num| int | Y | 10 | 单件商品销售数量 |

- ** 微店个人中心会员动态 **
> api_name: api/pc/store_member_state
> type: GET

```json
[
    {
        "type": 0,
        "fans_type": 1,
        "nickname": "13981872066",
        "uuid": "3644ca43-4e55-48d5-a5d8-2f250ec7f87c",
        "info": {
            "desc": "会员登录",
            "more": {
                "address": [
                    "XX",
                    "XX",
                    "内网IP",
                    "内网IP"
                ],
                "client": "Windows 10---Chrome(63.0.3239.132)",
                "ip": "127.0.0.1"
            },
            "created_at": "3周前"
        }
    },
    {
        "type": 1,
        "fans_type": 0,
        "nickname": "13981872066",
        "uuid": "3644ca43-4e55-48d5-a5d8-2f250ec7f87c",
        "info": {
            "desc": "浏览商品",
            "more": {
                "name": "YINER音儿2017冬新款中长款纯羊毛双面呢大衣女8C57580330",
                "img_path": "/storage/images/goods/list/2P36RtQDVgpAuJIa0Z5xj1itEyqF5DRXUvCySGYU.jpeg",
                "goods_id": 1
            },
            "created_at": "3周前"
        }
    }
]
```

| 字段名 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
|type| int | Y | 1 | 动态类型，0：会员登录 1：浏览商品 2：购买商品 |
|fans_type | int | Y | 1 | 粉丝类型 0:会员数 1：转粉数 |
|nickname| string | Y | "小伙子" | 会员昵称 |
|uuid| string | Y | 3644ca43-4e55-48d5-a5d8-2f250ec7f87c | 会员唯一识别号 |
|desc| string | Y | "浏览商品" | 会员动态描述 |
|more | array | Y | - | 详细信息，商品数据、登录信息 |
|name | string | Y | YINER音儿2017冬新款中长款纯羊毛双面呢大衣女8C57580330 | 商品名称 |
|img_path| string | Y | url | 商品封面图 |
|goods_id| intger | Y | - | 商品ID |
|created_at| string | Y | 3周前 | 动态产生时间 |
|address| array | Y | - | 登录地址信息 |
|address.0| string | Y | 中国 | 国家 |
|address.1| string | Y | 广东 | 省份 |
|address.2| string | Y | 深圳 | 市区 |
|address.3| string | Y | 电信 | 网络运营商 |
|client| string | Y | Windows 10---Chrome(63.0.3239.132) | 设备信息 |