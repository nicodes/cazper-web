# clearimg-web

The splash page at [clearimg.ai](https://clearimg.ai). One static page.

```sh
mise install
bun install
bun run dev      # http://localhost:4321
bun run build    # -> dist/
```

## What is here

```
src/layouts/Full.astro   <head>, meta, structured data
src/pages/index.astro    the page, and its styles
src/styles/global.css    palette, fonts, resets
```

Plain Astro with scoped CSS. No component framework and no CSS framework: this
is one page with no interactivity, and the scaffold's Qwik and Tailwind were a
runtime and a build step to produce markup that is written out directly.
Removing them is why the built page ships **no JavaScript at all**, which CI
checks rather than trusts.

## The hero is a render, not a screenshot

The two panes are one `<symbol>` `<use>`d twice, so the artwork is identical
across them and only the background differs — which is the whole claim the page
makes. The glass on the potion, the near facet of the gem and the hole in the
key's bow are genuinely semi-transparent, so the checkerboard shows through
exactly where it should and nowhere else.

A screenshot would have been the one part of this page able to quietly stop
being true.

The page describes what goes in and what comes back, and stops there. How the
alpha is recovered is not the site's to explain — keep it that way when editing.
Note that Astro emits `<!-- -->` comments into the built HTML and drops `{/* */}`
ones, so implementation notes in `index.astro` belong in the latter.

## The palette is the app's

`#059669` and `#34D399` are the accents the clearimg app uses on light and dark
backgrounds — the exact tokens from its theme. The site wears what the product
wears rather than inventing a brand alongside it.

## Related

- [app.clearimg.ai](https://app.clearimg.ai) — the application every call to action points at
- `clearimg-be` — the API, the app, and the CLI (private)
