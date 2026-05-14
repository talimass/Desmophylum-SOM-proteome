# Extracting orthogroups from Orthofinder output

>library(strings)

*#Load dataframe (DF) with character string to be searched in orthogroups.txt*

*#Make sure orthogroups.txt is in wd (Path to Orthofinder output file = Users/Orthofinder/../OrthoFinder/Results_DATE/Orthogroups*

>search_termsSps <- DF$termcolumn

>lines <- readLines(“orthogroups.txt”)

> results <- sapply(search_terms, function(termcolumn) {

+     match_line <- lines[str_detect(lines, fixed(termcolumn))][1]

+     

+     if (!is.na(match_line)) {

+         str_extract(match_line, "^[^:]+")

+     } else {

+         NA

+     }

+ })

>library(xlsx)

>write.xlsx(results, file = “SpsOrthogroups.xlsx”)
