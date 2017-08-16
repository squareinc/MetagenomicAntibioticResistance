# MetagenomicAntibioticResistance

### A Simple Method for Extracting Antimicrobial Resistance Information from Metagenomes
##### Hackathon team: Lead: Steve Tsang - SysAdmins: Greg Fedewa, Dan, Sherif Farag - Writers: Matthew Moss, Alexey V. Rakov


*Objective*: Create a reusable, reproducible, scalable, interoperable workflow 
to locate antimicrobial resistant genomic signatures in SRA shotgun sequencing (metagenomics) datasets

## Dependencies:computer:

*Software:*

Magic-BLAST 1.3b [link](https://github.com/boratyng/magicblast)

SAMtools 1.3.1 [link](http://www.htslib.org/)

STAR [link](https://github.com/alexdobin/STAR/releases)

Docker [link](https://www.docker.com/)

*DBs used for BLAST databases:*

hg19 [link](https://www.ncbi.nlm.nih.gov/projects/genome/guide/human/index.shtml)

CARD (Comprehensive Antibiotic Resistance Database) DB [link](https://card.mcmaster.ca/)

RefSeq Reference Bacterial Genomes [link](https://www.ncbi.nlm.nih.gov/refseq/)

## Workflow

![My image](https://github.com/NCBI-Hackathons/MetagenomicAntibioticResistance/blob/master/AbxResistanceMetagenomics.png)

## Workflow method

The pipeline use three databases that should be downloaded with the script:
1.	*hg19 human genome database* used for alignment and filtering reads of human origin from metagenomics samples.
2.	*CARD database* used for search of genomic signatures in the subset of reads unaligned to human genome.
3.	*RefSeq reference bacterial genome database* used for search and assigning of 16S RNA taxonomic labels the subset of reads unaligned to human genome.


## Deliverables

Documented workflow with containerized tools

## Installation



## Usage

scaleupUpScript.sh <options> -S SRA -o output_directory

## Input file format

SRA accession numbers (ERR or SRR)
or
FASTQ files

## Output

Table (in CSV or TAB-delimited format) with the next columns:
- Accession number (Nucleotide/Protein)
- Name
- ARO (Antibiotic Resistance Ontology)
- Score
- Resistance type

## Warnings

## People/Team
* Steve Tsang, NCI/NIH, Gaithersburg, MD, <tsang@mail.nih.gov>
* Greg Fedewa, UCSF, San Francisco, CA, <fedewag@gmail.com>
* Sherif Farag, UNC, Chapel Hill, NC, <farags@email.unc.edu>
* Matthew Moss, CSHL, Cold Spring Harbor, NY, <moss@cshl.edu>
* Dan, UCI, Irvine, CA, <>
* Alexey V. Rakov, UPenn, Philadelphia, PA, <rakovalexey@gmail.com>

