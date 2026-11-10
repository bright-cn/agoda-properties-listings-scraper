# Agoda 房源列表抓取工具

[![Bright Data](https://img.shields.io/badge/Powered%20by-Bright%20Data-FF9A00?style=flat-square)](https://www.bright.cn/) [![爬虫工具 API](https://img.shields.io/badge/Scraper%20API-Available-FF9A00?style=flat-square)](https://www.bright.cn/products/web-scraper/agoda) [![数据集](https://img.shields.io/badge/Dataset-Available-0066CC?style=flat-square)](https://www.bright.cn/products/datasets/agoda) [![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org) [![许可证：MIT](https://img.shields.io/badge/License-MIT-22C55E?style=flat-square)](LICENSE)

[![优惠活动](https://github.com/bright-cn/Awesome-Web-Scraping/raw/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner%20CN.png)](https://www.bright.cn/products/web-scraper/agoda)

> **由 [Bright Data](https://www.bright.cn/) 提供支持的 Agoda 房源列表数据。**

此存储库提供两种大规模访问 Agoda 房源列表数据的方法：

- **[方法 1：Bright Data Agoda 房源列表爬虫工具 API](#方法-1bright-data-agoda-房源列表爬虫工具-api)**（推荐），一款完全托管的企业级爬虫 API，可自动处理代理、CAPTCHA 和扩展问题。
- **[方法 2：Bright Data Agoda 房源列表数据集](#方法-2bright-data-agoda-房源列表数据集)**，可直接下载的预采集 Agoda 房源列表数据集，无需进行网页爬虫。

## 目录

- [为什么使用 Bright Data 抓取 Agoda 房源列表？](#为什么使用-bright-data-抓取-agoda-房源列表)
- [方法 1：Bright Data Agoda 房源列表爬虫工具 API](#方法-1bright-data-agoda-房源列表爬虫工具-api)
  - [快速入门](#agoda-房源列表爬虫工具-api-快速入门)
  - [1. Agoda 房源列表](#1-agoda-房源列表)
- [方法 2：Bright Data Agoda 房源列表数据集](#方法-2bright-data-agoda-房源列表数据集)
- [数据采集方法](#数据采集方法)

## 为什么使用 Bright Data 抓取 Agoda 房源列表？

抓取 Agoda 房源列表面临多项挑战：

- 速率限制：Agoda 房源列表会监控请求频率，并可能封禁超过限制的 IP。
- CAPTCHA 检测：自动访问可能会触发 CAPTCHA 验证。
- 身份验证障碍：某些数据需要登录才能访问，且平台会检测自动化操作。
- 动态内容加载：使用 JavaScript 渲染的内容很难通过简单的 HTTP 请求抓取。
- IP 封禁：从同一 IP 重复发送请求可能会导致封禁。

Bright Data 的 Agoda 房源列表爬虫工具 API 可通过以下功能解决这些问题：

- ✅ **内置动态代理**：自动绕过基于 IP 的速率限制
- ✅ **验证码破解**：无需任何额外设置即可应对机器人检测
- ✅ **结构化数据输出**：接收可直接用于分析的整洁 JSON
- ✅ **无需基础设施**：支持任意规模的云端托管抓取
- ✅ **99.9% 正常运行时间 SLA**：为业务关键型工作流提供可靠的数据采集

## 方法 1：Bright Data Agoda 房源列表爬虫工具 API

[Bright Data Agoda 房源列表爬虫工具 API](https://www.bright.cn/products/web-scraper/agoda) 是一款无需设置任何基础设施的完全托管解决方案。

### Agoda 房源列表爬虫工具 API 快速入门

1. **注册**一个[免费的 Bright Data 账户](https://www.bright.cn/)
2. **前往** [Agoda 房源列表爬虫工具 API](https://www.bright.cn/products/web-scraper/agoda)
3. 从控制面板**获取 API 令牌**
4. **安装** `requests` 库：`pip install requests`
5. **运行** `agoda-properties-listings_scraper_api_codes/` 中的任意脚本

### 1. Agoda 房源列表

采集 Agoda 的房源列表。

#### 输入参数

| 字段 | 类型 | 必填 | 描述 |
|-------|------|----------|-------------|
| `url` | 字符串 | 是 | 要抓取的 Agoda 房源列表条目的 URL |
| `limit` | 整数 | 否 | 返回结果的最大数量 |
| `include_errors` | 布尔值 | 否 | 在响应中包含错误详情 |
| `notify` | URL | 否 | 采集完成时用于接收通知的 Webhook URL |
| `format` | 枚举 | 否 | 输出格式：`JSON`、`NDJSON`、`JSON Lines`、`CSV` |

#### 响应示例

```json
{
  "city": "Ko Phi Phi",
  "country": "Thailand",
  "db_source": "1776443774941",
  "hotel_id": 1277006,
  "location": "157 Moo 7 , Aonang,, Ton Sai Bay, Ko Phi Phi, Thailand, 81210",
  "title": "ChaoKoh Phi Phi Hotel \u0026 Resort",
  "url": "https://www.agoda.com/en-gb/chaokoh-phi-phi-hotel-resort/hotel/koh-phi-phi-th.html?ds=dzGygd8GnnlfYqbD"
}
```

👉 查看[完整 Python 代码](agoda-properties-listings_scraper_api_codes/agoda_properties_listings_scraper.py)

## 方法 2：Bright Data Agoda 房源列表数据集

如果你需要无需编写任何抓取代码即可使用的数据，[Bright Data Agoda 房源列表数据集](https://www.bright.cn/products/datasets/agoda)可提供预先采集、定期更新且可立即下载的数据。

**为什么使用数据集而不是 API？**

- 📦 **即时访问**：无需设置、无需代码，也无需等待采集
- 🔄 **定期更新**：按照固定周期刷新最新数据
- 📊 **多种格式**：可下载为 JSON、JSONL 或 CSV
- 🌍 **超大规模**：涵盖 Agoda 房源列表所有主要类别的数百万条记录
- ✅ **完全合规**：数据来源符合道德规范并已通过法律审查

👉 **[探索 Agoda 房源列表数据集](https://www.bright.cn/products/datasets/agoda)**

## 数据采集方法

| 功能 | Bright Data 爬虫工具 API | Bright Data 数据集 |
|---------|------------------------|---------------------|
| 所需设置 | 仅需 API 令牌 | 无 |
| 实时数据 | ✅ 是 | ❌ 预先采集 |
| 自定义查询 | ✅ 完全控制 | ❌ 固定架构 |
| 包含代理 | ✅ 内置动态代理 | N/A |
| CAPTCHA 破解 | ✅ 自动 | N/A |
| 规模 | 无限制 | 无限制 |
| 结构化输出 | ✅ JSON / NDJSON / JSON Lines / CSV | ✅ JSON / JSONL / CSV |
| 支持 | 企业级全天候支持 | 企业级全天候支持 |

---

🔗 **了解更多**：[https://www.bright.cn/products/web-scraper/agoda](https://www.bright.cn/products/web-scraper/agoda)
