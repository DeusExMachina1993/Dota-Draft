# DOTA-Draft 2022 — statistics

Schema v2.1 · Kaggle periods: 2022

| Metric | Value |
|---|---|
| Matches | 20,875 |
| Team drafts (RecBole users) | 41,750 |
| Interactions (picks + bans) | 501,000 |
| Picks / bans | 208,750 / 292,250 |
| Distinct heroes | 123 |
| Radiant win rate | 48.7% |
| First match (UTC) | 2022-01-01 05:13 |
| Last match (UTC) | 2022-12-31 03:51 |
| Draft formats | cm24_7.30 (20,875) |
| Matches dropped (draft follows no known format) | 261 of 21,136 |
| Heroes appearing for the first time | Marci, Primal Beast |
| Patch labels fixed (patch not yet released) | none |

## Matches per patch

Completeness = share of the source's matches (main_metadata.csv) that have a usable draft.

| Patch id | Version | Draft format | Matches | In source | Completeness |
|---|---|---|---|---|---|
| 49 | 7.30 | cm24_7.30 | 2,724 | 2,825 | 96.4% |
| 50 | 7.31 | cm24_7.30 | 13,086 | 13,468 | 97.2% |
| 51 | 7.32 | cm24_7.30 | 5,065 | 8,629 | 58.7% ⚠ |

⚠ Low draft completeness (< 90%): the Kaggle source lacks pick/ban data for part of these patches' matches; statistics for them are based on a subset.

## Matches per month

| Month | Matches |
|---|---|
| 2022-01 | 1,492 |
| 2022-02 | 1,572 |
| 2022-03 | 1,973 |
| 2022-04 | 1,837 |
| 2022-05 | 2,037 |
| 2022-06 | 2,913 |
| 2022-07 | 2,368 |
| 2022-08 | 2,158 |
| 2022-09 | 1,363 |
| 2022-10 | 1,092 |
| 2022-11 | 1,049 |
| 2022-12 | 1,021 |

## Most picked heroes

| # | Hero | Picks | Pick rate |
|---|---|---|---|
| 1 | Tiny | 6172 | 29.6% |
| 2 | Mars | 5749 | 27.5% |
| 3 | Grimstroke | 4235 | 20.3% |
| 4 | Death Prophet | 4034 | 19.3% |
| 5 | Snapfire | 4002 | 19.2% |
| 6 | Puck | 3743 | 17.9% |
| 7 | Ember Spirit | 3690 | 17.7% |
| 8 | Rubick | 3678 | 17.6% |
| 9 | Pangolier | 3620 | 17.3% |
| 10 | Bane | 3614 | 17.3% |

## Most banned heroes

| # | Hero | Bans | Ban rate |
|---|---|---|---|
| 1 | Puck | 9090 | 43.5% |
| 2 | Medusa | 6794 | 32.6% |
| 3 | Batrider | 6357 | 30.4% |
| 4 | Death Prophet | 6078 | 29.1% |
| 5 | Templar Assassin | 6005 | 28.8% |
| 6 | Lina | 5958 | 28.5% |
| 7 | Monkey King | 5864 | 28.1% |
| 8 | Mars | 5807 | 27.8% |
| 9 | Viper | 5801 | 27.8% |
| 10 | Beastmaster | 5457 | 26.1% |
