# BRCA1-Protein-Analysis

This Project is the culmination of the bioinformatics and programming (Python) that I learnt in the Covid-19 Lockdown, after the first year of my Biochemistry Degree. 

The aim was to identify conserved residues within sequence of the breast cancer type 1 susceptibility (BRCA1) protein, across 8 different species, and highlight them as part of the sequence and structure of the human protein. This was done in the following steps:

	1. An input txt file of Protein Accession codes is given. These are used to access the sequence of each protein from the UniProt KnowledgeBase.
	2. The collected sequences are used for a Multiple sequence alignment, using Clustal Omega.
	3. The produced alignment and phylogenetic tree are then plotted (see Figures).
	4. The alignment is then converted into a 2D NumPy array, and scanned to find conserved residues; The position of each conserved residue is stored in a list.
	5. The list of conserved residues is used to colour residues on the structure of the human protein and saved as a PyMol session (see Figures).

## Results
![MSA](https://user-images.githubusercontent.com/66531998/94668270-be762400-0307-11eb-8aeb-e3b9bf85bdb4.png)
Figure 1. A multiple sequence alignment of the BRCA1 protein across 8 different species. The alignment was produced using Clustal Omega with using data collected from UniprotKB.

![brca1](https://user-images.githubusercontent.com/66531998/94670256-3a716b80-030a-11eb-9b10-31c201233052.png)
Figure 2. The structure of the Human BRCA1 protein. Conserved Residues are coloured red; or pink if they're part of the zinc finger RING binding domain. All unconserved residues are coloured green. Residues were labelled using data collected from Figure 1.

Figures 1. and 2. both clearly demonstrate that large portions of the BRCA1 protein are highly conserved across species. This likely due to the critical role the BRCA1 protein plays in DNA repair and tumuor suppression.

## Tools Used

- Clustal Omega 1.2.3
- PyMol 2.4
- BioPython 1.77
- Biotite 0.22.0
- Ammolite 0.4.0
- NumPy 1.19.1

## Comments
- Due to difficulty accessing the alignment file from the ClustalOmegaApp in Biotite, the alignment had to be ran again using Biopython; In order to collect the positions of the conserved residues from the raw alignment file.
- A possible lead from this project is the development of a generalised analytical tool that can run the entire analysis for any set of proteins; given only the protein accession codes and a PyMol structure.
