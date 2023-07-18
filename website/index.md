---
title: A Probabilistic Transformation of Distance-Based Outliers
author:
  - David Muhr
  - Michael Affenzeller
  - Josef Küng
date: 2023-07-11
---

Distance-based outlier detection methods are widely used across data domains,
yet the results of those methods are often tricky to interpret.
In particular, distance-based outlier scores require some additional context for
interpretation to convert the scores into binary decisions.
Previous methods to transform distance-based scores into some interpretable form
were either algorithm-specific, or completely algorithm-agnostic based purely on
the resulting scores.
In our work, we propose to use the distance-information to neighboring data
points, a prerequisite common across distance-based outlier detection
algorithms, to determine distance probability distributions and, subsequently,
use the distributions to turn distance-based outlier scores into interpretable
outlier probabilities.
We show that this transformation does not impact detection performance and
significantly increases the contrast between normal and outlier scores.
To evaluate the proposed probabilistic transformation, we generalize commonly
used k-nearest neighbors outlier detection methods as weighted k-nearest
neighbors outlier detection and evaluate it on a wide range of tabular datasets.
We further integrate our probabilistic transformation into the popular PatchCore
method and show how the resulting ProbabilisticPatchCore method improves upon
the original specification.

```
@article{Muhr2023,
  doi = {https://doi.org/10.3390/make5030042},
  url = {https://www.mdpi.com/2504-4990/5/3/42},
  year = {2023},
  publisher = {TBD},
  volume = {5},
  number = {3},
  pages = {782-802},
  author = {David Muhr, Michael Affenzeller and Josef Küng},
  title = {A Probabilistic Transformation of Distance-Based Outliers},
  journal = {Machine Learning and Knowledge Extraction}
}
```

To demonstrate the difference between distance-based and probabilistic outlier
scores, we visualize the distance-based and probabilistic PatchCore scores for
all test images of the
[MVTecAD](https://www.mvtec.com/company/research/datasets/mvtec-ad) dataset.

| Dataset                         | Train          | Normal        | Outlier        | Contrast     |
|---------------------------------|----------------|---------------|----------------|---------------
| [Carpet](/carpet.html)          | 280            | 28            | 89             | 787          |
| [Grid](/grid.html)              | 264            | 21            | 57             | 258          |
| [Leather](/leather.html)        | 245            | 32            | 92             | 186          |
| [Tile](/tile.html)              | 230            | 33            | 84             | 1024         |
| [Wood](/wood.html)              | 247            | 19            | 60             | 279          |
| [Bottle](/bottle.html)          | 209            | 20            | 63             | 1024         |
| [Cable](/cable.html)            | 224            | 58            | 92             | 1024         |
| [Capsule](/capsule.html)        | 219            | 23            | 109            | 191          |
| [Hazelnut](/hazelnut.html)      | 391            | 40            | 70             | 667          |
| [Metal Nut](/metal_nut.html)    | 220            | 22            | 93             | 713          |
| [Pill](/pill.html)              | 267            | 26            | 141            | 1024         |
| [Screw](/screw.html)            | 320            | 41            | 119            | 105          |
| [Toothbrush](/toothbrush.html)  | 60             | 12            | 30             | 346          |
| [Transistor](/transistor.html)  | 213            | 60            | 40             | 1024         |
| [Zipper](/zipper.html)          | 240            | 32            | 119            | 900          |
