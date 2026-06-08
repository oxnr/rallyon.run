# RALLY Pages Deploy

This repository is the public GitHub Pages deploy target for RALLY:

https://rallyon.run

The canonical source app and data live in:

https://github.com/oxnr/Rally

This repo is intentionally boring: it contains the built static site, the generated assets under `_astro/`, the favicon, and the `CNAME` file for `rallyon.run`.

## What This Site Contains

The current deployed build contains:

- 2,022 travel-worthy competitions and participatory events
- 40 standardized fitness and athletic tests
- 63 sport/category labels

The event catalog is static. It does not need realtime infrastructure; it is meant to be refreshed occasionally from the source repo as the research catalog improves.

## Data Provenance

RALLY's event and test data is curated in the source repo, then compiled into the static site. Each event record has a `sourceName` and `sourceUrl`, and each test record has the same provenance fields.

The catalog is built from official or close-to-official sources, including:

- official race and event pages
- federation and series calendars
- registration platforms
- published benchmark/test protocols
- manually researched long-tail competition pages

Current source families include AIMS, HYROX, Competition Corner, Spartan and DEKA, IRONMAN, Challenge Family, XTERRA, UCI, UCI Gran Fondo, UCI Gravel, Worldloppet, Ski Classics, ITF, GLTA, PPA Tour, UTMB, Ultra X, Oceanman, World Masters Games, and local functional-fitness or WOD competition pages.

The source repo also has a periodic research helper:

```bash
npm run validate -- --research
```

That generates source-coverage reports and query packs for finding more events, including long-tail competitions like local throwdowns, HYROX simulations, WOD events, road races, cycling sportives, rowing regattas, and triathlons.

## Deployment Notes

- GitHub Pages source: `main` branch, repository root
- Custom domain: `rallyon.run`
- `www.rallyon.run` redirects to `rallyon.run`
- HTTPS is enforced by GitHub Pages

To update this repo, build the source app, copy the source repo's `dist/` output here, then commit and push the generated files.
