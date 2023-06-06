# Bioc2023 Voyager ESDA workshop

## Overview

### Description

The `SpatialFeatureExperiment` (SFE) class brings Simple Features as in the `sf` package to `SpatialExperiment` (SPE) and `SingleCellExperiment` (SCE). Simple Features are a standard way to represent geometries, and `sf` performs many geometric operations that can be used to derive cell or Visium spot metadata and to subset the SFE object. In this workshop, you will learn the novel features of SFE by interacting with the geometries and spatial neighborhood graphs, and by performing geometric operations.

Then this workshop introduces exploratory spatial data analysis (ESDA) on the SFE object with the `Voyager` package. This includes visualizing data in space, and spatial statistics methods that exemplify each category of ESDA, including Moran's I (univariate global), local Moran's I (univariate local), Lee's L (bivariate), and MULTISPATI PCA (multivariate).

### Pre-requisites

List any workshop prerequisites, for example:

* Basic knowledge of R syntax
* Familiarity with `SingleCellExperiment`
* Basic statistics such as Pearson correlation

Much of the material can be found on the documentation websites of [`Voyager`](https://pachterlab.github.io/voyager/) and [`SpatialFeatureExperiment`](https://pachterlab.github.io/SpatialFeatureExperiment/). Relevant vignettes will be linked to in the following sections.

### Participation

This workshop consists of hands on demos, exercises, and Q&A.

### _R_ / _Bioconductor_ packages used

* [`Voyager`](https://pachterlab.github.io/voyager/)
* [`SpatialFeatureExperiment`](https://pachterlab.github.io/SpatialFeatureExperiment/)
* [`SFEData`](https://bioconductor.org/packages/release/data/experiment/html/SFEData.html)
* [`scater`](https://bioconductor.org/packages/release/bioc/html/scater.html)
* [`scran`](https://bioconductor.org/packages/release/bioc/html/scran.html)
* [`SingleCellExperiment`](https://bioconductor.org/packages/release/bioc/html/SingleCellExperiment.html)

### Time outline

Total: 90 minutes

| Activity                     | Time |
|------------------------------|------|
| Introduction                 | 15m  |
| Construct an SFE object      | 5m   |
| Novel fields of SFE          | 10m  |
| Geometric operations         | 10m  |
| Visualization and QC         | 10m  |
| Moran's I                    | 10m  |
| Local Moran's I              | 10m  |
| Lee's L                      | 10m  |
| MULTISPATI PCA               | 10m  |

### Workshop goals and objectives

* Appreciate the opportunities presented by the spatial information
* Learn basic spatial statistics

#### What you will learn
* Use and operate on `SpatialFeatureExperiment` (SFE) objects
* Spatial data visualization
* Create spatial neighborhood graphs
* Run spatial analyses on SFE objects
* Visualize spatial analysis results

#### What you will _not_ learn
* How different types of spatial transcriptomics technologies work
* Data integration across multiple samples
* Spatial multi-omics

## To use the Docker image

This workshop can be run remotely on the [Orchestra platform](http://app.orchestra.cancerdatasci.org/). Alternatively, it can be run
locally with the Docker image:

```sh
docker run -e PASSWORD=<choose_a_password_for_rstudio> -p 8787:8787 ghcr.io/lambdamoses/voyagerworkshop
```

Once running, navigate to http://localhost:8787/ and then login with `rstudio`:`yourchosenpassword`. 

The required packages of the appropriate version as of August 2023 have been
pre-installed on Orchestra and in the Docker image.
