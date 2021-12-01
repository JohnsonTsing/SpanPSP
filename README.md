# SpanPSP
The pretrained models will be released soon.

## Environment
* Python 3.7 or higher.
* Pytorch 1.6.0, or any compatible version.
* NLTK 3.2, torch-struct 0.4, transformers 4.3.0, or compatible.
* pytokenizations 0.7.2 or compatible.

## Repository structure
![image](https://user-images.githubusercontent.com/70370966/142816162-726ac560-cc82-4d04-820c-270c59e53e1d.png)


## Training and test with your dataset (soon)
### Data preprocessing
First prepare your own dataset into the following format, and put it in the right place as shown in the repository structure.
```
$ python src/train_seq2tree.py
```
### Training
Train your model using:
```
$ python src/main.py  train  --train-path [your_training_data_path]  --dev-path [your_dev_data_path]  --model-path-base [your_saving_model_path] 
```
### Test
Test your model using:
```
$ python src/main.py  test  --model-path [your_trained_model_path]  --test-path [your_test_data_path]
```
## Using the pre-trained model to automatically label the prosody structure of text data (soon)
### Data preprocessing

### Automatic labeling
