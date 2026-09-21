# politiquech.ch — redirect to politikch.ch

This repository exists only to serve `politiquech.ch` over **HTTPS** and forward it to
the main site in fr (`https://politikch.ch/?lang=fr`).

Hostpoint's registrar-level redirect service only answers on plain HTTP, so
browsers that try HTTPS first got a connection error. GitHub Pages issues a real
certificate for the custom domain, which fixes that.

- `index.html` / `404.html` — the forwarding page (meta refresh + JS, so any
  deep link's `#/…` fragment is preserved). Identical, so every path forwards.
- `CNAME` — the custom domain for GitHub Pages.
- `robots.txt` — keeps the redirect out of search results; `index.html` also
  carries `noindex` and a canonical link to politikch.ch.

The site itself lives in the `politikch` repository.
