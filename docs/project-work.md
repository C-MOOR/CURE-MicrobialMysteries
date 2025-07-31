# (PART\*) Project Work {-}

<!-- Set up code -->


# Kickstart Project Work

<h2>Purpose</h2>

The purpose of **Project Work** is to gain practice in scientific exploration and research, communication, and work on your scientific poster! The purpose of **Kickstart Project Work** lab is to kick off project work with reviewing project work goals, setting up project work expectations, and modeling getting started with data import and analysis.

![](resources/images/project-work_files/figure-docx//1hYKF7Ss3vJ8rrUIH7ByNh1BUlRa2fhsJhq8MXzEowCc_g370690c0d46_0_46.png){width=100%}

<h2>Learning Objectives</h2>

1. Capstone Project Overview - Testing Ideas
1. Practice drafting hypothesis
1. Obtain data and run analysis


## Lecture - Kickstart Project Work

![](resources/images/project-work_files/figure-docx//1j1u4frdYt18nVmjMs6ZPRoP1KfXxognVUYG-2itH6kE_g35f391192_00.png){width=100%}

[Slides: Possible Datasets](https://docs.google.com/presentation/d/1j1u4frdYt18nVmjMs6ZPRoP1KfXxognVUYG-2itH6kE/edit?usp=sharing)


## Activity - Kickstart Project Work

### Learning Objectives

1. Import an example SRA sequencing data file by accession id (e.g. SRR) 
2. Perform classification of nanopore-sequenced soil MAGs with GTDB-Tk
3. Import an SRA dataset you would like to analyze for your research project
4. Use a new Galaxy tool that we have not worked through in class


### Activity 1 - Import an SRA file into Galaxy

#### Instructions

1. Upload sequencing reads for accession id SRR29980924 in Galaxy using **Faster Download and Extract Reads in FASTQ** tool .
2. Make your Galaxy history sharable.

#### Questions

|1. Share your Galaxy history with SRR29980924fastq data you downloaded with Faster Download and Extract Reads in FASTQ tool.|
|:--------|
| Galaxy history Link: |
<br>


|2. Find and record the following features of your downloaded dataset below.|
|:--------|
| File size: |
|File format:|
|Job Runtime (Wall Clock):|
|First line of the sequencing file:|
<br>

|3. Inspect SRR29980924 entry in NCBI https://www.ncbi.nlm.nih.gov/sra. Obtain the following sequencing information.|
|:--------|
|Organism: |
|Instrument:|
|Strategy:|
|Run:|
<br>

### Activity 2 – Taxonomically classify nanopore-soil-subset MAGs with GTDB-Tk in Galaxy

#### Instructions

Using **GTDB-Tk Classify genomes** tool, classify the nanopore-soil MAGs you obtained  from **MetaBAT2** binning of contigs during Project: Finding AMRs, Activity 4. Note, `MetaBAT2 bins are a collection`, so try using **Dataset collection** (instead of multiple individual files) as input. 

#### Questions

|1. Record summary of MAG classification of Bacteria below.|
|:--------|
||
<br>

|2. Record summary of MAG classification of Archaea below.|
|:--------|
||
<br>

|3. Share your Galaxy history to GTDBtk classification below.|
|:--------|
||
<br>

### Activity 3 – Import an SRA dataset of interest for your research project

#### Instructions

Upload sequencing reads from a dataset of interest using the **Faster Download and Extract Reads in FASTQ** tool.  Refer back to the table in the **Activity: Possible Datasets** for BioProjects with known long read metagenomics datasets.

#### Questions

|1. Record the following features of your downloaded dataset below.|
|:--------|
|Accession ID:  |
|File size: |
|Job Runtime (Wall Clock): |
<br>

|2. Inspect your SRA entry in NCBI https://www.ncbi.nlm.nih.gov/sra. Obtain the following sequencing information.|
|:--------|
|Organism:   |
| Instrument:  |
|Strategy: |
| Run: |
<br>


### Activity 4 – Use a new Galaxy tool that may be useful for your project

#### Instructions

Find one new Galaxy tool that you think may be useful for your research project.  A few possibilities to get you started include:

- Prokka [Galaxy tutorial](http://training.galaxyproject.org/training-material/topics/genome-annotation/tutorials/annotation-with-prokka/tutorial.html)
- Bakta [Galaxy Tutorial](https://training.galaxyproject.org/training-material/topics/genome-annotation/tutorials/bacterial-genome-annotation/tutorial.html)
- antiSMASH [Galaxy tutorial](http://training.galaxyproject.org/training-material/topics/genome-annotation/tutorials/secondary-metabolite-discovery/tutorial.html 
- CheckM2 [Galaxy tutorial](https://training.galaxyproject.org/training-material/topics/genome-annotation/tutorials/bacterial-genome-quality-control/tutorial.html)
- Tools mentioned in tutorials like [GTN: Bacterial Genome Annotation](https://training.galaxyproject.org/training-material/topics/genome-annotation/tutorials/bacterial-genome-annotation/tutorial.html)
- Tools used in workflows like [https://nf-co.re/mag](https://nf-co.re/mag) (not all tools will be available on Galaxy)

#### Questions

|1. Briefly describe the tool e.g. how it works, what it takes as input, and what it produces as output.|
|:--------|
||
<br>

|2. Describe briefly any problems you had running the tool and troubleshooting steps you tried.|
|:--------|
||
<br>

|3.  If you were able to get the tool to run, describe the results and whether they provide additional information for your project.|
|:--------|
||
<br>

### Grading Criteria

- <mark style="background color: yellow">Download as Microsoft Word (.docx) and upload on Canvas

### Footnotes

**Resources**

- Google Doc

**Contributions and Affiliations**

- Valeriya Gaysinskaya, Johns Hopkins University
- Frederick Tan, Johns Hopkins University

Last Revised: June, 2025

# Identifying Datasets

## Lecture - Possible Datasets

![](resources/images/project-work_files/figure-docx//1VxwSmAY8BUs3EfVcxPm3I8kNYJWjVqoHJrGOX3X3sog_g35f391192_00.png)

[Slides: Possible Datasets](https://docs.google.com/presentation/d/1VxwSmAY8BUs3EfVcxPm3I8kNYJWjVqoHJrGOX3X3sog/edit?usp=sharing)


## Activity - Possible Datasets

A few ideas to get you started with the Project Work can be found in the **Possible Datasets** Lecture and Acvitivity below. **Your project work will culminate in Poster making, poster sharing and poster presentation.** a. Each group will present their capstone project during an in-class poster presentation. 

### Activity

*Estimated time: 50 min*

#### Instructions

1. Skim three abstracts

2. Pick one and answer the following questions

a) Notice – What about this abstract most interests you?

b) Dataset – Summarize at a high level where the samples came from, how many there are, and what technology was used for sequencing.

c) Wonder – Two or three questions you would like to ask using this (and any other) datasets.

3. Post your answers by replying to the “Project Work: Possible Datasets” topic in the Discussion Forum

|Possible Datasets (Long-read PacBio)|
|:--|:--|:--|:--|
|**Soil**| | | |
| |Antarctic |PRJNA1126331 | https://pubmed.gov/39300163/| 
| |Biocrust |PRJNA691698 | https://pubmed.gov/34795375/| 
|**Water**| | | |
| |Fresh Water |PRJNA924152 | https://pubmed.gov/36823661/|
| |Ocean Water |PRJNA853328 | https://pubmed.gov/36448813/|
|**Human Gut**| | | |
| |Vegan/Omnivore |PRJNA750084 | http://pubmed.gov/36289209|
| |Infant Nutrition |PRJNA1139951 | http://pubmed.gov/31022095|
|**and More!**| | | |
| |Lamb Gut |PRJNA595610 |http://pubmed.gov/34980911|
| |Deadwood |PRJNA603240 | http://pubmed.gov/39627869|
| |Cheese |PRJNA778418 | http://pubmed.gov/9948695|
| |Whey |PRJNA454439, PRJNA477604 | http://pubmed.gov/6593500 |
<br>

### Grading Criteria

- <mark style="background color: yellow">Submit URL to your reply on Canvas</mark>.

### Footnotes

**Contributions and Affiliations**

- Valeriya Gaysinskaya, Johns Hopkins University
- Frederick Tan, Johns Hopkins University

Last Revised: May 2025

# Conducting Your Research

Conducting your research involves prioritizing, scaffolding and organizing your research as you progress towards a final poster presentation.  To help you conduct your research in an organized and efficient manner, and with feedback and review from both, peers and instructors, several key aspects of conducting research will be a part of your resech work. They include round table updates, written check-ins, advisory meetings, and peer reviews.  During the Project Work phase, you will be documenting, summarizing and updating relevant documenents which will fall under 3 categories:


```
1. Round Table Data & Troubleshooting** - Reviewed and discussed as a community In-Class 
2. Written Check-Ins** - Group-specific write-ups checked by instructor(s)
3. Advisory Meetings** - Group-specific in-person meetings between individual groups and instructor(s)
```


### Project Work Organizer

Research lab meetings are great forums to receive community analysis and feedback.  Many classes going forward will be spent discussing your project progress, alternating between data results and troubleshooting methods.  Refer to this organizer to see what we’ll discuss on a given day and find the appropriate slidedeck.

<br>

<mark style="background color: yellow">Use this organizer to find instructions and track documents.

#### Round Table Data & Troubleshooting 

Research lab meetings are great forums to receive community analysis and feedback. In-class round table data and troubleshooting sessions and slidedecks will be used to report on and get feedback on your ongoing research. Consider these in-class project work updates your research lab meetings!

**1. Track and share your work and progress using Slidedecks**

a. Instructor will create a single Slidedeck - **Round Table Data** for all groups 

b. Instructor will create a single Slidedeck - **Round Table Troubleshooting**  for all groups

c. Instructor will create a single Slidedeck - **Poster** for all groups

d. Instructor will create a single Slidedeck - **Final Presentation** for all groups

**2. Use the following (sample) project Work organizer for your In-class Project Work updates.**


|Course Week | Day 1 | Day 2
|:--| --|-- | 
|6| Round Table Data| Round Table Troubleshooting |
|7| Round Table Data| Science Talks|
|8| Round Table Troubleshooting| Round Table Data | 
|9| Round Table Data | Round Table Troubleshooting|
|10|Round Table Data | Round Table Troubleshooting |
|11| Round Table Poster Review| Round Table Poster Review |
|12| Science Talks| Round Table Poster Review|
|13| Final Poster Presentations | Wrap-up |


#### Written check-ins

Written check-ins encompass a written document for groups-instructor interaction, and will also be used for peer reviews. 

**1. Track and share your work and progress using test document**

For each group, instructor will create a text document **Doc** which will include the following sections:

**a. Written Check-in (Doc)** - Progress will be assessed through several written check-ins.  These documents will allow you to summarize the work you’ve done, receive feedback from colleagues, and provide another opportunity to ask for help.  Your check-in should be concise but complete (full sentences) and include the following information:

- New progress since last submission (15 pts)
- How you’ve addressed prior feedback (15 pts)
- Poster organization (10 pts)
- Struggles you are encountering and questions you would like advice on (10 pts)

**b. Written Check-in (Poster)** - The second written check-in will focus on starting your poster using material you developed for your Round Table updates.  Posters should be 30 inches wide and we have provided a template with example two and three column formats.  You can make your own design by selecting the Blank layout.  Kickstart your poster by adding the following details:

- Title and authors (10 pts)
- Hypothesis along with diagram or figure (10 pts)
- Dataset table with sample metadata including accession ID, collection method, etc. (10 pts)
- Methods in the form of details and figure (10 pts)
- Results (10 pts)

**c. Peer Review** - Each person will work individually to peer review two separate projects.  Review the poster associated with each project and provide feedback in group's Check-in document on the following:

- Aspects of the project that you find fascinating
- Questions you have about the approach or results
- Suggestions on next steps, poster organization, etc.

#### Advisory Meetings

**Advisory Meeting** - Each group will schedule a meeting with the instructors to discuss their progress.  These meetings will take place outside of class and should be scheduled before the deadline.  A link to the when2meet schedule can be found in the Group Information section.

### Sample project work doc organizer

With your instructor, during your Project Work, fill out the Project Work organizer below. 


|Group | Check-in | Poster | Meeting #1 | Meeting # 2|
|:--| :--| :-- | :-- | :-- | 
|Group A| Doc | Slides | Date 1 | Date 2| 
|Group B| Doc | Slides | Date 1 | Date 2| 
|Group C| Doc | Slides | Date 1 | Date 2| 
|Group D| Doc | Slides | Date 1 | Date 2| 

### Project Work Sample Schedule

February 25 | Session 1

- Round Table Data (slidedeck)

February 27 | Session 2

- Round Table Troubleshooting (slidedeck)

March 4 | Session 3 

- Round Table Data (slidedeck)
- `Homework: Work on Written Check-in #1 (Doc) (Due day before next class, March 5)`

March 6 | Professional Development

- Science Talks: Guest Lecture and Q&A
- `Homework: Work on Written Check-in #2 (Doc) (Due day before next class, March 10)`

March 11 | Session 4

- Round Table Troubleshooting (slidedeck)
- `Homework: Work on Written Check-in #3 (Poster) (Due day before next class, March 12)`


March 13 | Session 5

- Round Table Data (slidedeck)
- `Advisory Meeting #1` (Due next day, March 14)`

March 18 

- Spring Break

March 20 

- Spring Break

March 25 | Session 6

- Round Table Data (slidedeck)

March 27 | Sessison 7

- Round Table Troubleshooting (slidedeck)
- `Homework: Work on Written Check-in #4 (Doc) (Due day before next class, March 31)`

April 1 | Session 8

- Round Table Data (slidedeck)
- `Homework: Work on Peer-review #1 (Doc) (Due day before next class, April 2)`

April 3 | Session 9
 
- Round Table Troubleshooting (slidedeck)
- `Advisory Meeting #1` (Due next day, April 4)`
- `Homework: Work on Written Check-in #5 (Doc) (Due day before next class, April 7)`

April 8 | Professional Development 

- Round Table Poster Review (slidedeck)
- `Homework: Work on Peer-review #2 (Doc) (Due day before next class, April 9)`

April 10 | Session 10

- - Round Table Poster Review (slidedeck)
 
April 15 | Session 11

- Science Talks: Guest Lecture and Q&A

April 17 | Professional Development

- Round Table Poster Review (slidedeck)
- **Finalize Poster for printing**
- In class activity: Scientific Communication

April 22 | Professional Development

- **Project Work Final Poster Presentation**

April 24 | Wrap-Up: Professional Development 

- Last Session
- Lecture: Next Steps
- In class activity: Next Steps


### Footnotes

**Contributions and Affiliations**

- Valeriya Gaysinskaya, Johns Hopkins University
- Frederick Tan, Johns Hopkins University

Last Revised: June 2025

