# Reddit Data Analysis: Topic Modeling, NER, and Predictive Modeling

## Project Overview

This project involves the analysis of Reddit posts using advanced Natural Language Processing (NLP) techniques to extract meaningful insights and build predictive models. The analysis is divided into three main tasks:

---

## Task 1: Topic Modeling

### Objective
Discover underlying themes within Reddit posts using Latent Dirichlet Allocation (LDA).

### Steps
1. **Data Preprocessing** (Optional):
   - Remove stopwords, special characters, and unnecessary whitespace.
   - Perform lemmatization to normalize words.
   
2. **Apply LDA for Topic Modeling**:
   - Experiment with topic numbers ranging from 1 to 10.
   - Evaluate models using the coherence score.
   - Select the optimal number of topics based on coherence scores.

3. **Topic Labeling**:
   - Manually interpret and assign meaningful labels to the discovered topics.
   
4. **Visualization**:
   - Create word clouds to visualize themes for each topic.

### Deliverables
- A table or brief discussion justifying the chosen number of topics and the themes they represent.
- Word clouds summarizing the key topics.

---

## Task 2: Named Entity Recognition (NER)

### Objective
Identify how key entities are portrayed (positive or negative) in the dataset.

### Entities to Analyze
- **Israel**
- **Hamas**
- **Antony Blinken**
- **Benjamin Netanyahu**
- **IDF (Israeli Defense Forces)**

### Steps
1. **NER Extraction**:
   - Use an NER tool (e.g., spaCy) to extract sentences mentioning the entities.
   - Account for alternate mentions (e.g., "Netanyahu" for "Benjamin Netanyahu").

2. **Sentiment Analysis**:
   - Use VADER to calculate the average sentiment score of sentences mentioning each entity.
   - Compare sentiment scores across entities.

3. **POS Tagging**:
   - Extract verbs, nouns, and adjectives from sentences containing the entities using NLTK.
   - Visualize these words using word clouds.

### Deliverables
- Sentiment score analysis and comparison across entities.
- Word clouds visualizing surrounding words for each entity.
- Discussion of findings.

---

## Task 3: Predicting Score for Each Reddit Post

### Objective
Build models to predict the “score” column (upvotes minus downvotes) for Reddit posts based on text and title.

### Steps
1. **Feature Selection**:
   - Utilize at least one of the following features:
     - Topics from Task 1
     - NER from Task 2
     - Lexicon-based scores (Valence, Arousal, Dominance from NRC-VAD lexicon)
   - Incorporate word or sentence embeddings (Word2Vec, GloVe, Sentence-BERT, or USE).
   - Optionally include POS tags.

2. **Model Training**:
   - Train models using SVM and XGBoost.
   - Evaluate model performance using MSE (Mean Squared Error).

### Deliverables
- Model performance comparison with evaluation metrics (e.g., MSE).
- Discussion on the effectiveness of different features in improving predictions.

---

## Installation and Usage

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
