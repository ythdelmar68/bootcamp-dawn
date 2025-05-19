# bootcamp-shopify

A Shopify project using the Shopify CLI and theme tools.

## Prerequisites

- [nvm](https://github.com/nvm-sh/nvm) (Node Version Manager) — recommended for easily managing and switching Node.js versions
- [Node.js](https://nodejs.org/) (required: version 18.20.2 or 20.11.1)
- [npm](https://www.npmjs.com/)
- [Git](https://git-scm.com/) (required: version 2.18.0 or higher)
- macOS, Windows, or Linux (Shopify CLI is supported on these operating systems)
- You must have a Shopify store and a store staff account with permission to manage themes ([Shopify requirements](https://shopify.dev/docs/api/shopify-cli#requirements))

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

2. To preview your store locally, change to the `theme` directory and run the development server:

   ```bash
   cd theme
   npm run shopify theme dev
   ```
   See the [Shopify CLI theme dev documentation](https://shopify.dev/docs/api/shopify-cli/theme/theme-dev) for more details.



- For theme development, refer to [Shopify Theme Docs](https://shopify.dev/docs/themes).

3. Run any Shopify CLI commands via npm script:

  ```bash
  npm run shopify <command>
  ```

## Scripts

- `npm run shopify` &mdash; Runs the Shopify CLI.

## Dependencies

- `@shopify/cli`
- `@shopify/theme`

## License

ISC
