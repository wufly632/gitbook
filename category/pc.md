## 前端类目接口(PC)
### 接口地址
/pc/cates
### 请求方式：post
### 请求参数：无
### 返回参数：
###  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | number | 状态码  200 |
| msg | String | 失败信息 成功：success 失败：'失败信息'|
| content | onject | 类目信息 |
### 返回示例：
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "cates":[
            {
                "name": "HOME & LIVING",
                "id": 193,
                "sub": [
                    {
                        "id": 1498,
                        "name": "Clothing",
                        "sub": [
                            {
                                "id": 1498,
                                "name": "Clothing"
                            }
                        ]
                    },{
                        "id": 1498,
                        "name": "Clothing",
                        "sub": [
                            {
                                "id": 1113,
                                "name": "skin care"
                            }
                        ]
                    }
                ]
            },
            {
                "id": 1078,
                "name": "BEAUTY",
                "sub": [
                    {
                        "id": 1498,
                        "name":"Clothing"
                    }
                ]
            }
        ] 
    }
}
```