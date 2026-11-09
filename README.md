## How the numbers are made

- Every swing is placed in one of 13 locations from the catcher's view: Statcast zones 1 to 9 inside the strike zone, and 11 to 14 for the four regions outside it.
- Hit rate is hits divided by swings. Whiff rate is swings and misses divided by swings. Contact rate is fouls plus balls in play, divided by swings.
- PAHAE is a batter's hits minus the hits expected at the league hit rate in each location he swung at.
- Matchup expected hit rate is the sum, over the 13 locations, of the pitcher's share of swings there times the batter's hit rate there. Where a batter has fewer swings than the slider minimum, the league rate is used.
- Left out: postseason games, bunts, and pitches without a tracked location. Batters need 100 swings and pitchers 300 pitches to be listed.

## Data

MLB Statcast pitch data from Baseball Savant, pulled with the pybaseball Python package. The page is a snapshot and does not update on its own. Before publishing it on a public site, check Baseball Savant's and MLB's terms of use for how this data may be shared.
