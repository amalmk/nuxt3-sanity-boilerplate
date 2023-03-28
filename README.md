# Nuxt 3 (SSG) + Sanity + Tailwind Minimal Starter


## Prerequisites

This setup requires @sanity/cli to be installed globally: `npm install -g @sanity/cli`

## Setting up Nuxt

Install the dependencies:

```bash
# yarn
yarn install

# npm
npm install

# pnpm
pnpm install
```

## Setting up Sanity

1. I have committed the `/studio` directory for reference purpose only. For a cleaner experience, you might need to delete the same and create a new sanity project using the command `sanity init`. This will ask you to choose an existing Sanity project or create a new one. You could choose any directory name as you wish, but for consistancy, I normally go with `/studio`.
2. Sanity CLI will create a `/studio` directory at project root with the Sanity Frontend code in it. 
3. Navigate to `/studio` directory and do a `sanity install` (an `npm install` should also work)
4. Make sure your sanity project ID is configured in both the sanity.json files in the `/studio` directory as well as in the project root.


## Nuxt dev server

To start the Nuxt development server on http://localhost:3000, from project root, run:

```bash
npm run dev
```

## Sanity dev server

To start Sanity development server, from `/studio`, run: 

```bash
sanity start
```

...local server will be running on http://localhost:3333

## Production

Generating static  the application for production:

```bash
npm run generate-nuxt-sanity
```

This will run internally run `nuxt generate`, builds the Sanity project and copies the output to `/public/studio` directory. You can then navigate to https://www.yourdomain.com/studio to access the Sanity admin console.

## References

1. [Nuxt 3 documentation](https://nuxt.com/docs/getting-started/introduction)
2. [Sanity module for Nuxt 3](https://sanity.nuxtjs.org/getting-started/quick-start)
3. [Tailwind configuration for Nuxt 3](https://tailwindcss.com/docs/guides/nuxtjs#3)

