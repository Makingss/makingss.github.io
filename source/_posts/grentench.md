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
    "res": true,
    "data": {
      "token_type": "Bearer",
      "expires_in": 17999,
      "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6ImNkOGVmYjcyNWVlYjRiMjIwYzVkODRhZjYwYWFiZThmOWJiYTEwOGMwNzZiMWNhMTUwM2MxZDE0MWEzZTcyNDg4NGIxYmFmMzZjOTZjZDAxIn0.eyJhdWQiOiIyNyIsImp0aSI6ImNkOGVmYjcyNWVlYjRiMjIwYzVkODRhZjYwYWFiZThmOWJiYTEwOGMwNzZiMWNhMTUwM2MxZDE0MWEzZTcyNDg4NGIxYmFmMzZjOTZjZDAxIiwiaWF0IjoxNDkwNTk3NjM1LCJuYmYiOjE0OTA1OTc2MzUsImV4cCI6MTQ5MDYxNTYzNCwic3ViIjoiMzEiLCJzY29wZXMiOltdfQ.WD-xjMGobVZjjw1a4ng2BgstnLagSQv2omEqmzbeTqgWGZ-bJfDePfiqI9Jks5Bvuc6gSG2zFvDbIpp4hrdg1zY_0FI7IGCoAqmtcP0lVAVpY_bPmDUPf68tBk5kKRG6tX7sB9dxrUyAVo37x0r3i5qUphZhzoqlKmE1WTaUCOtrobV1dCMqdXdgfP7n66qZKuz2EGgwmejhFQrkaUge2XUXrGgKPc6IPDJqZ0qnfBRgo0eBeGTl6Z0BmYM7R_iBRgffJnxM3fTxiWx3E9SlQ_4Xg3zxp91586v39rJ8WL3-oYtcGum0t75o9Fip_lLNYo-JpgI41bVd9uiJp5LDV4WXT7Z0WJTckMMCP3pcuMKOB4wr8bX3Bd8EdnbX-s9sEHjYvegkcZMPdUZx2618Daj5OTAVkXJCKijnrxSR_ewF2oGPxNWyeGRzbaS58uW3M3SZ6VgI_FCKpCY6_PZMXG9SITKQsIulaVBe04dRvlKLkj4TioEM7AxY5Pb53jY5chbcEdqr3YbHjLHzOKzUKsR96C5P2HE4UGmIF-sOjWcQR73iv8zSi9840UDUzH6IVIWw19jhjZfhVeF6hGDwbv_dqb05Ka6AQeX2z9w91p6BeJ7zbYTW1OZYFJutLH7eftYk6-pJupLSDAlq9PM4cDAYFPOPY4wLsWxgg-l3eSM",
      "refresh_token": "E2/AtJG+OyOB3wC0H6TWBJ5gisNrlSc9OQ4JI/qinyDXRkT9tmWu8zXZgph68J1Yg7HUujM4ZFjYUDDypnrHTWhat+mxt0KiY0yC/1fpU2zyI59WoQ9bBydrsdnSt/gpDxNRnVzWR1uPbo1vSmmvdHoEUJ6c69NZNOhjnKUPfppZikocMxZ5qQ6OdDgrt22a6/sgIvKB5RnjS1iM4pi6D5PTea+jwzmzHFMr/DJ6cZriIflI+YGHzSPDW4dzQudh78+vJzi4TXmZvpmbMvJbErqB3WMZjY5UtJGwhrGAhQIRLPPRqObUUM6uenOoASrgW6YxS+A/J5yIHQQSF8a1sBIB4UL97+WjhCH7rSlbDJqmPC/jTNap3yn9irY1lAzaxMyb1uSTO6uya/Q4SPfWn2wt/hKJ7U04V2hMIQmpS4nN4IfZ7QhicYtiwlEaf+5w7RvJeSftA/OOcGLzyY0R5tjZ5+OOcY4YSpunuV31+7wunO5a5svKpo0JXcGrLB96kpAjfOpGJwynRVMpcbOZElomChdDFS5MllfiwbTmqIDfAwAYe2iGP/3/LHy7A9aPLJFJm+DjLOoXGOq7NLcsgaklj5g+Xk6BwxfP0bsXOboVwekHdUvFfmQvoyY58qxBqaRK7JzFDQgjH789ACF47g2A6PSS1gHaq0pl0gIUdsk=",
      "client_id": 27,
      "client_secret": "01b3ba6f1fb31460df52e22f337b7c14"
    },
    "req": "激活成功"
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
          "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6ImMyMjg0ZTU0MGM2NDZmYzg4ODBmMTk2ZTE3ZTJjMjdiMmQ5N2FiOTY5NDY2ZDUzMmQ5MmNkNjQ0ODU2ZWNhNmY0ZDNmYmU2NTIzOTJiOGJkIn0.eyJhdWQiOiIyNSIsImp0aSI6ImMyMjg0ZTU0MGM2NDZmYzg4ODBmMTk2ZTE3ZTJjMjdiMmQ5N2FiOTY5NDY2ZDUzMmQ5MmNkNjQ0ODU2ZWNhNmY0ZDNmYmU2NTIzOTJiOGJkIiwiaWF0IjoxNDkwNTk2Mjc3LCJuYmYiOjE0OTA1OTYyNzcsImV4cCI6MTQ5MDYxNDI3Nywic3ViIjoiMjkiLCJzY29wZXMiOltdfQ.ib-htKJYz7OwPiY9YIAF2xwgrk5QyHGdZoH2UwoPcfDQJvj9vO5xU-VuI3PCX6MLFJRnEtqCRHdV5_PzQfqwMop59XcoEZWP_LsY3-UHy8eGtqsSO9FvOMi7ajrm9zDQS5tbRBcD_EgsMtWl1btGBaAtp6PGsrgGDlU9rXswTXx_w4NpKpZUSDhz4dGX4USvEkJxTsL1xF8oYP5yZAo3aBTFs6dksc3WygAuH8W60wYT0ulMm6RErQFHVN-ShqxAYSIR-kPaERfY19OC7_aPoTFZxj7fInAK8vFn7SaOcyW7Agu6t3mQRCzdUNwAUtoV1Uuvl-M7NP7y6W7Bv-Nm6pHcNrHYoy7kqKspe1i5UTrCmtn3dv-q5s0i7c8k4NgSqbAKzuHYDJL1pP4gQel5tGQW2AO-bAWglqocWz3EZHyuxKm8hzc62MzKDcQvqzgUfCWEGR_9KbnhMtTotyu2ykuzMK23o9VE_fx80o3KKmpJlTUc9tXKHSDoWMba3g4ovnpRuBTkhwOhoKfurlcZ7pN8yGyUnxNvoROsWlZYCznpTn-XF7IkXLk4c96A6UpujYISAoG_ZEnunc0YI3LcNwKMetqRk-dAsMmkqDBsK-wChuNIzVUtUbeFooz7vfBQ2rOyq1CKKajLlQlqCj02ZjoliH0YBKS6QfPl268nszE",
          "refresh_token": "W5j9n24SQ76hRTE7ZvnhkRHmYpz2PACNX8s3HvynlxNZx6gLAkcT2aIbS3kn77miyV1WQrSh6VfxsRUY6tdlM6zsxedEpugVWXYvUY8mUIIEUoa+gL+X9l9bCYPFmnIbBQwY/ipcWbdxyRO09MUFatMM2bZwYsld/dXd5FrPMSOJWayLx8w3N4+DtlnS1AhlZidyNMhiobFaHVOxY10iesd613czFJWpafnfAVw/eq7wa5KlZnYwhKUpeAvJjMLOk10n0csY+WVNTWqXlNB1nsqHXTDk5P1iZwiHUd24TSlwLpDv9dIs4ymctQsNPmEyxepMRt9FhOslXMeBILi/5ueQNIvOgq5aB8ouDz54+AQ8xUZ/UZCGJmsT7MqiktriHYnH//B1P5mUVZYbwnTBDIsOtEMGGIPua343MSjtJkCWkURoHAttIicGbc9e+qzpMnCHjrxUDN37csulm7al3saFCb3aoIwgMgSfd5meWvJNyBKlwbsox5FrBUJgLx2MAykrurmWj9kSOwR9Rbq7I8DmCwzhb+3BuSDDfqrEZPdMgPJG1SaGksbr2nTO16kcBqhdyRHvkehhL4JucAAenFLetnfa3tP7otD5ZvBVCOtgUAhsYzVQ+WkN6buHtQ7rRhzar9ZfyGRzfGraH7B62HyKlgjWncEWEwn+HVZEy0s=",
          "client_id": 25,
          "client_secret": "2709d31ea993d366e857043b28efaa22"
        },
        "req": "登录成功"
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

- ** 刷新access_token **
> api_name: oauth/token

| 参数        | 实例           | 说明  |
| ------------- |:-------------:| -----:|
| grant_type | refresh_token | 类型 |
| refresh_token | bx8BjnooLqfRiOtctxGa8iDyqQD2IgfV9Qpa1acI1ETA3RMEJYdTlEceqF1HUi.. | 刷新令牌 |
| client_id | 25 | 用户令牌ID(登录成功后端返回) |
| client_secret | 2709d31ea993d366e857043b28efaa22 | 密钥(登录成功后端返回) |
| scope |  | 作用域如为*无视后端权限策略，默认为空

        {
          "token_type": "Bearer",
          "expires_in": 18000,
          "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6Ijg4NmUxODIyNTYxZjAyYzYzZTQyZGYxYTRhZTBiM2RmYjEyZjRiNDJkNzQxOTNhNjI4OTE4MWIzNWIxYWY5ZGRkYTUwNDdkYWJiODYyYTBhIn0.eyJhdWQiOiIyNSIsImp0aSI6Ijg4NmUxODIyNTYxZjAyYzYzZTQyZGYxYTRhZTBiM2RmYjEyZjRiNDJkNzQxOTNhNjI4OTE4MWIzNWIxYWY5ZGRkYTUwNDdkYWJiODYyYTBhIiwiaWF0IjoxNDkwNTk2NjUzLCJuYmYiOjE0OTA1OTY2NTMsImV4cCI6MTQ5MDYxNDY1Mywic3ViIjoiMjkiLCJzY29wZXMiOltdfQ.iyT0q2H0kCKz6oFDAmHRS03DgfnonfQyKVg7vv5iSF3_kkaTmD7zq1EvQCFx0Y6TCuS1T4kq3BVyHnwy8_AlsRVTN_X0cR1tarQlvrZcey7O8htY6qDZbsEzGXUbTUNjRxyJsvM7BTbd367LTaaNGJpOBd2FKDyUoS1v8AS8KUA0K8numkcjBduNxG7YactSjr9h7d_ptDyLOXqaQfhmeHaCQ-4NT0UNPvpUni8iHOOAkbvCjXsyKLlEsz9peDMRn0LBFF73_yiupvr_6Yql2nq4QO9bvEtIpRJVNkWbbi2s6oXf8IdrU0uEXlaZm3bCJB6oCzSUVHoqYCYMV5Df8gp8uaeJChprLtKmUFmCLRHt4H8zj4tauTELsshR1A0wv6bn20-mOycCX5iKP7B1kmgunaZ7MBZZCAbOPdHCaz5V0sMJ1PV7vENaKkyDPbaiDzWSKRnlDcOeKvTPV-vhA_Gzw-hzNWUn2SNBU5wUHf-FqDwnoG5e0PhMQA6xU6eKm6BZafZZ9NVe4t4Pb05FvjvC-rb6SKRkFP-nkhNB8c8Vc4-hMbcEzztYnxxT8AkZmq-H0MemMXDn9-w3Td3dkHb0YG5-QGLfy8GjQrEhScybRN16eHAVzGuN7tUOleFTk_y-75CKCmFv3jRR3oJW1x6mK894cf8lQKJKSAW_khc",
          "refresh_token": "bx8BjnooLqfRiOtctxGa8iDyqQD2IgfV9Qpa1acI1ETA3RMEJYdTlEceqF1HUiO9RKv8ZILRsSPnO4HuyfdOSb8pCrdAFNS9Dwju+6+wSk5bdzs5Lnc+EIr4JQ4PWGZjMpZe87rP3lEtgTvYp+9SIHRelC6GefQIni/ID5i/V+crz1XdLjDGykh3fJnhtytbb3WabxnSvvNujVvfQx5uK92O5y9atVUlgeReSz4iTE8zkXr/J5rp0Ovj6oe97MBFVcBO/NO0KOhwK4RMtDiylj5ltpx4YkhB5+rRmH9og8qSRQX6+4hKIq6Sc8uFNr63h98xPD3o1xm8wl4NrrB7JOrP7cXt9AKhUpcwOBPJd8vS5KPUpqNYRxpGR2s33D2H4EiiOUjKbQZVlFbl3g5YqLJLXzqh78Ecg4XaIhSPa9+VWPZmfUx9cF6qiDxgDCdtUNjHlUmI3dgrqeTXCjfRMmDr/J9nNRbyxTBxVfRKJucmN3aE7Ce10xna7doIgg5HqDoHhufioJWXDaG2e+S4W6NQNQlMXdpUNIgoZ2cHrhN+d/mCsWyRF6QtsMt549dxD7BEFE6nFaLP/kGUmLjSX+ot3fUPGQNZ50my2TYjzRiSfdQMewBj1EiuCYYQJvKbQ4I0gPN0H621KoGh85GAMrZsrp2Su2Z5ltx1+UtCdyE="
        }
- ** 后台登录 **
> api_name: login

| 参数        | 实例           | 说明  |
| ------------- |:-------------:| -----:|
| username | admin | 用户名称 |
| password | 123456 | 密码 |
  #### 成功
        {
          "res": true,
          "data": {
            "id": 1,
            "username": "admin",
            "password": "$2y$10$Na09JEJ4/WR1zU7ecbmsOOBwqtOn8nmTOiiY.HPl/smUHrL6R0zvu",
            "name": "Administrator",
            "remember_token": "CXwa8e5WN5wyEb95r0TPVDywmifFrN0BMRKmLADAfBTTlXlnQ15lS6yEMscj",
            "created_at": "2016-12-28 14:13:27",
            "updated_at": "2017-03-24 00:55:36",
            "is_admin": "Y",
            "avatar": "http://grentech.app/uploads/image/Koala.jpg"
          },
          "req": "登录成功"
        }
  #### 失败
          {
          "res": false,
          "req": "账号或密码错误"
          }