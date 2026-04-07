---
editor_options: 
  markdown: 
    wrap: 72
---

# Linkage Probability Simulation

Simulates P(directly linked \| k mutations) for pairs of pathogen
genomes, recapitulating Figures 3.5 and 3.6 from Alli Black's [Applied
Genomic Epidemiology Handbook
§3.7.1](https://alliblk.github.io/genepi-book/fundamental-theory-in-genomic-epidemiology.html#how-many-mutations-are-enough-to-rule-linkage-out).

## How to render

Open `linkage_probability.qmd` in RStudio and click **Render**, or from
the terminal:

``` bash
quarto render linkage_probability.qmd
```

Requires R with `tidyverse` and Quarto installed.

## What the model assumes

-   Linked pairs diverge over a gamma-distributed serial interval;
    un-linked pairs diverge over a uniformly distributed time 5–50× the
    serial interval.
-   Mutations accumulate as a Poisson process at rate μ × L × τ (in
    years).
-   Equal numbers of linked and un-linked pairs are simulated, implying
    a 50/50 prior on linkage.

## Caveats

-   The 50/50 prior is unrealistic for most outbreak settings.
-   Within-host diversity, transmission bottlenecks, and double-sided
    MRCA divergence are collapsed into one Poisson draw.
-   Serial interval ≠ generation interval.
-   The serial-interval framing is a poor fit for vector-borne (WNV) and
    chronic (HIV) pathogens — those plots are illustrative only.
