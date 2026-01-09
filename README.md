# English to Turkish Neural Machine Translation (NMT)
This project explores the evolution of Sequence-to-Sequence (Seq2Seq) architectures for Machine Translation. Using a bilingual English-Turkish dataset, we implement and benchmark six different neural architectures, ranging from basic RNNs to the modern Transformer model.

File Name: nlp_4.ipynb

# Project Architecture
The project follows the progression of NMT technology:

Data Preprocessing: Cleaning, punctuation isolation, and vocabulary building for both languages.

Encoder-Decoder Framework: Moving from fixed-length context vectors to dynamic attention.

Self-Attention & Transformers: Implementing parallel processing without recurrence.

# Evolution of Architectures & Methodologies
# 1. Vanilla GRU & LSTM (Baseline)
These models use a standard approach where the encoder compresses the source sentence into a single context vector. While effective for short sentences, they suffer from the "information bottleneck" on longer sequences.

# 2. Bidirectional Encoder
By processing the English sentences in both forward and backward directions, this model captures global context more effectively than the baseline versions.

# 3. Bahdanau & Luong Attention
These models introduced the ability to "attend" to specific words in the source sentence during each decoding step. Bahdanau (Additive) and Luong (Multiplicative) attention significantly improved translation quality for complex Turkish grammar.

# 4. The Transformer
The final and most advanced model in the project. It discards recurrence entirely in favor of Self-Attention and Positional Encoding, allowing it to learn long-range dependencies between words much better than RNNs.

# Performance Summary
The performance was evaluated using BLEU Score (n-gram overlap) and BERTScore (semantic similarity).

The Transformer (Top Performer): Achieved the highest scores in both metrics. Its ability to process the entire sequence at once makes it the superior choice for English-to-Turkish translation.

Best BLEU & BERTScore results.

Bahdanau Attention: Showed the most significant jump in quality compared to non-attention models, handling Turkish word order (SOV) much more naturally.

Strong performance with high semantic accuracy.

Bidirectional GRU: Outperformed the Vanilla versions by providing the decoder with a richer representation of the input sentence.

Solid improvement over the baseline.

# Installation & Requirements
Ensure you have a GPU-enabled environment and install the following:

pip install torch pandas nltk bert-score

# Quick Start
Run the Dataset section to download the tur-eng.zip file.

Execute the Preprocessing cells to prepare the vocabularies.

Choose a model section (e.g., Transformer or Bahdanau) and run the training loop.

Use the provided translate functions to test your own English sentences. 

Vanilla Models (Baseline): Provided basic translations but struggled with word order and long-range context.

Baseline scores, served as a proof-of-concept.
