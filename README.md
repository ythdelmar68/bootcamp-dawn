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

3. Login to Store and pull the current theme from Shopify

    ```bash
    # Pull the current theme from Shopify
    npm run shopify theme pull -- --store=<store-name>.myshopify.com
    ```
## Usage

1. Before running any commands, ensure you are using the correct Node.js version by running:

   ```bash
   nvm use
   ```
   This uses the version specified in the `.nvmrc` file at the project root.

2. To preview your store locally, run the development server:

   ```bash
   npm run shopify theme dev
   ```
   See the [Shopify CLI theme dev documentation](https://shopify.dev/docs/api/shopify-cli/theme/theme-dev) for more details.

3. To push your theme changes to your store:

   ```bash
   # Push to your development theme, you will need to give the theme a name
   npm run shopify theme push -- --unpublished

   # After the theme is created, you can update your theme code by running the `push` command without any flags
   npm run shopify theme push

4. Run any other Shopify CLI commands via npm script:

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
