---
title: grentech api 文档
date: 2017-03-24 13:59:46
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

> update_time:'2017.03.04'

---
##### 用户注册相关
-  ** 请求注册 **
> api_name: register

| 参数        | 实例           | 说明  | 备注 |
| ------------- |:-------------:| -----:| -----:|
| 用户名 | name | making | 不能为空最长255字符 |
| 邮箱   | email  |   123@qq.com | 不能为空，验证邮箱格式，最长255字符，验证唯一性 |
| 密码 | password |    123456 | 不能为空，最少6位字符 |
| 确认密码  | password_confirmation | 123456 | 不能为空，与上一条password相同 |

> 接口返回值

        {
          "name": [
            "The name 必填字段."
          ],
          "email": [
            "The email 必填字段."
          ],
          "password": [
            "The password 必填字段."
          ]
        }

        {
          res:true,
          data:{
            member_id:'60905',
            nick_name:'symeny',
            login_account:'18503009595',
            avatar:'',
            point:'',
            level:'',
          }
        }
#### 返回地址
  + url格式：servername.com/jump?token=key&secret=key
  + 例如：http://grentech.dev/jump?token=ZDPfCSeSLQYRyq0KuPBgdpBAN1aOfseFKywF2KCU$secret=b62cmlvBZJEhA5r9ZFLVU4JtzMs2P7KlcDZHYJM/0l0VZFYV
  - ** 通过邮箱激活账号 **
  > api_name: verify 

| 参数      | 实例   | 说明 |
| ------    |:----:| -------:|
| 口令 | verify | alKWFc246ez1JsfvITV7YwCsL0NOtYFljmaTwUTq |
| 密码 | secret | f1b8KuA7bl2JpEOHHnA0rur+AoRpjm3nFe9rMBV8v8uFc+F1 |
        
        {
        "res": true,
        "data": {
            "token_type": "Bearer",
            "expires_in": 18000,
            "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6IjA3NzFkYWEzOWJhOTc4OWY1ZDdmNzQwMTM3YzdmNWMxMzVkZDljZDZmYjAwYWIwOWY0NWQ3NjgwYjI3ZmI2MjY3MWJjOWJmZWM0NmJlNDZlIn0.eyJhdWQiOiIyMyIsImp0aSI6IjA3NzFkYWEzOWJhOTc4OWY1ZDdmNzQwMTM3YzdmNWMxMzVkZDljZDZmYjAwYWIwOWY0NWQ3NjgwYjI3ZmI2MjY3MWJjOWJmZWM0NmJlNDZlIiwiaWF0IjoxNDkwMTgxNzk0LCJuYmYiOjE0OTAxODE3OTQsImV4cCI6MTQ5MDE5OTc5NCwic3ViIjoiMjMiLCJzY29wZXMiOltdfQ.G8e3yOfwcdcJ1VsKlbaykxGex8Jcq_q79WGG6b-YxsIn9uHJ0Bgja5wXtlxLpr8bTFyIWVR_xKeOyzEu28VL1p_VTnZhUgdGbThF6Jdb7KuQbzqt4T3kzPZkbMDVWnbj80COc5zFLsI1Sxd1pII3AlRjfC9nhg_6Lq739a_Y_IUyyK60Wx9heObU5YuJwk2yU4N0YYzk0FhvQb6_WN5OVhXybnRmlPzORmOcAY7T67EadqeTwPDW2ES2UBSv0tDHCwz_-fsQYC2-fRjjHQ--0xkOSQViQgT_bAySc97NzqxYORgnQaFa4ESEIxrbDZAkrp26hc-JRsjfyeVPZu80AWQI-cjYMScfyUWOUtRyaYY9iN1jmVuntvFUxWgRIzLrSAJLcnxU-0dMn6iiy5r8iOD0Vb6WOrqfXELqsroISllsfB8enWk-c9DlYlOcWwMtA4FJQoLCTXrir6UQNWv3KX7RxC8IJiQ5TtuxX_krNqLaR0kUWnJ8gj239nKA9AWL1m2yPEIFCrNiSIBMVlSwHSEGTdoNGZG3wqJf1023lz2oECRt7fgtga5tNFbyKLBCfqzUlrZ4GZ5e9hOWaAAxrZqCpdKBc7hqeDSssZxIFNzzqt6uc6NP3SZ6xPUxPlXHiz1l9uVNXI9AukXVAAXaxFfrHviUhXP7bk4_1Hu-H6U",
            "refresh_token": "vooByp8oPrK3ZQyG17sDfA5/WhKOPzAr+9EsDfQifSYTaXOXplLl03bTER1fPY4Ha5A9u5vaU47U3TC0wU+r7Fj3BgmmGQ5M6l2AVG7F8EoU5SdQh2ALiLcMXEUMNya5AiACsekyiQvF2tzp4wGnwpSkvLyFYETUh6+k8WcNJcyj9JeB6kNTGKBNPDKNo774mDcXfHn7dTxYLCtnL/sJeDdm2um1i3V6HSY6orclhV4fYacoPviZGWyFETCuSqUTGzGwcGAvZnHAKxlZWCmDmWqusuOziQuT5qG8bnYOT5TJ6azBlxiRoxcLQb+zzTqyBHWU84q0Fu4qpc78or+HLKtk3DfYK8v/BclWVS35GcTCF8EFOEeYDvdMZkkNOIOj2Fq6xVpwWr3ZtM64tChLWUifAYAC5wHycJPdPLyGe3uRXOS5V6kiilofihUtBFO07/79TqJ4CpnnL2FeruZY8EdV4+DAWco0G/usXiL+XNC8tFPz/xRjJXUJJScV19wJRkwmZhxULuNswzzu8aMgMzg1eJBMfOTxEFxz4t/1aSq+TUVj7OkoLSMOpzELTX87/D2cKYiuDFvm0yFD6lRjHXYFpik0/RvbuoZ5B6/K+y6z9yGSYf4wAg2LSbdG2KzrBv3+YV+Rf7XWK3L8TwcUpxJuqEsEUC3wJKax80zE8WA="
        },
        "req": "激活成功"
}

- ** 修改用户名 **
> api_name: update_user_name

| 参数        | 实例           | 说明  |
| ------------- |:-------------:| -----:|
| 用户id | member_id | making |
| 新用户名   | user_name  |   123456 |
| 密码 |  pwd      |    nbsp |
| 验证码 | vcode      |    非必须 |


      {
        res:true,
        data:{}
      }

+ #### 商品相关
- ** 获取商品列表 **
> api_name: get_googs_list

| 参数        | 实例           | 说明  |
| ------------- |:-------------:| -----:|
| 关键字 | kwds | 无人机 |
| 分页长度  | 10  |  必须  |
| 分页码 |  2     |   必须  |
        {
          res:true/false,
          data:{

          }
        }
- ** 获取商品详情 **
> api_name:get_goods_detail

| 参数        | 实例           | 说明  |
| ------------- |:-------------:| -----:|
| 商品 id | goods_id | 无人机 |
        {
          res:true/false,
          data:{}
        }
- ** 获取品类 **
> api_name:get_category_list

| 参数        | 实例           | 说明  |
| ------------- |:-------------:| -----:|
| 品牌 id | 1 | 品牌 |
        {
          res:,
          data:{}
        }
- ** 获取收藏商品  **
> api_name:get_fav_goods

| 参数        | 实例           | 说明  |
| ------------- |:-------------:| -----:|
| member_id | 60905 | 必须 |
        {
          res:true/false,
          data:{

          }
        }

