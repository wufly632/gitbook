## 粉丝列表
### 接口地址：
/personal/fans
### 请求类型：post
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| page | 否 | Number | 页数 |
###  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息   成功：空 |
| content | Object | 返回信息 |
#### content：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| total_page | Number | 总页数 |
| fans | Array | 收入列表 |
#### fans：（[object]）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| image | String | 用户头像 |
| name | String | 昵称 |
| sub_fans | Number | fans数量 |
|  currency_symbol | String | 货币符号 |
| benefit | Number |  累计收益 |
| date | String | 入账时间 |
### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "total_page": 2,
        "incomes": [
            {
                "image": "http://www.baidu.com",
                "name": "Co Co",
                "sub_fans": "10",
                "currency_symbol":"$",
                "benefit": "20",
                "date": "2018-09-25 10:23:56"
            },{
                "image": "http://www.baidu.com",
                "name": "Co Co",
                "sub_fans": "10",
                "currency_symbol":"$",
                "benefit": "20",
                "date": "2018-09-25 10:23:56"
            }
        ]
    }
}
```