## 密码重置邮件发送
### API名称
/users/pwreset
### 请求方式
post
### 请求参数
参数 | 类型 | 必选 | 说明
---|---|---|---
email | string | 是 | 用户邮箱
### 返回参数
###  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | number | 状态码  200 |
| msg | String | 失败信息 成功：success 失败：'失败信息'|
| content | String | 返回数据 success |
### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": "success"
}
```