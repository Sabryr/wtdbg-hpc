# Obtain sample data
## File with sample names
SRR.list

## Test URL fabrication

´´´
for sr in $(cat SRR.list); do curl --head --silent --fail  "https://sra-downloadb.be-md.ncbi.nlm.nih.gov/sos2/sra-pub-run-7/"$sr"/"$sr".1" | head -n 1; done;

´´´bash

##Download
´´´
for sr in $(cat SRR.list); do wget "https://sra-downloadb.be-md.ncbi.nlm.nih.gov/sos2/sra-pub-run-7/"$sr"/"$sr".1" 2>> dowload.log; done;
´´´bash
