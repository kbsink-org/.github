<div align="center">

<img src="https://kbsink-org.github.io/assets/logo.svg" width="96" alt="Kbsink logo" />

# Kbsink

**Multi-platform social content collector — sync to your private knowledge base**

[Website](https://kbsink-org.github.io/) · [Obsidian plugin](https://github.com/kbsink-org/obsidian-kbsink) · [CLI](https://github.com/kbsink-org/kbsink-cli)

</div>

---

**English** · [中文](#中文)

## What we build

**Kbsink** turns share links from social platforms into **Markdown + images/videos** you can keep in Obsidian, on disk, or in your own app. One conversion pipeline, multiple front-ends.

| Platform | Status |
|----------|--------|
| WeChat articles | Supported |
| Xiaohongshu (小红书) | Supported |
| Douyin (抖音) | Supported |

## Repositories

| Repo | Description |
|------|-------------|
| [**kbsink**](https://github.com/kbsink-org/kbsink) | Go library — Driver, Parser, Storage, `Convert` pipeline |
| [**kbsink-plugins**](https://github.com/kbsink-org/kbsink-plugins) | Platform parsers & drivers (wechat, xhs, douyin, …) |
| [**kbsink-cli**](https://github.com/kbsink-org/kbsink-cli) | CLI + `kbsink.wasm` for scripts and JS hosts |
| [**obsidian-kbsink**](https://github.com/kbsink-org/obsidian-kbsink) | Obsidian plugin (desktop & mobile), no external binary |
| [**kbsink-org.github.io**](https://github.com/kbsink-org/kbsink-org.github.io) | Project website (this landing page) |

## Quick start

**Obsidian** — install [obsidian-kbsink](https://github.com/kbsink-org/obsidian-kbsink/releases), enable the plugin, run **Import URL with kbsink**, paste a link.  
Docs: [kbsink-org.github.io](https://kbsink-org.github.io/#obsidian)

**Terminal**

```bash
go install github.com/kbsink-org/kbsink-cli/cmd/kbsink@latest
kbsink "https://mp.weixin.qq.com/s/…"
```

## Architecture

```text
  URL (WeChat / XHS / Douyin)
           │
           ▼
    kbsink-plugins  ──►  kbsink (core)
           │                  │
           ├──── kbsink-cli (CLI / WASM)
           └──── obsidian-kbsink (Obsidian + WASM)
           │
           ▼
    Markdown + assets  →  vault / output folder
```

## Contact

Questions and ideas: [GitHub Discussions](https://github.com/orgs/kbsink-org/discussions) (enable in org settings) or open an issue in the relevant repo.

---

## 中文

**Kbsink** 把微信、小红书、抖音等分享链接转为 **Markdown 与图片/视频**，方便存入 Obsidian、本地目录或自建应用。同一套转换核心，多种使用方式。

| 平台 | 状态 |
|------|------|
| 微信公众号文章 | 支持 |
| 小红书 | 支持 |
| 抖音 | 支持 |

### 仓库

| 仓库 | 说明 |
|------|------|
| [**kbsink**](https://github.com/kbsink-org/kbsink) | Go 核心库（Driver / Parser / Storage） |
| [**kbsink-plugins**](https://github.com/kbsink-org/kbsink-plugins) | 各平台解析与驱动 |
| [**kbsink-cli**](https://github.com/kbsink-org/kbsink-cli) | 命令行与 WASM 构建 |
| [**obsidian-kbsink**](https://github.com/kbsink-org/obsidian-kbsink) | Obsidian 插件（桌面与手机） |
| [**kbsink-org.github.io**](https://github.com/kbsink-org/kbsink-org.github.io) | 项目官网 |

### 快速上手

- **Obsidian**：安装 [obsidian-kbsink](https://github.com/kbsink-org/obsidian-kbsink/releases) → 启用插件 → 命令面板 **使用 kbsink 导入链接**  
  说明：[kbsink-org.github.io](https://kbsink-org.github.io/#obsidian)

- **命令行**：`go install github.com/kbsink-org/kbsink-cli/cmd/kbsink@latest`，然后 `kbsink "<文章链接>"`

---

<p align="center">
  <sub>MIT · <a href="https://kbsink-org.github.io/">kbsink-org.github.io</a></sub>
</p>
