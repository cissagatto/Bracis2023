# BRACIS 2023

Repository of the paper "Community Detection Methods for Multi-Label Classification" submitted to BRACIS 2023.

## CONCEPTS

### Partitions Simple Version
<img src="https://github.com/cissagatto/Bracis2023/blob/main/Figures/partitions-concept.png" width="200">

### Partitions Detailed Version
<img src="https://github.com/cissagatto/Bracis2023/blob/main/Figures/partitions-concept-detailed.png" width="200">

### Hybrid Partitions Flow
<img src="https://github.com/cissagatto/Bracis2023/blob/main/Figures/HPML-C.png" width="600">

### Random Partitions Flow
<img src="https://github.com/cissagatto/Bracis2023/blob/main/Figures/Random-Graphs-Communities.png" width="200">

## RESULTS

### Performance


### Statistical Tests


### Community Detection Methods 


### Partitioning


## INSTRUCTIONS TO REPRODUCE THE EXPERIMENTS

### Enviroments to run experiments

#### Conda
You can run this experiment in a Conda Environment. The name of our conda environment is "AmbienteTeste". To be able to use this env, you must first install conda in your computer or cluster and then install the env using the following command: *conda env create --file AmbienteTeste.yaml*

Click [here](https://www.dropbox.com/scl/fo/1mfzr32svgv3ahch9e6h0/h?dl=0&rlkey=xi8tojx4xqh407enkvdwb65t2) to download the files.


#### Singularity/AppTainer
You can also run this experiment in a singularity container. We do not provide a singularity container for this experiment, but you can build one. 

### SOURCE CODE
Our code is completely modular because of our servers - mainly job queue, time, and memory. In this way, we can run many jobs in parallel in different steps of the methodology. In the future, a package that executes all the flow will be developed and available for the scientific community.

#### Step 1: Pre-processing
- [Code]() to create the 10-Fold Cross Validation for each dataset. You can download our data splits [here](https://www.dropbox.com/scl/fo/hqsu0t1vo9lv4if3xlfs8/h?dl=0&rlkey=ztw34kh7d3ftasgijxr3sgvlc). 

#### Step 2: Modeling Label Correlation
- [SimilaritiesMultiLabel](https://www.dropbox.com/s/taviiq6osnrcfpp/SimilaritiesMultiLabel.zip?dl=0) to compute similarities measures;
- [GraphMultiLabel](https://www.dropbox.com/s/d16u66j76l2yrul/GraphMultiLabel.zip?dl=0) to build the label co-occurrence graphs.

#### Step 3: Applying Communities Detection Methods
- [GeneratePartitionsCommunities]() to generate partitions from the communities.

#### Steps 4, 5 and 6: Build, validate, chose and test hybrid partitions
- [Code]() for Sparsification with KNN + Hierarchical Methods 
- [Code]() for Sparsification with KNN + Non Hierarchical Methods
- [Code]() for Sparsification with Threshold + Hierarchical Methods
- [Code]() for Sparsification with Threshold + Non Hierarchical Methods

#### Code for Global, Local and Random Partitions
- [Global]()
- [Local]()
- [Generate Random Graphs]()
- [Test Random Graph + Hierarchical Methods]()
- [Test Random Graph + Non Hierarchical Methods]()


## Acknowledgment
This study is financed in part by the Coordenação de Aperfeiçoamento de Pessoal de Nível Superior - Brasil (CAPES) - Finance Code 001

# Thanks
