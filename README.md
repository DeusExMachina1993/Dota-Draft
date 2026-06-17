# DOTA-Draft: A Dataset for In-Game Recommendation in Multiplayer Online Battle Arenas

This repository contains the **DOTA-Draft** dataset and benchmark scripts introduced in the paper:

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
