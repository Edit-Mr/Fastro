<div align=center>

<img src="https://raw.githubusercontent.com/Edit-Mr/Fastro/main/frontend/src/assets/img/icon/EM.svg" alt="Fastro Logo" width="50">

# Fastro

EM's Website starter template using Astro and Fastify.

![Astro](https://img.shields.io/badge/Astro-5f3cbe?logo=astro) ![Fastify](https://img.shields.io/badge/Fastify-000000?logo=fastify)

</div>

> [繁體中文](README.zh-Hant.md) | English

## Features

- **Astro**: With Sitemap and i18n intergration.
    - Auto redirect to system language.
    - Save language preference in local storage.
- **Fastify**: A fast and low overhead web framework for Node.js.
- **Prettier**: Code formatter to maintain consistent style.
- **concurrently**: Run frontend and backend at the same time.

## How to use

Press the "Use this template" button at the top right to create a new repository with this template.

<img src=https://docs.github.com/assets/cb-76823/mw-1440/images/help/repository/use-this-template-button.webp width=500>

> No need to include all branches, though there's only one branch.

## Project Structure

```plaintext
.
├── frontend/   # Astro
├── backend/    # Fastify
```

if you only want to use one of them, kust simply delete the other folder, and move all files to the root.

## Development

> Make sure you have [pnpm](https://pnpm.io/) installed.

Both frontend and backend package will be installed or run if you run this command at the root of the project.

### Install dependencies

```bash
pnpm install
```

### Local development

```bash
pnpm dev
```

### Build (For Astro)

```bash
pnpm build:frontend
```
