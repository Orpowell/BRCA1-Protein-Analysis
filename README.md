# BRCA1-Protein-Analysis

This Project is the culmination of the bioinformatics and programming (Python) that I learnt in the Covid-19 Lockdown, after the first year of my Biochemistry Degree. 

The aim was to identify conserved residues within sequence of the breast cancer type 1 susceptibility (BRCA1) protein, across 8 different species, and highlight them as part of the sequence and structure of the human protein. This was done in the following steps:

	1. An input txt file of Protein Accession codes is given. These are used to access the sequence of each protein from the UniProt KnowledgeBase.
	2. The collected sequences are used for a Multiple sequence alignment, using Clustal Omega.
	3. The produced alignment and phylogenetic tree are then plotted (see Figures).
	4. The alignment is then converted into a 2D NumPy array, and scanned to find conserved residues; The position of each conserved residue is stored in a list.
	5. The list of conserved residues is used to colour residues on the structure of the human protein and saved as a PyMol session (see Figures).

## Figures
![MSA](https://user-images.githubusercontent.com/66531998/94668270-be762400-0307-11eb-8aeb-e3b9bf85bdb4.png)
Figure 1. A multiple sequence alignment of the BRCA1 protein across 8 different species. The alignment was produced using Clustal Omega with using data collected from UniprotKB.





## Tools Used

- Clustal Omega 1.2.3
- PyMol 2.4
- BioPython 1.77
- Biotite 0.22.0
- Ammolite 0.4.0
- NumPy 1.19.1

## Comments
- Due to difficulty accessing the alignment file from the ClustalOmegaApp in Biotite, the alignment had to be ran again using Biopython; In order to collect the positions of the conserved residues from the raw alignment file.
