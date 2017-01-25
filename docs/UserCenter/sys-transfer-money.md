# 微信转账

发送短信功能通过调用www.e-fast.cn接口实现

使用时，请调用`Task<bool> Hongding.WeChat.UserCenter.Lib.WeChat.TransferMoneyAsync(Guid OrderId, string OpenId, long Price, string Description);`

参数说明：

| 参数名 | 类型 | 备注 |
|-------|------|------|
| OrderId | Guid | 交易单号 |
| OpenId | string | 微信OpenID |
| Price | long | 交易金额(以分为单位，大于等于100) |
| Description | string | 交易备注（string不能为null和""） |

返回值说明

| 类型 | 备注 |
|-----|------|
| Task<bool> | 包含了交易是否成功的异步任务 |

调用实例：

```c#
var transfer_result = await Hongding.WeChat.UserCenter.Lib.WeChat.TransferMoneyAsync(Guid.Parse("1ae2c643-fd5c-4ed5-921d-92b513efa8e5"), "ol9Liw5EMh4q7zN9UMwCyEalgb2k", 100, "测试转账");
```