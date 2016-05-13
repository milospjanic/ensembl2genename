# ensemble2GeneNameMusMusculus

This is combined bash/R script that will use a file with **mouse** ENSEMBLE geneIDs in **a first column** of a file and append a gene name to it, while keeping the structure of the file from  other columns. Ensemble2GeneNameMusMusculus sets its host to ensembl.org thus it could be especially useful when biomaRt site is down.


# Dependencies
Rscript, BiomaRt

# Usage
chmod 775 ensemble2GeneNameMusMusculus

./ensemble2GeneNameMusMusculus file.txt

# Example

<pre>
head file.txt
ENSMUSG00000102693	0	0	0
ENSMUSG00000064842	0	0	0
ENSMUSG00000051951	0	0	0
ENSMUSG00000102851	0	0	0
ENSMUSG00000103377	0	0	0
ENSMUSG00000104017	0	0	0
ENSMUSG00000103025	0	0	0
ENSMUSG00000089699	0	0	0
ENSMUSG00000103201	0	0	0
ENSMUSG00000103147	0	0	0
ENSMUSG00000103161	0	0	0

chmod 775 ensemble2GeneNameMusMusculus
./ensemble2GeneNameMusMusculus file.txt


head file.txt.genename

Gm26206 ENSMUSG00000064842	0	0	0
Xkr4 ENSMUSG00000051951	0	0	0
Gm1992 ENSMUSG00000089699	0	0	0

Note that **only lines with mathces in the Biomart database** are present in the output , those without a match are not in the output file.

