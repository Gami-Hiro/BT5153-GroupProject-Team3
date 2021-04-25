# BT5153-GroupProject-Team3
This repository is a project for BT5153 Applied Machine Learning 2021 Spring. We developed a product description generator in English for fashion apparel products, to be implemented on e-commerce platforms.  

![Screenshot_2021-04-24 102440](https://user-images.githubusercontent.com/77659181/115944370-ee755680-a4e7-11eb-8fc3-9b421e01e87b.png)


## Requirements
To run the notebooks successfully, you need to set up:

Python (3.7)
Jupyter Notebook

Additional libraries/packages installation codes might be required depends on your environment.

## Dataset
[Data For Model Training]
Please Download Full image fies from here(Around 3GB): https://drive.google.com/file/d/1K-Rcm1OO6W6sbbKVyQm8tDGh3m-RsLR6/view?usp=sharing  

Processed Full Descriptions are in the following path  
Data > Data_processed_reduced_v4.csv

Also, small sample pictures and data are in the following path
Data > Sample

## Table of Contents
- [Scraping](#Scraping)
- [Data Preprocessing](#Data-Preprocessing)
- [LSTM](#LSTM)
- [Transformer1](#Transformer1)
- [Transformer2](#Transformer2)
- [Result Confirmation](#Result-Confirmation)

## Scraping
For data scraping, we used Thirdparty software "Octoparse", but some website reject it. Hence for the website we wrote code with Selenium in Python.

Path of Code:  
Code > DataScraping > Web scraping scripts for several brands

## EDA and Data Preprocessing
EDA and the data preprocessing is executed in the code.

Path of Code:  
Code > EDA_and_Processing > EDA_after_processing.ipynb  
Code > EDA_and_Processing > EDA_before_processing.ipynb  
Code > EDA_and_Processing > Text_Cleaning.ipynb.ipynb  

## LSTM
We constructed a baseline model with long-short term memory networks (LSTM). Pre-trained models InceptionV3 and GloVe were used to obtain image and word vectors. LSTM can learn the context and long-term relationship between words in a sentence, and is thus suitable for NLP tasks. Our model uses previous words and the image to generate the next word in sequence. 

Path of Code:  
Code > Model > LSTM_Beam.ipynb  
Code > Model > LSTM_Greedy.ipynb  

## Transformer1
Transformer 1 adopts a standard Transformer model architecture, incorporating both encoders and decoders that apply attention mechanism. In our project, image features and target captions are passed into the model for training, and test predictions on image captions are later generated through both Greedy Search and BEAM Search to study model performance under different search algorithms.

Path of Code:  
Code > Model > Transformer1_Greedy_Beam.ipynb  

## Transformer2
In addition to the traditional transformer architecture, our group also built another Transformer with a decoder-only architecture (Transformer 2) in comparison with Transformer 1.Moreover, Transformer 2 applies the GloVe for its word embeddings. Our hypothesis is that the pre-trained GloVe shall deliver a better quality of word embeddings which in turn will improve our model performance. With different architectures, we intend to examine and compare the two Transformers’ performances.  

Path of Code:  
Code > Model > Transformer2_Greedy.ipynb  
Code > Model > Transformer2_Beam.ipynb  

## Model Insights & Case Studies  
We analyse the performance of our selected model, Transformer 2, across brands, and examine several case studies using saliency maps for explainability.

Path of Code:  
Code > Performance_Evaluation > Model Performance Insights and Case Studies.ipynb
