# Amino Acid Composition in R Studio, R version 4.5.1

*Make sure filename.fasta is in working directory.*

>library(xlsx)

>library(Biostrings)

>DF_fasta_data <- readAAStringSet(“filename.fasta”)

>DF_aa_counts <- letterFrequency(DF_fasta_data, letters = AA_ALPHABET)

>write.xlsx(DF_aa_counts, file = “DF_aa_counts.xlsx”)

*#If “WARNING: An illegal reflective access operation has occurred” error is shown, ignore it and check to see if the file has been exported to the working directory anyway.*
