BioWordVec: Improving Biomedical Word Embeddings with Subowrd Information and MeSH
================================================================================

This sourcecode is a demo implementation described in the paper "BioWordVec:Improving Biomedical Word Embeddings with Subowrd Information and MeSH."

This is research software, provided as is without express or implied warranties etc. see licence.txt for more details. We have tried to make it reasonably usable and provided help options, but adapting the system to new environments or transforming a corpus to the format used by the system may require significant effort. 

The details of related files are described as follows:

Data: MeSH_graph.edgelist is the MeSH main-heading graph file.  MeSH_dic.pkl.gz is used to align the MeSH heading ids with mention words. Due to the limitation of the github, we only upload a sample PubMed corpus. The PubMed corpus and MeSH RDF data can be download from NCBI. 
 

Prerequisites

* python 3.5
* networkx 1.11
* gensim 2.3


Usage

User can use BioWordVec.py to automatically learn the biomedical word embedding based on PubMed text corpus and MeSH data.


List of Contributors

Yijia  Zhang
Qingyu Chen
Zhihao Yang
Hongfei Lin
Zhiyong Lu

Acknowledgments

This work was supported by the Intramural Research Programs of the National Institutes of Health, National Library of Medicine. 