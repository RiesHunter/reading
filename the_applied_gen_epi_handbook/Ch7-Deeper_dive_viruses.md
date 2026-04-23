# A Deeper Dive into Viral Genomic Complexity
 - Not all evolution is clonal evolution: mutations accruing through error-prone replication, being passed down to progeny.
 - Genetic variation can be generated through other methods, too!

## 7.1 Recombination
 - Bacteria can transfer genetic elements through horizontal gene transfer (HGT).
 - Viruses can transfer genetic elements through template-switching mechanisms.
 - Repeat mutations (homoplasies) in the phylogenetic tree suggest either recombination, convergent evolution, or chance.
 - If the homoplasies are a result of recombination, we would expect to also observe a string of mutations around the homoplastic mutation.
 - If you analyze recombinant homoplasies with clonal phylogenetic models, it will assume convergent evolution.
 - Convergent evolution typically occurs with non-synonymous mutations, but they can rarely occur as synonymous mutations.

## 7.2 Segmented genomes and reassortment
 - Influenza, Lassa, Hanta, rota, bluetongue.
 - Segments complicate the sequencing analysis.
 - Reassortment can occur when more than one unique virus infects a given cell.

## 7.2.1 Considerations for analysis
 - "[I]nfer the phylogenetic tree of each segment independently and at least initially compare them visually."
 - Keep an eye on the "hierarchical nesting" of the clades when comparing segments. They should be very similar if there is no reassortment, but you can still get reassortment with y-axis alignment!
 - Tanglegrams are useful for comparing tree topologies, but, as mentioned above, alignment of the y-axis does not indicate the absence of reassortment. Look at the clade nesting.
 - "Tangled chains" are an interesting plot type I had not previously considered. May be smart for flu, but tread lightly here. Trees, alone, are already a lot for non-specialists.

## 7.3 Hypermutation
 - APOBEC: cytidine deamination (C --> U) of RNA and DNA (C:G --> U:G (mismatch) --> T:A (U to T, which matches A)
 - ADAR: adenosine deaminase (A --> inosine, like G) of dsRNA (TC --> TT on the anti-sense dsRNA strand, 5' -> 3'; A --> G on the "sense" dsRNA strand, 3' -> 5')
 - Considering masking sites of hypermutation, as they won't necessarily follow the molecular clock model you choose. Your tree will look much younger if you include them.
## 7.3.1 Handling variable mutation rates with relaxed molecular clocks

### 7.3.1 Handling variable mutation rates with relaxed molecular clocks
 - Don't use a strict clock, assuming the same evolutionary rate across branches.
 - Evolutionary rate heterogeneity exists, and it's usually log-normally distributed and uncorrelated (independent branches).

## 7.4 Diversity of RNA virus genome organizations
 - Funky things exist, and you should be aware of them.

## 7.4.1 Ambisense
 - Two open reading frames, overlapping and running in opposite directions.
 - Lassa, Machupo

## 7.4.2 Reverse complementarity
 - Self-complementary sequences
 - Self-similarity dot-plots can elucidate repeats or reverse-complements if dots of similarity trend off the y=x trend.

## 7.4.3 Splicing
 - Splicing exists (flu), and sequences are suspect if there are long stretches of non-coding space.
 - Sequencing may find "both the genomic unspliced and spliced transcript RNAs."
