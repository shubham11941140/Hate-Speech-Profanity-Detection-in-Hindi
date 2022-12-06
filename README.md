# Hate-Speech-Profanity-Detection-in-Hindi

## Implemented a Multi-Class Hindi Hate Speech Classification Task using Lexicon and LSTM Approach

#### We have implemented a Multi-Class Hindi Hate Speech Classification Task using 2 approaches:

### 1. Lexicon-based approach

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

## Slides

Hate_Speech_Detection_Classification-Hindi(Lexicon Approach + LSTM).pptx
