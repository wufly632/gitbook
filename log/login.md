## 登录
### API名称
/users/login
### 请求方式
post
### 请求参数
参数 | 类型 | 必选 | 说明
---|---|---|---
email | string | 是 | 用户邮箱
password | string | 是 | 密码
token | string 否 | 游客token
### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "user_id": 162,
        "first_name": "hao",
        "last_name": "long",
        "email": "long.hao@cucoe.com",
        "last_login": "2018-09-04 01:46:50",
        "registered": 0,
        "member_since": 1535996810,
        "token": "bcdfilmopqtwxyzABEFHIJKMRSVWZ058162"
    }
}
```