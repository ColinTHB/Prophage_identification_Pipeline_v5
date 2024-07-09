Code for pipeline for identification and extraction of prophage elements in genomic assemblies - outputs *.gbk of prophage genomes & *.tsv files with details of prophages identified. It depends on several conda environments with particular tools loaded to function.

The current version of the pipeline depends on the presence of conda environments with the installed software.

##################################################################################################################################################################################

These are as follows.

virsorter2_env - virsorter2 (v2.2.4)

checkv_env - checkv (v1.0.3)

pharokka_env - pharokka (v1.7.2)

bedtools_env (need to fix enviroment name....) - biopython (v1.84)

##################################################################################################################################################################################

Usage is as follows

rewrite headers of input fast to ensure compatibility with the script
./rewrite_fasta_headers-4-prophage-hunting-v1.1.sh genome.fna input-genome-fixed.fna

Run the prophage hunting script
./prophage_gbk+tsv_here_checkv-v1 -i input-genome-fixed.fna

Extract prophage sequences from pharokka annotation
./prophage_gbk+tsv_here_checkv-v1 <path_to_virsorter_output>

####################################################################################################################################################################################

The last script calls on several scripts from the processing_scripts_v2 folder - ensure it is placed in the same directory as /prophage_extract_gbk+tsv_here-v5.sh script.
