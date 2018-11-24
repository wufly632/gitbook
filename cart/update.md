## 购物车更新
### 接口地址：
/carts/update
### 请求类型：post
#### 请求参数：
|参数 | 必填 | 类型 |  说明|
|:---|:---:|:---:|:---|
| token | 否 | String | 用户登录信令 |
| good_id | 是 | number | 商品ID |
| sku_id | 是 | number | sku ID |
| num | 是 | number | 商品数量 |
#### 返回参数：
返回数据与购物车详情相同