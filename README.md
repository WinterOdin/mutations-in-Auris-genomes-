# Mutations in Auris genomes 
### This script:
- determinates mutations in the Martia Auris genomes 
- checks for domain presence in genomes 
- visualizes the output data 
- filters for domains only containing ACTGN chars

### How to run it
We are using argparse so 
python script.py --input_csv --out_vis --out_csv --searched_domain --reference_id

-  --input_csv  Path to input CSV
-  --out_vis  Path to output pdf
-  -out_csv  Path to output CSV
-  --searched_domain  String to be searched
-  --reference_id  ID of the reference genome


##### Determination of mutations 
Script checks what mutations occurred between the sequences and the reference sequence. Script adds column called mutations to the output CSV that contains a list of mutations. A mutation is a triple RPG
R - nucleotide in the reference sequence (single capital letter, or - )
P - position in the reference sequence - ignoring - and counted from 1
G - nucleotide in the sequence (single capital letter, or -) 
** script ignores mutations containing the N character**

##### Domain presence
You have the ability to search for a specific sequence that occurs in the genomes
Example:
Domain ACCA is present in CCGACCAGT and CCGNCCAGT but not in CCGACCTGT. 

