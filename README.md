# XuMaMa 点餐系统

## 项目简介

XuMaMa 点餐系统是一个基于 Spring Boot 开发的企业级点餐管理平台，采用前后端分离架构，提供完整的餐饮服务解决方案。系统具备菜品管理、订单处理、用户管理等核心功能。

## 技术栈

### 后端
- Spring Boot 2.7.x
- Spring Security
- MyBatis Plus
- MySQL 8.0
- Maven

### 前端
- Thymeleaf 模板引擎
- Bootstrap 4
- jQuery
- Layer UI

## 主要功能

### 🍽️ 菜单管理
- 动态菜单配置
- 菜品分类管理
- 价格实时调整
- 库存状态监控

### 🥗 订餐功能
- 灵活配菜选择
- 套餐组合
- 特殊要求备注
- 实时库存检查

### 📝 订单系统
- 订单实时提交
- 状态自动更新
- 订单查询统计
- 打印功能支持

### 👤 用户管理
- 角色权限控制
- 员工账户管理
- 用户信息维护
- 操作日志记录

### 💰 结算系统
- 多种支付方式
- 订单金额统计
- 账单导出
- 营收报表

## 环境要求

- JDK 1.8+
- Maven 3.6+
- MySQL 8.0+

## 快速开始

### 1. 获取项目

```bash
git clone https://github.com/hexsean/xumama.git
cd xumama
```

### 2. 数据库配置

```sql
# 创建数据库
CREATE DATABASE xumama DEFAULT CHARACTER SET utf8mb4;
```

修改 `application.properties` 配置：

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/xumama?useSSL=false&serverTimezone=UTC
spring.datasource.username=your_username
spring.datasource.password=your_password
```

### 3. 构建运行

```bash
# 编译项目
mvn clean package

# 运行项目
java -jar target/xumama-1.0.0.jar
```

访问 http://localhost:8080

## 项目结构

```
xumama/
├── src/main/java/
│   └── com/xumama/
│       ├── controller/    # 控制器层
│       ├── service/      # 业务逻辑层
│       ├── dao/         # 数据访问层
│       ├── entity/      # 实体类
│       ├── config/      # 配置类
│       └── util/        # 工具类
├── src/main/resources/
│   ├── static/         # 静态资源
│   ├── templates/      # Thymeleaf模板
│   └── application.properties # 配置文件
├── src/test/          # 测试代码
└── pom.xml           # Maven配置文件
```

## 配置说明

### 应用配置
```properties
# 服务器配置
server.port=8080
server.servlet.context-path=/xumama

# 数据库配置
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.datasource.url=jdbc:mysql://localhost:3306/xumama
spring.datasource.username=root
spring.datasource.password=password

# MyBatis配置
mybatis-plus.mapper-locations=classpath:mapper/*.xml
mybatis-plus.type-aliases-package=com.xumama.entity
```

## 部署说明

### 生产环境部署
1. 修改配置文件为生产环境配置
2. 使用 Maven 打包：`mvn clean package -Pprod`
3. 将生成的 jar 文件部署到服务器
4. 使用 systemd 或其他工具管理服务

## 开发指南

### 代码规范
- 遵循阿里巴巴Java开发规范
- 使用统一的代码格式化配置
- 必要的注释和文档

### 分支管理
- master: 主分支，用于生产环境
- develop: 开发分支
- feature/*: 功能分支
- hotfix/*: 紧急修复分支

## 常见问题

1. Q: 系统无法启动？
   A: 检查数据库配置和端口占用情况

2. Q: 如何修改端口号？
   A: 在 application.properties 中修改 server.port

## 许可证

本项目使用 MIT 许可证 - 查看 [LICENSE.md](LICENSE.md) 了解详情


## 更新日志
--暂无
---

🍽️ XuMaMa - 让点餐更简单！
