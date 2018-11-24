## 积分列表
### 接口地址
/personal/integral
### 请求类型： post
### 请求参数
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| page | 否 | Int | 页数 |

### 返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | number | 状态码  |
| msg | String | 失败信息   成功：空   失败：'失败信息'|
| content | object | 返回数据  |
####  content：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| total_page | Number | 总页数 |
| personal_integral | number | 总积分数 |
| integrals | Array | 积分流水数据 |
#### integrals : ([object])
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| integral | Int | 积分数 |
| created_at | String | 创建时间 |
| source_type | String | 购物来源 |
### 返回示例
```
｛
    "status": 200,
    "msg": "success",
    "content": {
        "total_page": 2,
        "personal_integral": "100",
        "integral": [
            {
                "integral": "+20",
                "source_type": "购物奖励",
                "created_at": "2017-07-28 10:56:22"
            },
            {
                "integral": "-30",
                "source_type": "购物消费",
                "created_at": "2017-07-29 10:57:31"
            }
        ]
    }
}
```