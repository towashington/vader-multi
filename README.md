# VADER Sentiment Analysis Multilanguage
VADER (Valence Aware Dictionary and sEntiment Reasoner) is a lexicon and rule-based sentiment analysis tool that is specifically attuned to sentiments expressed in social media. It is fully open-sourced under the [MIT License] (we sincerely appreciate all attributions and readily accept most contributions, but please don't hold us liable).

> This version integrates the Google Translate API through the `translatte` Python library. It requires an active Internet connection in order to work.

## Installation
```bash
pip install vader-multi
```

### `class vaderSentiment.SentimentIntensityAnalyzer`
#### `polarity_scores(text)`
Returns a dictionary with the following keys: `{'neg': float, 'neu': float, 'pos': float, 'compound': float}`

```python
from vaderSentiment.vaderSentiment import SentimentIntensityAnalyzer

analyzer = SentimentIntensityAnalyzer()
analyzer.polarity_scores("VADER is smart, handsome, and funny.")
```

## Examples
```python
from vaderSentiment.vaderSentiment import SentimentIntensityAnalyzer

analyzer = SentimentIntensityAnalyzer()
analyzer.polarity_scores("VADER is smart, handsome, and funny.")
```