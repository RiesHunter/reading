# Tools and methods for Applied Genomic Epidemiological Analysis

## 6.1 Phylogenetic placements
 - "[T]hey place your sample of interest onto a previously-inferred, fixed phylogenetic tree."
 - Sequences are placed on the tree in the most "optimal" or "parsimonious" way. This method "requires the least number of _additional_ mutations in the sequence beyond the genetic changes summarised in the tree."
 - Because you can have multiple equally parsimonious placements, this is a good metric for uncertainty.

### 6.1.1 UShER
 - Basically BLASTs then makes a mini phylogenetic tree. Provides a nice output table with the uncertainty mentioned above.
 - If there are multiple equally parsimonious trees, you'll get multiple trees.
 - A fast-and-broad search for close relatives.

### 6.1.2 Nextclade
 - Seems to be a distance-based method relative to the tips. Also provides a nice output table, but I don't think it has a similar uncertainty metric.
 - A fast search, although less broad than USher, Nextstrain is limited to the contextual data provided (as opposed to _all_ data in public repos).
 - Can place sequences on personally curated trees -- good for situational awareness.

## 6.2 Phylogenetic trees
 - Distance-matrix methods (older; not recommended, as it doesn't model evolution)
 - Maximum-likelihood methods (newer; recommended, as it models evolution)
 - Bayesian methods (much newer; recommended for the die-hards, as it's tricky but probabilistic)

### 6.2.1 Nextstrain
 - Augur: chew fastas, output a JSON
 - Auspice: visualize JSON
 - Website: See curated trees

### 6.2.2 IQ-TREE
 - Good option, more general but quick.

### 6.2.3 RAxML
 - Little bit more intense (and accurate), although it takes a while.

### 6.2.4 BEAST
 - "[C]apture[s] phylogenetic uncertainty."
 - Can calculate Ro and pathogen population size.

## 6.3 When should I use a phylogenetic tree versus a phylogenetic placement?
 - Placements are quick, for determining close neighbors.
 - Trees are slower but more precise, asking _when_ in addition to a subset of _who_.

## 6.4 Selecting contextual data for phylogenetic tree analyses
 - Include high-quality external sequences.
 - Include some sequences from the larger outbreak.
 - Include some sequences from your local outbreak or suspect geographies.

## 6.5 Notes about node ages in temporally resolved trees
 - Different formats can be tricky.
