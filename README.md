# Nuxt PNPM Linting Template

[![Lint](https://github.com/iceship/nuxt-template-app/actions/workflows/lint.yaml/badge.svg)](https://github.com/iceship/nuxt-template-app/actions/workflows/lint.yaml)

A minimal Nuxt starter template using PNPM and ESLint to provide robust linting capabilities and an efficient development environment. This template offers a solid foundation for building modern web applications with Nuxt, leveraging the efficiency of PNPM and the code quality management of ESLint.

## Key Features ✨

- **Nuxt 3**: The latest version of the intuitive Vue framework.
- **PNPM**: A fast and disk-space-efficient package manager.
- **ESLint**: Configured with the comprehensive `@antfu/eslint-config` for high code quality standards.
- **GitHub Actions**: Automated linting workflow on pull requests to the `main` branch ensures code consistency.
- **VSCode Integration**:
  - Includes recommended extensions for ESLint, Tailwind CSS, Vue (Volar), and Pretty TypeScript Errors.
  - Configured to use ESLint as the default formatter with auto-fix on save.
- **Tailwind CSS**: A utility-first CSS framework for rapid UI development.
  - **DaisyUI**: A Tailwind CSS component plugin with default light and dark themes.
- **TypeScript**: Provides strong typing for enhanced code quality and maintainability.
- **Environment Variable Validation**: Uses Zod for runtime environment variable parsing and validation.
- **Icon Management**: Uses `@nuxt/icon`.
- **Color Mode**: Supports light and dark modes via `@nuxtjs/color-mode`.

## Project Setup 🚀

Ensure you have [PNPM](https://pnpm.io/installation) installed.

1.  **Clone the repository (or use as a template):**

    ```bash
    git clone [https://github.com/](https://github.com/)iceship/nuxt-template-app.git
    cd nuxt-template-app
    ```

2.  **Install dependencies:**
    This project uses PNPM.
    ```bash
    pnpm install
    ```
    _This command also prepares Nuxt and Husky._

## Development 💻

Start the development server on `http://localhost:3000`:

```bash
pnpm dev
```

## Linting 🧹

This project uses ESLint, configured with `@antfu/eslint-config`, to lint code.

- **Check for linting errors:**

  ```bash
  pnpm lint
  ```

- **Automatically fix linting errors:**
  ```bash
  pnpm lint:fix
  ```

Linting is also automatically run on pull requests to the `main` branch via a GitHub Action.

## Type Checking 🧐

To perform type checking across your application, run the following command:

```bash
pnpm typecheck
```

## Production 📦

1.  **Build the application for production:**

    ```bash
    pnpm build
    ```

2.  **Locally preview the production build:**
    ```bash
    pnpm preview
    ```

For more information, check the [Nuxt deployment documentation](https://nuxt.com/docs/getting-started/deployment).

## VSCode Configuration ⚙️

This template includes recommended VSCode extensions and settings for an optimal development experience.

- **Recommended Extensions** (`.vscode/extensions.json`):
  - `dbaeumer.vscode-eslint` - Integrates ESLint into VSCode.
  - `bradlc.vscode-tailwindcss` - Provides Tailwind CSS IntelliSense.
  - `Vue.volar` - Offers Vue 3 language support.
  - `yoavbls.pretty-ts-errors` - Makes TypeScript errors more readable.
- **Workspace Settings** (`.vscode/settings.json`):
  - Disables Prettier to use ESLint as the default formatter.
  - Enables ESLint auto-fix on save for supported languages.
  - Associates CSS files with Tailwind CSS.
  - Sets stylistic rules in the IDE to be auto-fixed without warnings.
  - Enables ESLint validation for a wide range of file types.

## Environment Variables 🔒

Environment variables are managed and validated using Zod.
Refer to `lib/env.ts` for the schema definition. The `tryParseEnv` utility in `lib/try-parse-env.ts` ensures that required environment variables are present during the build process.

## Additional Information

For more details, check the [Nuxt documentation](https://nuxt.com/docs/getting-started/introduction).

## Acknowledgements 🙏

This template was inspired by and references the work of w3cj in the [nuxt-travel-log](https://github.com/w3cj/nuxt-travel-log) project.
