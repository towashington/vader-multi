# VADER Sentiment Analysis Multilanguage
VADER (Valence Aware Dictionary and sEntiment Reasoner) is a lexicon and rule-based sentiment analysis tool that is specifically attuned to sentiments expressed in social media.

> This version integrates the Google Translate API through the `translatte` Python library. It requires an active Internet connection in order to work. Text language is automatically detected so it behaves exactly like the original version.

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
>>> from vaderSentiment.vaderSentiment import SentimentIntensityAnalyzer

>>> analyzer = SentimentIntensityAnalyzer()

>>> analyzer.polarity_scores("VADER is VERY SMART, handsome, and FUNNY!!!")
{'neg': 0.0, 'neu': 0.233, 'pos': 0.767, 'compound': 0.9342}

>>> analyzer.polarity_scores("VADER es MUY INTELIGENTE, guapo y DIVERTIDO!!!")
{'neg': 0.0, 'neu': 0.276, 'pos': 0.724, 'compound': 0.9342}
```
