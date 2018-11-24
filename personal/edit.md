## 修改资料
### 接口地址：
/personal/edit
### 请求类型：post
### 请求参数
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| name | 是 | String | 用户姓名 |
| birth | 是 | String | 生日 |
| email | 是 | String | 手机号 |
| gender | 是 | String | 性别 |
| phone | 是 | String | 电话 |

####  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | number | 状态码  |
| msg | String | 失败信息   成功：空   失败：'失败信息'|
| content | string | |

```
{
    "status": 200,
    "msg": "success",
    "content": "修改成功"
}
```