# The Great Repertoire Project v2

This repository contains code and data used in our study of the temporal dynamics of the circulating human antibody repertoire. Briefly, we investigated the dynamics of the human antibody repertoire over time using high-throughput sequencing of antibody transcripts in the peripheral blood. Our study uncovers a profound and previously underappreciated level of repertoire drift of the naïve B cell repertoire within individuals. Despite stable overall repertoire size and diversity, fine-level composition undergoes nearly complete turnover after four years. We observe a delicate interplay between the continuous replacement of naïve B cells and the imprint of immunological exposures, revealing a nuanced model of overall repertoire development. Additionally, a notable feature is the identification of persistent public clonotypes suggesting potentially convergent antibody responses. These findings deepen our understanding of immune system dynamics and offer important insights toward the optimization of vaccine and immunotherapy strategies.

## Code
The code used in this project is assembled into a series of Juypter notecooks. There are two sets of notebooks, those containing code used for [DATA PROCESSING](https://github.com/CollinJ0/grp2_paper/tree/master/data_processing) and those containing code used to [MAKE FIGURES](https://github.com/CollinJ0/grp2_paper/tree/master/make_figures). GitHub will render each of the notebooks, but the code cannot be executed from within GitHub. If you'd like to actually run the code contained in the notebooks, you must clone the repository.

**_NOTE:_** *Whenever possible, the intermediate datasets required to run the code are included in this repository, however, many intermediate datasets are too large to be included. In such cases, links to the required datasets are provided in the appropriate notebook.*

## Datasets  
We have generated several large datasets, in two primary groups: antibody sequences from two healthy adult subjects in 2016, and antibody sequences from the same two healthy adult subjects after four years. 

### Antibody sequencing data
Raw and processed datasets from each subject can be downloaded using the following links. Some of these datasets are quite large.

  - 327059-2016
    - Sequences: [**raw FASTQs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/327059_HCGTCBCXY_raw-fastqs.tar.gz), [**consensus FASTAs**](https://burtonlab.s3.amazonaws.com/Collin/Recalled_Leukopaks/UID18_Consensus_Fastas/327059-2016_UID18-cdr3nt-90-consensus_030323.tar.gz)
    - FASTQC:  [**pre-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/327059_HCGTCBCXY_pre-trimmed-fastqc.tar.gz)
    - Annotated data: [**consensus AIRR TSVs**](https://burtonlab.s3.amazonaws.com/Collin/Recalled_Leukopaks/UID18_Consensus_AIRR_Format/327059-2016_consensus_AIRR_format_03032023.tar.gz)
  - D103-2016
    - Sequences: [**raw FASTQs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/D103_HCGCLBCXY_raw-fastqs.tar.gz), [**consensus FASTAs**](https://burtonlab.s3.amazonaws.com/Collin/Recalled_Leukopaks/UID18_Consensus_Fastas/D103-2016_UID18-cdr3nt-90-consensus_030323.tar.gz)
    - FASTQC:  [**pre-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/D103_HCGCLBCXY_pre-trimmed-fastqc.tar.gz)
    - Annotated data: [**consensus AIRR TSVs**](https://burtonlab.s3.amazonaws.com/Collin/Recalled_Leukopaks/UID18_Consensus_AIRR_Format/D103_2016_UID18_consensus_AIRR_format_03032023.tar.gz)
  - 327059-2020
    - Sequences: [**raw FASTQs**](https://burtonlab.s3.amazonaws.com/Collin/Recalled_Leukopaks/Raw_Fastqs/327059_2020_AHW5K7DRXX_raw_fastqs.tar.gz), [**consensus FASTAs**](https://burtonlab.s3.amazonaws.com/Collin/Recalled_Leukopaks/UID18_Consensus_Fastas/327059-2020_UID18-cdr3nt-90-consensus_030323.tar.gz)
    - FASTQC:  [**pre-trimming**](https://burtonlab.s3.amazonaws.com/Collin/Recalled_Leukopaks/Raw_Fastqs/327059_2020_AHW5K7DRXX_pre-trimmed-fastqc.tar.gz)
    - Annotated data: [**consensus AIRR TSVs**](https://burtonlab.s3.amazonaws.com/Collin/Recalled_Leukopaks/UID18_Consensus_AIRR_Format/327059-2020_consensus_AIRR_format_03032023.tar.gz)
  - D103-2021
    - Sequences: [**raw FASTQs**](https://burtonlab.s3.amazonaws.com/Collin/Recalled_Leukopaks/Raw_Fastqs/D103_2021_AHMTFMDRXY_raw_fastqs.tar.gz), [**consensus FASTAs**](https://burtonlab.s3.amazonaws.com/Collin/Recalled_Leukopaks/UID18_Consensus_Fastas/D103_2021_UID18-cdr3nt-90-consensus_03032023.tar.gz)
    - FASTQC:  [**pre-trimming**](https://burtonlab.s3.amazonaws.com/Collin/Recalled_Leukopaks/Raw_Fastqs/D103_2021_AHMTFMDRXY_pre-trimmed-fastqc.tar.gz)
    - Annotated data: [**consensus AIRR TSVs**](https://burtonlab.s3.amazonaws.com/Collin/Recalled_Leukopaks/UID18_Consensus_AIRR_Format/D103_2021_UID18_consensus_AIRR_format_03032023.tar.gz)

For each timepoint, there are a total of 18 samples: 3 technical replicates of each of 6 biological replicates. Biological replicates refer to different aliquots of peripheral blood monomuclear cells (**PBMCs**), from which total RNA was separately isolated and processed. Thus, sequences or clonotypes found in multiple biological replicates are assumed to have independently occurred in different cells. Technical relicates refer to independent library preparations using the same aliquot of PBMC-derived RNA. In each of the above datasets, samples 1-6 are biological replicates. Samples 7-12 and 13-18 are technical replicates of samples 1-6.

## Requirements

  - Python 3.3+ (although Python 2.7 may work for many or most notebooks, this has not been tested)
  - [Jupyter Notebook](https://jupyter.org/install)

*Additionally, each notebook may require additional third-party Python packages. Any notebook-specific requirements, as well as instructions for package installation with [pip](https://pip.pypa.io/en/stable/installing/), are provided in each notebook.*

If you're new to Python, a great way to get started is to install the [Anaconda Python distribution](https://www.continuum.io/downloads), which includes pip as well as a ton of useful scientific Python packages.

