# bootcamp-dawn

A Shopify project using the Shopify CLI and theme tools.

## Prerequisites

- [nvm](https://github.com/nvm-sh/nvm) (Node Version Manager) — recommended for easily managing and switching Node.js versions
- [Node.js](https://nodejs.org/) (required: version 18.20.2 or 20.11.1, the project use version specified in the `.nvmrc` file, i.e. v24.0.2)
- [npm](https://www.npmjs.com/)
- [Git](https://git-scm.com/) (required: version 2.18.0 or higher)
- macOS, Windows, or Linux (Shopify CLI is supported on these operating systems)
- You must have a Shopify store and a store staff account with permission to manage themes ([Shopify requirements](https://shopify.dev/docs/api/shopify-cli#requirements))

## Setup

1. Clone this repository:

   ```bash
   git clone https://github.com/ythdelmar68/bootcamp-dawn.git
   cd bootcamp-dawn
   ```

2. Use the Node.js version specified in `.nvmrc` (ensures compatibility):

   ```bash
   nvm use
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

4. Login to Store and pull the current theme from Shopify

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

4. Publish your theme
    ```bash
    # Publish to make your theme live on your store, you must make sure that you've pushed all of your local changes to Shopify using the theme push command.
    shopify theme publish
    # Select the theme that you want to publish from the list.
    ```

## Scripts

- `npm run shopify` &mdash; Runs the Shopify CLI.

## Dependencies

- `@shopify/cli`
- `@shopify/theme`

## License

ISC
