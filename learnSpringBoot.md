# Spring Boot 学习笔记

## JDBC

### 在 Spring Boot 配置中修改 MySQL JDBC 时区

问题描述：写入数据库的日期和实际差一天。

解决方法：修改`application.properties`相关属性。

```
spring.datasource.url=jdbc:mysql://localhost:3306/db_name?serverTimezone=Asia/Shanghai

```

## 相关资源

[SpringBoot Thymeleaf 使用教程（实用版）](https://www.jianshu.com/p/908b48b10702)
