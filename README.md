# cazper website

Static Astro landing page for [cazper](https://cazper.ai).

Primary destination: [cazper](https://app.cazper.ai).

Create and refine an image through a chat, then download one transparent PNG. The alpha comparison is a labelled illustration, not a captured product result.

## Development

Use the Bun version in `.mise.toml`.

```sh
mise install
mise exec -- make install
mise exec -- make check
mise exec -- make dev
mise exec -- bun run preview
```

`make check` installs frozen dependencies, type-checks before building, and verifies the generated HTML and absence of client JavaScript. `make test` checks an existing build. Stop the foreground development server with Ctrl-C; `make clean` removes generated output.

The site is static and ships no client-side JavaScript. Existing CI validates the build and product-specific output contract.
