## 国家列表
### 接口地址
/country
### 请求方式：post
### 请求参数：无
### 返回参数：
###  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | number | 状态码  200 |
| msg | String | 失败信息 成功：success 失败：'失败信息'|
| content | Object | 返回数据  |
### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": [
        {
            "name": "United States",
            "abbreviation": "US",
            "flag": "http://patpatdev.s3.amazonaws.com/national_flag/58eb6beda1e35/1491823597.png"
        }
    ]
}
```