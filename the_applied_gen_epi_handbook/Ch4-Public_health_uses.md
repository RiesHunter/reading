# Public Health Use Cases of Genomic Epidemiology

## 4.1 Assessing epidemiologic linkage between cases
 - "In public health, we often question whether there is a connection between cases presenting with the same infection. Often we'll draw on an assessment of shared exposures, and geographic and temporal data, to determine whether infections are linked. Pathogen genomic data provide another data stream by which we can assess relationships between cases."

Questions (from text):
 - Both of these cases have similar reported exposures. Is that common exposure the likely source of both infections?
 - I'm observing multiple detections of disease in the same setting. Is this setting facilitating transmission, or are we simply detecting community-acquired infections in this setting due to enhanced screening or surveillance?

### 4.1.1 Fundamental principles to draw upon
 - "This process [the accumulation of mutations over time] also means that cases separated by a minimal amount of transmission will generaly have more genetically similar infections, while cases that are separated by large amounts of transmission will typically have more genetically divergent infections."

### 4.1.2 How should you sample?
 - Targeted (with contextual sequences) or representative

### 4.1.3 Tools and approaches you can use to explore the question
 - Phylogenetic placements or trees
 - When samples are _not_ similar, contextual sequences are hypothesis-generating.
 - Recommends using phylogenetic placements when "rapid situational awareness is more important than a richer analysis."

### 4.1.4 Caveats, limitations, and ways things go wrong
 - "[G]enomic data are powerful for ruling linkage out, but less powerful for unequivocally ruling linkage in. Furthermore, except in rare cases, you cannot infer the directionality of transmission from sequence data alone when you have highly genetically similar consensus genomes. This principle is probably cleanest when cases have identical genome sequences, since if all of the sequences are the same there's no genomic signal for directionality. However, we caution that directionality is still challenging to infer accurately even when some genomes are slightly diverged." (She then uses an example scenario where a donor transmits a low-frequency variant to one of many recipients.)
 - "If you're assessing linkage between two samples collected through representative surveillance, then consider what proportion of cases you have sequence data for. If you sequence only a small proportion of cases, then there may be intervening cases along a transmission chain that go unsequenced, and therefore do not appear in a phylogenetic tree."
 - "Finally, some molecular epidemiological methods suggest using Single Nucleotide Polymorphisms (SNP) distances and thresholds for ruling cases into the same outbreak or categorizing them as belonging to different outbreaks. While we understand how thresholds can make decision making easier, we generally discourage using SNP thresholds. This is because using SNP thresholds reduces the granularity of the data; they make a binary assessment (in or out of outbreak) when in fact the data are continuous (0, 1, 2, 3 ... SNPs separating two sequences). While reducing the data down to a single binary outcome does make assessment easier, it does so by hiding nuance and uncertainty, which is critical for making epidemiologic inferences and assessing your confidence in them. Furthermore, making genetic distance into a binary call results in a loss of information. Pathogens accrue mutations at specific evolutionary rates, thus the actual count of differences between two sequences provides a quantitative estimate of how related or unrelated two sequences are."

## 4.2 Exploring relationships between cases of interest and other sequenced infections
 - Determining whether two sequences are related: hypothesis-testing
 - Determining how two sequences are related to others: hypothesis-generating

Questions (from the text):
 - Is my outbreak related to other outbreaks occurring in other geographic locations?
 - Are there any additional cases in the community that might actually be part of this outbreak?

### 4.2.1 Fundamental principles to draw upon
 - The contextual sequences are usually not controlled by you, so you have to work with what you've got!

### 4.2.2 How should you sample?
 - Preferably, your contextual samples should be sampled representatively
 - "[T]he need for representatively sampled contextual data is one of the reasons why we need broad, baseline genomic surveillance programs. In such programs, sequencing is performed at random, without regard to specific clinical presentations, performance on diagnostic assays, or public health questions. Representative sequencing is done partially for the common good; everyone will need contextual data from other communities or populations at some point. This is the main reason why we encourage groups building genomic surveillance systems to perform some degree of representative sequencing beyond their targeted outbreak sequencing. Furthermore, this rationale is also why _annotating_ those sequences as representatively sampled surveillance specimens is a critical part of genomic surveillance data management."

### 4.2.3 Tools and approaches you can use to explore the question
 - Phylogenetic placement, trees, phylogeography.

### 4.2.4 Caveats, limitations, and ways things go wrong
 - Good-enough data is good enough, and you should recognize that it may be incomplete or biased. Interpretations must be allowed to change as things unravel.

## 4.3 Estimating the start and duration of an outbreak
 - "How did this outbreak begin, how long has it been going on for, and when will we be able to declare it over?"

### 4.3.1 Fundamental principles to draw upon
 - Even if you are undersampling, successive transmission accumulate mutations and can be informative.

### 4.3.2 How should you sample?
 - When you are looking for an ancestral sequence, remember that it is simply the MRCA of the _sampled_ dataset, not necessarily the true MRCA. (You would need to sample everything to get the _true_ MRCA.)

### 4.3.3 Tools and approaches you can use to explore the question
 - Nextstrain is probably good enough. 

### 4.3.4 Caveats, limitations, and ways things go wrong
 - Oversampling can lead to a perceived increase in the rate of evolution, as purifying selection has not yet sufficiently purged deleterious mutations. This is fine, but it should be recognized as such. 

## 4.4 Assessing how demographic, exposure, and other epidemiological data relate to a genomically defined outbreak
 - "Much of the richness of genomic epidemiological analysis comes not simply from the analysis of genomic data alone, but rather from the integration, and joint inference, of genomic and epidemiologic data together." (Think: PulseNet.)

Questions (from the text):
 - Are different lineages of this pathogen circulating in younger people versus older people?
 - Are different lineages of this pathogen circulating in vaccinated individuals versus unvaccinated individuals?
 - Does outbreak size or transmission intensity appear to correlate with circulation in particular populations of individuals?


### 4.4.1 Fundamental principles to draw upon
 - "[Lab-epi collaboration] allows the epidemiologist to qualitatively assess potential relationships between an exposure or demographic variable and clustering patterns in the tree."

### 4.4.2 How should you sample?
 - "Do individuals from a specific [facility] tend to cluster together in clades that are genetically diverged from cases in the other [facility]?"
 - You can do dense, targeted sequencing in these facilities and assess clustering.

### 4.4.3 Tools and approaches you can use to explore the question
 - Auspice, with metadata overlay.

### 4.4.4 Caveats, limitations, and ways things go wrong
 - Genomic-epi patterns are qualitative observations of correlation, and epis should design rigorous studies to test correlation. 
