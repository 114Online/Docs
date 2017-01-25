# User Center SDK

向项目根目录中添加`NuGet.config`文件，内容如下：

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <packageSources>
    <add key="114-online" value="https://www.myget.org/F/114online/api/v3/index.json" />
    <add key="nuget.org" value="https://www.nuget.org/api/v2" />
  </packageSources>
</configuration>
```

向`project.json`中添加`Hongding.WeChat.UserCenter.SDK`

```json
"dependencies": {
    "Hongding.WeChat.UserCenter.SDK": "1.0.0-*"
}
```

向`Startup.cs`中添加`UserCenter`

```c#
services.AddHongdingUserCenter(Guid.Parse("aa25f1f3-32c7-4552-9304-122e6fb4bba8"), "h1inru294mrqd09adwdif4wupwn7qrwb0mwdds20phci0yv3q583kuuvnwgwk69m");
```

在控制器中注入`HongdingUC`类，调用相关方法即可：

```c#
public async Task<IActionResult> Index([FromServices] HongdingUC UC)
{
    if (string.IsNullOrEmpty(HttpContext.Session.GetString("x-OpenId")))
    {
        var url = UC.GenerateAuthUrl($"{ HttpContext.Request.Scheme }://{ HttpContext.Request.Host }/WeChat/CallBack");
        return Redirect(url);
    }
    var internalOpenId = Guid.Parse(HttpContext.Session.GetString("x-OpenId"));
    var profile = await UC.GetProfileAsync(internalOpenId);
    return View(profile);
}
```

[在GitHub上查看完整示例](https://github.com/114Online/Hongding.WeChat.UserCenter.SDK/tree/master/samples/SampleWeb)