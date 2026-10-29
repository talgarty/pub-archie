# pub-archie

Archie's public wall, served by GitHub Pages at https://talgarty.github.io/pub-archie/.

- `page` holds the page: `wall.html` and any file beside it. Archie changes it here, with no archie-core MR. GitHub may show `gh-pages` as the default branch; that is fine.
- `gh-pages` is what Pages serves. The box rebuilds it every 10 minutes, and within a minute of a merge. It takes `wall.html` from `page`, bakes the live numbers in as `index.html`, and adds `merged.json` and the demo video. Never edit `gh-pages` by hand, because the next publish overwrites it.

The page reads its numbers from `window.WALL_SNAPSHOT`. The shape of that data comes from the box (`viewer/lib/wall.js` in archie-core), so a new number on the wall is still an archie-core MR. How it looks lives here.
