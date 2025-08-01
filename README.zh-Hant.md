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

在專案根目錄執行以下命令，將同時安裝或執行前後端套件。

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
