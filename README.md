# cusescrapeR

An R package for accessing Syracuse Men's Basketball data.

## Installation

```r
# install.packages("devtools")
devtools::install_github("jameson-bodenburg/cusescrapeR")
```

## Usage

```r
library(cusescrapeR)

# Connect with your credentials
connect(username = "your_username", password = "your_password")

# See what dates are available
list_dates("pbp_daily")

# Read play-by-play data for a date range
pbp <- read_daily("pbp_daily", start_date = "2026-02-01", end_date = "2026-02-28")

# Read box scores for a single date
box <- read_daily("players_box_daily", start_date = "2026-02-14", end_date = "2026-02-14")

# Read all game info
games <- read_daily("game_info_daily")

# Read stint data
stints <- read_daily("stints_daily", start_date = "2026-01-01")

# Read roster and team reference data
rosters <- read_rosters()
teams <- read_teams()
```

## Available Datasets

| Function | Dataset | Description |
|---|---|---|
| `read_daily("game_info_daily")` | Game Info | Scores, spreads, venue, referees, TV |
| `read_daily("pbp_daily")` | Play-by-Play | Every play with lineups and scores |
| `read_daily("players_box_daily")` | Box Scores | Player stats per game |
| `read_daily("stints_daily")` | Stints | Lineup stint data |
| `read_rosters()` | Rosters | ESPN roster for 2025-26 season |
| `read_teams()` | Teams | ESPN team info for 2025-26 season |

## Need credentials?

Contact Jameson Bodenburg (jgbodenb@syr.edu).
