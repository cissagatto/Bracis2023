# BRACIS 2023

Repository of the paper "Community Detection Methods for Multi-Label Classification" published in BRACIS 2023.

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



### Resulting Files

Here you can download the generated similarity matrices, label graphs, and partitions for our experiments. If you want to generate these for your experiments from the beginning, please check the source code section.

- [SimilarityMatrices](https://drive.google.com/drive/folders/1c7mH8C66oEH3Z3FhbfWN0wrgH5cD_k5P?usp=sharing)

- [Label Graphs](https://drive.google.com/drive/folders/1qZTpVlyxCUD5YjEYY8Jway3jymRu_6hc?usp=sharing)

- [Partitions](https://drive.google.com/drive/folders/1djINXsGzstBWGLtD3N4L8AT0YGgwyFK_?usp=sharing)



### Analysis

Here you will find all the documents (tables, plots, etc.) with an analysis of the results.

- [Performance](https://drive.google.com/drive/folders/1goyeMk2fFNJFWwyeETeeiw6xHwmjH4ve?usp=sharing)

- [Win-Loss-Tie](https://drive.google.com/drive/folders/1sW3PgvywMkmolxxWFVB7JaO8qr12_uDB?usp=sharing)

- [Method-Pair-Comparison](https://drive.google.com/drive/folders/1ImTaRPQPIjyjN2a0gisN3ewAP7uKNsCk?usp=sharing)

- [Statistical Tests](https://drive.google.com/drive/folders/17sYG_t772k3xYzA_SZOdK97ccTIbnE4u?usp=sharing)

- [Community Detection Methods](https://drive.google.com/drive/folders/1lrgzd2Vu2rsSnvOSHr9dfwtv_QsM433c?usp=sharing)

- [Partitioning](https://drive.google.com/drive/folders/18F6_DiGzZMlLnjkoK1uK0b5qAvcrdO99?usp=sharing)


## INSTRUCTIONS TO REPRODUCE THE EXPERIMENTS

### Environments to run experiments

#### Conda
You can run this experiment in a Conda Environment. The name of our conda environment is "AmbienteTeste". To be able to use this env, you must first install conda in your computer or cluster and then install the env using the following command: *conda env create --file AmbienteTeste.yaml*. Click [here](https://drive.google.com/drive/folders/1OGwZi8gPuoUF_DIshz7XsGIUurmQgKXe?usp=sharing) to download the files.


#### Singularity/AppTainer
You can also run this experiment in a singularity container. We do not provide a singularity container for this experiment, but you can build one. [Here](https://rpubs.com/cissagatto/apptainer-slurm-r), you can find a little tutorial about how to do that for our experiments. Using singularity is better than conda environments when you have to execute all the experiments in a tmp (scratch or dev/shm) folder. 

Pay attention to this because sometimes using the conda environment directly from the */home* can destroy hard disks and harm all users. In some situations, copying your singularity container to the server's temp folder and running absolutely everything from there is the best solution for everyone. Talk to the administrator about this before trying to reproduce the experiments.


### SOURCE CODE
Our code is completely modular because of our servers - mainly job queue, time, and memory. In this way, we can run many jobs in parallel in different methodology steps. In the future, a package that executes all the flow will be developed and available for the scientific community. 

In each source code, you will find instructions about how to run the code. You can also make adjustments in the main script to save the results in your machine or your cloud using rclone (there are some examples in the R scripts).

Attention: before using rclone, check with your institution's network administrator if uploading files and folders from the cluster to the cloud is possible. In the case of using Google accounts for universities, you need to follow specific steps to configure communication between google cloud and the server.

*Step 1: Pre-processing*
- [Code](https://github.com/cissagatto/CrossValidationMultiLabel) to create the 10-Fold Cross Validation for each dataset. You can download our data splits [here](https://drive.google.com/drive/folders/16t1rRptgULrM20IFItC_HlPJrmFZbIzH?usp=sharing). 

*Step 2: Modeling Label Correlation*
- [SimilaritiesMultiLabel](https://github.com/cissagatto/SimilaritiesMultiLabel) to compute similarities measures {OR [https://github.com/cissagatto/MultiLabelSimilaritiesMeasures];}
- [GraphMultiLabel](https://github.com/cissagatto/GraphMultiLabel) to build the label co-occurrence graphs.

*Step 3: Applying Communities Detection Methods*
- [GeneratePartitionsCommunities](https://github.com/cissagatto/Generate-Partitions-Communities) to generate partitions from the communities.

*Steps 4, 5, and 6: Build, validate, chose, and test hybrid partitions*
- [Code](https://github.com/cissagatto/TCP-KNN-H-Clus) for Sparsification with KNN + Hierarchical Methods 
- [Code](https://github.com/cissagatto/TCP-KNN-NH-Clus) for Sparsification with KNN + Non Hierarchical Methods
- [Code](https://github.com/cissagatto/TCP-TR-H-Clus) for Sparsification with Threshold + Hierarchical Methods
- [Code](https://github.com/cissagatto/TCP-TR-NH-Clus) for Sparsification with Threshold + Non Hierarchical Methods

*Code for Global, Local, and Random Partitions*
- [Global](https://github.com/cissagatto/Global-Partitions)
- [Local](https://github.com/cissagatto/Local-Partitions)
- [Generate Random Graphs](https://github.com/cissagatto/Generate-Random-Communities)
- [Test Random Graph + Hierarchical Methods](https://github.com/cissagatto/TCP-Random-H-Clus)
- [Test Random Graph + Non Hierarchical Methods](https://github.com/cissagatto/TCP-Random-NH-Clus)


## Acknowledgment
- This study was financed in part by the Coordenação de Aperfeiçoamento de Pessoal de Nível Superior - Brasil (CAPES) - Finance Code 001.
- This study was financed in part by the Conselho Nacional de Desenvolvimento Científico e Tecnológico - Brasil (CNPQ) - Process number 200371/2022-3.
- The authors also thank the Brazilian research agencies FAPESP financial support.

# Thanks
