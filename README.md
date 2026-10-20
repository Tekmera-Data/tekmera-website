# Tekmera website

Company site for tekmeradata.ai, built with [Astro](https://astro.build) and deployed on Netlify.

## Run locally

```bash
npm install
npm run dev        # http://localhost:4321
```

## Build

```bash
npm run build      # outputs static site to dist/
npm run preview    # serve the build locally
```

## Structure

```
src/
  layouts/Base.astro        # <head>, page wrapper, header + footer
  components/               # one file per homepage section
    Header.astro  Hero.astro  Services.astro  Industries.astro
    HowWeWork.astro  Affordia.astro  Contact.astro  Footer.astro
  pages/
    index.astro             # homepage (composes the sections)
    privacy.astro           # privacy policy
    success.astro           # contact form thank-you page
  styles/global.css
public/favicon.svg
netlify.toml                # build settings + redirects
```

## Adding a page

Create `src/pages/<name>.astro`, wrap content in `<Base title="...">`, and it is served at `/<name>`.

## Contact form

The form uses Netlify Forms (`data-netlify="true"`). Submissions appear in Netlify under **Forms**; set up email notifications there.
