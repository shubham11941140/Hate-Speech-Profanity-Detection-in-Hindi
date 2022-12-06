# Hate-Speech-Profanity-Detection-in-Hindi

## Implemented a Multi-Class Hindi Hate Speech Classification Task using Lexicon and LSTM Approach

#### We have implemented a Multi-Class Hindi Hate Speech Classification Task using 2 approaches:

### 1. Lexicon-based approach

### Full-fledged Research Paper Implementation
**A Lexicon-based approach for Hate Speech Detection** - https://gvpress.com/journals/IJMUE/vol10_no4/21.pdf

```
Rule based approach to apply sentiment/subjectivity analysis - Identification of polarity of sentiment expressions
Extract lexical features to build a lexicon -> Fed into a classifier
Testing on real-world web discourse
```


**Dataset.csv** - Dataset for the task (https://github.com/mohit19014/Hindi-Hostility-Detection-CONSTRAINT-2021)

**Hate_Speech_Detection_Classification_Lexicon.ipynb** - Jupyter Notebook for the task

**Results_Output.csv** - Results of the task

Reference Files:
```
a) SUBJCLUE.txt - Subjectivity Lexicon Hindi (Taken from Hindi Sentiment Analysis WordNet) - https://www.cfilt.iitb.ac.in/wordnet/webhwn/downloaderInfo.php?lang=hi
b) themenouns.txt - Theme Nouns
c) Synset.txt - Synonyms
```

### 2. LSTM based approach (Using Deep Learning)

Dataset folder contains the dataset for the task (train.csv, test.csv, valid.csv)

**Dataset_Preprocessing_and_Cleaning.ipynb** - Jupyter Notebook for preprocessing and cleaning the dataset

Generated files from the above notebook:
```
a) cleaned_train.csv
b) cleaned_test.csv
c) cleaned_valid.csv
d) cleaned_string_train.csv
e) cleaned_string_test.csv
f) cleaned_string_valid.csv
```

This is used for the LSTM based approach

It is combined to form a single file (compiled_LSTM_Dataset.csv) and then used for the LSTM based approach

**Hate_Speech_Detection_Classification_LSTM.ipynb** - Jupyter Notebook for the task

##  Results

### Lexicon Approach

### Input

![image](https://user-images.githubusercontent.com/63910248/205922391-3f1e0f89-02cb-4053-94b5-16f5818c3872.png)

### Subjectivity Analysis

1. **Usage of https://amitavadas.com/sentiwordnet.php (SentiWordNet) which gives us the sentiments associated with a particular word in Hindi Language**

2. **Direct correlation between sentiments of sentences and objectivity i.e. it tells us that this sentence is a clean one based on presence of profanity words or not (Similar to 0-1 classification)**

3. **Key role in Data Reduction into sentences which are actually hateful and need to be classified**

4. **Negative scoring indicates hate speech presence and positive indicates absence**

### Building Hate Lexicon

1. **Based on SentiWordNet scores associated with particular words and scores, detect negative polarity and hate content in tweets.**
2. **Scores < -0.25 -> Strongly Negative**
3. **-0.25 < Scores < 0 -> Weakly Negative**
4. **With this built, we add SYNSET (All possible synonyms) of these verbs and make a list of hateful verbs.**
5. **Adding on this, we add all verbs in the dataset vocabulary that belong to the SYNSET and add them to the hateful verb list.**

### Theme-Based Noun Identification

1. **Find nouns associated with relevant topic of discussion (specific to tweet)**
2. **Politically significant words are taken into account**
3. **Make a list of all distinct nouns from the corpus and take the most frequent NPs (Noun Phrases)**
4. **Few other commonly occurring noun words from Hindi Dictionary are added to this list**
5. **Can directly link nouns to context in which tweets are specified.**
6. **Provides insights into the Theme-Based Hate Speech Classification Task**

### Scores - Without Subjectivity Analysis

![image](https://user-images.githubusercontent.com/63910248/205922678-682fd4dd-849a-4c48-8a0b-332d5a3fac7f.png)


### Scores - With Subjectivity Analysis

![image](https://user-images.githubusercontent.com/63910248/205922742-3e86b5c8-da29-44f2-b9eb-d3b4f39fc0f1.png)


### Sentence Number, Sentence, Output Class, Hate Score (Scale 1-5)

![image](https://user-images.githubusercontent.com/63910248/205915490-183a2d14-238a-46b2-bc5a-a2c4608bb5c5.png)

![image](https://user-images.githubusercontent.com/63910248/205923309-b0a5fbe6-026b-4c51-beff-bc605586ed78.png)

### Impact

1. **Impact of subjectivity. Using a baseline and reduction of dataset helps us to derive better results**
2. **Recall is much higher than Precision -> Tagging the hate speech tweets is good leaving very few false negatives (Misses)**

#### Impact is significant - 
1. **We are able to quantify hate speech for a variety of reasons to a reasonable precision**
2. **Subjective classification of data eases the classification to a great deal**
3. **Speed -> Algorithm is of linear time complexity (O(N)) which gives us efficient speedup as the dataset can scale.**
4. **The paper implements the results for English language which is extended to Hindi. It shows that we can extend it to other regional languages.**


### LSTM Approach

#### Input

![image](https://user-images.githubusercontent.com/63910248/205917112-29b0de76-5969-4361-8a01-457d622926d9.png)

#### Labels

![image](https://user-images.githubusercontent.com/63910248/205917463-0b59da59-522d-4f11-a121-1f495e319615.png)

#### RNN Architecture

![image](https://user-images.githubusercontent.com/63910248/205917617-c1f65d47-3c36-4c6a-b7d2-f852bef13aa8.png)

#### Hyper-Parameters

1. Loss - Cross Entropy Loss
2. Learning Rate - 0.001
3. Optimizer - Adam Optimizer
4. Dropout - 0.3
5. Epoch - 50
6. Batch Size - 50

#### Epoch Loss Values

![image](https://user-images.githubusercontent.com/63910248/205917840-1271c9c8-1150-4778-91da-f1cbbee711ac.png)

#### Test Loss/Accuracy

![image](https://user-images.githubusercontent.com/63910248/205917982-dd928c1f-8359-4553-a43f-53e40693e4a4.png)

#### Predictions

![image](https://user-images.githubusercontent.com/63910248/205918105-3f058a59-27fd-46f5-a187-e624a6101616.png)

## Slides

Hate_Speech_Detection_Classification-Hindi(Lexicon Approach + LSTM).pptx

## Novelty

### Lexicon-Based Approach:
1. **Paper implementation - A Lexicon-based approach for Hate Speech Detection - https://gvpress.com/journals/IJMUE/vol10_no4/21.pdf**
2. **Paper implementation is in English. Extended to Hindi to build lexicons, obtain accuracy (Precision, Recall, F1 Score) and classify the degree of sentences on a 1-5 scale**
3. **Focus on recall that we are able to reduce false negatives before actually dealing with a high accuracy**

### LSTM-Based Approach:
1. **Multi-Class Classification - Multi-Class Classification works on this dataset or Hindi Language Dataset, have not been performed before.**
2. **Sentiment Analysis - Binary classification tasks on each class of this dataset (HINDI LANGUAGE specifically) have been done previously but we perform sentiment analysis based on the last cell output.**

## Reasoning and Justification

This accuracy obtained is due to the following two phenomena -
1. **Class Imbalance - As seen in the dataset distribution, the dataset is affected by class imbalance with large number of examples for non-hostile sentences.**
2. **Less Dataset Size - The online available dataset for “HINDI” Hate Speech detection were very few. And those present were not large enough in size for a considerable amount of deep-learning training for NLP.**

### We conclude that we have increased the classification accuracy over the basic classifier baseline model (3 classes) while having to classify more classes (5 classes)

## References

1. Hindi Sentiment Analysis WordNet - https://www.cfilt.iitb.ac.in/wordnet/webhwn/downloaderInfo.php?lang=hi
2. Dataset for the task - https://github.com/mohit19014/Hindi-Hostility-Detection-CONSTRAINT-2021
3. Research Paper - https://gvpress.com/journals/IJMUE/vol10_no4/21.pdf

## Web Links

1. https://www.analyticsvidhya.com/blog/2021/10/hands-on-hindi-text-analysis-using-natural-language-processing-nlp/
2. https://pypi.org/project/indic-nlp-library/
3. https://www.analyticsvidhya.com/blog/2020/01/3-important-nlp-libraries-indian-languages-python/
4. https://arxiv.org/pdf/2101.05494v1.pdf
5. https://www.kaggle.com/abhinavwalia95/entity-annotated-corpus

## GitHub

1. https://github.com/kamalojasv181/Hostility-Detection-in-Hindi-Posts
2. https://github.com/victorknox/Hate-Speech-Detection-in-Hindi
3. https://github.com/NakulLakhotia/Hate-Speech-Detection-in-Social-Media-using-Python
4. https://github.com/ecanbazer/hatred-speech-classifier
5. https://github.com/manikbhandari/hindi-word-embeddings
6. https://github.com/datascisteven/Automated-Hate-Tweet-Detection/tree/main/py
7. https://github.com/hate-alert/HateCheckHIn
8. https://github.com/punyajoy/HateSpeech-Hindi-English-Code-Mixed-Social-Media-Text
9. https://github.com/victor7246/Hinglish_Hate_Detection
10. https://github.com/pmathur5k10/Hinglish-Offensive-Text-Classification
11. https://github.com/udacity/deep-learning-v2-pytorch/tree/master/sentiment-rnn
12. https://github.com/kopalgarg/hate_speech_classification
