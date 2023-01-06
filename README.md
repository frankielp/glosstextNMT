# Neural Machine Translation Methods for Sign Language Translation using Transformer and RNN Encoder-Decoder
 This repository provides the reimplement of the experiments described in the paper [Using Neural Machine Translation Methods for Sign Language Translation](https://aclanthology.org/2022.acl-srw.21) (Angelova et al., ACL 2022). 
 
![header](demo/data.png)
 ## File Structure
 ```
 .
├── LICENSE
├── README.md
├── Transformer
│   ├── dataset
│   ├── transformer.ipynb
│   └── transformer_training.ipynb
├── data
│   ├── gloss-text-augmented.txt
│   ├── gloss-text.txt
│   └── test.txt
├── german
└── seq2seq-tf
    ├── model
    ├── backtranslation.ipynb
    ├── data_processing.ipynb
    ├── nmt_with_attention_augmented.ipynb
    ├── nmt_with_attention_baseline.ipynb
    └── predict.ipynb

29 directories, 82 files
 ```
 
 ## Table of Content
- Requirements
- Dataset
- Implementation
- Evaluation

## Requirements
- python=3.7
- tensorflow-text>=2.10

## Dataset
The paper approach focuses on investigating two large German gloss-to-text dataset RWTH-PHOENIX-Weather 2014T and The Public DGS Corpus.
To experiment the adaptability of this approach and make the process more universal, we try a new English gloss-to-text dataset Synthetic English-ASL Gloss Parallel Corpus 2012.

## Implementation
 * `notebooks`: Python notebooks containing the code for reproducing the experiments
 
### Data preprocessing
- Tokenization: Byte-pair Encoding and Unigram Tokenizer.
- Data augmentation: Backtranslation.

### Training
In this task we train the dataset solely on Transformer and RNN Encoder-Decoder for performance comparison.

**Transformer**
```
Transformer/transformer_training.ipynb
``` 

**RNN Encoder-Decoder**
```
seq2seq-tf/nmt_with_attention_baseline.ipynb
``` 

### Predict
Translate some sample to demonstrate how the system works.

**Transformer**
```
Transformer/transformer.ipynb
``` 

**RNN Encoder-Decoder**
```
seq2seq-tf/predict.ipynb
``` 

## Evaluation 
We use SacreBLEU to compute the accuracy of each approach. The best performance of Transformer network and RNN Encoder-Decoder is on augmented dataset with respectively 71.0 and 62.9 BLEUScore.

## Citation
```
@inproceedings{angelova-etal-2022-using,
    title = "Using Neural Machine Translation Methods for Sign Language Translation",
    author = {Angelova, Galina  and
      Avramidis, Eleftherios  and
      M{\"o}ller, Sebastian},
    booktitle = "Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics: Student Research Workshop",
    month = may,
    year = "2022",
    address = "Dublin, Ireland",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2022.acl-srw.21",
    pages = "273--284",
}
```
