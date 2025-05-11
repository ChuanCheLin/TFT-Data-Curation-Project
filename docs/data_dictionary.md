# Data Dictionary

| Column | Type | Description |
| --- | --- | --- |
| match_id | object | Unique ID for each TFT match |
| game_time | object | UTC timestamp when the game started |
| patch | float64 | TFT patch major.minor (e.g., 15.7) |
| queue_id | int64 | Riot queue identifier (e.g., 1100 for ranked) |
| puuid | object | Player Universally Unique Identifier |
| placement | int64 | Final placement (1 = first place, 8 = last place) |
| level | int64 | Player level at end of game |
| gold_left | int64 | Gold remaining at the end of game |
| status | object | 'ok', 'missing', or 'invalid' after QC |
| traits | object | Comma-separated list of trait-tier pairs (e.g., OxForce-2) |
| units | object | Comma-separated list of unit-star pairs (e.g., Ahri-3) |
