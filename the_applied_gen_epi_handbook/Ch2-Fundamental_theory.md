# Fundamental Theory in Genomic Epidemiology
 - "Genomic epidemiology uses theory, analytical approaches, and jargon that surveillance epidemiologists may not be familiar with."

## 2.1 The overlapping timescales of pathogen evolution and pathogen transmission
 - "Our ability to explore infectious disease dynamics using evolutionary analysis of pathogen genome sequences depends on a fundamental principle; pathogens evolve on roughly the same timescales as they circulate through a population of hosts. This principle means that the evolutionary trajectories of pathogens are shaped by...epidemiological and immunological forces."
 - "Pathogen genetic diversity becomes distributed in different ways depending on varying host movements, transmission dynamics, environments, and selective pressurures, among other forces. Exploring those pattens can help us to understand to what extent these different factors shape epidemics."

### 2.1.1 Viral diversity accumulates over the course of a single individual's infection
 - RdRps make mistakes often, and this composes within-host viral diversity.

### 2.1.2 Stochasticity and selection influence variant frequency within an infection
 - Viruses don't evolve "_towards_ some trait." (That is, deterministically.)
 - Deleterious mutations reduce fitness, neutral mutations have no effect on fitness, and beneficial mutations improve a fitness advantage.
 - "While the occurrence of mutations themselves is a random process...the impact that different mutations...will influence the frequency of those mutations within the diversity of an individual's infection."

### 2.1.3 When a transmission event occurs, the within-host viral diversity of the infector is sampled and transmitted to the recipient
 - "Because the within-host diversity of an infection is changing over the whole duration of that person's infection, transmission events occurring at different time points in the infector's infection will result in different samples of the viral diversity being transmitted."
 - "Siilarly, because only a sample of the infector's viral diversity is transmitted on to a recipient if a single infector were to infect many recipients at the same time, those recipient infections would be founded with slightly different samples of the infector's within-host diversity as well." 

### 2.1.4 Consensus genomes provide a summary of the within-host diversity
 - "There are various decisions surrounding what threshold you use for making an unambiguous or ambiguous base call. However, a deep discussion of these trade-offs, and the parameterisation of bioinformatic pipelines for calling consensus genomes, is beyond the scope of this introduction."
 - "Many of the mutations that arise during the process of viral replication will remain at such low frequencies that a 'real' mutation is not discernible from a mutation arising from PCR amplification or sequencing errors. As such, the consensus genome will not capture many of the mutations that occur over the course of an infection. This is one of the reasons why consensus genome sequences can be identical between closely linked infections, even though viruses are mutating with every replication cycle. This dynamic aso means that the rate at which we _observe_ changes in the consensus genome sequence of different infections is slower than the biologically governed mutational rate of the pathogen."

## 2.2 Terminology for describing changes in genetic sequences
 - Mutation/SNP/allele: "changes in the genetic sequence of the organism, at a single site in that organism's genome."
 - Genotype: "[t]he pattern of mutations that you observe across a sequence, summarised by the consensus genome sequence."
 - Substitution: "when a mutation has become completely dominant." "Fixed" when population-wide. (I disagree with this framing, preferring substitution to refer to a type of mutation characterized by NS/S/Stop/etc. mutation types.)

## 2.3 Mutation rates, evolutionary rates, and the molecular clock
 - Mutation rate: the "rate at which a microbe's DNA or RNA polymerase makes errors while replicating the genome."
 - Evolutionary rate: the "rate at which mutations accumulate after selection."
 - "Unlike the mutation rate, which depends most greatly on the functional characteristics of the polymerase, the evolutionary rate is the product of multiple intersecting features of the organism. These include the mutation rate, the amount of time it takes for the organism to replicate its genome and produce progeny, the size of the population of replicating individuals, the ability of the organism's genome to tolerate mutations, and the degree and type of selection acting upon the organism."
 - Molecular clock: "the signal of evolution through time." Or, how we convert nucleotide changes to calendar time. Directionality: nuc -> time.
 - Evolutionary rates can be normalized by the number of sites or non-normalized. While non-normized rates are more intuitive (e.g., # subs/year), normalized rates are more comparable between pathogens (with different mutation rates and genome lengths; e.g., # subs/site/year).
 - Normalized -> non-normalized: Normalized rate * genome length
 - Non-normalized -> normalized: Non-normalized rate / genome length
 - Usefulness: "Firstly, it enables 'back-of-the-envelope' calculations of how much time likely separates two sequences. This can be particularly handy when investigating potential epidemiological linkage between two sequence cases. Secondly, molecular clocks enable us to translate genetic divergence trees into temporally-resolved phylogenetic trees, or time trees. Finally, root-to-tip plots are also excellent (and quick!) ways to perform data quality control and look for interesting biology and epidemiological patterns."

## 2.4 Multiple sequence alignment
 - Didn't take many notes on this, but there was a funny bit about misaligned sequences (like misaligned taxa columns) placing "a fish that now errantly lactates and flies onto a phylogeny amongst vertebrates that perform these functions as well."

## 2.5 Phylogenetic trees

## 2.5.1 What is a phylogenetic tree?
 - Tips/leaves: directly observed samples
 - Internal nodes: inferred samples ("hypothetical common ancestors that were not directly observed, but that we infer existed given the genetic patterns we see among the tips")
 - Branches: connect tips and nodes. Internal branches connect internal nodes; an external branch connects a node and a descendent tip.
 - "Groups of sequences that share a particular mutation are inferred to have inherited that mutation and cluster together, descending from the branch where that mutation occurred. In contrast, sequences that do not share that same mutation are likely not part of the same pattern of descent, and will cluster in a different part of the tree."
 - "Notably, because the phylogenetic clustering pattern is hierarchical, so are clades. Two sequences might cluster together into a small clade defined by a mutation that only they share. But those sequences can also be grouped within a larger clade, with additional sapmles, defined by a different set of mutations that occurred further back in the tree and were inherited by additional samples in the tree." Big sentences, but clades are hierarchical and can be nested.

## 2.5.2 Assessing and reading a phylogenetic tree
 - y-axis is "meaningless." (I disagree; it tells you tip number.)
 - "The root of the tree represents the common ancestor of all your samples. Rooting determines the order of branching in the tree."
 - Outgroup: "a fairly distinct but related organism."

## 2.5.3 Temporally resolved phylogenetic trees
 - "[B]ranch lengths are measured in _absolute time_ rather than in genetic divergence."

## 2.6 The transmission tree does not equate the phylogenetic tree
 - Transmission trees: "nodes represent known cases, and edges connecting nodes represent the directionality of who-infected-whom."
 - Phylogenetic trees are different. "First and foremost, genetic mutations are not markers that a transmissio nevent has occurred. Mutations occur spontaneously as the virus replicates, and this process is independent of whether the infection is passed on to another individual." "Secondly, phylogenetic trees are inferred from sequences that are sampled from infected individuals at the time that a specimen is collected, not at the time that a transmission event occurs."
 - "[T]he _sequence_ that is ancestral in a phylogenetic tree may not actually represent the _infection_ that is ancestral."

## 2.7 Why is sequencing better at dismissing links than confirming them?
 - Distinct genotypes with strong epi linkage are likely not true transmission links.
 - Similar genotypes with strong epi linkage may be true transmission links. "Their infections are likely related, but you can't tell from the genomic data who infected whom. Moreover, you can't actually tell whether the transmission is even _between_ these two cases." The transmission could have occurred at the same time from another source, or they could be infected by a distinct or shared common ancestor at the same or a different time. Tricky.

### 2.7.1 How many mutations are enough to rule linkage out?
 - Evolutionary rate and serial interval (time between infections) both have distributions, so we should think about these probabilistically.
 - As sequence divergence increases, the probability of case linkage decreases -- but by how much? This depends on the evolutionary rate and serial interval, and also the genome length.
 - For flu, the rate is high, and the serial interval and genome length short. For SC2, the rate is less high, the serial interval is still short, and the genome is longer. SC2's slightly slower evolutionary rate and longer genome give us  more resolution: tighter distributions and faster drop-off.
