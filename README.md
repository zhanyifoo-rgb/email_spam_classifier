# Email Spam Classifier

An NLP-based email spam classifier using TF-IDF and machine learning to distinguish spam from legitimate emails.
Contains 2 scripts, 'spam_email_preprocessor.ipynb' to preprocess 'email_origin.csv' raw data and extract the actual email text, and 'spam_email_classifier.ipynb' to train the actual model.

## Features
- Extracts and cleans raw email content.
- Converts email text into TF-IDF features.
- Compares Logistic Regression, Multinomial Naive Bayes, Complement Naive Bayes, and Linear SVM.
- Uses 5-fold stratified cross-validation for model evaluation.
- Performs error analysis based on email length.

## Best Model

**Linear SVM**

- TF-IDF features: 30,000
- N-grams: Unigrams and bigrams
- Minimum document frequency: 1
- Mean cross-validation F1-score: **99.50%**

## Project Structure

```text
email_spam_classifier/
├── Data/
│   └── email_preprocessed.csv
├── spam_email_preprocessor.ipynb
├── spam_email_classifier.ipynb
├── requirements.txt
└── README.md
```

## Getting Started

```bash
git clone https://github.com/zhanyifoo-rgb/email_spam_classifier.git
cd email_spam_classifier

python -m venv venv
```

Activate the environment:

```bash
# Windows
venv\Scripts\activate

# Linux / WSL
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the notebooks in order:
1. `spam_email_preprocessor.ipynb`
2. `spam_email_classifier.ipynb`

## Key Finding

The classifier achieved strong overall performance, but short legitimate emails were more challenging to identify correctly, highlighting an area for further improvement.

## Future Improvements
- Improve classification of short legitimate emails.
- Test on unseen, real-world email data.
- Explore additional feature engineering and model tuning.
