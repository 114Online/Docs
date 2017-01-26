# 租户帐号校验

## 用户名密码验证

接口地址：[http://uc.114-online.com/Api/CheckTenantAccount](http://uc.114-online.com/Api/CheckTenantAccount)

调用方式：`POST`

参数说明：

| 参数名 | 格式 | 备注 |
|-------|------|-----|
| appid | GUID | 在本系统中创建的应用ID |
| secret | string | 创建应用时系统提供的64字符的私钥 |
| username | string | 租户的用户名 |
| password | string | 租户的密码 |

举例：

```
POST 
appid = 9b61f74a-9164-4767-add2-912387213b96
secret = sh4x91ipa01n24jx8fh2b15v95ui0lm5xsa0zp149slf85cnml0954iza48jfc14
username = lg1045
password = 123456
```

返回值说明：

| 参数名 | 格式 | 备注 |
|-------|------|-----|
| data | object | 租户基本信息对象 |
| data.role | string | 用户角色（`Root`或`Tenant`）|
| data.id | long | 租户ID |
| data.name | string | 租户名称 | 

返回值或行为：

```json
{
    "code": 200,
    "msg": "success",
    "data": {
        "role": "Tenant",
        "id": 1,
        "name": "龙广汽车人"
    }
}
```