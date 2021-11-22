# SpanPSP
The pretrained models will be released soon.

## Environment
* Python 3.7 or higher.
* Pytorch 1.6.0, or any compatible version.
* NLTK 3.2, torch-struct 0.4, transformers 4.3.0, or compatible.
* pytokenizations 0.7.2 or compatible.

## Repository structure
Tacotron-2
├── datasets
├── en_UK		(0)
│   └── by_book
│       └── female
├── en_US		(0)
│   └── by_book
│       ├── female
│       └── male
├── LJSpeech-1.1	(0)
│   └── wavs
├── logs-Tacotron	(2)
│   ├── eval_-dir
│   │ 	├── plots
│ 	│ 	└── wavs
│   ├── mel-spectrograms
│   ├── plots
│   ├── taco_pretrained
│   ├── metas
│   └── wavs
├── logs-Wavenet	(4)
│   ├── eval-dir
│   │ 	├── plots
│ 	│ 	└── wavs
│   ├── plots
│   ├── wave_pretrained
│   ├── metas
│   └── wavs
├── logs-Tacotron-2	( * )
│   ├── eval-dir
│   │ 	├── plots
│ 	│ 	└── wavs
│   ├── plots
│   ├── taco_pretrained
│   ├── wave_pretrained
│   ├── metas
│   └── wavs
├── papers
├── tacotron
│   ├── models
│   └── utils
├── tacotron_output	(3)
│   ├── eval
│   ├── gta
│   ├── logs-eval
│   │   ├── plots
│   │   └── wavs
│   └── natural
├── wavenet_output	(5)
│   ├── plots
│   └── wavs
├── training_data	(1)
│   ├── audio
│   ├── linear
│	└── mels
└── wavenet_vocoder
	└── models

## Training and test with your dataset (soon)
### Data preprocessing

### Training

### Test

## Using the pre-trained model to automatically label the prosody structure of text data (soon)
### Data preprocessing

### Automatic labeling
