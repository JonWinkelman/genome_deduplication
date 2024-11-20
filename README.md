## De-duplicate genomes at a chosen distance threshold  
dependencies:
* mash https://github.com/marbl/Mash/releases
* datasets https://www.ncbi.nlm.nih.gov/datasets/docs/v2/reference-docs/command-line/datasets/
* python3 `Bio` `pandas` `plotly` `numpy` 

1) Download summaries/genomes/proteomes using datasets CLI
2) Create minhash sketches of each genome and calculate distance matrix using mash
3) Choose a distance threshold to de-duplicate by
   * if a set of genomes are below this threshold, the genome with the highest n50 score is selected.
  
