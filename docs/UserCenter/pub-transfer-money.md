# 微信转账接口

## 转账接口

接口地址：[http://uc.114-online.com/Api/TransferMoney](http://uc.114-online.com/Api/TransferMoney)

调用方式：`POST`

参数说明：

| 参数名 | 格式 | 备注 |
|-------|------|-----|
| appid | GUID | 在本系统中创建的应用ID |
| secret | string | 创建应用时系统提供的64字符的私钥 |
| openid | GUID | 回调时提供的Internal Open ID |
| count | int | 转账金额(以分为单位的整数) |
| description | string | 可选参数，转账备注 |

举例：

```
POST 
appid = 9b61f74a-9164-4767-add2-912387213b96
secret = sh4x91ipa01n24jx8fh2b15v95ui0lm5xsa0zp149slf85cnml0954iza48jfc14
openid = a5315695-b1d8-4db9-a8af-9aad8cc160de
count = 100
```

返回值说明：

| 参数名 | 格式 | 备注 |
|-------|------|-----|
| data | GUID | 交易单号 |

返回值或行为：

```json
{
    "code": 200,
    "msg": "success",
    "data": null
}
```