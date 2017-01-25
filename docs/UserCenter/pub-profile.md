# 用户信息接口

## 获取用户信息

接口地址：[http://uc.114-online.com/Api/GetProfile](http://uc.114-online.com/Api/GetProfile)

调用方式：`POST`

参数说明：

| 参数名 | 格式 | 备注 |
|-------|------|-----|
| appid | GUID | 在本系统中创建的应用ID |
| secret | string | 创建应用时系统提供的64字符的私钥 |
| openid | GUID | 回调时提供的Internal Open ID |

举例：

```
POST 
appid = 9b61f74a-9164-4767-add2-912387213b96
secret = sh4x91ipa01n24jx8fh2b15v95ui0lm5xsa0zp149slf85cnml0954iza48jfc14
openid = a5315695-b1d8-4db9-a8af-9aad8cc160de
```

返回值说明：

| 参数名 | 格式 | 备注 |
|-------|------|-----|
| data | object | 返回的用户信息对象 |
| data.name | string | 该用户的真实姓名 |
| data.phone | string | 该用户的手机号 |
| data.plate | string | 该用户的车牌号 |
| data.prcid | string | 该用户的身份证号 |
| data.avatar | string | 该用户的头像URL |
| data.nickname | string | 该用户的昵称 |

返回值或行为：

```json
{
    "code": 200,
    "msg": "success",
    "data": {
        "name": "张三",
        "phone": "18888888888",
        "plate": "黑A 12345",
        "prcid": "230103199901011111",
        "nickname": "blablabla",
        "avatar": "http://wx.qlogo.cn/mmopen/k8mFfEmdQe32bFJVaacSFdR1hANgYO9cRUMQJBIjZPSqP1ByhCHodYwibwuGwxaFP0x01JXUHKv5cSygGvXxOnQ/0"
    }
}
```