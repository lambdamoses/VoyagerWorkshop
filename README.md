# Bioc2023 Voyager ESDA workshop

## Overview

### Description

Exploratory spatial data analysis (ESDA) can be a powerful approach to understanding single-cell genomics datasets, but it is not yet part of standard data analysis workflows. In particular, geospatial analyses, which have been developed and refined for decades, have yet to be fully adapted and applied to spatial single-cell analysis. We introduce the `Voyager` platform, which systematically brings the geospatial ESDA tradition to (spatial) -omics, with local, bivariate, and multivariate spatial methods not yet commonly applied to spatial -omics, united by a uniform user interface. Using `Voyager`, we showcase biological insights that can be derived with its methods, such as biologically relevant negative spatial autocorrelation. Underlying `Voyager` is the `SpatialFeatureExperiment` (SFE) data structure, which combines Simple Feature with `SingleCellExperiment` and `AnnData` to represent and operate on geometries bundled with gene expression data. Voyager has comprehensive tutorials demonstrating ESDA built on GitHub Actions to ensure reproducibility and scalability, using data from popular commercial technologies. Voyager is implemented in both R/Bioconductor and Python/PyPI, and features compatibility tests to ensure that both implementations return consistent results. 

In this workshop, you will get hands on experiences on the R implementation of SFE and Voyager. First, you will learn to create and operate on SFE objects. Next you will perform various types of ESDA on an SFE object with Voyager, and learn the spatial statistics behind these methods. The workshop material points you to further reading on these methods. You can read more about Voyager in [this preprint](https://www.biorxiv.org/content/10.1101/2023.07.20.549945v1?ct=).

### Pre-requisites

To understand the workshop material, you are expected to have:

* Intermediate knowledge of R syntax and `ggplot2`
* Familiarity with `SingleCellExperiment`
* Familiarity with statistics and linear algebra, including principal component analysis (PCA)

The workshop material is taken from the documentation websites of [`Voyager`](https://pachterlab.github.io/voyager/) and [`SpatialFeatureExperiment`](https://pachterlab.github.io/SpatialFeatureExperiment/). Relevant vignettes will be linked to in the relevant sections.

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

| Activity                       | Time |
|--------------------------------|------|
| Introduction and setup         | 15m  |
| Construct an SFE object        | 5m   |
| Operations of SFE objects      | 15m  |
| ESDA with geometric operations | 15m  |
| Univariate global              | 10m  |
| Univariate local               | 10m  |
| Bivariate                      | 5m   |
| Multivariate                   | 15m  |

### Workshop goals and objectives

* Experience exploratory data analysis with the spatial information front and center
* Get a taste of the geospatial tradition

#### What you will learn
* Use and operate on SFE objects
* Spatial data visualization
* Geometric operations
* Create spatial neighborhood graphs
* Run spatial analyses on different fields of SFE objects
* Visualize spatial analysis results
* Math of some commonly used ESDA methods

#### What you will _not_ learn
* Technologies to collect spatial transcriptomics data
* Data integration across multiple samples
* Spatial multi-omics

## To use the Docker image

This workshop can be run remotely on the [Bioconductor Workshop Galaxy](https://workshop.bioconductor.org/). Alternatively, it can be run
locally with the Docker image:

```sh
docker run -e PASSWORD=<choose_a_password_for_rstudio> -p 8787:8787 ghcr.io/lambdamoses/voyagerworkshop
```

Once running, navigate to http://localhost:8787/ and then log in with `rstudio`:`yourchosenpassword`. 

The required packages of the appropriate version as of July 2023 have been
pre-installed on the Workshop Galaxy and in the Docker image.
