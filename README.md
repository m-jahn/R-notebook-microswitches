# R-notebook-microswitches

![Last commit](https://img.shields.io/github/last-commit/m-jahn/r-notebook-microswitches/main)
[![Published](https://img.shields.io/badge/Published-Nat.Comm.2023-green.svg)](https://github.com/m-jahn)
[![DOI](https://zenodo.org/badge/476293457.svg)](https://zenodo.org/badge/latestdoi/476293457)


Analysis of human Frizzled 5 receptor mutants.

### Overview

This R notebook attempts the analysis of an array of mutants in one of the 10 human [Frizzled](https://en.wikipedia.org/wiki/Frizzled) receptors, Frizzled 5 (FZD5). Each mutant was predicted to alter receptor function based on computational structure/function analysis. The mutants are expected to either promote or repress receptor activation through Wnt binding. The canonical signaling cascade is: Wnt --> FZDR --> DVL --> GSK-3b --> APC --> beta-catenin --> gene regulation.

Different types of experimental data are available:

- `data/input/FZD_mutations.csv` - original GPCR computer model prediction of mutant effects
- `data/input/DVL_shift.csv` - Dishevelled (DVL) shift assay. Measures the phosphorylation status of the intracellular signal protein DVL through the FZD5 receptor (and its mutants)
- `data/input/DEP_recruitment.csv` - DEP recruitment assay. DEP is a truncated DVL and recruitment is measured via BRET, that indicates proximity of the two proteins with fluorescence transfer
- `data/input/TOPFlash.csv` - Top flash assay. Measures if a target gene of the beta-catenin signaling pathway becomes activated, relative to WT


All care was taken to adhere to good scientific practice in terms of statistics, reproducibility and code documentation. Please report any errors by filing a [github issue](https://github.com/m-jahn/R-notebook-microswitches) for this repository, or contact michael.jahn@scilifelab.se.


### Contents

- `data` - directory containing the input and output data
- `docs`- rendered pipeline in `html` format
  - [Analysis of human Frizzled receptor mutants](https://m-jahn.github.io/R-notebook-microswitches/Microswitches-analysis.nb.html)
- `figures` - exported figures from pipelines
- `pipeline` - data processing pipelines, R markdown format (`.Rmd`)

### How to run the pipeline(s)

The pipelines in this repository are self-contained and executable. The code _and_ the documentation are part of one and the same R markdown document for each pipeline. Pipelines can be downloaded and executed from the `pipeline` sub-folders. To simply view the rendered pipelines follow the links to the `*.html` reports at [Contents](#Contents).

To download the repository on your local drive use `git clone` in a (linux) terminal:

``` bash
cd /your-target-folder
git clone https://github.com/m-jahn/R-notebook-microswitches
```

Open a pipeline with Rstudio and execute code (chunks) with the `Run` button.
Alternatively, open an interactive R session and render the R markdown pipeline:

``` bash
require(rmarkdown)
rmarkdown::render("pipeline.Rmd")
```
