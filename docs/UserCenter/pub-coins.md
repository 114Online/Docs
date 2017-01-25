# 用户虚拟货币

用户虚拟货币是跨应用的货币计量系统，只要货币字段填写一直，可实现跨App的虚拟货币操作。

## 查询用户虚拟货币余额

接口地址：[http://uc.114-online.com/Api/GetExtensionCoins](http://uc.114-online.com/Api/GetExtensionCoins)

调用方式：`POST`

参数说明：

| 参数名 | 格式 | 备注 |
|-------|------|-----|
| appid | GUID | 在本系统中创建的应用ID |
| secret | string | 创建应用时系统提供的64字符的私钥 |
| openid | GUID | 回调时提供的Internal Open ID |
| field | string | 虚拟货币字段名称 |

举例：

```
POST 
appid = 9b61f74a-9164-4767-add2-912387213b96
secret = sh4x91ipa01n24jx8fh2b15v95ui0lm5xsa0zp149slf85cnml0954iza48jfc14
openid = a5315695-b1d8-4db9-a8af-9aad8cc160de
field = 砸金蛋奖券
```

返回值说明：

| 参数名 | 格式 | 备注 |
|-------|------|-----|
| data | int | 该用户指定货币的余额 |

返回值或行为：

```json
{
    "code": 200,
    "msg": "success",
    "data": 0
}
```

## 设置用户虚拟货币

接口地址：[http://uc.114-online.com/Api/SetExtensionCoins](http://uc.114-online.com/Api/SetExtensionCoins)

调用方式：`POST`

参数说明：

| 参数名 | 格式 | 备注 |
|-------|------|-----|
| appid | GUID | 在本系统中创建的应用ID |
| secret | string | 创建应用时系统提供的64字符的私钥 |
| openid | GUID | 回调时提供的Internal Open ID |
| field | string | 虚拟货币字段名称 |
| value | int | 欲指定该用户该货币的数量 |

举例：

```
POST 
appid = 9b61f74a-9164-4767-add2-912387213b96
secret = sh4x91ipa01n24jx8fh2b15v95ui0lm5xsa0zp149slf85cnml0954iza48jfc14
openid = a5315695-b1d8-4db9-a8af-9aad8cc160de
field = 砸金蛋奖券
value = 1
```

返回值或行为：

```json
{
    "code": 200,
    "msg": "success",
    "data": null
}
```

## 增加用户虚拟货币

接口地址：[http://uc.114-online.com/Api/IncreaseExtensionCoins](http://uc.114-online.com/Api/IncreaseExtensionCoins)

调用方式：`POST`

参数说明：

| 参数名 | 格式 | 备注 |
|-------|------|-----|
| appid | GUID | 在本系统中创建的应用ID |
| secret | string | 创建应用时系统提供的64字符的私钥 |
| openid | GUID | 回调时提供的Internal Open ID |
| field | string | 虚拟货币字段名称 |
| value | int | 欲指定该用户该货币增加的数量 |

举例：

```
POST 
appid = 9b61f74a-9164-4767-add2-912387213b96
secret = sh4x91ipa01n24jx8fh2b15v95ui0lm5xsa0zp149slf85cnml0954iza48jfc14
openid = a5315695-b1d8-4db9-a8af-9aad8cc160de
field = 砸金蛋奖券
value = 1
```

返回值或行为：

```json
{
    "code": 200,
    "msg": "success",
    "data": null
}
```

执行后该用户的砸金蛋奖券增加了1

## 减少用户虚拟货币

接口地址：[http://uc.114-online.com/Api/DecreaseExtensionCoins](http://uc.114-online.com/Api/DecreaseExtensionCoins)

调用方式：`POST`

参数说明：

| 参数名 | 格式 | 备注 |
|-------|------|-----|
| appid | GUID | 在本系统中创建的应用ID |
| secret | string | 创建应用时系统提供的64字符的私钥 |
| openid | GUID | 回调时提供的Internal Open ID |
| field | string | 虚拟货币字段名称 |
| value | int | 欲指定该用户该货币减少的数量 |

举例：

```
POST 
appid = 9b61f74a-9164-4767-add2-912387213b96
secret = sh4x91ipa01n24jx8fh2b15v95ui0lm5xsa0zp149slf85cnml0954iza48jfc14
openid = a5315695-b1d8-4db9-a8af-9aad8cc160de
field = 砸金蛋奖券
value = 1
```

返回值或行为：

```json
{
    "code": 200,
    "msg": "success",
    "data": null
}
```

执行后该用户的砸金蛋奖券减少了1

