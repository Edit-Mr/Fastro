<div align=center>

<img src="https://raw.githubusercontent.com/Edit-Mr/Fastro/main/frontend/src/assets/img/icon/EM.svg" alt="Fastro Logo" width="50">

# Fastro

EM's Website starter template using Astro and Fastify.

![Astro](https://img.shields.io/badge/Astro-5f3cbe?logo=astro) ![Fastify](https://img.shields.io/badge/Fastify-000000?logo=fastify)

</div>

## Features

- **Astro**: With Sitemap and i18n intergration.
    - Auto redirect to system language.
    - Save language preference in local storage.
- **Fastify**: A fast and low overhead web framework for Node.js.
- **Prettier**: Code formatter to maintain consistent style.

## How to use

Press the "Use this template" button at the top right to create a new repository with this template.

![Use this template](https://docs.github.com/assets/cb-76823/mw-1440/images/help/repository/use-this-template-button.webp)

> No need to include all branches, though there's only one branch.

## Project Structure

```plaintext
.
├── frontend/   # Astro
├── backend/    # Fastify
```

if you only want to use one of them, kust simply delete the other folder.

For example, if you want to use Astro only, you can run the following command:

```bash
rm -rf backend && rm -rf ./* && mv frontend/* . && rm -rf frontend
```

## Development

### Install dependencies

```bash
pnpm install
```

Both frontend and backend package will be installed if you run this command at the root of the project.

> Make sure you have [pnpm](https://pnpm.io/) installed.

### Local development

```bash
pnpm dev
```

Both frontend and backend will be started in development mode.

### Build (For Astro)

```bash
pnpm build
```
