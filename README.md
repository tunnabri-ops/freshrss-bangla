# FreshRSS Bangla — বাংলায় নিজের নিউজ রিডার

Bangla news reader setup, built on **FreshRSS/FreshRSS**.

- **Original repo:** https://github.com/FreshRSS/FreshRSS (a free, self-hostable news aggregator)

## কী আছে / What is inside

- `bangla-feeds.opml` — 5 Bangla/world news feeds, ready to import.
- `docker-compose.yml` — runs FreshRSS on http://localhost:8080 (image `freshrss/freshrss:latest`, verified on Docker Hub, 41M+ pulls; timezone Asia/Dhaka).

## যা ঠিক করা হয়েছে / What was fixed

- Upstream ships with no feeds — a fresh install is empty. This adds a ready OPML of **live-verified** feeds (checked 2026-11-23, each returned HTTP 200 + real RSS XML): Prothom Alo, BBC Bangla, The Daily Star, Al Jazeera, BBC News.
- **Dropped, not faked:** Jugantor, Somoy TV, Jamuna TV and Kaler Kantho returned Cloudflare 403 from here; Dhaka Tribune and NTV returned 404; bdnews24's `/rss` path returned an HTML page, not a feed. They are listed in the OPML comments as unverified — not included as working feeds.

## ব্যবহার / How to use

```bash
docker compose up -d
```

Open http://localhost:8080, finish the setup wizard, then Subscription management → Import → choose `bangla-feeds.opml`.
