# Bracis2023

Repository of the article "Community Detection Methods for Multi-Label Classification" submitted to BRACIS 2023

## Concepts

### Partitions Simple Version
<img src="https://github.com/cissagatto/Bracis2023/blob/main/Figures/partitions-concept.png" width="600">

### Partitions Detailed Version
<img src="https://github.com/cissagatto/Bracis2023/blob/main/Figures/partitions-concept-detailed.png" width="600">

### Hybrid Partitions Flow
<img src="https://github.com/cissagatto/Bracis2023/blob/main/Figures/HPML-C.png" width="600">

### Random Partitions Flow
<img src="https://github.com/cissagatto/Bracis2023/blob/main/Figures/Random-Graph-Communities.png" width="600">

## Results

### Performance


### Statistical Tests


### Partitioning


### Partitioning


## Instructions for running this experiment

### Enviroments to run experiments
Click [here]() to download 

#### Conda
You can run this experiment in Conda Environment. The name is "AmbienteTeste". To be able to use this env you must first install conda in your computer or cluster and then install the env using the following command: *conda env create --file AmbienteTeste.yaml*

#### Singularity
You can also run this experiment in a singularity container. Download the recipes and follow this tutorial (in portuguese): https://prensa.li/@cissa.gatto/tutorial-como-criar-um-container-singularity-para-executar-scripts-r-com-java-e-rclone

### Step-by-Step Procedures

#### Step 1: Pre-processing
- [Code](https://github.com/cissagatto/CrossValidationMultiLabel) to create the 10-Fold Cross Validation for each dataset.

#### Step 2: Modeling Label Correlation
- [Code](https://github.com/cissagatto/MultiLabelSimilaritiesMeasures) to compute similarities measures
- [Code](https://github.com/cissagatto/BuildDataFrameGraphMLC) to build graphs

#### Step 3: Applying Communities Detection Methods
- [Code](https://github.com/cissagatto/Generate-Partitions-Communities) to generate partitions from communities

#### Steps 4, 5 and 6: Build, validate, chose and test hybrid partitions
- [Code](https://github.com/cissagatto/TCP-KNN-H-Clus) for sparsification with KNN + Hierarchical Methods 
- [Code](https://github.com/cissagatto/TCP-KNN-NH-Clus) for sparsification with KNN + Non Hierarchical Methods
- [Code](https://github.com/cissagatto/TCP-TR-H-Clus) for sparsification with Threshold + Hierarchical Methods
- [Code](https://github.com/cissagatto/TCP-TR-NH-Clus) for sparsification with Threshold + Non Hierarchical Methods

#### Code for Global, Local and Random Partitions
- [Global](https://github.com/cissagatto/Global-Clus)
- [Local](https://github.com/cissagatto/Local-Clus)
- [Generate Random Graphs](https://github.com/cissagatto/Generate-Random-Communities)
- [Test Random Graph + Hierarchical Methods](https://github.com/cissagatto/TCP-Random-H-Clus)
- [Test Random Graph + Non Hierarchical Methods](https://github.com/cissagatto/TCP-Random-NH-Clus)




## Acknowledgment
This study is financed in part by the Coordenação de Aperfeiçoamento de Pessoal de Nível Superior - Brasil (CAPES) - Finance Code 001

# Thanks
