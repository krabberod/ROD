#  Ribosomal Operon Database (ROD)

This is the home of the **Ribosomal Operon Database (ROD)**.  
**News 2 April 2025:  We are happy to anounce that ROD is now part of the PR2 database**
- ROD has been added to PR2 v 5.1.0 an can be accessed through the PR2 website [PR2](https://github.com/pr2database/pr2database).

The database contains full-length eukaryotic ribosomal operons. The database is based on the genome assemblies from NCBI, and the operons are extracted from the assemblies. The database currently contains 69,480 operon variants from more than 11,935 genomes.

### Citation
The database is publised in Molecular Ecology Resources. Please cite the paper if you use the database.
**Krabberød, A. K., Stokke, E., Thoen, E., Skrede, I., & Kauserud, H.** (2024). *The Ribosomal Operon Database: A Full‐Length rDNA Operon Database Derived From Genome Assemblies*. Molecular Ecology Resources. [https://doi.org/10.1111/1755-0998.14031](https://doi.org/10.1111/1755-0998.14031) 


**The current release is ROD v1.2 - Golden Rod**  
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.12558683.svg)](https://doi.org/10.5281/zenodo.12558683)


The database contains full-length ribosomal operons extracted from genome assemblies. The database is based on the genome assemblies from NCBI, and the operons are extracted from the assemblies. The database currently contains 69,480 operon variants from more than 11,935 genomes. 



### File Description
There are three files associated with the database (all in flat tab-separated format, and as .rds objects for R):
- _Genome Statistics_: statistics based on the genome assemblies. Contains the number of copies pr. genome, the number of operon variants (see paper for definition), length distribution and genetic distance statistics. 
- _Operon variants_: statistics based on the **variant** from the genomes, i.e. it has multiple entries for the genomes with multiple variants, one for each variant.   
### Krona plot
For an interactive Krona plot of the genomes in the data base see here [Krona plot](https://htmlpreview.github.io/?https://github.com/krabberod/ROD/blob/main/Krona/krona_genius.html)

---
## Updates 24.10.2024
-  The paper is now published in Molecular Ecology Resources. Please cite the paper if you use the database.
- We are currently integrating ROD with PR2, and it will be included in the next PR2 release.

## Updates 27.06.2024
-  Updated to **ROD v1.2**
-  Corrected wrongly spelled Oochrophyta to the correct Ochrophyta.
-  Added a new column to the operon variants file with an annotation stating operon is in the reference dataset or not.
-  Added the metadata from NCBI.
### To Do: 
- Add explanations for all the statistics and columns in the files.
- Add scripts used in the paper to calculate statistics and make figures
![./Images/ROD_v1.0.png][def2]
---
## Updates 24.04.2024
-  Updated to Version *v1.1*
-  Corrected taxonomy for 8 entries of Cryptococcus with a wrong _subdivision__ assignment. 

## Updates 19.04.2024
- Updated to Version *v1.0*
## Updates 23.02.2024
- Plans for the next version (nicknamed **ROD Stewart**): update and clean some of the taxonomy and provide more statistics.
- We also have plans for testing different clustering strategies to see how real Operons when treated with common clustering approaches used in many metabarcoding studies. 
## Updates 13.02.2024 
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

Overview of genomes in NCBI as of Dec. 2023

```
##  See rsync://ftp.ncbi.nlm.nih.gov/genomes/ASSEMBLY_REPORTS/assembly_summary_genbank.txt
## This is from column 25: 
  16572 fungi
   6249 invertebrate
   7232 metagenome # Not included in ROD
   7593 other # Not included in ROD
   3604 plant
   1978 protozoa
   2854 vertebrate_mammalian
   3746 vertebrate_other
  80657 viral # Not included in ROD
  16538 archaea # Not included in ROD
1779617 bacteria # Not included in ROD

```

***


[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fkrabberod%2FROD&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

--- 

"All the keywords in this explanation, by the way, are totally misleading due to the everyday quirks of language " - Don DeLillo, <i> Ratner's Star </i>

[def]: https://doi.org/10.5281/zenodo.11060492
[def2]: ./Images/ROD_v1.0.png