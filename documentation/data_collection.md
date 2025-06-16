# Data Collection

## Overview
Our project focuses on detecting machine-generated text in isiZulu and isiXhosa. To build robust models, we gathered both human-written and machine-generated text for these languages. We prioritized data diversity and representativeness to ensure our model could generalize well.

## Human-Written Data Sources

- **isiZulu:**
  - [ZA isiZulu-Siswati News](https://github.com/dsfsi/za-isizulu-siswati-news-2022): Over 10,000 news articles and headlines scraped from South African media (e.g., Isolezwe), annotated and cleaned for NLP use.
  - **NCHLT isiZulu Named Entity Corpus**: Manually annotated texts from SADiLaR, containing named entities and other linguistic features.
- **isiXhosa:**
  - **MasakhaPOS**: Part-of-speech tagged sentences, providing high-quality annotated isiXhosa data.
  - **MasakhaNER 2.0**: Named entity recognition corpus with diverse text samples.
  - **Leipzig Web Corpus**: Web-crawled isiXhosa texts for additional variety.

## Machine-Generated Data

To create machine-generated samples:
- We used template-based and pattern-based generation, designing sentences with realistic structures, vocabulary, and varying lengths.
- We also generated synthetic text using large language models (e.g., GPT-4, Gemini) prompted to produce isiZulu and isiXhosa sentences.
- Controlled for sentence length and content diversity to avoid simple detection based on superficial cues.

## Data Format

- Each data entry includes:
  - The sentence
  - The language label (`isiZulu` or `isiXhosa`)
  - A label indicating human (`0`) or machine-generated (`1`)
- Data is stored in CSV files, with separate files for isiZulu and isiXhosa.

## Preprocessing

- Cleaned data to remove special characters, English words, and non-ASCII symbols.
- Mixed human and machine-generated samples to prevent order-based bias.
- Augmented data using back-translation and synonym replacement to increase diversity and robustness.

## Ethical Considerations

- All data sources are open-access or used with permission.
- No sensitive personal data was included.
- Augmented (synthetic) data is clearly labeled and not treated as genuine user-generated content.
