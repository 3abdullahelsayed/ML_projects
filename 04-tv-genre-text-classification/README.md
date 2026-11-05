# TV Series Genre Classification from Plot Descriptions

A classical NLP project that predicts a title's genre from its plot description.

## Project details

- **Task:** Three-class text classification
- **Dataset:** Kaggle `payamamanat/imbd-dataset`; 1,658 selected records across Drama, Animation/Action/Adventure, and Documentary
- **Methods:** Tokenization, WordNet lemmatization, TF-IDF (unigrams and bigrams), Multinomial Naive Bayes
- **Reported result:** 81.9% test accuracy (provisional)

## Method

- Selected three genre groups.
- Cleaned and lemmatized plot descriptions.
- Converted text to TF-IDF features.
- Trained a Multinomial Naive Bayes classifier.

## Important evaluation note

The current notebook fits TF-IDF on the full text dataset before splitting into training and test sets. This leaks vocabulary information from the test set. **The reported 81.9% score should be treated as provisional.** Split the raw text first, fit TF-IDF on training text only, and transform validation/test text with the fitted vectorizer. A scikit-learn Pipeline is recommended.

## Next improvements

Remove placeholder descriptions such as “Add a Plot”, compare Logistic Regression and linear SVM, and use cross-validation within the training set.
