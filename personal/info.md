## 个人资料
### 接口地址：
/personal/info
### 请求类型：post
### 请求参数
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
###  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | number | 状态码  |
| msg | String | 失败信息   成功：空   失败：'失败信息'|
| content | string | 用户信息 |
### content：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| image | string | 个人头像 |
| name | String | 用户姓名 |
| gender | String | 性别 |
| birth | String | 生日 |
| email | string | 邮箱 |
| phone | String | 电话 |
### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "image": "http://192.168.1.122:6006/goods/20170718/thumb/201707181645191500367519172.jpg",
        "name": "long.hao",
        "gender": "male",
        "birth": "2018-09-30 12:20:30",
        "email": "long.hao@cucoe.com",
        "phone": "12346"
    }
}
```