#  Ribosomal Operon Database (ROD)

This is the future home for the **Ribosomal Operon Database (ROD)**.  It is still in its early stages and there are bound to be some errors.  
The current release is ROD v1.0 - Golden Rod   
[![DOI](https://zenodo.org/badge/730400345.svg)](https://zenodo.org/doi/10.5281/zenodo.10948219)  

A preprint is availble on bioRxiv: 
**The Ribosomal Operon Database (ROD): A full-length rDNA operon database extracted from genome assemblies**, _Anders K. Krabberød, Embla Stokke, Ella Thoen, Inger Skrede, Håvard Kauserud_

https://www.biorxiv.org/content/10.1101/2024.04.19.590225v1




### File description
There are three files dataframes associated with the database ( all in flat tab-separated format, and as .rds objects for R):
- _Genome Statistics_: statistics based on the genome assemblies. Contains the number of copies pr. genome, the number of operon variants (see paper for definition), length distribution and genetic distance statistics. 
- _Operon variants_: statistics based on the **variant** from the genomes, i.e. it has multiple entries for the genomes with multiple variants, one for each variant.   

  
![](./Images/ROD_v1.0.png)
  
---
## Updates 19.04.2023
- Updated to Version v1.0
## Updates 23.02.2023
- Plans for the next version (nicknamed **ROD Stewart**): update and clean some of the taxonomy and provide more statistics.
- We also have plans for testing different clustering strategies to see how real Operons when treated with common clustering approaches used in many metabarcoding studies. 
## Updates 13.02.2023 
### ROD v0.4
- **ROD** is born. 69k glorious whole operons sequence variants from 11k genomes in their full length! More stats coming...  
- Fasta and a Tibble in .rds format 
ba
---
### Old stuff
- *(Early February 2024)* The first version of the database has been uploaded [ROD v0.3](./ROD_v0.3.fasta.gz). For now, it is a fasta file with ribosomal sequences, and all the info is in the header. This version contains a set of **near**-full-length ribosomal operons. It contains 104k operons, representing 16k genomes fished from 35k downloaded from NCBI. The operons span at least 4000 bp. But some lack the beginning of 18S others the end of 28S (and sadly some lack both). 
-  The plan for the next release (nicknamed **v0.4 GoldenROD**) is to remove lacking the beginning or the end. 
The initial analysis of ROD seems to indicate that about 33% of the operons are missing portions in either '3 or '5. The updated number of full-length operons is 69K from 12K genome.
***

## Data 
The main source for data is the genome assemblies from NCBI, downloaded Medio 2023: 
```
# To download the meta data: 
rsync -t -v rsync://ftp.ncbi.nlm.nih.gov/genomes/ASSEMBLY_REPORTS/assembly_summary_genbank.txt .
```

Overview of genomes in NCBI as of Oct. 16 2023

```
##  See ftp://ftp.ncbi.nlm.nih.gov/genomes/README_assembly_summary.txt
## This is from column 25: 
  16538 archaea
1779617 bacteria
  16572 fungi
   6249 invertebrate
   7232 metagenomes
   7593 other (???)
   3604 plant
   1978 protozoa
   2854 vertebrate_mammalian
   3746 vertebrate_other
  80657 viral
```

***


[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fkrabberod%2FROD&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

--- 

"All the keywords in this explanation, by the way, are totally misleading due to the everyday quirks of language " - Don DeLillo, <i> Ratner's Star </i>