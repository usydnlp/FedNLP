# FedNLP: An Interpretable NLP System to Decode Federal Reserve Communications

This repository contains dataset for paper [FedNLP: An interpretable NLP System to Decode Federal Reserve Communications](https://arxiv.org/pdf/2106.06247.pdf). 

### <div align="center"> Jean Lee, Hoyoul Luis Youn, Nicholas Stevens, Josiah Poon, and Soyeon Caren Han. <br> [FedNLP: An interpretable NLP System to Decode Federal Reserve Communications](https://arxiv.org/pdf/2106.06247.pdf) <br> Accepted by the ACM SIGIR Conference on Research and Development in Information Retrieval (SIGIR 2021) </div>


#### :desktop_computer: [Live Demo] https://fednlp.net

#### :movie_camera: [Demo Video] Please click on the image below:

[<img src="https://github.com/usydnlp/FedNLP/blob/main/resources/FedNLP_img.gif" width="70%">](https://youtu.be/Pn3OrWdzwws)



## Abstract
The Federal Reserve System (the Fed) plays a significant role in affecting monetary policy and financial conditions worldwide. Although it is important to analyse the Fed's communications to extract useful information, it is generally long-form and complex due to the ambiguous and esoteric nature of content. In this paper, we present FedNLP, an interpretable multi-component Natural Language Processing (NLP) system to decode Federal Reserve communications. This system is designed for end-users to explore how NLP techniques can assist their holistic understanding of the Fed's communications with NO coding. Behind the scenes, FedNLP uses multiple NLP models from traditional machine learning algorithms to deep neural network architectures in each downstream task. The demonstration shows multiple results at once including sentiment analysis, summary of the document, prediction of the Federal Funds Rate movement and visualization for interpreting the prediction model's result. Our application system and demonstration are available at https://fednlp.net.


## Dataset
We collect the various forms of Federal Reserve communications within the period of January 2015 to July 2020. 
In this `data` repository, it provides final text file in pickle format.
- `fomc_doc.pkl` : FOMC post-meeting statements, Minutes, and press conferences. 
- `speaker_doc.pkl` :FOMC member’ speeches from over 30 different websites.


## Demo 
[Live Demo] https://fednlp.net

We build a demo for non-technical users to get experiences how NLP components analyse the new input document. The NLP models are deployed using Flask, Docker and AWS.

The Demo page consists of multiple components: (1) Word, Sentence Count (2) WordCloud (3) General Sentiment (TextBlob) (4) Financial Sentiment (LM) (5) Summarization (General, TextRank) (6) Summarization (Financial, fine tuning T5) (7) Prediction (Financial, fine tuning FinBERT) (8) Explanation (General, XGBoost).

In the task of prediction and explanation, we build the models to predict the decision of changes in target Federal Funds Rate (e.g. Lower: 1% -> 0.75%, Maintain 1% -> 1%, Raise: 1% -> 1.25%).



## Citation
If you use the dataset or the code, please cite this paper:

```
@inproceedings{lee2021fednlp,
  title     = {FedNLP: An Interpretable {NLP} System to Decode Federal Reserve Communications},
  author    = {Jean Lee and Hoyoul Luis Youn and Nicholas Stevens and Josiah Poon and Soyeon Caren Han},
  booktitle = {{SIGIR} '21: The 44th International {ACM} {SIGIR} Conference on Research and Development in Information Retrieval, Virtual Event, Canada, July 11-15, 2021},
  pages     = {2560--2564},
  publisher = {{ACM}},
  year      = {2021}
}
```
