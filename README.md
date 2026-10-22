# Reddit User Viewer

A single-page tool to see a Reddit user's posts and comments without using `site:reddit.com u/username` on Google.

## Use

1. Open `index.html` in a browser (or the GitHub Pages URL, once enabled).
2. Enter a username (`spez`, `u/spez` or a full profile URL all work).
3. Switch between **All**, **Posts** and **Comments**, filter by subreddit or text, and use **Load more** for older history.
4. Tap **Stats** for most active communities, approximate topic categories, time-of-day, day-of-week and monthly activity, and highest-scoring items. Stats cover the items loaded so far; **Load full history** fetches up to 1,000 items from Reddit (3,000 from the archive).
5. **Home** (or the page title) clears everything for a new search.

Typing `r/name` in the filter shows only that community.

Bookmark `index.html?u=username` to open someone directly.

## Data sources

| Source | What it gives | Limits |
| --- | --- | --- |
| Reddit (live) | Current posts and comments, karma, join date | Reddit rate-limits or blocks some anonymous requests; returns nothing if the user hides their profile history |
| [Arctic Shift](https://arctic-shift.photon-reddit.com) (archive) | Historical posts and comments, including for hidden profiles | Can lag behind live Reddit; deleted or removed content may be missing |

**Auto** (the default) tries Reddit first and falls back to the archive if Reddit fails or returns nothing.

## Hosting on GitHub Pages

Repository **Settings → Pages → Build and deployment → Deploy from a branch**, select `main` and `/ (root)`. The page is static, with no server, keys or build step.
