

# Finding AMRs

[Antimicrobial resistance genes](https://en.wikipedia.org/wiki/Antimicrobial_resistance) (AMR genes) allow microbes to counteract the effects of antimicrobial drugs used to treat infections.
Databases such as the [NCBI Pathogen Detection Reference Gene Catalog](https://www.ncbi.nlm.nih.gov/pathogens/antimicrobial-resistance) and the [Comprehensive Antibiotic Resistance Database](https://card.mcmaster.ca) contain thousands of curated resistance genes and help make AMR-related data more widely available.

![](resources/images/finding-AMRs_files/figure-docx//1hYKF7Ss3vJ8rrUIH7ByNh1BUlRa2fhsJhq8MXzEowCc_g344ad28629a_0_440.png){width=100%}

In the **Finding AMRs module**, the **lecture** material will cover antibiotic resistance and concepts of genome assembly and genome annotation. In the **Prelab** activity, using `Galaxy` platform, we will assemble the prototype of gut microbiome using gut microbiome standard from Zymo Research.  We will first assemble the genomes into *contigs*, then visualize the contigs using `Bandage Image` tool, followed by screening contigs for AMRs using the tool [ABRicate](https://github.com/tseemann/abricate)antimicrobial genes using a variety of databases including the NCBI database. 
A similar strategy can be used to screen for virulence factors using databases such as the [Virulence Factor Database](https://pubmed.gov/34850947) (VFDB). For **Project** activity, students will perform *soil* genome assembly and in addition to annotating soil metagenomes with AMRs, we will assemble contigs into larger *MAGs*, and learn about annotating MAGs with tools like `GTDB-Tk`. 

![](resources/images/finding-AMRs_files/figure-docx//1hYKF7Ss3vJ8rrUIH7ByNh1BUlRa2fhsJhq8MXzEowCc_g344ad28629a_0_345.png){width=100%}

## Lecture - Finding AMRs

![](resources/images/finding-AMRs_files/figure-docx//165OHha9IYOctuyzg1CG0LwGxNnbC85JyJfMZT6xnYHw_g35f391192_00.png){width=100%}

[Slides: Finding AMRs](https://docs.google.com/presentation/d/165OHha9IYOctuyzg1CG0LwGxNnbC85JyJfMZT6xnYHw/edit?usp=sharing)

## Prelab - Finding AMRs

### Purpose

To use a Galaxy tools to perform *de novo* genome assembly of sequencing reads into contigs, visualize the contigs and find antimicrobial resistance (AMR) genes.

### Learning Objectives

Use Galaxy platform to:

1. Perform *de novo* genome assembly of long reads into ‘contigs’, using the `Flye` tool.
2. Visualize contigs with the `Bandage Image` tool
3. Identify AMRs in the contig assemblies using the `ABRicate` tool

### Introduction

Genome assembly is the process of reconstructing genomes from the DNA sequencing reads. Accurate and continuous genome assembly from sequenced fragments, even very long fragments, is challenging. `Flye`, is a long-read assembly algorithm that aims to produce highly contiguous genome assemblies and overcome some of the assembly challenges, like repetitive DNA sequences. Using `Flye` we will aim to reconstruct bacterial genomes and plasmids and enable detection of important genes implicated in anbibiotic resistance. Ideally, after assembly we want to get back circular contigs as that would typically indicate the identification of entire microbial genome(s) or plasmid(s)!

![](resources/images/finding-AMRs_files/figure-docx//1hYKF7Ss3vJ8rrUIH7ByNh1BUlRa2fhsJhq8MXzEowCc_g344ad28629a_0_459.png){width=100%}

Antimicrobial resistance is the ability of microbes to evade one or more antibiotics, leading to multidrug resistance and ability to survive and even thrive in the presence of antibiotics. Detecting and studying antibiotic-resistant pathogens is therefore extremely important to human health. However, the environmental reservoirs of resistance determinants are poorly understood. Certainly the indiscriminate and sometimes inappropriate use of antibiotics by humans (e.g. in the hospitals, in food production) has contributed to the emergence of resistant bacterial strains, but there are many other ways microbes can acquire AMRs. For example, the environment like soil is emerging as a key reservoir of these antibiotic resistance genes. For more information on AMRs see the following review articles: [10.1038/nrmicro2312](https://doi.org/10.1038/nrmicro2312) and [10.3390/antibiotics13121112](https://doi.org/10.3390/antibiotics13121112).

**Overview of the approximate minimum times for a job to be completed on Galaxy using specified tools.**

- Note, these times apply only to the specific input file we will be using in this activity, the `Zymo_Gut_Standard_D6331_subset` that is ~342.5MB, and will take longer (or much longer) for larger (or much larger) input files.

| Flye | Bandage Image | ABRicate |
| :--| :--| :--|
| 5 min | < 5 min | < 5 min |


### Activity 1 – Flye assembly

*Estimated time: 45 min*

::: {.notice} 
The sample used in this activity is the [Zymo Gut Microbiome Standard](https://www.zymoresearch.com/products/zymobiomics-gut-microbiome-standard?srsltid=AfmBOoqP_zq131c2GTidPCM0j6yA3JFcGQ0haUNu1jAJI9RQ9qsXLYSF), sequenced by Pacific Biosciences using PacBio Sequel II Instrument, and corresponds to sequencing read file SRR13128014. A subset of this data is used in this Activity.
:::

#### Instructions

**1. Run Flye assembly tool in Galaxy using <mark style="background-color: yellow">Zymo Gut Standard D6331 subset2</mark> to assemble gut microbial genomes.**

a. Obtain **.fastq** file from `Zymo_Gut_Standard_D6331_subset2`: [https://usegalaxy.org/u/valerie-g/h/zymo-gut-standard-d6331-subset2](https://usegalaxy.org/u/valerie-g/h/zymo-gut-standard-d6331-subset2).

b. Name your new history **“Finding gut AMRs”**.

c. Run **Flye** tool to assess sequence quality using the following Tool Parameters:

    - Under **Input Reads**: select your `aymo_gut_standard_D6331_subset2` **.fastq** dataset.
    - Under **Mode**: select `PacBio HiFi (--pacbio-hifi)` option, since the sequences were obtained using PacBio HiFi sequencing technology.
    - Under **Perform metagenomic assembly**: select `Yes`.
    - Under **Generate a log file**: select `Yes`.

![](resources/images/finding-AMRs_files/figure-docx//1hYKF7Ss3vJ8rrUIH7ByNh1BUlRa2fhsJhq8MXzEowCc_g33689793048_0_0.png){width=100%}

![](resources/images/finding-AMRs_files/figure-docx//1hYKF7Ss3vJ8rrUIH7ByNh1BUlRa2fhsJhq8MXzEowCc_g33689793048_0_10.png){width=100%}

**2. View Flye results** - Explore Flye output files and answer questions below.

![](resources/images/finding-AMRs_files/figure-docx//1hYKF7Ss3vJ8rrUIH7ByNh1BUlRa2fhsJhq8MXzEowCc_g33689793048_0_21.png){width=100%}

#### Questions

**1. Explore Flye tool purpose and output.**

|1A. In your own words describe the purpose of Flye based on the Introduction section, and from the 'Purpose' section of Flye tool description.|
|:--|
| <br> |


|1B. How many Flye output files did you get back, and what are they?|
|:--|
| <br> |

|1C. What are the file extensions (formats) for the following Flye output files?|
|:--|
| consensus |
| graphical fragment assembly | 
|<br>| 

**2. Explore Flye log report file.**

|2A. Based on your Flye output `log report file`: At the very bottom of the very long file find how many bases were assembled. What is the `Total length`?|
|:--|
|<br> |

|2B. Based on your Flye output `log report file`: At the very bottom of the file find the length of the longest assembled fragment? Look for `Largest frg`?|
|:--|
|<br> |

|2C. What proportion of input was assembled into contigs?|
|:--|
| *At the very top of the log file you will find that the input number of bases was 177,760,975 (Look for Total read length). Compare to the total length after assembly from your answer to question 2A above` |
|<br> |

**3. Explore Flye assembly info file.**

|3A. Based on your Flye output `assembly info file` sorted by contig length (high to low, in base pairs, bp) - What is the longest `contig size?|
|:--|
|<br> |

|3B. Based on your Flye output `assembly info file` sorted by contig length (high to low, in base pairs, bp) - What is the shortest contig size?|
|:--|
|<br> |

**4. Explore Flye output consensus file (in FASTA format).**

|4A. What is the beginning line of the FASTA format?|
|:--|
| <br>|

|4B. How does FASTA sequence format differ from FASTQ sequence format?|
|:--|
|*See this link for a quick summary comparison of the 2 formats [https://compgenomr.github.io/book/fasta-and-fastq-formats.html](https://compgenomr.github.io/book/fasta-and-fastq-formats.html)*|
|<br> |

**5. Test your general understanding of genome assembly.**

|5A. Summarize your experience with assembling a genome with Flye.|
|:--|
| *E.g., were you surprised at the percentage of assembled input, at the length of the largest contig, at the abundance of linear contigs, or anything else?*|
|<br> |

|5B.  What would you want the ideal genome assembly tool to do?|
|:--|
| <br>|

### Activity 2 – Visualizing contigs

*Estimated time: 15 min*

#### Instructions

Run **Bandage Image** tool in Galaxy on your Flye: **graphical fragment assembly** output (in gfa1 format) using default parameters.

#### Questions

|1. Paste the resulting image below.|
|:--|
| <br>|

|2. Describe contig profile based on the Bandage Image.|
|:--|
|<br> |

|3. Do you expect to obtain more contigs, larger or circular contigs with more sequencing reads? why?|
|:--|
|<br> |

### Activity 3 – Finding AMRs

*Estimated time: 30 min* 

#### Instructions

1. Run **ABRicate** tool in Galaxy using Flye **consensus** as input using the following `Tool Parameters`:

- Under **Input Reads**: select your Flye: consensus output in FASTA format
- IMPORTANT: Under **Advanced Option**s: select `NCBI Bacterial Antimicrobial Resistance Reference Gene Database` as your database option; the default‘resfinder’ may not work well.

2. Explore **ABRicate report file**.

**Abricate output report** has the following information:

|Column |Description |
|:--| :--|
|FILE | The filename this hit came from |
| SEQUENCE | The sequence in the filename |
| START | Start coordinate in the sequence |
| END | End coordinate in the sequence |
| GENE | ABR gene name |
|COVERAGE | What proportion of the gene is in our sequence |
| COVERAGE_MAP | A visual of coverage map (gaps or no gaps)|
| GAPS | Was there any gaps in the alignment - possible pseudogene? |
| %COVERAGE | Proportion of gene covered |
| %IDENTITY | Proportion of exact nucleotide matches |
| DATABASE | The database this sequence comes from |
| ACCESSION | The genomic source of the sequence |
|<br>| |

3. Answer questions below.

#### Questions

**1. Explore Abricate output report.**

|1A. How  many AMR genes were detected? This is the number of rows in your file.|
|:--|
|<br>|

|1B. How many DIFFERENT AMR genes were detected and what are their GENE names?|
|:--|
|<br>|

|1C. What are the different AMR genes resistant to? What is their RESISTANCE? |
|:--|
|<br>|

|1D. How many DIFFERENT contigs had AMRs? |
|:--|
|<br>|

**2. Research an AMR gene.**

- Use any search tools for your research, but we encourage you to use PubMed [https://pubmed.ncbi.nlm.nih.gov/](https://pubmed.ncbi.nlm.nih.gov/) where you can find many scientific articles on the topic if you search for e.g. your AMR gene name, or resistance name or using a sentence as input. Talk about anything of interest, e.g., which microbes have the AMR of interest, what is the substance to which the gene shows resistance to, where could the resistance to this substance come from, what are possible health implications, etc.

|2A. Research and write a small paragraph report on one of the AMR genes.| 
|:---|
| <br>|

|2B. Ask one question you want to know about AMRs?| 
|:---|
|<br> |

### Grading Criteria

- <mark style="background-color: yellow">Download as Microsoft Word (.docx) and upload on Canvas</mark>.

### Footnotes

**Resources**

- Google Doc

**Contributions and Affiliations**

- Valeriya Gaysinskaya, Johns Hopkins University
- Frederick Tan, Johns Hopkins University

Last Revised: May 2025




## Discussion - Finding AMRs

### Activity

*Estimated time: 25 min*

#### Instructions

1. Form new groups of four

- [https://docs.google.com/spreadsheets/d/11eoJgm9mehxGWWzh8IZYDCDmnCmSyshopPYHewvpC8c/edit?usp=sharing](https://docs.google.com/spreadsheets/d/11eoJgm9mehxGWWzh8IZYDCDmnCmSyshopPYHewvpC8c/edit?usp=sharing)

2.Gather into groups (10 min)

a. Discuss -- Each group member briefly describes their answers to prelab assignment

b. Summarize -- Identify best answer and add it to slidedeck

- [https://docs.google.com/presentation/d/1ZC8yjuk8V5pt3yh1p4_jkhTw0Pu4mHViAmNF-UPWAHs/edit?usp=sharing](https://docs.google.com/presentation/d/1ZC8yjuk8V5pt3yh1p4_jkhTw0Pu4mHViAmNF-UPWAHs/edit?usp=sharing)

3. Share your group discussion (2 min each group)


## Project - Finding AMRs

### Purpose

To explore soil metagenomics using Galaxy tools for de novo genome assembly (Flye), assembled contig visualization (Bandage),  finding antimicrobial resistance (AMR) genes (ABRicate) and binning contigs into larger groups/bins (MetaBAT2). You will also explore information about the taxonomic classifier GTDB-Tk.  This will allow you to compare genomic assemblies and AMRs between soil and Zymo gut standard.


### Learning Objectives

1. Use **Galaxy** tools to
2. Use **Flye** tool to perform de novo genome assembly of long reads into ‘contigs’ 
3. Visualize the contigs with **Bandage** visualization tool
4. Use **ABRicate** tool to find AMRs in contig assemblies
5. Use **MetaBAT2** to bin contigs into larger MAGs
6. Learn about **GTDB-Tk** taxonomy classifier tool

### Introduction

In this activity we will practice *de novo* metagenome assembly with `Flye`, using **soil** sample sequenced by Nanopore sequencing. We will have an opportunity to compare and contrast assembled contigs and antimicrobial resistance profiles of soil and gut and think about the differences and similarities in microbial diversity of the two environments.


In this project you will also learn about MetaBAT2 and GTDB-Tk. Let's start now. The most up to date long read metagenomics workflow includes contig assembly (e.g. using Flye tool), followed by contig binning into larger metagenome-assembled genomes (MAGs) (with e.g. MetaBAT2 tool) and finally MAG classification (e.g. with GTDB-Tk). MetaBAT2 is an algorithm that bins (or groups) sequence fragments (contigs) into larger MAGs or draft genomes. Subsequently, MAGs can be taxonomically classified by GTDB-Tk.


`You will not be executing GTDB-Tk in this activity to stay within a reasonable activity time frame.` However, for your project work, you will have a chance to test GTDB-Tk on your genome assemblies and bins. A note to your future self working on a project - as a rule, after genome assembly, if your contigs are 500 kb or above, they will be considered large enough to be passed on to GTDB-Tk without the need for binning. Contigs of < 500 kb will be binned and passed on to GTDB-Tk for taxonomy classification as bins.

**Overview of the approximate minimum times for a job to be completed on Galaxy using specified tools.** 

- Note, these times apply only to the specific input file we will be using in this activity, the nanopore-soil-subset that is 5.4 GB.

| Flye | Bandage | ABRicate | MetaBAT2|
| :--|:-- |:--  | :-- | 
|5 hours | < 5 min | < 10 min | < 10 min|

### Activity 1 – Genome assembly with Flye

*Estimated time: 30 min (activity time DOES NOT include the Flye run time on Galaxy)*

::: {.notice} 
The sample used in this activity is from the [BioDIGS Project](https://biodigs.org/#about), sequenced using Oxford Nanopore Technologies’ [PromethION Instrument](https://nanoporetech.com/products/sequence/promethion). A subset of this data is used in this Activity.
:::

#### Instructions

1. Run Flye in Galaxy on quality filtered (with fastp tool) <mark style="background-color: yellow">nanopore soil pilot subset</mark> [nanopore-soil-subset-filtered](https://usegalaxy.org/u/valerie-g/h/nano-pore-soil-subset-filtered) to de novo assemble soil microbial genomes. 

a. Obtain .fastq file from a subset of Nanopore-sequencing soil study.

    - [https://usegalaxy.org/u/valerie-g/h/nanopore-soil-subset-filtered](https://usegalaxy.org/u/valerie-g/h/nano-pore-soil-subset-filtered).

b. Name your new history **Finding soil AMRs**.

c. Run **Flye** tool to assess sequence quality using the following **Tool Parameters**.

    - Under **Input Reads**: select your nano `pore-soil-subset-filtered` **.fastq** dataset.
    - Under **Mode**: select `--nano-raw` option, since the sequences were obtained using Nanopore sequencing technology.
    - Under **Perform metagenomic assembly**: select `Yes`.
    - Under **Generate a log file**: select `Yes`.

2. Explore Flye output **assembly info** file which is sorted by length (in base pairs, bp) of the contig (high to low). 

#### Questions 

| 1. How many contigs were assembled?|
|:-----|
|*Note: Since each contig is represented by a separate row (or line) in the assembly info file, simply clicking on the assembly info file and recording the number of lines listed in the file will correspond to the number of contigs*|
|<br> | 

| 2. What is the longest contig size?|
|:-----|
|<br> | 

| 3. What percent of input was assembled into contigs? |
|:-----|
|- *Hint 1: In the log file, find the input number of bases going into flye assembly - this info corresponds to the "Total read length" value on top of the log file.*| 
|- *Hint 2: In the log file, find the output number of bases after flye assembly - this info corresponds to the "Total length" value on the bottom of the log file.* |
|- *Hint 3: calculate percent of input assembled into contigs using the 2 input and output values you obtained above.*|
| <br> | 

| 4. Why do you think only a small fraction of reads was assembled into contigs? |
|:-----|
|<br> | 

**5. Compare soil assembly to the Zymo gut standard assembly provided the following observations:**

- For this activity you can consult back to your Prelab: Finding AMRs.
- The number of contigs assembled from **342.5 MB** of sequencing data from the Zymo gut standard D6331 subset was **289**, much smaller than for the filtered soil sample of 5.5 GB! Yet, the largest contig size for the Zymo gut standard was over 2 million bases (almost 10 times larger) and circular (while the largest contig for the soil sample was smaller and linear).

| 5A. Why do you think the number of contigs in the soil sample was so much higher than the number of contigs in the Zymo gut standard?  |
|:-----|
|- *Hint 1: it is NOT because of the difference in the size of the sequencing file.*| 
|- *Hint 2: Think about possible differences in the microbial diversity of the two samples.* |
|<br> | 

| 5B. Why do you think it was possible to assemble a much larger and circular contig with the Zymo gut standard sample compared to the soil sample? |
|:-----|
| <br>| 


### Activity 2 – Contig visualization with Bandage

*Estimated time: 15 min *

#### Instructions

1. Run **Bandage** Image tool in Galaxy to visualize contigs. 

- Run **Bandage Image** tool  in Galaxy using  your **Flye: graphical fragment assembly file** (in gfa1 format) as input, using default parameters.

#### Questions

| 1. Paste the resulting image below. |
|:-----|
|<br>  |  

| 2. Describe contig profile based on the Bandage Image result. |
|:-----|
|<br>  | 


### Activity 3 – Finding AMRs

*Estimated time: 30 min*

#### Instructions

1. Run **ABRicate** tool in Galaxy using Flye consensus as input using the following **Tool Parameters**:

    - Under **Input Reads**: select your `Flye: consensus` output in FASTA format.
    - IMPORTANT: Under **Advanced Options**: select `NCBI Bacterial Antimicrobial Resistance Reference Gene Database` as your database option; the default ‘resfinder’ may not work well.

2. Explore **ABRicate report** file.

    - Note, Abricate output report has the following information.

|Column |Description |
|:--| :--|
|FILE | The filename this hit came from |
| SEQUENCE | The sequence in the filename |
| START | Start coordinate in the sequence |
| END | End coordinate in the sequence |
| GENE | ABR gene name |
|COVERAGE | What proportion of the gene is in our sequence |
| COVERAGE_MAP | A visual of coverage map (gaps or no gaps)|
| GAPS | Was there any gaps in the alignment - possible pseudogene? |
| %COVERAGE | Proportion of gene covered |
| %IDENTITY | Proportion of exact nucleotide matches |
| DATABASE | The database this sequence comes from |
| ACCESSION | The genomic source of the sequence |

#### Questions

| 1. How  many AMR genes were detected? This is the number of rows in your file. |
|:-----|
| <br> | 

| 2. How many DIFFERENT AMR genes were detected and what are their GENE names? |
|:-----|
|<br>  | 

| 3. What are the different AMR genes resistant to? What is their RESISTANCE? |
|:-----|
|<br> | 

| 4. How many DIFFERENT contigs had AMRs? |
|:-----|
|<br> | 

**5. Research and write a small paragraph report on one of the AMR genes you found.**

    - Use any search tools for your research, but we encourage you to use PubMed [https://pubmed.ncbi.nlm.nih.gov/](https://pubmed.ncbi.nlm.nih.gov/) where you can find many scientific articles on the topic if you search for e.g. your AMR gene name, or resistance name or using a sentence as input.
    - Talk about anything of interest, e.g., which microbes have the AMR of interest, what is the substance to which the gene shows resistance to, where could the resistance to this substance come from, what are possible health implications, etc.

| 5A. Report on one of the AMR genes you found. |
|:-----|
| <br>| 

| 5B. Why do you think the AMRs you found in soil differ from the AMRs you found in the gut (from your pre-lab)? |
|:-----|
|<br> | 

### Activity 4 – Bin contigs with MetaBAT2

*Estimated time: 20 min*

#### Instructions

1. In Galaxy, find and click on **MetaBAT2** tool and explore tool parameters.
2. Run **MetaBAT2** tool in Galaxy using `Flye consensus` as input using the **following Tool Parameters**:

- Under **Fasta file containing contigs**: select your Flye: consensus output in FASTA format.
- Under **Output options**: from the **Extra outputs** dropdown menu select: `Process log file`.

#### Questions

**1. Explore MetaBAT2 tool and parameters.**

| 1A. What is the function of MetaBAT2 tool based on Galaxy tool description on top? |
|:-----|
|<br> |  

| 1B. Under Tool Parameters for MetaBAT2, find and record below the Minimum size of a contig for binning (a value given in basepairs, bp). |
|:-----|
|<br> | 

| 1C. Under Tool Parameters and Output options for MetaBAT2, find and record below the Minimum size of a bin as the output. |
|:-----|
|<br> | 

**2. Explore MetaBAT2 tool output.**


| 2A. Open MetaBAT2 Process log output file and record how many bins were formed from contigs. |
|:-----|
|<br> |  

| 2B. Open MetaBAT2 Process log output file and record how many bases in total  were used to form bins. |
|:-----|
| <br>| 

| 2C. What percent of contig bases formed bins (given that 154,251,885 bases were in Flye output)? |
|:-----|
| <br>| 

| 2D. Based on percent of contigs that formed bins (from activity 4-2.1 above) did metaBAT2 do a good job of binning the contigs? |
|:-----|
|<br>  | 

**3. Examine MetaBAT2 Bin sequences output, which is a `DATASET COLLECTION`, where each collection is a separate bin.**

| 3A. Click on the MetaBAT2 Bin sequences output. How many bins (or Galaxy ‘folders’) are there? |
|:-----|
|<br> | 

| 3B. Click on the MetaBAT2 Bin sequences output and then on bin 1. Without ‘eyeballing’ the fasta file, note how many sequences (contigs) were included in bin 1. |
|:-----|
|<br> |  

| 3C. Click on the MetaBAT2 Bin sequences output and then on bin 2. Without ‘eyeballing’ the fasta file, note how many sequences (contigs) were included in bin 2? |
|:-----|
| <br>| 

### Activity 5 – Read about GTDBtk tool in Galaxy 

*Estimated time: 15 min*

#### Instructions

1. In Galaxy, find and click on **GTDB-Tk Classify genomes.** 

#### Questions

| 1. Read the GTDB-Tk Classify genomes tool’s “What it does” part  and summarize what GTDB-Tk does. |
|:-----|
|<br> | 

| 2. What is the ideal input sequence for GTDB-Tk classification: 1) raw sequences, 2) contigs or 3) large contigs(>500kb) and MAGs? |
|:-----|
|<br> | 

**3. Visit [https://gtdb.ecogenomic.org/stats/r220](https://gtdb.ecogenomic.org/stats/r220) to explore the database and database statistics.**

| 3A. How many bacterial species are present in GTDB database Release 220? |
|:-----|
|<br> | 

| 3B. Scroll through website . Although it has a lot of complex information, what is one thing you found interesting about GTDB-Tk content? |
|:-----|
|<br> | 

### Grading Criteria

    - <mark style="background-color: yellow">Download as Microsoft Word (.docx) and upload on Canvas</mark>.

### Footnotes

**Resources**

- Google Doc

**Contributions and Affiliations**

- Valeriya Gaysinskaya, Johns Hopkins University
- Frederick Tan, Johns Hopkins University

Last Revised: June 2025


## Presentation - Finding AMRs

### Activity

*Estimated time: 25 min*

#### Instructions

1. Open the “Finding AMRs Presentation” slidedeck

- [https://docs.google.com/presentation/d/1AXZkQ0CyIasnkwyz0uvPsFic9eFrnPDQX_DbyffNmxQ/edit?usp=sharing](https://docs.google.com/presentation/d/1AXZkQ0CyIasnkwyz0uvPsFic9eFrnPDQX_DbyffNmxQ/edit?usp=sharing)

2. Create slides covering at least two of these topics

a. Summarize the metagenome assembly statistics for the BioDIGS soil sample (Results).

b. Report on one of the AMR genes you found (Discussion).

c. Describe GTDB and the associated GTDB-Tk software toolkit (Methods).


3. Iterate your slides being sure to:

a. Add bullet points on key details you understand (Notice) and questions you have (Wonder).

b. Include one or more plots or images that support your points.

c. Create slide titles that summarize your main takeaway.

4. Present at next class (5 min each group).

#### Footnotes

**Contributions and Affiliations**

- Valeriya Gaysinskaya, Johns Hopkins University
- Frederick Tan, Johns Hopkins University

Last Revised: February 2025





