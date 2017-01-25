# 短信接口

发送短信功能通过调用www.e-fast.cn接口实现

使用时，请调用`Task<int> Hongding.WeChat.UserCenter.Lib.Sms.SendAsync(string phone, string content);`

参数说明：

| 参数名 | 类型 | 备注 |
|-------|------|------|
| phone | string | 手机号码 |
| content | string | 短信内容 |

返回值说明

| 类型 | 备注 |
|-----|------|
| Task<int> | 包含了短信编号的异步任务 |

调用实例：

```c#
var order_id = await Hongding.WeChat.UserCenter.Lib.Sms.SendAsync("18000000000", "Hello World");
```