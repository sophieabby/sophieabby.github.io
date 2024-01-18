---
title: "Genome Annotation"
excerpt: "We develop software and methods to improve genome annotations.<br/><img src='/images/logo_macsyfinder_sq_128.png' width='300'>"
collection: projects
---

We develop software and methods to improve genome annotations.

## MacSyFinder, the macromolecular system finder

In particular we developed [MacSyFinder](https://github.com/gem-pasteur/macsyfinder), a software to:

1. **model** molecular systems (pathways, machineries...) in microbial genomes
1. **annotate** them in genomes

MacSyFinder takes advantage of the genomic organization by function of archaeal and bacterial genomes: genes participating in a same function, complex, pathway...
tend to co-localize on the genome. This enables powerful, system-level (instead of gene-by-gene) annotation of functions.

For more details, have a look at the [corresponding publication(s)](https://doi.org/10.24072/pcjournal.250).

*The MacSyFinder v2 search engine*

<br/><img src='/images/Figure1_search_engine_MSF_v4.png' width='600'><br/>

Figure from [Néron et. al 2023.](https://doi.org/10.24072/pcjournal.250), the MSF v2 paper reviewed and [recommended by PCI Genomics](https://doi.org/10.24072/pci.genomics.100233).

## MacsyModels, an organization for sharing MacSyFinder models

Since MacSyFinder version 2, it is possible to easily download, install and share publicly available MacSyFinder models.
This is done from the [official MacSy-models organization](https://github.com/macsy-models). 
Several models are readily available, as [described in Néron et. al 2023.](https://doi.org/10.24072/pcjournal.250).

As of March 2023, Macsy Models included models for the detection of:

- CRISPR-Cas systems [CasFinder](https://github.com/macsy-models/CasFinder)
- bacterial protein secretion systems and type IV-filament super-family members [TXSScan](https://github.com/macsy-models/TXSScan)
- conjugative systems [CONJScan](https://github.com/macsy-models/CONJScan)

For more on how to install MacSyFinder and the associated Macsy Models, have a look at the comprehensive [MacSyFinder's documentation](https://macsyfinder.readthedocs.io/en/latest/).

## Writing own MacsyModels

In the following publication, we explain step-by-step how one can write its own MacsyModels (models' definition and profiles). 
If interested, have a look here:

[Abby, Denise and Rocha 2024](https://hal.science/hal-04257010v1) Identification of Protein Secretion Systems in Bacterial Genomes Using MacSyFinder Version 2, 2024 [https://link.springer.com/10.1007/978-1-0716-3445-5_1](https://link.springer.com/10.1007/978-1-0716-3445-5_1)