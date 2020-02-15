# gmall
分布式商城项目（纯后端）

Springboot+dubbo的模拟分布式商城微服务demo

## web项目

1、gmall-admin-web

后台web项目，提供管理员注册，登录校验，商品上下架到es，及文件上传到oss等Controller层功能

2、gmall-shop-portal

前台web项目，提供商品检索、商品具体信息查询、用户登录、在线及离线购物车、订单创建及支付等Controller层功能

## 微服务项目

1、gmall-oms

提供购物车及订单相关服务

2、gmall-pms

提供商品检索及商品信息详情查询等功能

3、gmall-oms

提供用户管理员登录及信息查询等相关功能

2/16 记一件小事
晚上调试接口时发现数据库无法查询到东西，但是更新操作却可以，想来想去一个多小时也不知道哪里出了问题，最后发现是下午整理数据库时从库断开连接了，
最后才弄好，因为增删改都是直接在主库进行的，而查询是在从库进行的，一个大坑，耽误了两个小时。