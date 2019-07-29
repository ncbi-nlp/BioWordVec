# BioWordVec: Improving Biomedical Word Embeddings with Subowrd Information and MeSH #
This sourcecode is a demo implementation described in the paper "BioWordVec:Improving Biomedical Word Embeddings with Subowrd Information and MeSH." This is research software, provided as is without express or implied warranties etc. see licence.txt for more details. We have tried to make it reasonably usable and provided help options, but adapting the system to new environments or transforming a corpus to the format used by the system may require significant effort. 

## Data files ##
Data: MeSH_graph.edgelist is the MeSH main-heading graph file. MeSH_dic.pkl.gz is used to align the MeSH heading ids with mention words. The PubMed corpus and MeSH RDF data can be download from NCBI. 
 
## Prerequisites ##
- python 3.5
- networkx 1.11
- gensim 2.3

## Usage ##

User can use BioWordVec.py to automatically learn the biomedical word embedding based on PubMed text corpus and MeSH data.

## Pre-trained word embedding ##

We created two specialized, task-dependent sets of word embeddings “Bio-embedding-intrinsic” and “Bio-embedding-extrinsic” via setting the context window size as 20 and 5, respectively. The pre-trained BioWordVec data are freely available on [Figshare](https://doi.org/10.6084/m9.figshare.6882647 ). "Bio-embedding-intrinsic" is for intrinsic tasks and used to calculate or predict semantic similarity between words, terms or sentences. "Bio_embedding_extrinsic" is for extrinsic tasks and used as the input for various downstream NLP tasks, such as relation extraction or text classification. Both sets are in binary format and contain 2,324,849 distinct words in total. All words were converted to lowercase and the number of dimensions is 200.

We used [UMNSRS](http://rxinformatics.umn.edu/SemanticRelatednessResources.html) datasets to evaluate the pre-trained word embeddings on medical word pair similarity.

| Word embeddings       |UMNSRS-Sim  (Pearson score)        | UMNSRS-Sim  (Spearman score)  | UMNSRS-Rel  (Pearson score)           |UMNSRS-Rel  (Pearson score)  |
| ------------- |:-------------:| -----:|:-------------:| -----:|
|[Pyysalo et al.](http://http://evexdb.org/pmresources/vec-space-models/)     | 0.662 | 0.652 |0.600 | 0.601 |
|[Chiu et al.](http://github.com/cambridgeltl/BioNLP-2016)     | 0.665     |  0.654|0.608      |  0.607|
| BioWordVec (win20) | 0.667    |   0.657 |0.619    |    0.617 |

We also used [BioCreative/OHNLP STS](https://sites.google.com/view/ohnlp2018/home) dataset to evaluate the pre-trained word embeddings on clinical sentence pair similarity. 

| Similarity measures      |[Pyysalo et al.](http://http://evexdb.org/pmresources/vec-space-models/)        | [Chiu et al.](http://github.com/cambridgeltl/BioNLP-2016)   | BioWordVec (win20) |
| ------------- |:-------------:| -----:|:-------------:|
|Cosine    | 0.755| 0.757 |0.771 |
|Euclidean     | 0.723     | 0.727|0.753 |
| Block |   0.722 |0.727   |    0.752 |

User can find more usage notes in our paper.

## References
When using some of our pre-trained models for your application, please cite the following paper:

Zhang Y, Chen Q, Yang Z, Lin H, Lu Z. [BioWordVec, improving biomedical word embeddings with subword information and MeSH](https://www.nature.com/articles/s41597-019-0055-0). Scientific Data. 2019.

## List of Contributors ##
Yijia  Zhang, Qingyu Chen, Zhihao Yang, Hongfei Lin and Zhiyong Lu

## Acknowledgments ##
This work was supported by the Intramural Research Programs of the National Institutes of Health, National Library of Medicine. We are grateful to the authors of fastText, Node2vec and UMNSRS for making their software and data publicly available.
> 
> 
