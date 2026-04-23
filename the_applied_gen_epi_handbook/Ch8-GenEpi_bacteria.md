# Genomic Epidemiology of Bacteria

## 8.1 Bacterial mechanisms for generating genetic diversity
 - DNApol _does_ have proofreading, resulting in slower mutation and evolutionary rate. Still, they have bigger genomes than viruses, so they still generate a handful of mutatiosn per year. This reduced rate results in reduced resolution of transmission.
 - Can easily exclude samples from a given outbreak, but it's tougher to resolve tranmission within a given outbreak, as the samples are often genetically quite similar.

### 8.1.1 How does horizontally acquired DNA get into the bacterial cell?
 - Transformation: pore
 - Transduction: phage
 - Conjugation: pilus


### 8.1.2 Integration of horizontally acquired DNA into the chromosome
 - Often homologous recombination (replaced section of genome by similar section of another bacteria's genome). This messes with clonal-evolution assumptions: "_multiple_ changes...during a _single event_, essentially accelerating the incorporation of polymorphic sites in the genome."

### 8.1.3 Acquisition and exchange of extrachromosomal DNA

#### 8.1.3.1 Plasmids
 - Usually circular dsDNA; "bonus material," as they "do not encode most essential genes."
 - "Bacteria can gain and lose plasmids, and they can harbour more than one plasmid, although certain plasmids may not be able to stably co-exist within a bacterium, a feature known as **plasmid incompatibility**."

#### 8.1.3.2 Analysis
 - Plasmid typing
 - "[I]dentify the presence and absence of plasmids or at least the epidemiologically important genes such as antimicrobial resistance determinance."

#### 8.1.3.3
 - "Plasmid assembly can be hard using short read sequence data because portions of the plasmid may have sequence homology with the chromosome or even contain repeat regions within the plasmid. In addition, plasmids are often present in high copy numbers in relation to the bacterial genome."

## 8.2 A brief note about bacterial population structure
 - "As described, genetic variation in bacteria is driven by recombination and mutation, and that variation is acted upon by selection and chance. Combined with other biological and ecological factors, these processes can shape the structure of a species or blur the boundaries between them."
 - Unstructured ("**panmictic**") to well-structured ("**clonal**")
 - Statistical association of loci: "**linkage disequilibrium**"
 - "[T]he more recombination a species experiences, the more mixed it becomes, and the less structured the population."
 - "In practice, few bacterial species are regarded as truly panmictic; _Helicobacter pylori_ and some environmental species of _Vibrio_ are included in that group. _Staphylococcus aureus_ and _Mycobacterium tuberculosis_ are canonically referred to as clonal, while most others, such as species of _Neisseria_ and _Steptococcus_, fall in the middle. When investigating a putative outbreak, it is important to have a general knowledge of the suspected species' population structure."

## 8.3 Bacterial sequence typing
 - Many methods, but MLST (multi-locus sequence typing) is most common for "allele profiling in seven housekeeping genes."
 - Good because it's quick and relatively specific; insufficient because it doesn't tell you genetic distance or relation. Also, convergent evolution and recombination muddy the waters.

## 8.4 Defining bacterial genome elements

### 8.4.1 Core genome
 - "[T]he set of genes that are present across all strains within a particular sample from a bacterial species."

### 8.4.1.1 Analysis
 - A lossy analysis compared to viral genomes, which are smaller.
 - Focuses on loci or sequence types.
 - "The size of the core genome will decrease as the number of samples you consider increases."
 - When you only look at small bits of the genome, a bacterial species will have short terminal branch lengths, as they all appear to be astonishingly similar.

### 8.4.2 Accessory genome
 - "[A]ll the genetic elements, either on the chromosome or harboured on mobile genetic elements such as plasmids, phages or integrative and conjugative elements, that are present within a particular bacterial strain, but are not found across all samples in your sample set." That last part is key.
 - "These genes are often epidemiologically relevant, conferring antibiotic resistance or virulence...and can come an go."

### 8.4.2.1 Analysis
 - Presence/absence, apparently.

### 8.4.3 Pangenome
 - All genetic elements
 - "A notable characteristic of pangenome variation is that, due to patterns of recombination, core genome SNP diversity and accessory genome diversity (measured by the presence and absence of accessory genes) are correlated. The more distantly related members of a species are in their core genome SNPs, the more dissimilar their accessory genomes."

## 8.5 Bacterial genome sequencing and assembly
 - Reference-based and _de novo_ assembly
 - For _de novo_ assembly, contigs ("a contiguous sequence derived from multiple overlapping sequencing reads") are generated and can be annotated with Prokka or PGAP.
 - For reference-based assembly, "reference selection can significantly impact downstream analysis. Most notably, you can only identify variation in regiosn of the genome that are shared between the reference and the sequenced bacterial isolates."

### 8.5.1 Considerations for long-read sequencing data
 - Lower per-base read accuracy than short-read platforms, but this is improving with kit chemistry.
 - A good method may be hybrid approach, where you use iterate between long-read technology (to generate scaffold for the short-read contigs) and short-read technology (to correct the scaffold, termed "polishing").

## 8.6 A practical workflow for bacterial genomic epidemiology
 - _De novo_ assembly, genome annotation, SNP distance matrix or phylogeny, annotate with MLST and epi data.

## 8.7 Intrahost diversity and implications for inferring transmission
 - HGT, recombination, etc.
 - We've covered much of this already.

## 8.8 Investigation of transmission
 - "No pathogen-centric model, sequencing or otherwise, will ever replace the need for classic shoe-leather epidemiology investigation. Another truism is that it is far easier to _rule-out_ a case using pathogen genomic data than it is to _rule-in_.
 1) SNP distances (cutoffs, can be derived empirically with a histogram of the distance matrix)
 2) Phylogenetics (data-rich but nuanced)
 3) Modeling (use epi and genetic info)

## 8.9 Conclusions
 - "[O]ne must consider the nuances of bacterial evolution when investigating transmission. This includes an understanding of 1) the epidemiology of the pathogen, 2) recombination and mutation and how they shape population structure with the help of selection and drift, 3) genome content variation and pangenome analysis, and 4) intrahost evolution.
