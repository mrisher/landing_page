---
draft: true
id: 2
title: Common datasets snapshots
weight: 1
---

Understanding that creating embeddings every time can be a resource-intensive task, we have 
devised a more efficient solution for you. In this section, we will regularly publish 
snapshots of common public datasets often used for general or educational purposes. These 
snapshots contain pre-computed vectors, critical for semantic search, that you can easily 
import into your Qdrant instance. Our objective is to streamline your process and accelerate 
your progress. Say goodbye to redundant operations and harness the power of Qdrant with 
a simple [snapshot import](/documentation/concepts/snapshots/).

# Datasets

## Arxiv.org

[Arxiv.org](https://arxiv.org), often simply referred to as arXiv, is a highly-regarded, 
open-access repository of electronic preprints in multiple fields. Operated by Cornell 
University, arXiv allows researchers to share their findings with the scientific community 
and receive feedback before they undergo peer review for formal publication. Its archives 
host millions of scholarly articles, making it an invaluable resource for those looking 
to explore the cutting edge of scientific research. With a high frequency of daily 
submissions from scientists around the world, arXiv forms a comprehensive, evolving dataset 
that is ripe for mining, analysis, and the development of future innovations.

Arxiv.org snapshots were created using precomputed embeddings exposed by
[the Alexandria Index](https://alex.macrocosm.so/download).

### Only titles

This dataset contains embeddings generated from the paper titles only. Each vector has a
payload with the title used to create it, along with the DOI (Digital Object Identifier).

```json
{
    "title": "Nash Social Welfare for Indivisible Items under Separable, Piecewise-Linear Concave Utilities",
    "DOI": "1612.05191"
}
```

#### Snapshots

<table>
   <thead>
      <tr>
         <th>Model</th>
         <th>Dimensionality</th>
         <th>Documents</th>
         <th>Size</th>
         <th>Link</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td><a href="https://huggingface.co/hkunlp/instructor-xl">InstructorXL</a></td>
         <td>768</td>
         <td>2.3M</td>
         <td>7.1 GB</td>
         <td>
            <a href="https://storage.googleapis.com/common-datasets-snapshots/arxiv_titles-3083016565637815127-2023-05-29-13-56-22.snapshot">
                <img src="/images/icons/download.svg" alt="download" />
            </a>
         </td>
      </tr>
   </tbody>
</table>

### Only abstracts

This dataset contains embeddings generated from the paper abstracts. Each vector has a
payload with the abstract used to create it, along with the DOI (Digital Object Identifier).

```json
{
    "abstract": "Recently Cole and Gkatzelis gave the first constant factor approximation\nalgorithm for the problem of allocating indivisible items to agents, under\nadditive valuations, so as to maximize the Nash Social Welfare. We give\nconstant factor algorithms for a substantial generalization of their problem --\nto the case of separable, piecewise-linear concave utility functions. We give\ntwo such algorithms, the first using market equilibria and the second using the\ntheory of stable polynomials.\n  In AGT, there is a paucity of methods for the design of mechanisms for the\nallocation of indivisible goods and the result of Cole and Gkatzelis seemed to\nbe taking a major step towards filling this gap. Our result can be seen as\nanother step in this direction.\n",
    "DOI": "1612.05191"
}
```
<table>
   <thead>
      <tr>
         <th>Model</th>
         <th>Dimensionality</th>
         <th>Documents</th>
         <th>Size</th>
         <th>Link</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td><a href="https://huggingface.co/hkunlp/instructor-xl">InstructorXL</a></td>
         <td>768</td>
         <td>2.3M</td>
         <td>8.4 GB</td>
         <td>
            <a href="https://storage.googleapis.com/common-datasets-snapshots/arxiv_abstracts-3083016565637815127-2023-06-02-07-26-29.snapshot">
                <img src="/images/icons/download.svg" alt="download" />
            </a>
         </td>
      </tr>
   </tbody>
</table>

# Importing the snapshot

Qdrant documentation describes the process of [recovering a snapshot](/documentation/concepts/snapshots/#restore-snapshot)
from a .tar archive.
