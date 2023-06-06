

# NegMed: Leveraging NLP Techniques for Negation and Uncertainty Detection in Medical Texts

Welcome to 'NegMed', on this project we will perform a Comparative Study of Rule-based and Deep Learning Approaches for negation, uncertainty and scope detection in medical documents


## Goals

Our Objective is to implement two different methods with which we are able to achieve the detection of Uncertainties, Negations and scopes.


## Content

This repository contains the code and report for the NLP project on Negation, Uncertainty and Scopes detection, using a Rule Based and a Deep Learning approach. 

## Table of Contents

- [Data](#Data)
- [Files](#Files)
- [Usage](#Execution)
- [Qualitative Evaluation](#Qualitative-Evaluation)
- [Final Words](#Final-Words)
- [Contributors](#Contributors)


### Data

You can get all the data you will need in the following folder from google drive so you don't need to search for it.

[ASHO Data](https://drive.google.com/file/d/1T64hrblTrrFRY6d9vLgFSjkM8Elrl9Vt/view?usp=sharing)



### Files

- **[NegMed_RuleBased.ipynb](https://github.com/Neilus03/NegMed/blob/main/NegMed_RuleBased.ipynb)**: This file contains:
  - `data handling`: A ResNet CNN pretrained on ImageNet that extracts features from the images.
  - `rule based algorithm`: An LSTM network that generates words recursively using the image features and captions as inputs.
  - `evaluation`: Combines the functionality of `encoderCNN` and `decoderRNN` to encode images and captions and produce codified sentences.
  
- **[NegMed_NER.ipynb](https://github.com/Neilus03/NegMed/blob/main/NegMed_NER.ipynb)**:  This file contains:
  - `data handling`: A ResNet CNN pretrained on ImageNet that extracts features from the images.
  - `Deep Learning based algorithm`: An LSTM network that generates words recursively using the image features and captions as inputs.
  - `evaluation`: Combines the functionality of `encoderCNN` and `decoderRNN` to encode images and captions and produce codified sentences.
  
  **DOWNLOAD THE NOTEBOOK AND OPEN IT IN COLAB FOR A BETTER VISUALIZATION**


### Qualitative Evaluation

Our evaluation focuses on two areas: the BLEU score and a visual inspection of the generated captions. The BLEU score gives us a quantitative measure of our model's performance, while the visual inspection of the generated captions lets us qualitatively assess the model's output. The original and generated captions are printed, and the average BLEU score across all images is computed.

### Final Words

This project is an exciting journey into the intersection of computer vision and natural language processing. We hope that this project can serve as a helpful resource for those interested in image captioning, deep learning, and AI in general.

It´s worth to note that our main goal has been always learning as much as we can, that´s why we chose this project, we really thought that would be the most challenging as well as self-rewarding, and so it has been, we put a lot of effort but it paid off completely, regardless of te mark.

We appreciate having had this experience that has helped us a lot to understand how complicated a Deep Learning project can be, but also how exciting it is to get results after having done hard work.





## Contributors

Authors: Neil De La Fuente, Maiol Sabater, Daniel Vidal

Subject: Neural Networks and Deep Learning.

Degreee in Artificial Intelligence, 2n course.

UAB, 2023.
