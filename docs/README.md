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

## 当前仓库默认配置特性

- 默认启用 `ipv6 = true`，并补充 IPv6 DNS 与本地 IPv6 网段直连规则。
- 预置 `PROXY`、`自动选择`、`香港节点`、`台湾节点`、`日本节点`、`狮城节点`、`美国节点` 等地区策略组。
- 预置 Apple、AI、Telegram、YouTube、Netflix、Spotify、Microsoft、Game、漏网之鱼 等常见服务策略组。
- `GEOIP,CN,DIRECT` + `FINAL,漏网之鱼` 可满足大多数日常使用场景。

## 使用建议

1. 先在 `[Proxy]` 中填入你自己的节点。
2. 节点命名时尽量包含地区关键字，例如 `HK-01`、`JP-Tokyo`、`US-LA`，这样策略组可以自动归类。
3. 如果你常用流媒体或 AI 服务，可以在 `[Rule]` 中继续补充更细的域名规则。

