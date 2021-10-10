# HowSumm dataset

HowSumm is a large-scale Query-focused multi-document summarization dataset.
It is focused on summarization of various sources to create HowTo guides. It is derived from [wikiHow](https://www.wikihow.com/) articles.

HowSumm is partitioned into HowSumm-Step where target summary is relatively short (avg. 90  words) and HowSumm-Method where target summary is a concatenation of several steps an therefore longer (avg. 500 words). 
HowSumm-Method and HowSumm-Step contain 11,121 and 84348 instances, respectively. 

For more information regarding the dataset derivation and characteristics as well as various models results on this dataset please see our paper [here](https://arxiv.org/abs/2110.03179).

## HowSumm format

HowSumm is released with a partition in Train/Test/Valid files.
Each file is in [JSON Lines format](https://jsonlines.org/).

A HowSumm-Step entry (line) has the following format:
- **url** : wikiHow article's url
- **title** : wikiHow article's title
- **target-summary** : summary extracted from wikiHow article (step text) 
- **method** : corresponding method name 
- **step** : step title
- **sources** : a list of archived urls of references for the given step
- **categories** : the list of categories of the wikiHow article
 
A HowSumm-Method entry (line) has the following format:
- **url** : wikiHow article's url
- **title** : wikiHow article's title
- **target-summary** : summary extracted from wikiHow article (method text) 
- **method** : method title 
- **steps** : a list of step titles comprising the given method
- **sources** : a list of archived urls of references for the given method
- **categories** : the list of categories of the wikiHow article.

## Acqiuring the data
The text files containing the data reside under data folder. 
You can either download the data files one by one directly from GitHub, or clone this entire repository. 
Please note that since training files are large, your local repository will contain only the links to these files. 
In order to pull the files themselves, you should use [git large file storage](https://git-lfs.github.com).


## Citation
If you use this dataset in your work, please cite our paper:

@misc{boni2021howsumm,
      title={HowSumm: A Multi-Document Summarization Dataset Derived from WikiHow Articles}, 
      author={Odellia Boni and Guy Feigenblat and Guy Lev and Michal Shmueli-Scheuer and Benjamin Sznajder and David Konopnicki},
      year={2021},
      eprint={2110.03179},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}

## License
Dataset released under the CC BY-NC-SA 3.0 license https://creativecommons.org/licenses/by-nc-sa/3.0/legalcode

## Disclaimer
IBM is not responsible for the content of the data, nor for any claim related to the data (including claims related to alleged intellectual property or privacy breach).
