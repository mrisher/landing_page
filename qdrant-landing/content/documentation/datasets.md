---
title: Practice Datasets
weight: 31
---

# Common Datasets in Snapshot Format

You may find that creating embeddings from datasets is a very resource-intensive task. 
If you need a practice dataset, feel free to pick one of the ready-made snapshots on this page.
These snapshots contain pre-computed vectors that you can easily import into your Qdrant instance.

Once you download a snapshot, you need to restore it using the Qdrant CLI upon startup. 

**Tutorials:** You may either [**restore a dataset from a snapshot**](/documentation/concepts/snapshots/#restore-snapshot) or [**create a snapshot from a dataset**](/documentation/tutorials/create-snapshot/).

## Arxiv.org Sample Text Data

Our snapshots are generated from publicly available datasets, which are often used for commercial or academic purposes. [Arxiv.org](https://arxiv.org) is a highly-regarded open-access repository of electronic preprints in multiple fields. Operated by Cornell University, arXiv allows researchers to share their findings with the scientific community 
and receive feedback before they undergo peer review for formal publication. Its archives 
host millions of scholarly articles, making it an invaluable resource for those looking 
to explore the cutting edge of scientific research. With a high frequency of daily 
submissions from scientists around the world, arXiv forms a comprehensive, evolving dataset 
that is ripe for mining, analysis, and the development of future innovations.

Arxiv.org snapshots were created using precomputed embeddings exposed by
[the Alexandria Index](https://alex.macrocosm.so/download).


## Journal Article Titles 

This dataset contains embeddings generated from the paper titles only. Each vector has a
payload with the title used to create it, along with the DOI (Digital Object Identifier).

```json
{
    "title": "Nash Social Welfare for Indivisible Items under Separable, Piecewise-Linear Concave Utilities",
    "DOI": "1612.05191"
}
```
|Models|Dimensionality|Documents|Size|Link|
|-|-|-|-|-|
|[InstructorXL](https://huggingface.co/hkunlp/instructor-xl)|768|2.3M|7.1 GB|[DOWNLOAD LINK](https://storage.googleapis.com/common-datasets-snapshots/arxiv_titles-3083016565637815127-2023-05-29-13-56-22.snapshot)|


## Journal Article Abstracts

This dataset contains embeddings generated from the paper abstracts. Each vector has a
payload with the abstract used to create it, along with the DOI (Digital Object Identifier).

```json
{
    "abstract": "Recently Cole and Gkatzelis gave the first constant factor approximation\nalgorithm for the problem of allocating indivisible items to agents, under\nadditive valuations, so as to maximize the Nash Social Welfare. We give\nconstant factor algorithms for a substantial generalization of their problem --\nto the case of separable, piecewise-linear concave utility functions. We give\ntwo such algorithms, the first using market equilibria and the second using the\ntheory of stable polynomials.\n  In AGT, there is a paucity of methods for the design of mechanisms for the\nallocation of indivisible goods and the result of Cole and Gkatzelis seemed to\nbe taking a major step towards filling this gap. Our result can be seen as\nanother step in this direction.\n",
    "DOI": "1612.05191"
}
```
|Models|Dimensionality|Documents|Size|Link|
|-|-|-|-|-|
|[InstructorXL](https://huggingface.co/hkunlp/instructor-xl)|768|2.3M|8.4 GB|[DOWNLOAD LINK](https://storage.googleapis.com/common-datasets-snapshots/arxiv_abstracts-3083016565637815127-2023-06-02-07-26-29.snapshot)|



