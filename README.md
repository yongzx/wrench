<h1 style="text-align:center">
<img style="vertical-align:middle" width="500" height="180" src="./images/wrench_logo.png" />
</h1>

## 🔧 Installation
[1] Install anaconda:
Instructions here: https://www.anaconda.com/download/

[2] Clone the repository:
```
git clone https://github.com/JieyuZ2/wrench.git
cd wrench
```

[3] Create virtual environment:
```
conda env create -f environment.yml
source activate wrench
```
If this not working or you want to use only a subset of modules of Wrench, check out this [wiki page](https://github.com/JieyuZ2/wrench/wiki/Environment-Installation)

## 🔧 Available Datasets

The datasets can be downloaded via [this](https://drive.google.com/drive/folders/1v55IKG2JN9fMtKJWU48B_5_DcPWGnpTq?usp=sharing).

or via command line

```
pip install gdown 
gdown https://drive.google.com/uc?id=19wMFmpoo_0ORhBzB6n16B1nRRX508AnJ
unzip datasets.zip
rm datasets.zip 
```

A documentation of dataset format and usage can be found in this [wiki-page](https://github.com/JieyuZ2/wrench/wiki/Dataset:-Format-and-Usage)

### classification:
| Name | Task | # class | # LF | # train | # validation | # test | data source | LF source | Multlling |
|:--------|:---------|:------|:------|:------|:------|:------|:------|:------|:------|
| Census | income clasification | 2 | 83 | 10083 | 5561 | 16281 | [link](http://archive.ics.uci.edu/ml/datasets/Census+Income) |[link](https://openreview.net/forum?id=SkeuexBtDr) | - |
| Youtube | spam clasification | 2 | 10 | 1586 | 120 | 250 | [link](https://archive.ics.uci.edu/ml/datasets/YouTube+Spam+Collection) | [link](https://github.com/snorkel-team/snorkel-tutorials/tree/master/spam) | - |
| SMS | spam clasification | 2 | 73 | 4571 | 500 | 500 | [link](https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection) | [link](https://openreview.net/forum?id=SkeuexBtDr) | - |
| IMDB | sentiment clasification | 2 | 8 | 20000 | 2500 | 2500 | [link](https://dl.acm.org/doi/10.5555/2002472.2002491) | [link](https://arxiv.org/abs/2010.04582) |
| Yelp | sentiment clasification | 2 | 8 | 30400 | 3800 | 3800 | [link](https://arxiv.org/abs/1509.01626) | [link](https://arxiv.org/abs/2010.04582) |
| AGNews | topic clasification | 4 | 9 | 96000 | 12000 | 12000 | [link](https://arxiv.org/abs/1509.01626) | [link](https://arxiv.org/abs/2010.04582) |
| TREC | question classification | 6 | 68 | 4965 | 500 | 500 | [link](https://aclanthology.org/C02-1150.pdf) | [link](https://openreview.net/forum?id=SkeuexBtDr) |
| Spouse | relation classification | 2 | 9 | 22254 | 2801 | 2701 | [link](http://ceur-ws.org/Vol-1568/paper8.pdf) | [link](https://arxiv.org/abs/1711.10160) |
| SemEval | relation classification | 9 | 164 | 1749 | 200 | 692 | [link](https://aclanthology.org/S10-1006/) | [link](https://arxiv.org/abs/1909.02177) |
| CDR | bio relation classification | 2 | 33 | 8430 | 920 | 4673 | [link](https://pubmed.ncbi.nlm.nih.gov/27651457/) | [link](https://arxiv.org/abs/1711.10160) |
| Chemprot | chemical relation classification | 10 | 26 | 12861 | 1607 | 1607 | [link](https://www.semanticscholar.org/paper/Overview-of-the-BioCreative-VI-chemical-protein-Krallinger-Rabal/eed781f498b563df5a9e8a241c67d63dd1d92ad5) | [link](https://arxiv.org/abs/2010.07835) |
| Commercial | video frame classification | 2 | 4 | 64130 | 9479 | 7496 | [link](https://arxiv.org/pdf/2002.11955.pdf) | [link](https://arxiv.org/abs/2002.11955) |
| Tennis Rally | video frame classification | 2 | 6 | 6959 | 746 | 1098 | [link](https://arxiv.org/pdf/2002.11955.pdf) | [link](https://arxiv.org/abs/2002.11955) |
| Basketball | video frame classification | 2 | 4 | 17970 | 1064 | 1222 | [link](https://arxiv.org/pdf/2002.11955.pdf) | [link](https://arxiv.org/abs/2002.11955) |
| [DomainNet](https://github.com/JieyuZ2/wrench/tree/main/datasets/domainnet) | image classification | - | - | - | - | - | [link](https://arxiv.org/pdf/1812.01754.pdf) | [link](http://cs.brown.edu/people/sbach/files/mazzetto-icml21.pdf) |

### sequence tagging:
| Name | # class | # LF | # train | # validation | # test | data source | LF source |
|:--------|:---------|:------|:------|:------|:------|:------|:------|
| CoNLL-03 | 4 | 16 | 14041 | 3250 | 3453 | [link](https://arxiv.org/abs/cs/0306050) | [link](https://arxiv.org/abs/2004.14723) |
| WikiGold | 4 | 16 | 1355 | 169 | 170 | [link](https://dl.acm.org/doi/10.5555/1699765.1699767) | [link](https://arxiv.org/abs/2004.14723) |
| OntoNotes 5.0 | 18 | 17 | 115812 | 5000 | 22897 | [link](https://catalog.ldc.upenn.edu/LDC2013T19) | [link]() |
| BC5CDR | 2 | 9 | 500 | 500 | 500 | [link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4860626/) | [link](https://arxiv.org/abs/2105.12848) |
| NCBI-Disease  | 1 | 5 | 592 | 99 | 99 | [link](https://pubmed.ncbi.nlm.nih.gov/24393765/) | [link](https://arxiv.org/abs/2105.12848) |
| Laptop-Review | 1 | 3 | 2436 | 609 | 800 | [link](https://aclanthology.org/S14-2004/) | [link](https://arxiv.org/abs/2105.12848) |
| MIT-Restaurant | 8 | 16 | 7159 | 500 | 1521 | [link](https://groups.csail.mit.edu/sls/publications/2013/Liu_ASRU_2013.pdf) | [link]() |
| MIT-Movies | 12 | 7 | 9241 | 500 | 2441 | [link](http://people.csail.mit.edu/jrg/2013/liu-icassp13.pdf) | [link]() |

