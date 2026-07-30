# frp v0.70.1 中文汉化版

> 基于 [fatedier/frp](https://github.com/fatedier/frp) v0.70.1，完成 frps Dashboard 与 frpc Web UI 的全面中文本地化。

[![GitHub release](https://img.shields.io/github/v/release/effectlve/frp_zh-cn.svg?label=release)](https://github.com/effectlve/frp_zh-cn/releases/tag/v0.70.1)
[![License](https://img.shields.io/github/license/effectlve/frp_zh-cn.svg)](LICENSE)

---

## 项目简介

本仓库对 frp v0.70.1 的 Web 管理界面进行了完整的中文汉化，便于国内用户部署、使用和运维。

- **frps Dashboard**：服务端管理面板，用于监控服务端状态、客户端连接和代理列表
- **frpc Web UI**：客户端管理面板，用于管理本地代理、访问器和配置

汉化覆盖所有面向用户的可见文本，包括导航菜单、表单标签、按钮、状态提示、确认对话框、空状态、时间显示等。

---

## 汉化范围

### frps Dashboard（服务端面板）

| 模块 | 汉化内容 |
|------|----------|
| 侧边栏导航 | 概览、客户端、代理 |
| ServerOverview | 服务器概览页面所有统计卡片、流量图表、状态信息 |
| Clients | 客户端列表页面标题、状态筛选标签（全部/在线/离线）、搜索框、空状态提示 |
| ClientDetail | 客户端详情信息标签（连接数、运行 ID、协议、客户端地址等）、代理列表空状态 |
| Proxies | 代理列表页面标题、类型筛选、清理确认对话框 |
| ProxyDetail | 代理详情页面所有信息字段、流量统计 |
| Traffic | 流量统计图表标签与时间距离显示 |

### frpc Web UI（客户端面板）

| 模块 | 汉化内容 |
|------|----------|
| 侧边栏导航 | 代理、访问器、配置 |
| ProxyList | 代理列表标题、状态筛选标签（全部/运行中/错误/等待中）、存储/配置页签、删除确认 |
| ProxyEdit | 面包屑导航、表单标题、保存/取消按钮、表单验证规则、离开确认 |
| ProxyDetail | 代理详情信息字段、状态文本映射、流量统计 |
| VisitorList | 访问器列表标题、标签页、删除确认 |
| VisitorEdit | 面包屑导航、表单验证规则、加载/保存提示 |
| VisitorDetail | 访问器详情信息字段、状态文本 |
| ClientConfigure | 配置页面标题、上传确认对话框、文件上传提示 |
| ProxyCard | 状态标签映射、操作菜单（编辑/删除/查看详情） |
| StatusPills | 状态筛选标签全部汉化 |

### 表单组件汉化

**proxy-form（代理表单）**

- ProxyBaseSection：名称、类型、启用
- ProxyRemoteSection：远程端口、自定义域名、子域名
- ProxyBackendSection：后端模式、本地 IP、本地端口、插件类型
- ProxyAuthSection：HTTP 用户名、密码
- ProxyHttpSection：HTTP 选项、路径、请求头
- ProxyTransportSection：传输选项、启用加密、带宽限制
- ProxyHealthSection：健康检查、超时、路径
- ProxyLoadBalanceSection：负载均衡、分组、分组密钥
- ProxyNatSection：NAT 穿透、禁用辅助地址
- ProxyMetadataSection：元数据

**visitor-form（访问器表单）**

- VisitorBaseSection：名称、类型、启用
- VisitorConnectionSection：服务端名称、绑定端口
- VisitorTransportSection：传输选项
- VisitorXtcpSection：XTCP 选项、协议、回退至

### 共享组件

| 组件 | 汉化内容 |
|------|----------|
| ConfirmDialog | 确认/取消按钮（默认值汉化） |
| FilterDropdown | 全部标签（默认值汉化） |
| PopoverMenu | 搜索占位符（默认值汉化） |
| ConfigField | 请选择...、键、值 |
| ConfigSection | 未配置徽章 |
| KeyValueEditor | 添加按钮、键/值占位符 |
| StringListEditor | 添加按钮、请输入值占位符 |

### 工具函数

- `formatDistanceToNow`：时间距离显示汉化（X 年前/个月前/天前/小时前/分钟前/秒前）

---

## 保留英文的内容

以下内容为 frp 协议/技术术语，按惯例保留英文：

- **协议名称**：TCP、UDP、HTTP、HTTPS、STCP、SUDP、XTCP、TCPMUX、QUIC、KCP
- **HTTP 头字段占位符**：`Header`（技术术语）
- **配置项代码标识符**：组件名、路由名、事件名等

---

## 界面截图

### frps Dashboard

#### 服务端概览



#### 客户端列表

<!-- 截图占位：frps 客户端列表页面 -->

#### 客户端详情

<!-- 截图占位：frps 客户端详情页面 -->

#### 代理列表

<!-- 截图占位：frps 代理列表页面 -->

### frpc Web UI

#### 代理列表

<!-- 截图占位：frpc 代理列表页面 -->

#### 代理编辑

<!-- 截图占位：frpc 代理编辑表单页面 -->

#### 访问器列表

<!-- 截图占位：frpc 访问器列表页面 -->

#### 配置页面

<!-- 截图占位：frpc 配置上传页面 -->

---

## 下载与使用

### 下载地址

前往 [Releases 页面](https://github.com/effectlve/frp_zh-cn/releases/tag/v0.70.1) 下载对应平台的安装包：

### 启用 Dashboard

**frps**：在 `frps.toml` 中配置：

```toml
webServer.addr = "0.0.0.0"
webServer.port = 7500
webServer.user = "admin"
webServer.password = "your_password"
```

**frpc**：在 `frpc.toml` 中配置：

```toml
webServer.addr = "0.0.0.0"
webServer.port = 7400
webServer.user = "admin"
webServer.password = "your_password"
```

启动后访问对应地址即可看到汉化后的管理界面。

---

## 致谢

- 原项目：[fatedier/frp](https://github.com/fatedier/frp) - A fast reverse proxy to help you expose a local server behind a NAT or firewall to the internet.
- 感谢 frp 开源社区的所有贡献者

## License

本项目遵循原 frp 项目的 [Apache License 2.0](LICENSE) 开源协议。
