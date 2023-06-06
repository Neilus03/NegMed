

# NegMed: Leveraging NLP Techniques for Negation and Uncertainty Detection in Medical Texts

Welcome to 'NegMed', on this project we will perform a Comparative Study of Rule-based and Deep Learning Approaches for negation, uncertainty and scope detection in medical documents

## Content

This folder contains the code and files for the Image Captioning project, using a CNN and RNN. 

## Table of Contents

- [Files](#Files)
- [Requirements](#Requirements)
- [Installation and Usage](#Execution)
- [Using different datasets](#Using-Different-Datasets)
- [Configuration](#Trying-Different-Configurations)
- [APP](#APP)
- [QUANTITATIVE and QUALITATIVE ANALYSIS](#QUANTITATIVE-and-QUALITATIVE-ANALYSIS)## Content

This folder contains the code and files for the Image Captioning project, using a CNN and RNN. 

## Table of Contents

- [Files](#Files)
- [Requirements](#Requirements)
- [Installation and Usage](#Execution)
- [Using different datasets](#Using-Different-Datasets)
- [Configuration](#Trying-Different-Configurations)
- [APP](#APP)
- [QUANTITATIVE and QUALITATIVE ANALYSIS](#QUANTITATIVE-and-QUALITATIVE-ANALYSIS)

## Goals

Our Objective is to implement different models with different configurations and structures that are able to train and provide some results, and highlight the best results. Another goal is to try different ways to test our model, using different metrics and testing it with different datasets such as COCO dataset or Flickr30k dataset, but in principle we are going to use the Flickr8k dataset.

## Data

You can get all the data you will need in the following folder from google drive so you don't need to search for it.

[Image Captioning Data](https://drive.google.com/drive/folders/1skoIZFClsh_Ol-wiwG_Foo53BQF8KOMW?usp=sharing)



### Files

- **model.py**: This file contains the structure of the model in different classes. The classes include:
  - `encoderCNN`: A ResNet CNN pretrained on ImageNet that extracts features from the images.
  - `decoderRNN`: An LSTM network that generates words recursively using the image features and captions as inputs.
  - `CNNtoRNN`: Combines the functionality of `encoderCNN` and `decoderRNN` to encode images and captions and produce codified sentences.

- **get_loader.py**: This file contains a function to create data loaders for the project. It includes the following classes:
  - `Vocabulary`: Creates the vocabulary by tokenizing words in the captions using the "en_core_web_sm" language model from spacy.
  - `FlickrDataset`: Generates a data loader by loading image filenames, captions, and the vocabulary.
  - `Padding`: Adds padding to captions in a batch to ensure uniform length.

- **utils.py**: This file contains two utility functions:
  - `save_checkpoint`: Saves the model in a .pth file.
  - `load_checkpoint`: Loads a pre-trained model from a .pth file.

- **train.py**: This script trains an image captioning model using a CNN-to-RNN architecture. It loads the image and caption datasets, creates data loaders, initializes the model, loss function, and optimizer. The script performs the training loop for a specified number of epochs, logs the training loss using TensorBoard, and saves the final model checkpoint and training loss curve.

- **evaluation.py**: This script evaluates the trained model. It prompts the user to enter the path to the trained model checkpoint, generates captions for sample images, and displays the generated captions, BLEU scores, and ground truth captions for comparison.

### Requirements

To run this project, you need to download the image and caption datasets. The datasets are available for download using the following link: [flickr8k Dataset](https://drive.google.com/drive/folders/1skoIZFClsh_Ol-wiwG_Foo53BQF8KOMW?usp=sharing). Download the training images and captions, as well as the validation images and captions as separate files.

You will also need the following libraries, packages, and frameworks:
- PyTorch
- Spacy
- OS
- Pandas
- NumPy
- PIL (Pillow)


## Getting Started

First, you need to set clone this repository in your local (or virtual) machine

```
git@github.com:DCC-UAB/dlnn-project_ia-group_05.git
```

You will need to install the needed libraries and set up a good environment with pytorch, spacy, PIL and many more. You will also need to download the en_core_web_sm language model using:

```
python -m spacy download en_core_web_sm
```

Next, to train either of the models, use:

for model without attention:
```
cd Pixtales/Image_captioning 
```
for model with attention: 
```
cd Pixtales/Image_captioning_with_attention
```
then:
```
python train.py
```
If you want to use our already trained models just load the checkpoint we have prepared in a folder from drive. Here you can found checkpoints for different models, you can download from here to use them for testing the model or training it a little more:

[Checkpoints of different models](https://drive.google.com/drive/folders/1ada905qZpaIdcILrhixOt4uVA2xHtHzt?usp=sharing)

and run evaluation:

```
python evaluation.py
```
## Code Structure

The code in this repository primarily consists of a model implementation (CNNtoRNN), a dataset loading function (get_loader), a utils.py file that is used to save and load the models and a train file for training the model and saving the model with in a pth file called checkpoint; the training uses all previous files. We also have an evaluation.py file that loads a model already trained to do some test and show some examples, it provides utility functions for generating and visualizing image captions and calculating BLEU scores, a popular metric for evaluating the quality of generated text in comparison to reference text. 

## Model Evaluation

Our evaluation focuses on two areas: the BLEU score and a visual inspection of the generated captions. The BLEU score gives us a quantitative measure of our model's performance, while the visual inspection of the generated captions lets us qualitatively assess the model's output. The original and generated captions are printed, and the average BLEU score across all images is computed.

## Final Words

This project is an exciting journey into the intersection of computer vision and natural language processing. We hope that this project can serve as a helpful resource for those interested in image captioning, deep learning, and AI in general.

It´s worth to note that our main goal has been always learning as much as we can, that´s why we chose this project, we really thought that would be the most challenging as well as self-rewarding, and so it has been, we put a lot of effort but it paid off completely, regardless of te mark.

We appreciate having had this experience that has helped us a lot to understand how complicated a Deep Learning project can be, but also how exciting it is to get results after having done hard work.



## References
[CS 152 NN—25: Attention: Image Captioning by Neil Rhodes](https://youtu.be/JTXPrjvhLl8)

[Show, Attend and Tell](https://arxiv.org/abs/1502.03044)


## Contributors

Authors: Neil De La Fuente, Maiol Sabater, Daniel Vidal

Subject: Neural Networks and Deep Learning.

Degreee in Artificial Intelligence, 2n course.

UAB, 2023.
