# 修改租户密码

## 验证旧密码修改密码

接口地址：[http://uc.114-online.com/Api/ChangeTenantPassword](http://uc.114-online.com/Api/ChangeTenantPassword)

调用方式：`POST`

参数说明：

| 参数名 | 格式 | 备注 |
|-------|------|-----|
| appid | GUID | 在本系统中创建的应用ID |
| secret | string | 创建应用时系统提供的64字符的私钥 |
| username | string | 租户的用户名 |
| password | string | 租户的密码 |
| newpassword | string | 租户的密码 |

举例：

```
POST 
appid = 9b61f74a-9164-4767-add2-912387213b96
secret = sh4x91ipa01n24jx8fh2b15v95ui0lm5xsa0zp149slf85cnml0954iza48jfc14
username = lg1045
password = 123456
newpassword = 654321
```

返回值或行为：

```json
{
    "code": 200,
    "msg": "success",
    "data": null
}
```