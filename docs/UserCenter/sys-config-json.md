# 系统配置文件

系统配置文件位于系统根目录，文件名为`config.json`

## 样例

```json
{
    "Management": {
        "Username": "root",
        "Password": "sha1-hashed-password"
    },
    "WeChat": {
        "AppId": "your-wechat-app-id",
        "Secret": "your-wechat-secret",
        "MchId": "your-mch-id",
        "SignKey": "your-sign-key",
        "AuthCaching": 15
    },
    "Host": {
        "ConnectionString": "server=localhost;uid=root;pwd=123456;database=hd_usercenter",
        "Redis": "localhost"
    },
    "Sms": {
        "CorpId": "your-corp-id",
        "Pwd": "your-pwd"
    }
}
```

## 配置文件字段说明

### Management

| 成员名 | 类型 | 备注 |
|--------|-----|------|
| Username | string | 管理员用户名，用于登录本系统 |
| Password | string | 经过SHA1加密后的密码 |

### WeChat

| 成员名 | 类型 | 备注 |
|--------|-----|------|
| AppId | string | 微信公众平台App ID |
| Secret | string | 微信公众平台私钥 |
| MchId | string | 微信商户平台ID |
| SignKey | string | 微信商户平台预留私钥 |
| AuthCaching | int | 授权缓存时间（以天为单位） |

### Host

| 成员名 | 类型 | 备注 |
|--------|-----|------|
| ConnectionString | string | MySQL数据库连接字符串 |
| Redis | string | Redis连接字符串 |

### Sms

| 成员名 | 类型 | 备注 |
|--------|-----|------|
| CorpId | string | E-Fast短信平台提供的企业号 |
| Pwd | string | E-Fast短信平台设置的密钥 |