# AI Safety Opportunity Map

An interactive world map of AI safety opportunities: fellowships, coworking spaces, research organisations and communities, placed at their cities. Click a country to see where it ranks on provision, which topics it over-indexes on, and a treemap of what its organisations work on. Hatched countries were searched and nothing was found.

The site is a single static HTML file with the data embedded. There is no build step and no dependencies; fonts load from Google Fonts.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
# or
python3 -m http.server 8000
```

## Deploy on Vercel

1. Push this folder to a GitHub repository.
2. In Vercel, choose **Add New → Project** and import the repository.
3. Leave the settings as detected: Framework Preset **Other**, no build command, output directory = the repository root.
4. Deploy. Every push to the default branch redeploys automatically.

`vercel.json` enables clean URLs and adds a few standard security headers.

## Updating the data

The dataset lives inline in `index.html` (the `D={...}` object inside the `<script>` block). The header stamp (entry, country and searched-zero counts, and the update date) and the note at the bottom of the page are written by hand, so update them whenever the data changes. The **Download data** button exports the current dataset as CSV.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: markup, styles, script and data |
| `favicon.svg` | Browser tab icon |
| `vercel.json` | Vercel config (clean URLs, headers) |
