# mA density calculator in given regions
This script is used to calculate mA density in different given regions. The code takes different genome coordination files. 
 The first section takes in the bam file and the reference genome, so that the script cancalculate the chromosome sequence length for each and every chromosome for later analyses. 

 The second part of the script parses the active array into the format of 
 {dictionary name} = 'chromosome name': [[start_position1, end_position1] [startposition2, endposition2]]

The following parts of the script go and calculate the CDR and CDR_adjacent regions in the genome. 

Finally, in the last parsing feature, the script takes random active array lengths in the genome, and the number of these regions can be pre-defined in the function.

Finally, the density calculation function is able to take in the position coordinates to calculate the mA density in these defined regions. Because not all the bases in reads are representative in the genome, the code eliminates the bases in the reads that aren't mapped to the genome (insertions) and it adds place holders in positions where bases in the genome are present but not in the reads (deletions). 