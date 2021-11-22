# SpanPSP
The pretrained models will be released soon.

## Environment
* Python 3.7 or higher.
* Pytorch 1.6.0, or any compatible version.
* NLTK 3.2, torch-struct 0.4, transformers 4.3.0, or compatible.
* pytokenizations 0.7.2 or compatible.

## Repository structure
|——bert-base-chinese
|          |——config.json
|          |——pytorch_model.bin
|          |——vocab.txt
|——data
|          |——train
|          |          |——raw_data
|          |          |          |——raw_train.txt
|          |          |          |——raw_validate.txt
|          |          |          |——raw_test.txt
|          |          |——tree_data
|          |                     |——tree_train.txt
|          |                     |——tree_validate.txt
|          |                     |——tree_test.txt
|          |——inference
|                     |——raw_data
|                     |          |——raw_data.txt
|                     |——tree_data
|                                |——tree_data.txt
|——models
|         |——pretrained_model
|         |           |——pretrained_SpanPSP.pt
|         |——yours
|——src
|         |——benepar
|                     |—— ...
|         |——count_fscore.py
|         |——evaluate.py
|         |——export.py
|         |——inference_seq2tree.py
|         |——learning_rate.py
|         |——main.py
|         |——seq_with_label.py
|         |——train_seq2tree.py
|         |——transliterate.py
|         |——treebank.py
|——README.md

## Training and test with your dataset (soon)
### Data preprocessing

### Training

### Test

## Using the pre-trained model to automatically label the prosody structure of text data (soon)
### Data preprocessing

### Automatic labeling
