# sith007.github.io

Personal portfolio of **Oudamsith Samin** ("Sith") — computer vision & MLOps engineer.

## Theme

**"Human, Detected"** — the site is framed as the output of a computer-vision pipeline: bounding-box hero with a confidence tag, detection-card projects, and a terminal-log timeline. Near-black navy with amber (racing) and cyan (scanner) accents.

## Stack

- SvelteKit (Svelte 4) + `@sveltejs/adapter-static`
- Vite 5, no runtime dependencies

## Develop

```bash
npm install
npm run dev
```

## Build & deploy

```bash
npm run build      # writes static site to build/
```

Push to `main` → GitHub Actions builds and deploys to https://sith007.github.io/ (Pages source = "GitHub Actions").
