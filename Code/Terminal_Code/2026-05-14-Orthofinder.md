# Orthofinder in Terminal

*#It is easiest to use Bioconda for Macs.*

$mkdir ~/orthofinder

$cd ~/orthofinder

$wget https://github.com/davidemms/OrthoFinder/releases/latest/download/OrthoFinder.tar.gz

*#Downloads the latest version of Orthofinder.*

$tar xzvf OrthoFinder.tar.gz

$cd OrthoFinder/

*#Extracts the package and then navigates to the OF directory.*

*#Genome-based proteomes should be reduced to just the longest transcript variant per gene, which can be done in Galaxy’s AGAT using the .gff file in NCBI, and then the genome .fna file and the AGAT .gff3 output file.*

$conda activate ortho_env

*#Navigate to folder above containing proteomes to be aligned into orthogroups.*

$orthofinder -f NAMEOFFOLDERWITHPROTEOMES

*#Orthofinder takes minutes to hours for 4-10 proteomes.*

*#If completed successfully, Orthofinder will output a paragraph of summary of the findings followed by the path to the results directory, citations, and the time to completion.*

*#If error that a module is missing, run the following commands:*

$conda config --add channels defaults

$conda config --add channels bioconda

$conda config --add channels conda-forge

$conda create -n ortho_env orthofinder brotli (OR OTHER MODULE NAME)

*#Then activate the created ortho_env as above.*
