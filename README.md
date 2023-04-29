# BRACIS 2023

Repository of the paper "Community Detection Methods for Multi-Label Classification" submitted to BRACIS 2023.

## CONCEPTS

### Partitions Simple Version
<img src="https://github.com/cissagatto/Bracis2023/blob/main/Figures/partitions-concept.png" width="400">

### Partitions Detailed Version
<img src="https://github.com/cissagatto/Bracis2023/blob/main/Figures/partitions-concept-detailed.png" width="200">

### Hybrid Partitions Flow
<img src="https://github.com/cissagatto/Bracis2023/blob/main/Figures/HPML-C.png" width="600">

### Random Partitions Flow
<img src="https://github.com/cissagatto/Bracis2023/blob/main/Figures/Random-Graphs-Communities.png" width="600">

## RESULTS

*[SimilarityMatrices]*(https://drive.google.com/drive/folders/1c7mH8C66oEH3Z3FhbfWN0wrgH5cD_k5P?usp=sharing)
*[Label Graphs]*(https://drive.google.com/drive/folders/1qZTpVlyxCUD5YjEYY8Jway3jymRu_6hc?usp=sharing)
*[Partitions]*(https://drive.google.com/drive/folders/1djINXsGzstBWGLtD3N4L8AT0YGgwyFK_?usp=sharing)

*Performance*
[Download](https://drive.google.com/drive/folders/1goyeMk2fFNJFWwyeETeeiw6xHwmjH4ve?usp=sharing)

*Win-Loss-Tie*
[Download](https://drive.google.com/drive/folders/1sW3PgvywMkmolxxWFVB7JaO8qr12_uDB?usp=sharing)

*Method-Pair-Comparison*
[Download](https://drive.google.com/drive/folders/1ImTaRPQPIjyjN2a0gisN3ewAP7uKNsCk?usp=sharing)

*Statistical Tests*
[Download](https://drive.google.com/drive/folders/17sYG_t772k3xYzA_SZOdK97ccTIbnE4u?usp=sharing)

*Community Detection Methods*
[Download](https://drive.google.com/drive/folders/1lrgzd2Vu2rsSnvOSHr9dfwtv_QsM433c?usp=sharing)

*Partitioning*
[Download](https://drive.google.com/drive/folders/18F6_DiGzZMlLnjkoK1uK0b5qAvcrdO99?usp=sharing)


## INSTRUCTIONS TO REPRODUCE THE EXPERIMENTS

### Enviroments to run experiments

#### Conda
You can run this experiment in a Conda Environment. The name of our conda environment is "AmbienteTeste". To be able to use this env, you must first install conda in your computer or cluster and then install the env using the following command: *conda env create --file AmbienteTeste.yaml*. Click [here](https://drive.google.com/drive/folders/1OGwZi8gPuoUF_DIshz7XsGIUurmQgKXe?usp=sharing) to download the files.


#### Singularity/AppTainer
You can also run this experiment in a singularity container. We do not provide a singularity container for this experiment, but you can build one. 


### SOURCE CODE
Our code is completely modular because of our servers - mainly job queue, time, and memory. In this way, we can run many jobs in parallel in different steps of the methodology. In the future, a package that executes all the flow will be developed and available for the scientific community.

*Step 1: Pre-processing*
- [Code]() to create the 10-Fold Cross Validation for each dataset. You can download our data splits [here](https://drive.google.com/drive/folders/16t1rRptgULrM20IFItC_HlPJrmFZbIzH?usp=sharing). 

*Step 2: Modeling Label Correlation*
- [SimilaritiesMultiLabel](https://drive.google.com/file/d/1Gq5YuReKkbrGE0lGMii671qAdvKRi5jF/view?usp=sharing) to compute similarities measures;
- [GraphMultiLabel](https://drive.google.com/file/d/1C9WLZtoYuk6RW1397iwPH9p2ytOVQSme/view?usp=sharing) to build the label co-occurrence graphs.

*Step 3: Applying Communities Detection Methods*
- [GeneratePartitionsCommunities]() to generate partitions from the communities.

*Steps 4, 5 and 6: Build, validate, chose and test hybrid partitions*
- [Code]() for Sparsification with KNN + Hierarchical Methods 
- [Code]() for Sparsification with KNN + Non Hierarchical Methods
- [Code]() for Sparsification with Threshold + Hierarchical Methods
- [Code]() for Sparsification with Threshold + Non Hierarchical Methods

*Code for Global, Local and Random Partitions*
- [Global]()
- [Local]()
- [Generate Random Graphs]()
- [Test Random Graph + Hierarchical Methods]()
- [Test Random Graph + Non Hierarchical Methods]()


## Acknowledgment
This study is financed in part by the Coordenação de Aperfeiçoamento de Pessoal de Nível Superior - Brasil (CAPES) - Finance Code 001

# Thanks
