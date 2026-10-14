# CS6765 Natural Language Processing

Coursework and class materials for CS6765 at the University of New Brunswick.

## Contents

- `a1.ipynb` — Assignment 1 notebook.
- `a2/` — Assignment 2: three-class sentiment analysis of climate-related text from corporate disclosures.
- `pythontutorialexamples/` — Python and NLP tutorial notebooks and supporting text files.

## Assignment 2

The completed [`a2/a2.ipynb`](a2/a2.ipynb) compares several sentiment classifiers:

- a most-frequent-class baseline;
- logistic regression with textbook sentiment features;
- textbook features extended with climate-domain risk and opportunity counts;
- logistic regression with unigram counts;
- logistic regression with TF–IDF-weighted unigrams; and
- logistic regression combining word unigram and character 3–4-gram TF–IDF features.

The notebook contains the implementation, saved outputs, and a short results report. The combined word and character model achieved the best held-out test result, with **0.692 macro-F1** and **0.741 accuracy**.

### Data

The `a2/data/` directory contains the supplied training, development, and test CSV files. The data originates from the [ClimateBERT climate sentiment dataset](https://huggingface.co/datasets/climatebert/climate_sentiment) and is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).

### Running the notebook

From the repository root, activate the existing virtual environment and start Jupyter:

```bash
source .venv/bin/activate
cd a2
jupyter notebook a2.ipynb
```

The notebook requires Python 3, NumPy, scikit-learn, NLTK, and the NLTK `opinion_lexicon` corpus. Its file-loading paths are relative to `a2/`, so use that directory as the notebook's working directory when running it through another editor or command-line tool.
