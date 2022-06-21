# Standard Single Cell Workflow

## Setup

The main tool used for single cell workflow is *Seurat*, additional packages such as *SingleR* or *scCATCH* is used for labelling cell subtypes.

```R
library(Seurat)
library(SingleR)
```

## Load File

```R
apt69_file <- Read10X('data/69_aptamer')
apt69 <- CreateSeuratObject(counts = apt69_file, project = "emt6", min.cells = 10, min.features = 200)
```

## (Optional) Regressing Out Variables

Some variables can be regressed out via 


## PCA Analysis


## Reduction and Clustering 


## Labelling Clusters

### SingleR

### scCATCH


# Additional Functions

## Subsetting Seurat Object


## Exporting Expression Matrix

There are three types of expression data under each type of data: ***Counts***, ***Data***, and ***Scaled Data***.
**Counts**: Raw counts for after cell ranger workflow, each count represent a unique UMI identified by sequencing
**Data**: Obtained after *NormalizeData* function, normalize data so each cell contains the same total count number
**Scaled Data**: Obtained after *ScaleData* function, data scaled to have mean of 0 and sd of 1

## Including Plots

