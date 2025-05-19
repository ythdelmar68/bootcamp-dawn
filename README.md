# bootcamp-shopify

A Shopify project using the Shopify CLI and theme tools.

## Prerequisites

- [Node.js](https://nodejs.org/) (recommended: latest LTS)
- [npm](https://www.npmjs.com/)
- [nvm](https://github.com/nvm-sh/nvm) (Node Version Manager) — recommended for easily managing and switching Node.js versions

## Setup

1. Use the Node.js version specified in `.nvmrc` (ensures compatibility):

   ```bash
   nvm use
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Theme files are located in the `theme/` directory. Make your theme customizations and development changes there.

    ```bash
    cd theme
    ```

4. Login to Store and pull the current theme from Shopify

    ```bash
    npm run shopify them pull -- --store=<store-name>.myshopify.com
    ```
## Usage

1. Before running any commands, ensure you are using the correct Node.js version by running:

   ```bash
   nvm use
   ```
   This uses the version specified in the `.nvmrc` file at the project root.

- Run Shopify CLI commands via npm script:

  ```bash
  npm run shopify <command>
  ```

- For theme development, refer to [Shopify Theme Docs](https://shopify.dev/docs/themes).

## Scripts

- `npm run shopify` &mdash; Runs the Shopify CLI.

## Dependencies

- `@shopify/cli`
- `@shopify/theme`

## License

ISC
