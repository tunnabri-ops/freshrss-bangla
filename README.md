# 📰 FreshRSS Bangla

**Your own Bangla news reader — 5 live-checked feeds, self-hosted, Dhaka timezone.**

## ✨ Features

- `bangla-feeds.opml` — 5 Bangla/world news feeds, ready to import: Prothom Alo, BBC Bangla, The Daily Star, Al Jazeera, BBC News.
- `docker-compose.yml` — runs on http://localhost:8080, timezone Asia/Dhaka, auto-refresh twice an hour.

## 🚀 How to use

```bash
docker compose up -d
```

Open http://localhost:8080, finish the setup wizard, then Subscription management → Import → choose `bangla-feeds.opml`.

## ⚠️ Honest limits

- Every feed in the OPML was live-checked (each returned HTTP 200 + real RSS XML). Feeds that failed the check are **not** included as working feeds — Jugantor, Somoy TV, Jamuna TV and Kaler Kantho returned Cloudflare 403 from here; Dhaka Tribune and NTV returned 404; bdnews24's `/rss` path returned an HTML page, not a feed. They are noted as unverified in the OPML comments.
- A feed can still go offline later — if one stops updating, remove it and check the site for a new feed address.

## 🇧🇩 বাংলা

**ফ্রেশআরএসএস বাংলা — নিজের বাংলা নিউজ রিডার।**

- ৫টা যাচাই করা ফিড এক ক্লিকে ইম্পোর্ট করা যায় (OPML ফাইল)
- ডকার দিয়ে এক কমান্ডে চালু হয় — http://localhost:8080
- ঢাকা টাইমজোনে চলে, আধা ঘণ্টায় দুইবার নিজে নিজে খবর টানে

## 📄 License

MIT — use it however you like.
