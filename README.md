# Position Adjusted Batting Average

An interactive dashboard of hit, whiff and contact rates by pitch location for MLB batters and pitchers, 2023 to 2026 regular seasons. It includes a PAHAE leaderboard, batter and pitcher profiles, best and worst matchups for each batter, and a matchup calculator.

The whole site is one file, `index.html`. All data, charts and code are inside it, so there is no build step and no server.

## Publish it with GitHub Pages

1. Sign in at github.com and create a new repository. Use a public repository unless your plan includes Pages for private repositories.
2. On the repository page, choose **Add file**, then **Upload files**, and drag in `index.html`, `.nojekyll` and `README.md`. Commit the upload to the `main` branch.
3. Open **Settings**, then **Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, pick the `main` branch and the `/ (root)` folder, and save.
4. Wait a minute or two. The site appears at `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`, and the Pages settings screen shows the exact address.

The page uses no absolute links, so it works the same at a repository address and at a custom domain. `.nojekyll` is optional for a single-page site. It only tells GitHub not to run its Jekyll processor.

## How the numbers are made

- Every swing is placed in one of 13 locations from the catcher's view: Statcast zones 1 to 9 inside the strike zone, and 11 to 14 for the four regions outside it.
- Hit rate is hits divided by swings. Whiff rate is swings and misses divided by swings. Contact rate is fouls plus balls in play, divided by swings.
- PAHAE is a batter's hits minus the hits expected at the league hit rate in each location he swung at.
- Matchup expected hit rate is the sum, over the 13 locations, of the pitcher's share of swings there times the batter's hit rate there. Where a batter has fewer swings than the slider minimum, the league rate is used.
- Left out: postseason games, bunts, and pitches without a tracked location. Batters need 100 swings and pitchers 300 pitches to be listed.

## Data

MLB Statcast pitch data from Baseball Savant, pulled with the pybaseball Python package. The page is a snapshot and does not update on its own. Before publishing it on a public site, check Baseball Savant's and MLB's terms of use for how this data may be shared.
