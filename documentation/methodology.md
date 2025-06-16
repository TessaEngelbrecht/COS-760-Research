# Methodology

## Model Architecture

We used the Afro-XLM-R-large model, a multilingual transformer pre-trained on African languages, as our base. This model is well-suited for isiZulu and isiXhosa due to its architecture and prior training on similar language data.

- **Encoder:** Afro-XLM-R transformer layers process input text into contextual embeddings.
- **Classifier:** A feed-forward neural network head predicts whether text is human- or machine-generated.
- **Loss Function:** Binary cross-entropy loss for binary classification.

## Training Process

1. **Data Preparation:**
   - Combined human and machine-generated samples for each language.
   - Applied data augmentation (see below).
   - Split data into training (80%) and test (20%) sets, ensuring class and language balance.

2. **Data Augmentation:**
   - **Back-Translation:** Used Helsinki-NLP Opus-MT models to translate isiXhosa/isiZulu to English and back, increasing data diversity while preserving meaning.
   - **Synonym Replacement:** Replaced words with context-appropriate synonyms, focusing on maintaining grammatical correctness.

3. **Fine-Tuning:**
   - Fine-tuned Afro-XLM-R on the prepared dataset for binary classification.
   - Used early stopping and validation sets to prevent overfitting.
   - Hyperparameters (batch size, learning rate, epochs) were tuned based on validation performance.

4. **Evaluation:**
   - Evaluated on held-out test data using accuracy, F1-score, precision, and recall.
   - Compared models trained with and without data augmentation.

## Responsible NLP Practices

- Documented all data sources and augmentation processes.
- Clearly labeled synthetic and augmented data.
- Used open-source models and tools under permissive licenses (MIT/Apache 2.0).
- No personal or sensitive data was included.
