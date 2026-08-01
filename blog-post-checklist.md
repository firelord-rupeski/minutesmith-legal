# Per-post metadata checklist

Run through this every time a new blog post goes live. The site is hand-maintained flat HTML (no Jekyll), so nothing here is generated automatically — every step is a manual edit and a manual chance to drift out of sync.

The recurring bug so far: the canonical/OG URL, the sitemap `loc`, the feed `link`, and the syndicated copy's canonical setting all need to be the *exact same string* (including the `.html` suffix), and they keep getting out of sync because they're set in four different places by hand.

**One rule that prevents most of this: decide the live URL first, then paste that exact string into every field below. Never retype it.**

## 1. New post file (`blog/<slug>.html`)

- [ ] `<title>` — post title, ends with `— Minutesmith Blog`
- [ ] `<meta name="description">` — 1-2 sentence summary
- [ ] `<link rel="canonical" href="...">` — full URL, must match the file's actual live path exactly (e.g. `https://minutesmith.dev/blog/<slug>.html`, not a pretty/trailing-slash URL)
- [ ] `<meta property="og:title">`
- [ ] `<meta property="og:description">`
- [ ] `<meta property="og:image">` + `og:image:width` (1200) + `og:image:height` (630) + `og:image:alt`
- [ ] `<meta property="og:url">` — same exact string as the canonical link above
- [ ] `<meta property="og:type" content="article">`
- [ ] `<meta property="og:site_name" content="Minutesmith">`
- [ ] `twitter:card`, `twitter:title`, `twitter:description`, `twitter:image`, `twitter:image:alt`

## 2. `feed.xml`

- [ ] New `<item>` added inside `<channel>`
- [ ] `<link>` and `<guid isPermaLink="true">` both equal the canonical URL from step 1, exactly
- [ ] `<pubDate>` in RFC-822 format (e.g. `Thu, 30 Jul 2026 09:00:00 -0700`)
- [ ] `<description>` matches (or closely mirrors) the meta description

## 3. `sitemap.xml`

- [ ] New `<url>` block added
- [ ] `<loc>` equals the canonical URL from step 1, exactly
- [ ] `<lastmod>` set to the actual publish date, not left blank or copy-pasted from another entry
- [ ] `<changefreq>` and `<priority>` set deliberately (don't just copy the previous post's values without thinking about whether this post should be weighted the same)

## 4. Blog index (`blog/index.html`)

- [ ] New post added to the listing with correct relative link and date

## 5. Footer / nav (if the post introduces a new nav-level link)

- [ ] Site footer is **not templated** — it's duplicated across all 6 HTML files (`index.html`, `features.html`, `support.html`, `privacy.html`, `blog/index.html`, `blog/<slug>.html`). Any nav-level addition needs to be pasted into all six, not just one.

## 6. Syndication (Medium, Indie Hackers, etc.)

- [ ] Canonical URL field on the syndicated copy is set to the exact live URL from step 1 — not a permalink guessed from an old scaffold, not a pretty URL that doesn't actually resolve

## 7. Final check

- [ ] Open the canonical URL, the `og:url` value, the `sitemap.xml` `loc`, and the `feed.xml` `link`/`guid` side by side and confirm all four are character-for-character identical
- [ ] View-source the live page (not just the local file) to confirm the deployed version matches
