# Hate-Speech-Profanity-Detection-in-Hindi

## Implemented a Multi-Class Hindi Hate Speech Classification Task using Lexicon and LSTM Approach

#### We have implemented a Multi-Class Hindi Hate Speech Classification Task using 2 approaches:

### 1. Lexicon-based approach

### Full-fledged Paper Implementation
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

#### Scores - Without Subjectivity Analysis

![image](https://user-images.githubusercontent.com/63910248/205916298-1118d060-8bc3-4eec-a9b9-e55ba020deb5.png)


#### Scores - With Subjectivity Analysis

![image](https://user-images.githubusercontent.com/63910248/205916356-b6ae2595-ebaa-46b7-9da7-5b6cbb5774c0.png)


#### Sentence Number, Sentence, Output Class, Hate Score (Scale 1-5)

![image](https://user-images.githubusercontent.com/63910248/205915490-183a2d14-238a-46b2-bc5a-a2c4608bb5c5.png)


### LSTM Approach

#### Input

![image](https://user-images.githubusercontent.com/63910248/205917112-29b0de76-5969-4361-8a01-457d622926d9.png)

#### Labels

![image](https://user-images.githubusercontent.com/63910248/205917463-0b59da59-522d-4f11-a121-1f495e319615.png)

#### RNN Architecture

![image](https://user-images.githubusercontent.com/63910248/205917617-c1f65d47-3c36-4c6a-b7d2-f852bef13aa8.png)

#### Epoch Loss Values

![image](https://user-images.githubusercontent.com/63910248/205917840-1271c9c8-1150-4778-91da-f1cbbee711ac.png)

#### Test Loss/Accuracy

![image](https://user-images.githubusercontent.com/63910248/205917982-dd928c1f-8359-4553-a43f-53e40693e4a4.png)

#### Predictions

![image](https://user-images.githubusercontent.com/63910248/205918105-3f058a59-27fd-46f5-a187-e624a6101616.png)

## Slides

Hate_Speech_Detection_Classification-Hindi(Lexicon Approach + LSTM).pptx

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
