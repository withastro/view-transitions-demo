# View-Transitions-Demo

## Usage

Clone this repo, `npm i`, then `npm run dev`.  Or try the live demo:

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/withastro/view-transitions-demo)

## View Transitions Information:

This repo shows examples of [View Transitions](https://docs.astro.build/en/guides/view-transitions/) in [Astro](https://astro.build/), most dramatically between the blog index & individual blog posts.

The following codes enable VTs; note the `transition:name`:

`src/components/BaseHead.astro`:
```jsx
import { ViewTransitions } from 'astro:transitions';
...
<ViewTransitions />
```

`src/layouts/BlogPost.astro`:
```jsx
<html lang="en" transition:name="root" transition:animate="slide">
...
{heroImage && <img width={720} height={360} src={heroImage} alt="" transition:name={slug} />}
```

`src/pages/blog/index.astro`:
```jsx
<html lang="en" transition:name="root" transition:animate="slide">
...
<img src={post.data.heroImage} alt={post.data.title} transition:name={post.slug} />
```

`src/pages/index.astro`:
```jsx
<html lang="en" transition:name="root" transition:animate="slide">
```

![blog](https://user-images.githubusercontent.com/4677417/186189140-4ef17aac-c3c9-4918-a8c2-ce86ba1bb394.png)

Other Features:

- ✅ Minimal styling (make it your own!)
- ✅ 100/100 Lighthouse performance
- ✅ SEO-friendly with canonical URLs and OpenGraph data
- ✅ Sitemap support
- ✅ RSS Feed support
- ✅ Markdown & MDX support

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```
├── public/
├── src/
│   ├── components/
│   ├── content/
│   ├── layouts/
│   └── pages/
├── astro.config.mjs
├── README.md
├── package.json
└── tsconfig.json
```


Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

The `src/content/` directory contains "collections" of related Markdown and MDX documents. Use `getCollection()` to retrieve posts from `src/content/blog/`, and type-check your frontmatter using an optional schema. See [Astro's Content Collections docs](https://docs.astro.build/en/guides/content-collections/) to learn more.

Any static assets, like images, can be placed in the `public/` directory.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:3000`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Check out [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).

## Credit

This theme is based off of the lovely [Bear Blog](https://github.com/HermanMartinus/bearblog/).
