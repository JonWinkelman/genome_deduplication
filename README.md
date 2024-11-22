## De-duplicate genomes at a chosen distance threshold  
Dependencies:
* mash https://github.com/marbl/Mash/releases
* datasets https://www.ncbi.nlm.nih.gov/datasets/docs/v2/reference-docs/command-line/datasets/
* python3 `Bio` `pandas` `plotly` `numpy` 

### Process  
1) Download summaries/genomes/proteomes using datasets CLI
2) Optional filtering step:
   * any genomes with an n50 below a given threshold are not downloaded.
<img src=figures/genome_filtering_top70.0_perc.png alt="Example Image" width="600" />

3) Create minhash sketches of each genome and calculate distance matrix using mash  
4) Choose a distance threshold to de-duplicate by  
   * if a set of genomes are below this threshold, the genome with the highest n50 score is selected.
     
<img src=figures/n50_scores.png alt="Assembly level" width="600" />

### minHash genome distances
<img src=figures/distances_all.png alt="Assembly level" width="600" />  

### minHash genome distances after deduplication, notice the absence of highly similar genomes
<img src=figures/distances_deduped.png alt="Assembly level" width="600" />  
