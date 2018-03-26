---
title: font_print
date: 2018-01-31 14:15:29
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
##### 足迹数据
-  ** 获取足迹 **
> api_name: api/pc/foot_print
> type: GET

```json
{
    "status": "success",
    "code": 200,
    "message": null,
    "modul": "Message",
    "data": [
        {
            "goods_id": 1,
            "member_id": 5,
            "p_order": 27,
            "created_at": "2018-01-11 14:19:56"
        },
        {
            "goods_id": 3,
            "member_id": 5,
            "p_order": 26,
            "created_at": "2018-01-11 14:38:59"
        },
        {
            "goods_id": 2,
            "member_id": 5,
            "p_order": 23,
            "created_at": "2018-01-11 14:19:56"
        }
    ]
}
```
| 字段名 | 类型/长度 | 非必须 | 事例 |备注 |
| -----|:-------|:-------|:-----|:--------|
| goods_id | int |  Y  | 1 | 商品
