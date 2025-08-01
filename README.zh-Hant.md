<div align=center>

<img src="https://raw.githubusercontent.com/Edit-Mr/Fastro/main/frontend/src/assets/img/icon/EM.svg" alt="Fastro Logo" width="50">

# Fastro

毛哥EM的網站起始模板，使用 Astro 與 Fastify。

![Astro](https://img.shields.io/badge/Astro-5f3cbe?logo=astro) ![Fastify](https://img.shields.io/badge/Fastify-000000?logo=fastify)

</div>

> 繁體中文 | [English](README.md)

## 功能特點

- **Astro**：整合了 Sitemap 和 i18n。
    - 自動重定向至系統語言。
    - 在本地儲存中保存語言偏好設定。
- **Fastify**：一個快速且輕量的 Node.js 網頁框架。
- **Prettier**：程式碼格式化工具，維持一致的風格。
- **concurrently**：前後端同時執行。

## 如何使用

點擊右上角的「Use this template」按鈕，使用此模板創建新的儲存庫。

<img src=https://docs.github.com/assets/cb-76823/mw-1440/images/help/repository/use-this-template-button.webp width=500>

> 無需包含所有分支，但其實也只有一個分支。

## 專案結構

```plaintext
.
├── frontend/   # Astro
├── backend/    # Fastify
```

如果你只想使用其中一個，只需刪除另一個資料夾，並將所有檔案移至根目錄。

## 開發

> 確保你已安裝 [pnpm](https://pnpm.io/)。

如果你在專案根目錄執行以下命令，前後端套件都會被安裝或執行。

### 安裝依賴套件

```bash
pnpm install
```

### 本地開發

```bash
pnpm dev
```

### 構建（適用於 Astro）

```bash
pnpm build:frontend
```

## 如何部署

部署 Node.js 應用程式非常簡單。Astro 是靜態網站生成器，因此可以部署到任何靜態託管服務，GitHub pages、三角形公司 Vercel、網路活佛 Cloudflare Pages、Netlify、Zeabur... 你爽就好。Fastify 可以部署到任何 Node.js 託管服務。

### Zeabur (Astro + Fastify)

選擇從 GitHub 或任何你想要的地方部署。前端應該預設部署，因為它是第一個。

如果你想部署後端，可以添加以下環境變數：

```plaintext
ZBPACK_APP_DIR=backend
```

兩個專案可以部署在一個 Project 中，但是兩個分開的服務。可以使用 Caddy 或 Nginx 來反向代理。

這裡是一個簡單的 Caddyfile 範例，把 `/api` 路徑的請求以及 `/openapi.json` 反向代理到後端服務，其他的都丟給前端：

```plaintext
:80 {
    @backend path /api* /openapi.json
    reverse_proxy @backend backend.zeabur.internal:8000
    reverse_proxy frontend.zeabur.internal:8080
}
```

### Github Pages (Astro)

GitHub Pages 只支援靜態檔案，所以你只能部署前端。在你的儲存庫中配置 `.github/workflows/gh-pages.yml` 工作流程以開啟觸發器。

```yml
on:
    push:
        branches: ["main"]
        paths: ["frontend/**"]
    workflow_dispatch:
```
