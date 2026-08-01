# Minutesmith Marketing Campaign, Summary
**As of end of day, Friday July 31, 2026 (Week 1, Day 4 of an 8-week organic campaign)**

This file summarizes everything decided, built, and still open across this conversation, so a new session can pick up without re-deriving context.

---

## Product and campaign basics

- **Product:** Minutesmith, a Mac app (Apple silicon, macOS 12+) that records, transcribes, and summarizes meetings and lectures entirely on-device. No account, no cloud, no server. Optional bring-your-own-key for OpenAI/Anthropic/Ollama if the user wants a cloud model for summaries.
- **Positioning:** privacy by architecture, not policy, "we don't have a server to leak."
- **Target segments:** students, freelancers/consultants, people on too many calls.
- **Site:** minutesmith.dev, migrated from ghostlymage.com. Plain static HTML (not Jekyll, decision confirmed today, see below). Hosted on GitHub Pages.
- **Local repo path:** /Users/rupertyip/development/minutesmith-legal (Claude has no filesystem access to this, all files are handed off via download).
- **Launch pricing:** 50% off through Oct 31, 2026. Windows version in progress (not yet launched).
- **Campaign goal:** drive Mac App Store downloads, organic-only budget, 8 weeks, Jul 28 to Sep 21, 2026.
- **Rupert's background/voice:** parent, founding product manager in Silicon Valley, personal narrative angle is "missed the important part in college lectures, still missing it in VC/customer meetings now."

---

## Master tracking file

**minutesmith-campaign-tracker.xlsx** is the single source of truth. Tabs, in order:

1. **Schedule** — full 8-week, 38-item dated schedule with status/notes columns, progress counter
2. **Site Setup** — 11 dated infrastructure tasks (canonical fix, blog standup, plugins, Search Console, etc.)
3. **Gantt** — visual timeline, 5 swimlanes (Site and infra, Account setup, Content production, Publishing, Outreach, Ongoing), static color-painted bars (conditional formatting didn't render reliably, so bars are hard-coded)
4. **Account Setup** — per-platform tracker with deadlines derived from Schedule, days-left countdown, risk flags
5. **Content Library** — all drafted copy, C-01 through C-17 (see below)
6. **Outreach Targets** — blank tracker for press/newsletter contacts, not yet populated
7. **Metrics** — weekly download/traffic log, Week 0 baseline row, first real entry due Mon Aug 3

Separate standalone files also delivered: **minutesmith-week-1-checklist.md** (daily breakdown) and **minutesmith-week-1-status-check.md** (EOD Jul 31 status confirmation). A **minutesmith-blog-scaffold.zip** was also built (Jekyll-based) but is now superseded, see Site Setup decision below.

---

## Content Library contents (C-01 to C-17)

- C-01: Cornerstone blog post outline
- C-02: X/LinkedIn announcement posts (two versions, link handling differs per platform, see below)
- C-03/C-04/C-05: Founder story set (X thread, LinkedIn, Indie Hackers outline)
- C-06: Product Hunt listing + maker comment
- C-07/C-08: Reddit self-promo posts (r/macapps, r/privacy) — **MOVED**, see below
- C-09/C-10: Press pitch and creator/newsletter outreach templates
- C-11/C-12: Non-promotional discussion starters, technical audience (r/privacy, r/macapps)
- C-13/C-14/C-15: Non-promotional discussion starters, lay audience (students/r-college, freelancers/r-freelance, general/r-productivity)
- C-16: Medium syndication of cornerstone post — **published**, see status below
- C-17: Indie Hackers syndication of cornerstone post — **on hold**, see status below

---

## Key decisions and standing rules

- **LinkedIn:** post as yourself, not a brand page. Do NOT put the link in the first comment (outdated, now flagged as "bridge behavior" and penalized). Instead: write posts that stand alone, DM the link to anyone who asks. Company Page exists only for credibility, never post from it.
- **X:** link can go directly in the post body, this is fine on X unlike LinkedIn.
- **YouTube:** use a Brand Account channel (not personal), under the existing Gmail. Handle target: @minutesmith.
- **Reddit and Hacker News:** both gate posting behind account age/karma. Accounts created Jul 28. Karma-building window running now through Aug 24 (Reddit) and Aug 27 (HN). The two promotional Reddit posts (C-07 r/macapps, C-08 r/privacy) were **moved from Aug 7/Aug 10 to Aug 25/Sep 1** to allow for account aging.
- **Indie Hackers:** discovered Jul 31 to have its own gate, new accounts cannot post until moderators grant "special privileges" based on genuine comments, or by paying for Indie Hackers Plus. Account created Jul 31, currently gated. C-17 is drafted and ready but on hold.
- **Medium:** account created (@rupertyip), bio set with minutesmith.dev link. Cornerstone post (C-16) **published**, cover image added, 5 topics tagged (Privacy, Productivity, AI, Startup, Mac).
- **Blog hosting decision (Jul 31):** confirmed the site is plain static HTML, not Jekyll. Decided NOT to migrate to Jekyll this close to Product Hunt launch (Aug 6). Instead: hand-maintain flat `.html` files per post, hand-maintain `feed.xml` and `sitemap.xml` per post. Per-post metadata checklist written, see `blog-post-checklist.md` in the repo.
- **Live URL convention (Jul 31):** GitHub Pages serves flat files with no server-side rewriting, so URLs must match what's actually on disk.
  - Directory-style pages (homepage, blog index) use the clean trailing-slash form: `https://minutesmith.dev/`, `https://minutesmith.dev/blog/`.
  - Individual content pages (features, support, privacy, every blog post) keep the explicit `.html`: `https://minutesmith.dev/features.html`, `https://minutesmith.dev/blog/<slug>.html`.
  - This is the canonical URL to paste everywhere for a given page (canonical tag, og:url, sitemap.xml loc, feed.xml link/guid, syndication canonical) per `blog-post-checklist.md`. All future URL references (new pages, new posts, outreach copy, syndication) should follow this convention.

---

## Bugs found and fixed this week

1. **Canonical/OG tags on minutesmith.dev pointed to ghostlymage.com** after the domain migration. Found and fixed Jul 28, verified corrected Jul 31.
2. **ghostlymage.com status** — confirmed by Rupert on Jul 31 to now be inactive (not redirecting). Accepted as-is given zero budget; old inbound links/bookmarks now dead-end. Revisit only if a free/cheap Cloudflare redirect becomes easy later.
3. **Medium canonical URL mismatch** — found Jul 31. Medium's canonical was set to the pretty URL `.../why-your-meeting-notes-app-can-read-your-meetings/` (from the now-abandoned Jekyll scaffold's permalink setting), but the actual live post is at `.../why-your-meeting-notes-app-can-read-your-meetings.html`. **Fixed Jul 31** — corrected in Medium Story Settings > Advanced Settings.

---

## Confirmed done (as of Jul 31 EOD)

- X, Reddit, Hacker News, Medium, Indie Hackers accounts all created
- X: bio, photo, link (minutesmith.dev) set
- Medium: bio, website link set; cornerstone post published with cover image, topics, and a corrected canonical link (URL-mismatch fix confirmed)
- Canonical/OG tags fixed on minutesmith.dev
- `/blog/` stood up and live, confirmed matches drafted content
- Cornerstone post live at minutesmith.dev/blog/why-your-meeting-notes-app-can-read-your-meetings.html
- ghostlymage.com situation resolved (confirmed inactive)
- One non-promotional discussion post published (r/GetStudying, based on C-13)
- feed.xml and sitemap.xml committed and pushed to the repo (commit fb51dd3)
- RSS feed linked from site footer on all pages (commit 443f7a4)
- Per-post metadata checklist written (blog-post-checklist.md); feed.xml channel link also reconciled to match sitemap.xml's clean /blog/ URL form
- X and LinkedIn announcement posts (C-02) published Jul 31. Final copy: no pricing mention (founder voice, architecture-first framing), no link in the LinkedIn post or its first comment (link goes out via DM to commenters instead), X post links directly to minutesmith.dev/blog/why-your-meeting-notes-app-can-read-your-meetings.html (own site, not Medium, since Medium's canonical already points back to it)
- App Store Connect marketing/support URL confirmed pointing to minutesmith.dev
- Google Search Console: minutesmith.dev verified via HTML tag method (meta tag committed and pushed, commit a11ea8d), sitemap.xml submitted
- LinkedIn profile refresh (headline/About/Featured) done
- Bluesky account created
- "Windows coming soon" pill added next to every Download for Mac / Download on the Mac App Store button sitewide (nav on all 6 pages, homepage hero and bottom CTA, features intro and bottom CTA, blog post CTA). Styled to match the Mac button (same font, weight, shape) but in Windows blue (#0078d4 → #005a9e gradient) instead of the site's orange. Replaces the earlier buried fineprint mention, which was judged too easy to miss for Windows-curious visitors. Committed and pushed (commit 6d6e718)

- Founder story drafts (C-03 X thread, C-04 LinkedIn, C-05 Indie Hackers) finalized with real specifics (build timeline, LLM benchmarking, Apple notarization, motivation) and written into the xlsx Content Library tab. Scheduled per Schedule tab: C-03 and C-04 post same day, Tue Aug 4; C-05 posts Wed Aug 5 but is blocked on the same Indie Hackers gating as C-17
- Mastodon account — deliberately skipped (Rupert's decision, Jul 31)
- Product Hunt maker profile and launch assets (gallery images, demo video) — not started, due before Aug 6 launch
- YouTube Brand Account — not yet created
- Skip-tier handles (Facebook, Threads, Pinterest) — not yet claimed
- Weekly metrics logging — first entry due Mon Aug 3
- Reddit/HN daily genuine commenting to build karma/age toward Aug 24-27
- Indie Hackers genuine commenting toward unlocking posting privileges
- Search a social card re-scrape (LinkedIn Post Inspector, X validator) on the blog URL

---

## Standing style/process notes for future sessions

- No em-dashes in any copy or written output (user preference).
- Claude does not have local filesystem access; all files are handed off via chat download, Rupert copies them into his local repo himself.
- Claude does not post directly to social platforms; navigates Chrome to the right composer/page, drafts the copy, and Rupert reviews and submits manually. This is deliberate for Reddit/HN specifically, since manual pacing is part of what keeps new-account posting from looking automated.
- When something is uncertain (e.g. whether Jekyll plugins are active), Claude checks directly rather than assuming, and clearly separates "confirmed" from "needs verification" in the tracker.
