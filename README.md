# Astro Blog + TinaCMS Starter Kit ❤️

This template is based on Astro's official [Blog Example](https://github.com/withastro/astro/tree/latest/examples/blog), a lightweight, minimally-styled starting point for creating a fast and SEO-friendly blog with [Astro](https://astro.build).

It incorporates a few small changes to accommodate [Tina](https://tina.io/), an open-source, Git-backed headless CMS which supports [MDX components](https://mdxjs.com/).

![blog](https://user-images.githubusercontent.com/4677417/186189140-4ef17aac-c3c9-4918-a8c2-ce86ba1bb394.png)

Features:

- ✅ Minimal styling (make it your own!)
- ✅ 100/100 Lighthouse performance
- ✅ SEO-friendly with canonical URLs and OpenGraph data
- ✅ Sitemap & RSS feed support
- ✅ Markdown & MDX support
- ✅ A modern headless CMS for editing rich content

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```
├── public/
├── src/
│   ├── components/
│   ├── content/
│   ├── layouts/
│   └── pages/
├── astro.config.mjs
├── README.md
├── package.json
└── tsconfig.json
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

The `[slug].astro` file is a [dynamic route](https://docs.astro.build/en/core-concepts/routing/#dynamic-routes). This generates a page based on each `*.{md,mdx}` blog post in the `src/content` directory and exposes it on the root (e.g. `localhost:3000/using-mdx`). **This is the content which is managed as a collection in Tina**.

If you require the ability to edit *all* content in Tina (e.g. the About page, or a second collection), this is easy. Simply define [a new collection](https://tina.io/docs/schema/) in `.tina/config.ts`.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

Any static assets, like images, can be placed in the `public/` directory.

## 😎 MDX Components

This template includes one example of an [MDX custom component](https://docs.astro.build/en/guides/integrations-guide/mdx/#custom-components): a simple counter built with Vue 3. This demonstrates how you can add rich interactive components to your markdown content - including components with input parameters - *and* edit them via the CMS!

![blog](/public/mdx-component.png)

Creating new components for use in Tina is easy. First define your component using React, Vue, or any of the [UI frameworks](https://docs.astro.build/en/guides/integrations-guide/) supported by Astro, then `import` it and add it to the `components` prop in the blog post template (`[slug].astro`). Next add it to your Tina schema in `.tina/config.ts` [as a template](https://tina.io/docs/editing/markdown/#defining-a-template-in-a-collection) in your `body` field.

This will make it available to content editors under the 'Embed' menu in Tina CMS.

## ✍️ Tina CMS

Tina offers a fantastic editing experience which includes support for MDX components, setting it apart from many competitors. Thanks to the simple and accessible UI (and the ability to edit without a Git account thanks to [Tina Cloud](https://tina.io/docs/product-tour/#tina-cloud), rich interactivity can be added to pages by non-technical users.

However, because Astro isn't NextJS-based, we do lose the ability to do full contextual editing and to see previews (for the time being...). You can read more about the non-React mode of Tina [in their documentation](https://tina.io/guides/tinacms/non-react-based-ssg/guide/).

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                | Action                                                |
| :--------------------- | :---------------------------------------------------- |
| `npm install`          | Installs dependencies                                 |
| `npm run dev`          | Starts Astro's local dev server at `localhost:3000`   |
| `npm run build`        | Build your production site to `./dist/`               |
| `npm run preview`      | Preview your build locally, before deploying          |
| `npm run astro ...`    | Run CLI commands like `astro add`, `astro check`      |
| `npm run astro --help` | Get help using the Astro CLI                          |
| `npm run tina`         | Initialises Tina at `localhost:3000/admin/index.html` |

## 👀 Want to learn more?

Check out [Astro's documentation](https://docs.astro.build) or jump into their [Discord server](https://astro.build/chat).

To learn more about Tina, the next-gen version of Forestry CMS, check out the [Tina docs](https://tina.io/docs/) or join their [Discord server](https://discord.com/invite/zumN63Ybpf).

If you found this template useful, please consider **submitting a PR**.

## Credit

This theme is based off of the lovely [Bear Blog](https://github.com/HermanMartinus/bearblog/).
