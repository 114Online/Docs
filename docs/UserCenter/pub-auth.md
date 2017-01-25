# 子系统授权

## 授权接口

接口地址：[http://uc.114-online.com/WeChat/Auth](http://uc.114-online.com/WeChat/Auth)

调用方式：`GET`

参数说明：

| 参数名 | 格式 | 备注 |
|-------|------|-----|
| appid | GUID | 在本系统中创建的应用ID |
| redirect_url | string | 接受回调的URL(需Url Encode) |

举例：

```
http://uc.114-online.com/WeChat/Auth?appid=9b61f74a-9164-4767-add2-912387213b96&redirect_url=http%3a%2f%2fsample.114-online.com%2fapi%2fcallback
```

返回值说明：

| 参数名 | 格式 | 备注 |
|-------|------|-----|
| open_id | GUID | 针对特定App生成的用户ID（固定且唯一） |
| nick_name | string | 该微信用户的昵称 |
| avatar_url | string | 该用户的头像URL |

返回值或行为：

```
跳转至：
http://sample.114-online.com/api/callback?open_id=a5315695-b1d8-4db9-a8af-9aad8cc160de&nick_name=blablabla&avatar_url=http%3a%2f%2fwx.qlogo.cn%2fmmopen%2fk8mFfEmdQe32bFJVaacSFdR1hANgYO9cRUMQJBIjZPSqP1ByhCHodYwibwuGwxaFP0x01JXUHKv5cSygGvXxOnQ%2f0
```