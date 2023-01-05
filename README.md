# Sign Language Translation using Transformer and RNN Encoder-Decoder

 The paper proposed some machine translation (MT) models to convert sign language into spoken language. The project focuses on the reimplementation of training the MT model to translate gloss-to-text to spoken language.
 
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
    ├── backtranslation.ipynb
    ├── backtranslator
    ├── data_processing.ipynb
    ├── nmt_with_attention_augmented.ipynb
    ├── nmt_with_attention_baseline.ipynb
    ├── predict.ipynb
    ├── translator
    └── translator_augmented

29 directories, 82 files
 ```
 
 ## Table of Content
- Requirements
- Dataset
- Data preprocessing
- Training
- Predict
- Evaluation

## Requirements
- python=3.7
- tensorflow-text>=2.10

## Dataset
The paper approach focuses on investigating two large German gloss-to-text dataset RWTH-PHOENIX-Weather 2014T and The Public DGS Corpus.
To experiment the adaptability of this approach and make the process more universal, we try a new English gloss-to-text dataset Synthetic English-ASL Gloss Parallel Corpus 2012.


## Data preprocessing
- Tokenization: Byte-pair Encoding and Unigram Tokenizer.
- Data augmentation: Backtranslation.


## Training
In this task we train the dataset solely on Transformer and RNN to compare the result.

Transformer
```
Transformer/transformer_training.ipynb
``` 

RNN Encoder-Decoder
```
seq2seq-tf/nmt_with_attention_baseline.ipynb
``` 

## Predict
Translate some sample to demonstrate how the system works.

Transformer
```
Transformer/transformer.ipynb
``` 

RNN Encoder-Decoder
```
seq2seq-tf/predict.ipynb
``` 

## Evaluation 
We use SacreBLEU to compute the accuracy of each approach. The best performance of Transformer network and RNN Encoder-Decoder is respectively 59.0 and 62.9
