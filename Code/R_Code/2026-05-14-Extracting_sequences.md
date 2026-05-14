# Extracting a subset of sequences in R Studio, R version 4.5.1

>library(seqinr)

*#make sure SequenceFile.fasta is in working directory*

*#Load dataframe (DF) with list of sequences IDs in subset. Make sure the sequence ID does NOT have ">" and column has a title.*

>NewFastaName <- read.fasta(file = “SequenceFile.fasta”, seqtype = c(“AA”), as.string = FALSE, seqonly = FALSE, strip.desc = FALSE)

>NewFastaName2 <- NewFastaName[names(NewFastaName) %in% DF$ColumnTitle]

>write.fasta(sequences = NewFastaName2, names = names(NewFastaName2), file.out = “NewFastaName2.fasta”, open = “w”, nbchar = 60, as.string = FALSE)
