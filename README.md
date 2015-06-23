# MANTA
A tool for prioritizing single nucleotide variants (SNVs) within transcription factor binding sites (TFBS). 

> This is a fork of the original MANTA repository developed by the Wasserman Lab at the CMMT. Please see this [link for the original repository](https://github.com/wassermanlab/Manta).

* See this [page for more documentation on the MANTA software](http://manta.cmmt.ubc.ca/manta/help.html).

# Installing MANTA

First clone the repository:

```
git clone git@github.com:tinyheero/Manta.git
```

Before you can run MANTA, you need to make sure you the following python modules:

* pymongo

You can install this using pip:

```
pip install pymongo
```

# To Run MANTA

MANTA can take several input files (VCF, GFF, BED) as specified in this [page](http://manta.cmmt.ubc.ca/manta/help.html). To run MANTA, you can go:

```
MANTA_PATH=/path/to/MANTA
$MANTA_PATH/scripts/search_impacts.py -i /path/to/input/file -o out.manta
```

# MANTA Output

The output of MANTA is specified in the "MANTA Results" section in this [page](http://manta.cmmt.ubc.ca/manta/help.html). This section is taken from it:

1. Chromosome - Name of the chromosome on which the SNV/TFBS appear
1. Position - Chromosomal location of the SNV
1. Ref Allele - The reference allele at this chromosomal location
1. Alt Allele - The specified alternate allele for this chromosomal location
1. SNV ID - ID/name of the SNV if the input file format allows for it. Otherwise displayed as '.'.
1. TF - The name of the transcription factor whose binding site is impacted by this SNV
1. JASPAR ID - The JASPAR ID of the position weight matrix used to predict the binding site for this transcription factor
1. Ref TFBS Start - The start position of the predicted TFBS on the reference sequence
1. Ref TFBS End - The end position of the predicted TFBS on the reference sequence
1. Ref Strand - The strand of the predicted TFBS on the reference sequence
1. Ref Abs Score - The absolute (raw) score of the predicted TFBS at this position on the reference sequence
1. Ref Rel Score - The relative score of the predicted TFBS at this position on the reference sequence in the range 0 to 1.0
1. Alt TFBS Start - The start position of the best scoring predicted TFBS on the SNV mutated sequence
1. Alt TFBS End - The end position of the best scoring predicted TFBS on the SNV mutated sequence
1. Alt Strand - The strand of the best scoring predicted TFBS on the SNV mutated sequence
1. Alt Abs Score - The absolute (raw) score of the predicted TFBS at the alternate position on the SNV mutated sequence
1. Alt Rel Score - The relative score of the predicted TFBS at the alternate position on the SNV mutated sequence
1. Impact Score - A measure of the impact of the SNV on the predicted TFBS
