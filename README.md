# English-to-French Transformer

This project is a small English-to-French translation model built with TensorFlow and Keras.

I made this project to understand how an encoder-decoder Transformer works by implementing its main parts instead of using a ready-made Transformer model.

## What I implemented

- Text tokenization and padding
- Token and positional embeddings
- Encoder self-attention
- Decoder masked self-attention
- Encoder-decoder cross-attention
- Feed-forward networks
- Padding and causal masks
- Masked loss and accuracy
- Greedy decoding for translation

## How it works

The encoder receives an English sentence and creates a contextual representation for each word.

The decoder receives the previous French words and the encoder output. A causal mask prevents it from seeing future French words while making a prediction.

The decoder predicts one word at a time until it generates the `end` token.

## Dataset

The dataset contains 1,000 short English-French sentence pairs.

It is divided into:

- 80% training data
- 10% validation data
- 10% test data

The CSV file should contain two columns:

```text
English,French
```

## Project files

```text
encoder_decoder_transformer_github.ipynb
english_french_1000_short_pairs.csv
README.md
```

Keep the notebook and CSV file in the same folder.

## Requirements

Install the required libraries using:

```bash
pip install tensorflow pandas numpy scikit-learn
```

## Running the project

1. Clone or download this repository.
2. Open the notebook in Jupyter Notebook or Google Colab.
3. Make sure the CSV file is in the same folder as the notebook.
4. Run all cells in order.
5. Use the translation function at the end to test new English sentences.

## Note

This is a learning project trained on a small dataset, so it is not meant to compete with real translation systems.

A high accuracy does not necessarily mean the model will translate every new sentence correctly. The dataset is small and contains simple sentence patterns, so the model may memorize some of them.
