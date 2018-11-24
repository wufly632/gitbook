## 头像修改
### 接口地址
/personal/logo
### 请求类型：post
### 请求参数
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| img_name | 是 | String | 表单名称 |
####  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | number | 状态码  |
| msg | String | 失败信息   成功：空   失败：'失败信息'|
| content | string | 头像地址 |
```
{
    "status": 200,
    "msg": "success",
    "content": "http://192.168.1.122:6006/goods/20170718/thumb/201707181645191500367519172.jpg"
}
```