# Case studies in applying genomic epidemiology

## 5.1 Are cases of the same variant of concern lineage linked?
 - We often want to know whether a specific variant _has_ arrived, and, if so, how it is distributed within the population.
 - "[W]hile Pango lineage assignment can provide a useful summary of different genetic linkages, most Pango lineages have genetic diversity within the lineage. Especially for lineages whose frequency grows significantly...there may be many different transmission chains...circulating within different geographic areas. In such cases, phylogenetic analyses can provide higher resolution for refining relationships between cases."
 - Inspecting the alignment (.bam) is good practice for unique samples. (Looking at lineage-defining sites is often most fruitful.)
 - "In Nextclade, we can take our two sequences and 'graft' them onto a pre-inferred Nextstrain phylogeny in a process that is termed 'phylogenetic placement.' The sequences are placed onto the tree according to the patterns of substitutions that the tree summarises, and that your sequences have. The sequences of interest are placed onto the tree at the point where most of the SNPs in your genome sequence have also been observed in the tree. Then, any mutations that are unique to your sample, and not yet detected in the background tree, are shown in a branch length leading from the tree to the sample of interest."
 - When two samples are epidemiologically but not genetically/phylogenetically linked, they are likely two independent introductions. 

## 5.2 Evaluating an intake screening program to prevent introduction of SARS-CoV-2 to prisons
 - When sequences are assigned the same lineage, phylogenetic methods can be used for higher resolution regarding their genetic relationships. 

## 5.3 Identifying, assigning, and investigating a new SARS-CoV-2 lineage in Lithuania
 - Bioinformatic errors (not calling indels, for example) and edge cases (co-infection, divergent strain), Pango lineage misclassification (computational errors, lack of other sequences), and the justified reluctance of public health agencies to release personal information (sample collection date, location; travel history, risk factors of patient) stymie applied genomic epidemiology investigations.
 - Pango lineage classification provides simple shorthand for researchers, public health officials, and the public. It's also less scary than "unidentified" or other "needlessly ominous term[s]."

## 5.4 Estimating when the Zika virus epidemic began in Colombia
 - Syndromic surveillance is useful but necessarily depends on the presentation of symptoms, which does not occur with every pathogen or with every case of a specific pathogen.
 - "[E]ven if syndromic surveillance systems capture an uptick in febrile illness, this may be attributed to different viral diseases."
 - If you want to investigate the effect of a virus on a population, it's useful to know the date cutoff for study inclusion/exclusion. It's also useful for a before-and-after comparison.
 - When ascertaining the circulation start date, you must include representative samples (of the population of interest) and contextual samples (of other populations). The representative samples provide the bounds, and the contextual samples strengthen the "accurate inference of the rate of evolution." When possible, collect samples serially to strengthen temporal resolution.
 - Internal node dates (in Nextstain, anyway) also provide 95% confidence intervals. Report the point estimate and the intervals. These values are liable to change with the inclusion of new samples.
 - Inferring the directionality of circulation is challenging, as you must consider sampling intensity. If there is a long period of undersampling, these nodes may not resolve clearly. For example, if Country A and B both had samples from a given year, but there is a long internal branch between their common ancestors, there may not _actually_ be any directionality of circulation between the two. It is possible that Country C was undersampled and transmitted to both in the long internal branch period. Similarly, it's additionally possible that, after spread to both Country A and B, that Country A transmitted to B — or the inverse. To confidently resolve the directionality, we need additional samples with metadata on collection date and location. Additionally, you can use advanced phylogeographic reconstruction tools, such as BEAST.


