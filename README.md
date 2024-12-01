
# Sentiment and Emotion Analysis

This repository contains a Python script that performs text preprocessing, sentiment analysis, and emotion classification using Natural Language Processing (NLP) techniques and pre-trained models.

## Features

1. **Text Preprocessing**
   - Converts text to lowercase.
   - Removes URLs, mentions, and non-alphanumeric characters.
   - Tokenizes text into words.
   - Lemmatizes words to their root form.
   - Removes stopwords from the text.

2. **Sentiment Analysis**
   - Uses the pre-trained `cardiffnlp/twitter-roberta-base-sentiment` model for classifying text as Negative, Neutral, or Positive.
   - Calculates probabilities using softmax.

3. **Emotion Analysis**
   - Utilizes the `SamLowe/roberta-base-go_emotions` model to classify emotions in text and provide corresponding confidence scores.

## Prerequisites

The script requires the following Python libraries:
- `nltk`
- `re`
- `transformers`
- `pandas`
- `numpy`
- `scipy`

## Usage

### Step 1: Download Necessary NLTK Resources
The script downloads `stopwords`, `wordnet`, and `punkt_tab` required for text preprocessing.

### Step 2: Define Functions
- **`preprocess_text(text)`**: Cleans and preprocesses input text for NLP tasks.
- **`identify_emotion(text)`**: Classifies emotions in the text.
- **`identify_sentiments(text)`**: Analyzes sentiments in the text (Negative, Neutral, Positive).
- **`get_emotion_analysis(text)`**: Combines both sentiment and emotion analysis.

### Step 3: Execute Analysis
Run the script with your input text to receive the sentiment and emotion analysis.

```python
example = """Today was a rollercoaster of emotions. The morning started beautifully with a stunning sunrise and a warm cup of coffee, which filled me with gratitude. However, the traffic on the way to work was horrendous, leaving me frustrated and irritable. At work, I received praise for completing a challenging project, which boosted my confidence. But later, a technical glitch caused a major delay, adding stress to my already busy day. By evening, I was relieved to unwind with a good book, though a lingering headache made it hard to focus. Overall, it was a day of highs and lows, leaving me reflective about its unpredictability."""

response = get_emotion_analysis(example)
```

### Output Example

The script will print the sentiments and emotions along with their confidence scores.

## Notes

- Ensure all prerequisites are installed before running the script.
- Replace the `example` text with your custom input for analysis.

## Author

This script demonstrates a practical application of NLP using pre-trained models for sentiment and emotion analysis.
