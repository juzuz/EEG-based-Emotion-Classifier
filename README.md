# EEG-based-Emotion-Classifier

## Introduction

The purpose of a machine-learning emotion classifier
is to enable a machine to recognize, understand and
represent a user’s emotional state. This is a hot topic in
emotional AI research, which contains multiple fields of
study such as neural science, psychology, data science. The
EEG-based emotion classifier is a representative problem
for classification. Unlike the traditional data - image and
sound - EEG data is unstable due to noise and its discrete
characteristic, thus a challenging research topic. This experiment
extends on the proposal of a new EEG feature named
differential entropy (DE), which claims to be a more stable
and accurate EEG feature than traditional features such as
the energy spectrum.[1] We will be attempting to create a
three-class classifier that takes in the DE data and outputs
either a ”positive,” ”neutral,” or ”negative” response.
This paper will outline the steps taken and discoveries
while attempting to improve the accuracy of the model. A
detailed comparison of which combinations of preprocessing
tools and classifiers are used to achieve our goal will be
presented.

## Data

The data used in this research origins from the SJTU
emotion EEG dataset, SEED. We will be using a subset of
the dataset that contains 15 samples of the participant’s
data. The EEG data is recorded while the participants
watch 5 separate films that evoke each of the three
emotions: positive, neutral, negative. The DE feature
has 62 outputs which were read every second. The
feature has a dimension of (62,5), therefore contains 310
features to feed the model. Throughout this research,
testing will be conducted with 15-fold cross-validation.

The data can be received from this link: https://bcmi.sjtu.edu.cn/home/seed/


## Feature Extraction 

Feature selection identifies subsets of data relevant to the
parameters used and is usually called Maximum Relevance.
Features can be selected in many different ways. One
scheme is to choose features that correlate strongest to the
classification variable. This is called the maximum-relevance
selection. The mRMR is a maximum-relevance selection
heuristic that also selects features that are far away from
each other while still having a ”high” correlation to the
classification variable.



## Dimension Reduction

LDA is a dimension reduction algorithm,that maximizes the ratio of the between-class
variance to the within-class variance. This guarantees maximum class separability.

![ICA](/assets/ICA.png)
![PCA](/assets/PCA.png)
![LDA](/assets/LDA.png)


## Decision Surface

After running the model, the accuracy of the model is a high 99.48% and a maximum difference in the cross validation of 2.48%.

![results](/assets/results.png)
![surface](/assets/decision.png)
# Detailed Information and though processes

Detailed information of the data preprocessing and classifier choices are written in the detail.pdf file.
This is the final report for this project.






