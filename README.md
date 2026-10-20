# 分布式主机监控与 Web 远程运维平台

由监控客户端、服务端和 Web 管理端组成的主机监控平台。客户端采集主机运行信息，服务端提供账号、客户端管理和数据接口，Web 端使用图表展示状态并通过终端界面进行远程运维。

## 技术栈

- 后端与客户端：Java 17、Spring Boot、MyBatis-Plus、WebSocket
- 前端：Vue 3、Element Plus、ECharts、xterm.js
- 数据与中间件：MySQL、Redis、RabbitMQ、InfluxDB

## 项目结构

- `itbaima-monitor-client/`：部署在被监控主机上的采集客户端
- `itbaima-monitor-server/`：平台 API、认证和客户端管理服务
- `itbaima-monitor-web/`：监控管理界面

## 本地配置

服务端的邮件、数据库、RabbitMQ、InfluxDB 和 JWT 配置使用环境变量。请在本地准备相应服务，并为远程终端功能配置专用的测试主机。客户端连接信息保存在本地 `config/` 目录，该目录已加入 Git 忽略规则。

数据库导出和运行时配置不包含在公开仓库中。请使用自己的测试数据和凭据运行项目。
