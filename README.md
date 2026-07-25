# Prism

**Every story, in full spectrum.**

Prism is a genre-balanced reading and writing app — a place to discover and
write stories across *any* genre, with a feed designed so no single genre
crowds out the rest.

🔗 **Live app:** https://sugandhamvishwak-alt.github.io/Prism/

---

## What Prism does

- **Home** — a feed built by interleaving stories across your selected
  genres, so crime, fantasy, romance, sci-fi, and everything else all get
  fair shelf space
- **Search** — find stories by title, genre, or status, with filters and
  sorting
- **Write** — create a book, design its cover, and write chapters part by
  part, publish-as-you-go, just like a traditional serial fiction platform
- **Follow & Notifications** — follow writers you like and get notified when
  they publish
- **Sign in** with Google (X/Twitter coming soon)

## Tech stack

- Plain HTML, CSS, and JavaScript — no build step, no framework
- [Supabase](https://supabase.com) for auth, the database, and row-level
  security
- Installable as a Progressive Web App (PWA) — add it to your home screen
  from the browser and it opens full-screen like a native app
- Hosted on GitHub Pages

## Project structure

```
index.html        the entire app (UI + logic)
manifest.json      PWA manifest — app name, icons, theme color
sw.js              service worker — caches the app shell for offline use
icons/             app icons used by the manifest
schema.sql         Supabase database schema (tables + row-level security)
```

## Running your own copy

1. Fork or clone this repo
2. Create a [Supabase](https://supabase.com) project
3. Run `schema.sql` in the Supabase SQL editor to set up the database
4. Enable the login providers you want under Supabase → Authentication →
   Providers
5. Paste your Supabase project URL and anon key into the `SUPABASE_URL` and
   `SUPABASE_ANON_KEY` constants near the top of `index.html`
6. Enable GitHub Pages on the repo (Settings → Pages → deploy from the
   `main` branch, root folder)

## Status

Actively in progress — genres, the write flow, and Google sign-in are live.
