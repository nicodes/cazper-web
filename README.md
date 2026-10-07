# cazper website

Static Astro landing page for [cazper](https://cazper.ai).

Primary destination: [cazper](https://app.cazper.ai).

Create and refine an image through a chat, then download one transparent PNG. The alpha comparison is a labelled illustration, not a captured product result.

## Development

Use the Bun version in `.mise.toml`.

```sh
bun install --frozen-lockfile
bun run dev
bun run build
bun run preview
```

Run `bun run typecheck` before building.

The site is static and ships no client-side JavaScript. Existing CI validates the build and product-specific output contract.
