# Changelog

Release notes of the monthly dataset updates.

## v2026.08.1 — data through 2026-08-31

- Kaggle snapshot: 2026-09-14; last match: 2026-08-31 22:41 UTC
- New periods: 2020, 2021, 2022, 2023
- 2020: 21,857 matches (+21,857), 500,670 interactions, through 2020-12-31
  - New patches: 42 (7.23), 43 (7.24), 44 (7.25), 45 (7.26), 46 (7.27), 47 (7.28)
  - Dropped 296 of 22,153 matches whose draft follows no known format
- 2021: 16,043 matches (+16,043), 385,032 interactions, through 2021-12-31
  - New patches: 47 (7.28), 48 (7.29), 49 (7.30)
  - Dropped 210 of 16,253 matches whose draft follows no known format
  - Heroes appearing for the first time: Hoodwink, Dawnbreaker
- 2022: 20,875 matches (+20,875), 501,000 interactions, through 2022-12-31
  - New patches: 49 (7.30), 50 (7.31), 51 (7.32)
  - Dropped 261 of 21,136 matches whose draft follows no known format
  - Low draft completeness in the source: 7.32 59% (5,065 of 8,629)
  - Heroes appearing for the first time: Marci, Primal Beast
- 2023: 29,453 matches (+29,453), 706,872 interactions, through 2023-12-31
  - New patches: 51 (7.32), 52 (7.33), 53 (7.34)
  - Dropped 190 of 29,643 matches whose draft follows no known format
  - Heroes appearing for the first time: Muerta
- 2024: 29,327 matches (+0), 703,848 interactions, through 2024-12-31
  - Dropped 380 of 29,707 matches whose draft follows no known format
  - Fixed patch labels (patch not released yet at match time): 57->56: 643 matches
- 2025: 29,793 matches (+0), 715,032 interactions, through 2025-12-31
  - Dropped 385 of 30,178 matches whose draft follows no known format
  - Heroes appearing for the first time: Ring Master, Kez
- 2026: 13,983 matches (+0), 335,592 interactions, through 2026-08-31
  - Dropped 58 of 14,041 matches whose draft follows no known format
  - Heroes appearing for the first time: Largo
- Schema v2 -> v2.1: every year rebuilt; new columns `draft_format:token` (pick/ban order) and `first_team:float` (1 = team acting first)
- New draft formats detected: cm22_7.23, cm22_7.25, cm24_7.27, cm24_7.29, cm24_7.30, cm24_7.34, cm24_7.40
- New patch notes: `patch_notes/43-patch_7_24.json`, `patch_notes/44-patch_7_25.json`, `patch_notes/45-patch_7_26.json`, `patch_notes/46-patch_7_27.json`, `patch_notes/48-patch_7_29.json`, `patch_notes/49-patch_7_30.json`, `patch_notes/50-patch_7_31.json`, `patch_notes/51-patch_7_32.json`, `patch_notes/52-patch_7_33.json`, `patch_notes/53-patch_7_34.json`
- Patch notes for patch 42 not available yet (no notes for 7.23 in Constants.PatchNotes.csv)
- Patch notes for patch 47 not available yet (no notes for 7.28 in Constants.PatchNotes.csv)

### Coverage

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

## v2026.08 — data through 2026-08-31

- Kaggle snapshot: 2026-09-14; last match: 2026-08-31 22:41 UTC
- New periods: 2024, 2025, 202601, 202602, 202603, 202604, 202605, 202606, 202607, 202608
- 2024: 29,327 matches (+29,327), 703,848 interactions, through 2024-12-31
  - Dropped 380 of 29,707 matches without a full 24-action draft
  - Fixed patch labels (patch not released yet at match time): 57->56: 643 matches
- 2025: 29,793 matches (+29,793), 715,032 interactions, through 2025-12-31
  - Dropped 385 of 30,178 matches without a full 24-action draft
- 2026: 13,983 matches (+13,983), 335,592 interactions, through 2026-08-31
  - Dropped 58 of 14,041 matches without a full 24-action draft
- New patch notes: `patch_notes/60-patch_7_41.json`

### Coverage

**Data through:** 2026-08-31 · **Last match:** 2026-08-31 22:41 UTC · **Kaggle snapshot:** 2026-09-14 · **Release:** v2026.08

| Year | From | Through | Matches | Interactions | Patches |
|---|---|---|---|---|---|
| [2024](2024/STATS.md) | 2024-01-01 | 2024-12-31 | 29,327 | 703,848 | 54, 55, 56 |
| [2025](2025/STATS.md) | 2025-01-01 | 2025-12-31 | 29,793 | 715,032 | 56, 57, 58, 59 |
| [2026](2026/STATS.md) | 2026-01-01 | 2026-08-31 | 13,983 | 335,592 | 59, 60 |

Total (schema v2 folders): 73,103 matches, 1,754,472 interactions.

