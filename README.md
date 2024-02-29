# Genomic-Data-Science-Notes

-
  > Part 1 of 6 Specialization | **Genomic Data Science**  
{Coursera Certificate Link} ([Introduction to Genomic Technologies](https://coursera.org/share/3ceea7a4a77868012aeaf2425948b49d))  
-
---
- ### Introduction 
---
- **Why Genomics?**
	- We have unique identity but same cell structure or function
	- We are 99.9% identitical
	- To study cancer
	- Proteins self-regulate
	- NCBI - SRA [Sequence Read Archive]
	-
- **What is Genomics?**
	- The branch of molecular biology concerned with the structure, function, evolution and mapping of genomes.
	- Structure
		- 23 chromosomes pairs
		- A, C, G, T -> Nucleotides
	- Function
		- Instructions are present
	- Evolution
		- How sequences change over evolutionary time
		- Generation to generation are very slow
	- Mapping
		- where are the genes and other interesting bits
	- The branch of molecular genetics concerned with the study of genomes, specifically the identification and sequencing of their constituent genes and application of this knowledge in medicine, pharmacy, agriculture, etc.

- **Genomics vs Biology & Genetics**
  | Criteria | Genomics | Genetics & Biology |
  |---|---|---|
  | Scope | Studies considering all genes in a genome | Targeted studies of one or a few genes |
  | Technology | Global, high-throughput experiments | Targeted, low-throughput experiments |
  | Hard part | Tons of data, uncertainty, computation | Clever experimental design, painstaking experimentation |
- **What is Genomic Data Science**
	- Biology <-> Statistics <-> Computer Science
	- Process
		- 1) Experimental Design
		- 2) Alignment & Assembly
		- 3) Preprocessing & Normalization
		- 4) Statistics & Machine Learning
		- 5)
	- RNAC - set of experiments
	- What is studied ->
		- Population Genomics
		- Integrative Genomics / Systems Biology
-
- **Cell Biology Pre-req**
	- Prokaryotes -> Bacteria + Archaea (nucleoid, no nucleus)
	- Eukaryotes (cell nucleus)
	- Mitochondria has it's own DNA
	- Mitochondria may have been a prokaryote ages ago and it could have been taken up by eukaryotes (just a theory)
	- Mitosis -> Cell divides to two cells
	- DNA replication happens before Mitosis
	- Diploid -> 2 copies - one from dad, other mom ... like that
	- Stem cells have the capabilities of dividing and differentiating into mature cells of different types.
		- Meiosis -> happens during reproduction -> it has re-combination which happens by accident (crossing over)
-
- **Important Molecules in Molecular Biology**
	- Purines - Adenine , Guanine
	- Pyrimidines - Cytosine , Uracil , Thymine
	- Phosphate deoxyribose backbone
	- A - T
	- G - C
	- 5' is first & 3' is always second -> positive strand
	- 3' is first & 5' is always second -> negative strand
	- RNA -> A G C U -> not inheritance, make proteins
	- DNA -> A G C T -> inheritance
	- RNA Translation -> Protein Synthesis
	- mRNA is a copy of DNA in which T is changed to U
	- Codon - 3 letters of RNA encodes an amino acids
	- 20 amino acids (+2 more recently discovered)
	- 64 codons in human and 3 are stop codons

 - **The Human Genome Project**
	- Biology's Manhattan project
	- 1989 -> DOE USA + NIH
	- sequence 3 billion basepairs for $1 / base by 2005 -> Goal
	- 1998 -> the race starts
	- Feb 2001 research paper - rough number - 30k to 40k genes (THGP)
	- 26588 + around 12k unique ones (Celera)
	- Today's Genome - 99.99% only
	- Achievements :
		- $1 / base ? -> $1 / 700 bases
		- by 2005 ? -> done in 2001
		- Cost today -> $1 per 3,000,000 bases ; 4000-fold cheaper
-
- **Molecular Biology Structures**
	- naked duplex DNA -> beads on a string formed of nucleosomes -> 30nm solenoid -> extended form of chromosome -> condensed section of chromatin -> mitotic chromosome
	- Repeats ->
		- Tandem Repeats - ATTCG _ ATTCG _ ATTCG
		- Interspersed Repeats - ACACAC ___*____ ACACAC __*_____ ACACAC => Cause problems since they seem similar
		- The structure of a typical human protein coding mRNA including the untranslatedd regions (UTRs)
		- 5' || 5' UTR || start ---- coding sequence (cds) ---- stop || 3' UTR || Poly-A tail || 3'
		- Alternative splicing -> forming combinations of exons
		- DNA methylation (methyl group - an epigenetic factor found in some dietary sources can tag DNA and activate or repress genes
-
- **Genotype to Phenotype**
	- The human [genetic code](https://byjus.com/biology/genetic-code/) could be found by their genotype. It determines the traits which will be expressed. Organisms that look the same do not have the same genotype. Biological tests can determine genotype.
	- The phenotype is determined by an individual’s genotype and expressed [genes](https://byjus.com/biology/genes/) or by visible traits, for instance, hair colour or type, eye colour, body shape, and height. It depends on the genotype but is also influenced by environmental factors.
	-
	  | **Genotype** | **Phenotype** |
	  |---|---|
	  | The hereditary information of the organism is in the form of genes in the DNA and remains the same throughout the life. | The characteristics of an organism which are visible are known as phenotypes. |
	  | The same genotype produces the same phenotype. | The same phenotype may or may not belong to the same genotype. |
	  | Present inside the body as genetic material. | Expression of genes as the external appearance. |
	  | The genotype is inherited from the parent to the offspring. | The phenotype is not inherited from the parent. |
	  | It can be determined by scientific methods such as the polymerase chain reaction. | It can be determined by observing the organism. |
	  | It is affected by genes. | It is affected by genotype and environmental conditions. |
	  | For e.g., Blood group, eye colour, height, and genetic diseases. | For e.g., Weight, physique, and beak of birds |
	- Genome wide Association studies
-
- ### Measurement Technology
---
- **Polymerase Chain Reaction**
	- Genome assembly refers to a computational method for reconstructing chromosomes from short reads.
	- How do we make copies of DNA?
		- DNA sticks to itself -> Hybridizes
		- Primers - 15 to 20 bases long
		- What we do -> Primers + DNA -> Heat gently -> Anneal (cool down gently)
		- DNA polymerase -> copy machine basically
		- polymerase fills up
		- Result after one round -> 2 strains are obtained
		- This is why its called chain reaction
		- primer stick to DNA during annealing and then DNA polymerase builds up the rest.
		- Ingredients : DNA , primers , DNA polymerase , A C G T
		- Recipe : melt at 94 degree C, Cool to 54 degree C, warm to 72 degree C, step 1
 
- **Next Generation Sequencing (NGS)**
	- Sanger DNA sequencing 1977 to 1990s
	- DNA Microarrays since mid-1990s
	- 2nd Generation DNA Sequencing since 2007
	- 3rd Generation & single molecule sequencing since 2010 (not matured)
	- TEMPLATE - Chop DNA up into single stranded fragments and attach to a slide -> PCR -> Use PCR to make clusters of identical fragments
	- We use laser to get lights to identify (florescence)
	-
- **Applications of Sequencing**
	- NGS applications -> basic idea : 1. convert molecule to DNA 2. Apply 2nd gen sequencing
	- 1. Exon sequencing -> 1.5% of genome (30 to 60 million order of basis)
	  Exonic DNA binds to complementary DNA on beads (magnetic) attached to a chip  
	- 2. Capture mature RNA by poly(A) tail
	  Reverse Transcribe into complementary DNA (cDNA)  
	- 3. ChIP-Seq -> where may it bind?
	  Cross-link protein to DNA to stick / freeze and now we can fragment DNA after which we can use Anti-body pulldown to remove the protein. Now we have a sequencing problem.  
	- 4. Bisulfate sequencing / Methelsync - so where on the genome the DNA has been methylated, so methylation is this important epigenetic modification that also affects which proteins are being expressed in the cell. Methylation can be from round to round. Methyl groups are only attached to Cs. So what we do is C -> U. Now we sequence and compare. This way we identify where methylation happens.
-
- ### Computing Technology
---
- **What is Computer Science**
	- Theory <-> Systems <-> Applications
	- Think Computationally
	- Good Code is Hard
- **What are Algorithms**
	- Algorithms don't need computers
	- Series of instructions
	- sorting / optimization / searching
	- Efficiency matters when we have huge data
- **How we store data**
	- Data structures
	- Pointers -> Address
	- DNA = { A , C , G , T }* -> 00 01 10 11
	- Introns -> GT ------ AG -> cause problems
- **Efficiency**
	- Traveling Salesman problem
	- Optimizations
- **Software Engineering**
	- Considering all dimensions of a software
	- Why do we need to understand genomics software?
		- RNA editing example ->-> DNA -> RNA -> RNA can be different and only 1 or 2 nucleotide is affected. Used to regulate genes.
		- How can we detect RNA editing?
			- Alignment reveals RNA-DNA differences
		- Are the differences real?
			- Mostly... but 1 mis-alignment in 1 million... yields 100s of errors in large genomic datasets
			- Needs to handle all possible cases
	- Trust, but verify -> Understand your algorithms and how they can go wrong.
	- Just because it runs doesn't mean it's free of bugs
- **What is Computational Biology Software**
	- Raw data must be transformed
	- "ANALYSIS Pipelines"
		- DNA ---> Brilliant Insights
	- NCBI Genome Workbench
	- Genetic Variant Calling
	- RNA-seq : is a high-throughput technology that provides insights into the transcriptome. It has many applications, including : quantifying genes and isoforms, detecting non-coding RNA, alternative splicing, splice junctions, so on.
	- An RNA-seq pipeline ---> Bowtie2 fast alignment -> TopHat2 Spliced alignment -> Cufflinks transcript assembly + Quantitation -> Cuffdiff2 differential expression
	- Pipelines evolve
	- Next-gen ---> Bowtie2 -> HISAT -> StringTie -> Ballgown
	- SOFTWARE CHOICE MATTERS!

 - - ### Data Science Technology
---
- **Why care about Statistics?**
	- Causes scandals XD
	- Lack of statistics causes problems both high scale and low scale
- **What went wrong?**
	- What went wrong in the Duke analysis?
		- Lack of transparency - the data and code weren't reproducible
		- Lack of co-operation
		- Lack of expertise - Silly prediction rules & had study design problems & their predictions weren't locked down
- **The Central Dogma of Statistics**
	- Population -> problem making -> optimised methods -> inference
	- Knowing the population
	  logseq.order-list-type:: number
	- Variability of Population should be known
	  logseq.order-list-type:: number
- **Data Sharing Plans**
	- The raw data
	- A tidy data set - one variable per column, one observation per row, one table per kind of variable linking indicators for columns
	- A code book describing each variable and its values in the tidy data set -  Variable names, descriptions, units, study design quirks
	- An explicit and exact recipe you used to go from 1 -> 2,3 - R/Python code, input raw data -> output tidy, no parameters
	- Explicit instructions , versions of software , parametrs included
	- Avoid Vague instructions, missing versions, skipped steps
- **Getting Help with Statistics**
	- collaborations
	- pet bioinformaticians (avoid solo)
	- know it yourself
- **Plotting Your Data**
	- Show raw data also if possible, not just box plot.
	- Plotting replicates - R1 vs R2 -> be careful of the scale and use transformations (log and other functions)
	- ridiculogram : meaningless albeit visually impressive image of a network
- **Sample Size & Variability**
	- We also get variability estimates
	- $N = Number Of Measurements$
	  $N = (Money You Have)/(Money Per Measurement)$  
	- Power ->
	- Variability : 3 kinds
		- Phenotypic variability
		- Measurement error
		- Natural biological variation
		- $Var(Genomic Measurement) = PhenotypicVariability + Measurement Error + Natural Biological Variation$
		- Biological Variance does not get eliminated by Technology
- **Statistical Significance**
	- t-statistic -> less likely difference if small, most difference if large
	- p - value -> p - values which are low are very significant.
	- p - value -> The probability of observing a statistic that extreme if the null hypothesis is true.
	- The p-value is not :
		- Probability the null is true
		- Probability the alternative is true
		- A measure of statistical evidence
- **Multiple Testing**
	- Family wise error rate
	- False discovery rate
	- Avoid publication bias
	- Don't hack statistics
- **Study Design, Batch Effects & Confounding**
	- Confounder is a variable on which 2 variables may vary, but these 2 variables aren't related.
	- Without randomization, the confounding variable differs among treatments
	- With randomization, the confounding variable does not differ among treatments
	- Stratification - design experiments about known confounders.
	- Good designs
		- Balanced
		- Replicated
		- Has Controls
	-
	-
- COURSEWORK
	- ([Microbial Genes in the Human Genome: Lateral Transfer or Gene Loss?](https://d3c33hcgiwev3.cloudfront.net/_669db620ef363727a43d57b59bcbbc11_Salzberg-etal-Science2001-annotated.pdf?Expires=1709164800&Signature=WLflOpTcuZSeBurfQUBVyAJA9HeG3unSsO5pCk73EXyhQ0pYJszWeKEc7pCWjX0PU5JJj-gJJqze49czliL7HuTbFTjvfa7BMRwgdJiCSMPnHJFMWM8AadqiAs3HcMh4QQWzZ2f3wdLXgR-9ljEQ39unuqBSfbOtlD5DeP0ZjWo_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)) {annoted}
	- [Microbial Genes in the Human Genome: Lateral Transfer or Gene Loss?](https://d396qusza40orc.cloudfront.net/genintro/misc/Salzberg-etal-2001-Science.pdf) {magazine section}
-
-
  > Part 2 of 6 Specialization | **Genomic Data Science**  
{Coursera Certificate Link} ([Python for Genomic ](https://coursera.org/share/3ceea7a4a77868012aeaf2425948b49d))  
