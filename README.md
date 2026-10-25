# zero.in / guiGoog (2009) — restored demo

**Live demo: https://citizenziggy2022.github.io/zero-in-demo/**

guiGoog ("Advanced Visual Power Search"), later zero.in, was a point-and-click GUI for Google advanced search, built in 2009. You typed a normal query, clicked icons, sliders and toggles, and the app silently built the operator string (`daterange:`, `site:` / `-site:`, `filetype:`, `OR`, region and language) and ran it through Google.

This is the classic zero.in UI (v1.3.6, "classic guiGoog — where we began"), restored from Wayback Machine captures and patched just enough to run in a 2026 browser.

## What works
- The original look and every filter: date range slider, From/To pickers and presets (past year / 6 months / month / week / today), the 23 website toggles (include-only or exclude) plus custom sites, file types plus custom extensions, region, city/zip, language, results per page, saved profiles and the nuke reset.
- The query guiGoog builds is shown live under the controls as you type and click.
- **Search Google** (or Enter) opens that exact query on google.com in a new tab. The date range also goes along as Google's own date filter (`tbs=cdr`), since today's Google largely ignores the 2009 `daterange:` operator (Julian day numbers).
- The suggestion cloud ("click a word once to add it, twice to exclude it") gets live suggestions from Google's public suggest endpoint (JSONP). If that endpoint can't be reached it falls back to a small built-in word list.
- `index.html?q=your+words` pre-fills the search box.

## What was changed from the 2009 files
- Results: the Google Custom Search / AdSense-for-Search iframe is gone (that API no longer exists), so results open on google.com instead.
- Removed dead scripts: Google CSE branding, AdSense for Search, Google Analytics, AddThis.
- Fixed three time bombs: the app's cookies were hard-coded to expire on 1 Jan 2024 (so filters and profiles couldn't be saved), the Julian-date math broke when browsers added `Math.sign`, and a corrupted line in the `?q=` handler.
- The site favicons and file-type icons were never archived; they're re-created (site favicons fetched fresh, file-type icons drawn).
- A banner marks it as a restored demo.

The full recovered archive (all versions, the mobile app, the rebuild spec) is kept separately.
