# DOTA-Draft: A Dataset for In-Game Recommendation in Multiplayer Online Battle Arenas

This repository contains the **DOTA-Draft** dataset introduced in the paper:

> Mohammadnejad, M., Dorrigiv, M., & Yaghmaee, F. (2026). *DOTA-Draft: A Dataset for In-Game Recommendation in Multiplayer Online Battle Arenas*. Journal of AI and Data Mining.

Research in recommender systems has largely relied on standardized datasets such as MovieLens, Amazon Reviews, and Last.fm. However, these datasets are not designed for **in-game recommendation**, particularly in complex Multiplayer Online Battle Arena (MOBA) environments where recommendations must account for sequential, team-based, and adversarial decision-making.

DOTA-Draft addresses this gap by providing a research-ready benchmark dataset derived from professional Dota 2 matches, specifically designed for hero drafting recommendation tasks.

## 📖 Overview

### Domain Gap

Most publicly available game-related datasets focus on recommending games to players rather than supporting decision-making within games.

### Dataset Contribution

DOTA-Draft provides structured drafting data from professional Dota 2 matches, including:

* Sequential pick and ban actions
* Match outcomes
* Patch versions
* Team compositions
* Draft-state information suitable for recommendation research

### Benchmark Integration

The dataset is packaged in a format compatible with the RecBole recommendation framework, enabling reproducible experimentation and comparison with existing recommendation models.

### Research Challenges

DOTA-Draft highlights several challenges unique to in-game recommendation:

* Patch-driven dynamics
* Multi-agent interactions
* Hero synergy and counterplay
* Sequential decision-making
* High-dimensional contextual information

## 🧾 Dataset Description

**Source:** Professional Dota 2 match logs collected from publicly available match data and curated for recommendation research.

**Task:** Hero drafting recommendation during the pick/ban phase of professional matches.

**Format:** RecBole-compatible dataset files and preprocessing scripts.

<!-- DATASET-STATS:START -->
## 📦 Dataset versions and coverage

The dataset is updated monthly from the [Kaggle source](https://www.kaggle.com/datasets/bwandowando/dota-2-pro-league-matches-2023). Each year has its own folder, in RecBole format:

```
<year>/all_patches/all_patches.inter   all matches of that year
<year>/patch_<id>/patch_<id>.inter     one patch (patch ids are OpenDota ids, e.g. 59 = 7.40)
<year>/STATS.md, <year>/stats.json     statistics
```

**Data through:** 2026-08-31 · **Last match:** 2026-08-31 22:41 UTC · **Kaggle snapshot:** 2026-09-14 · **Release:** v2026.08.1

| Year | From | Through | Matches | Interactions | Patches |
|---|---|---|---|---|---|
| [2020](2020/STATS.md) | 2020-01-01 | 2020-12-31 | 21,857 | 500,670 | 42, 43, 44, 45, 46, 47 |
| [2021](2021/STATS.md) | 2021-01-01 | 2021-12-31 | 16,043 | 385,032 | 47, 48, 49 |
| [2022](2022/STATS.md) | 2022-01-01 | 2022-12-31 | 20,875 | 501,000 | 49, 50, 51 |
| [2023](2023/STATS.md) | 2023-01-01 | 2023-12-31 | 29,453 | 706,872 | 51, 52, 53, 54 |
| [2024](2024/STATS.md) | 2024-01-01 | 2024-12-31 | 29,327 | 703,848 | 54, 55, 56 |
| [2025](2025/STATS.md) | 2025-01-01 | 2025-12-31 | 29,793 | 715,032 | 56, 57, 58, 59 |
| [2026](2026/STATS.md) | 2026-01-01 | 2026-08-31 | 13,983 | 335,592 | 59, 60 |

Total (schema v2.1 folders): 161,331 matches, 3,848,046 interactions.

**Schema v2** (year folders): `user_id` = `<match_id>_<team>` (stable everywhere), `item_id` = real hero id, `hero_action` = `hero_<hero_id>_<pick|ban>`, plus `start_time` (unix seconds). Each row also has `draft_format` (the Captains Mode pick/ban order of that match) and `first_team` (1 = this team made the first draft action). Only matches whose draft follows a known format are kept. Matches that the source labels with a patch released after the match started are relabelled to the patch current at that time (counted in each year's STATS.md).

**Draft formats** (b = ban, P = pick, 1 = team acting first, 2 = the other team):

| Format | Actions | Patches | Order |
|---|---|---|---|
| `cm22_7.23` | 22 | 7.23–7.25 | `b1 b2 b1 b2 b1 b2 P1 P2 P2 P1 b1 b2 b1 b2 P2 P1 P2 P1 b2 b1 P1 P2` |
| `cm22_7.25` | 22 | 7.25–7.26 | `b1 b2 b1 b2 b1 b2 b1 b2 P1 P2 P2 P1 b1 b2 P2 P1 P2 P1 b2 b1 P1 P2` |
| `cm24_7.27` | 24 | 7.27–7.28 | `b1 b2 b1 b2 P1 P2 P1 P2 b1 b2 b1 b2 b1 b2 P2 P1 P2 P1 b1 b2 b1 b2 P1 P2` |
| `cm24_7.29` | 24 | 7.29–7.29 | `b1 b2 b1 b2 P1 P2 P2 P1 b1 b2 b1 b2 b1 b2 P2 P1 P2 P1 b1 b2 b1 b2 P1 P2` |
| `cm24_7.30` | 24 | 7.30–7.33 | `b1 b2 b1 b2 P1 P2 P2 P1 b1 b2 b1 b2 b1 b2 P2 P1 P1 P2 b1 b2 b1 b2 P1 P2` |
| `cm24_7.34` | 24 | 7.33–7.39 | `b1 b2 b2 b1 b2 b2 b1 P1 P2 b1 b1 b2 P2 P1 P1 P2 P2 P1 b1 b2 b2 b1 P1 P2` |
| `cm24_7.40` | 24 | 7.39–7.41 | `b1 b1 b2 b2 b1 b2 b2 P1 P2 b1 b1 b2 P2 P1 P1 P2 P2 P1 b1 b2 b1 b2 P1 P2` |

**Schema v1** ([`paper-v1/`](paper-v1)) holds the exact files used in the paper: `all_patches/` and `patch_54`–`patch_56/` hold 2024 matches, `patch_57`–`patch_59/` hold 2025 matches. In v1 `user_id` is a per-file counter and `item_id`/`hero_action` use `hero_id + 1`. They are kept unchanged; to reproduce the paper use `data_path: ./paper-v1`.

Machine-readable definitions (action and team of every draft slot, for masking or conditioning models): [draft_formats.json](draft_formats.json).

See [CHANGELOG.md](CHANGELOG.md) for release notes and [STATS.md](STATS.md) for statistics.
<!-- DATASET-STATS:END -->

## 📌 Citation

If you use this dataset in your research, please cite:

```bibtex
@article{mohammadnejad2026dotadraft,
  author = {Mohammadnejad, Mohammadreza and Dorrigiv, Morteza and Yaghmaee, Farzin},
  title = {DOTA-Draft: A Dataset for In-Game Recommendation in Multiplayer Online Battle Arenas},
  journal = {Journal of AI and Data Mining},
  year = {2026},
  pages = {-},
  publisher = {Shahrood University of Technology},
  issn = {2322-5211},
  eissn = {2322-4444},
  doi = {10.22044/jadm.2026.16888.2819},
  url = {https://jad.shahroodut.ac.ir/article_3801.html}
}
```

**DOI:** https://doi.org/10.22044/jadm.2026.16888.2819

## 📬 Contact

For academic correspondence:

📧 [mreza.mohammadnejad@semnan.ac.ir](mailto:mreza.mohammadnejad@semnan.ac.ir)
