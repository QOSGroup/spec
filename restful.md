# Restful Spec

scheme:[//[user[:password]@]host[:port]][/path][?query][#fragment]

## 规则

1. 合法的scheme只限于http/https/ws
2. path必须使用小写
3. query必须是小写或者是驼峰样式（首字母小写）
4. fragment不允许使用
5. 只使用HTTP的状态码
6. 响应体必须是合法的JSON
7. POST、PUT请求方法BODY体不能为空，body同时必须是合法的JSON数据
8. GET、DELETE必须保证是幂等性的
8. 业务无关的功能只使用HTTP HEADER，不能使用BODY和URL参数

## 举例

1. 查看用户列表

```
GET  /users/
```

2. 查看用户详情

```
GET  /users/1
```

3. 创建用户

```
POST  /users/1
```

3. 更新用户信息

```
PUT  /users/1
```

4. 删除用户

```
DELETE  /users/1
```
