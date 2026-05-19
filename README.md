# VYRO-VR Documentation

Source for [docs.vyrovr.com](https://docs.vyrovr.com), the official documentation site for VYRO-VR's SlimeVR-compatible IBIS trackers, straps, and accessories.

Built with [Astro](https://astro.build) + [Starlight](https://starlight.astro.build). Content is written in Markdown under `src/content/docs/`.

## Running locally

Requires Node.js 20 or newer.

```sh
npm install
npm run dev
```

The site will be available at `http://localhost:4321`.

## Building

```sh
npm run build
```

Output goes to `dist/`.

## Deployment

Pushes to `main` are built and deployed to GitHub Pages by `.github/workflows/deploy.yml`. The custom domain `docs.vyrovr.com` is configured via `public/CNAME`.

To enable deployment on a fresh repo:

1. Settings → Pages → Source = "GitHub Actions"
2. Settings → Pages → Custom domain = `docs.vyrovr.com`
3. DNS: `CNAME` record `docs` → `<owner>.github.io`

## Contributing

Open a PR against `main`. Every page has an "Edit this page" link in the footer.

## TODO — items needing VYRO input

- Replace `src/assets/logo.svg` placeholder with the real VYRO logo
- Replace `public/og-image.png` placeholder
- Drop product photos into `src/assets/trackers/` and link them from the relevant pages
- Confirm or correct the button-press table on `src/content/docs/trackers/pairing.md` against current shipping firmware
- Fill in premium-strap specifics in `src/content/docs/straps/premium-strap.md`
- Pick a final accent color in `src/styles/custom.css`

## License

Documentation content © VYRO-VR. Site framework MIT.
