# Surge 5 配置文档

## 文件说明

- `surge.conf` - Surge 5 主配置文件

## 快速开始

1. 打开 Surge 应用
2. 导入 `surge.conf` 配置文件
3. 根据自己的需求修改代理和规则

## 配置部分说明

### [General]
基础配置，包括日志等级、DNS 服务器等

### [Proxy]
定义代理服务器

### [Proxy Group]
定义策略组，用于灵活切换代理

### [Rule]
定义流量规则，决定不同的流量走哪个策略

### [Script]
可选的脚本配置

### [Mitm]
可选的中间人攻击配置

## 常用代理类型

- `ss` - Shadowsocks
- `vmess` - VMess
- `trojan` - Trojan
- `http` - HTTP 代理
- `socks5` - SOCKS5 代理

## 更多信息

访问 [Surge 官方文档](https://manual.nssurge.com/) 了解更多配置选项。