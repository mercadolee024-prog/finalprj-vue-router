# FIN-LAB-1 VueJS Routing

Five-view gelato and macaron business Vue 3 SPA by Justin Lee B. Mercado (WD-301).

## Local setup

Use Node.js 24 LTS. Run `npm install`, then `npm run dev`. Run `npm run build` for production output in `dist/` and `npm run preview` to test it locally.

## Deploy

Import this repository into Vercel or Netlify. Use the Vite framework preset, build command `npm run build`, and output directory `dist`. `vercel.json` and `public/_redirects` / `netlify.toml` include SPA fallbacks for direct route requests.

The contact form is a local validation demonstration and does not send data.

## Apache subdirectory alternative

For `/vuejs-routing/` on Apache, change `base` in `vite.config.js` to `/vuejs-routing/`, rebuild, and upload `dist/` to `public_html/vuejs-routing/`. The router already reads `import.meta.env.BASE_URL`. Place the provided `.htaccess` inside that folder. Do not use the subdirectory base for a Vercel or Netlify root deployment.

Older Vue CLI templates may depend on `spdy` / `http-deceiver` code that accesses Node's removed `http_parser`. This Vite project avoids those legacy dependencies.
