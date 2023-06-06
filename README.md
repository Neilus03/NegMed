

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
  - `data handling`: Create the groundtruth used for the qualitative evaluation for the negations, uncertainties and its respectives scopes. We have also extracted the texts in order to evaluate out method
  - `rule based algorithm`: Series of functions in order to detect and extract the negations, uncertainties and its scopes and return the respectives in the same format as the grountruth to then evaluate.
  - `evaluation`: Quantitative results of the rule-based method, `precision`, `recall` and `f-score`.
  
- **[NegMed_NER.ipynb](https://github.com/Neilus03/NegMed/blob/main/NegMed_NER.ipynb)**:  This file contains:
  - `data handling`: A ResNet CNN pretrained on ImageNet that extracts features from the images.
  - `Deep Learning based algorithm`: An LSTM network that generates words recursively using the image features and captions as inputs.
  - `evaluation`: Both quantitaive and qualitative results of the deep learning model, `precision`, `recall` and `f-score` and examples of what returns our model when passing different texts (both medical and from other diverse topics such as legal or sports-related).
  
  **DOWNLOAD THE NOTEBOOK AND OPEN IT IN COLAB FOR A BETTER VISUALIZATION**


- **[NegMed Report](https://github.com/Neilus03/NegMed/blob/main/NegMed-Report%20.pdf)** This file contains:
  - A deep explanation of all our code and project in general along with results and analysis
- **[NegMed Presentation](https://github.com/Neilus03/NegMed/blob/main/NegMed-Presentation.pdf)** This file contains:
  - The presentation where we summarizae and show the project and results

### Qualitative Evaluation
Below some qualitative examples that show the nice performance of our Deep Learning based **NER** model:

**1) Validation data from the original dataset:**
![Screen Shot 2023-06-06 at 6 25 25 PM](https://github.com/Neilus03/NegMed/assets/87651732/7fa1e94b-2f51-4a30-8371-9c0b60172a73)


![Screen Shot 2023-06-06 at 6 26 35 PM](https://github.com/Neilus03/NegMed/assets/87651732/58c1219c-24b6-410c-9f80-53f46e599e02)

**2) Medical data outside the original dataset, never seen before by our model**
![Screen Shot 2023-06-06 at 6 27 37 PM](https://github.com/Neilus03/NegMed/assets/87651732/9f787a39-b8dc-4787-8ae1-481799edeac8)
![Screen Shot 2023-06-06 at 6 30 12 PM (1)](https://github.com/Neilus03/NegMed/assets/87651732/af7ca88f-56c4-41e1-a768-3c991a449242)

**3) Generalization to Law texts**
![Screen Shot 2023-06-06 at 6 31 14 PM](https://github.com/Neilus03/NegMed/assets/87651732/2868a6aa-eb9d-4a5d-acc4-16cba2b26963)
**4) Generalization to Sports texts**
![Screen Shot 2023-06-06 at 6 32 02 PM](https://github.com/Neilus03/NegMed/assets/87651732/77f7e938-72cc-45de-8c30-3fa87e1b2d34)

### Final Words

This project is an exciting journey into the intersection of medical texts and natural language processing. We hope that this project can serve as a helpful resource for those interested in Named Entity Recognition, deep learning, and AI in general.

We appreciate having had this experience that has helped us a lot to understand how complicated a real world NLP project can be, but also how exciting it is to get results after having done hard work.





### Contributors

Authors: **[Neil De La Fuente](https://github.com/Neilus03)** , **[Paula Feliu](https://github.com/paulafeliu)** , **[Roger Garcia](https://github.com/RoysGC)** , **[Daniel Vidal](https://github.com/Dani13vg)**

Subject: Natural Language Processing.

Degreee in Artificial Intelligence, 2nd course.

UAB, 2023.
