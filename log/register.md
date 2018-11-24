## 注册
### API 名称
/users/register
### 请求方式
post
### 请求参数
参数 | 类型 | 必选 | 说明
---|---|---|---
email | string | 是 | 用户邮箱 必填最大长度320字符 |
password | string | 是 | 密码 必填长度6～18字符 |
subscribe | boolean | 否 | 是否订阅消息 |
token | string | 否 | 游客token
### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "user_id": 162,
        "token": "bcdfilmopqtwxyzABEFHIJKMRSVWZ058162"
    }
}
```