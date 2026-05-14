# Finding Unallowed Characters in Fasta Headers in Terminal

*#Navigate to folder containing fasta files to be checked.*

$grep “^>” Filename.fasta | “ “

*#Finds spaces in headers.*

$grep -U $ ‘\r’ Filename.fasta

*#Finds hidden carriage returns.*

$grep “^>” Filename.fasta | grep -E “[^>A-Za-z0-9_.]”

*#Finds non-alphanumeric, non-underscore, non-period in headers and outputs offending headers.*
