# 🧠 Recurrent Neural Networks (RNN)

Welcome to the **Recurrent Neural Networks** module. While ANNs and CNNs assume that all inputs and outputs are independent of each other, RNNs are built for sequential data. By maintaining a "memory" of previous inputs via hidden states, RNNs excel at Natural Language Processing (NLP), time-series analysis, and any task where the *order* of the data matters.

## 📓 Notebooks in this Folder

### 1. IMDB Sentiment Analysis & Text Preprocessing
This notebook tackles a classic Natural Language Processing (NLP) classification problem: determining whether a movie review is positive or negative.

* **Dataset:** The IMDB dataset, consisting of highly polar movie reviews.
* **Objective:** Train an RNN to read sequences of text, retain context over the length of the review, and predict the underlying sentiment.
* **Core Focus — Text Preprocessing:** Text data cannot be fed directly into a neural network. This notebook heavily emphasizes the data preparation pipeline:
  * **Tokenization:** Breaking down raw text sentences into individual words or subwords.
  * **Vocabulary Building:** Mapping every unique word in the dataset to a specific integer index.
  * **Word Embeddings:** Converting integer tokens into dense vectors that capture semantic meaning.
  * **Padding & Truncating:** Ensuring all review sequences are of the same uniform length (e.g., padding short reviews with zeros) so they can be processed in batches by the network.

## 🏗️ Core Architecture & Math Concepts

To understand how an RNN processes a sequence of words (where $x_t$ is the word at time step $t$), we look at the hidden state $h_t$, which acts as the network's memory:

* **Hidden State Update:** At each time step $t$, the RNN calculates a new hidden state by combining the input at the current step $x_t$ with the hidden state from the previous step $h_{t-1}$:

  $$h_t = \tanh(W_{hh} h_{t-1} + W_{xh} x_t + b_h)$$

  *Where $W_{hh}$ and $W_{xh}$ are the learnable weight matrices, and $b_h$ is the bias.*

* **Output Generation:** The final prediction (e.g., positive or negative sentiment) is computed using the final hidden state:

  $$y_t = W_{hy} h_t + b_y$$

* **Challenges Addressed:** Basic RNNs struggle with long sentences due to the **vanishing gradient problem**. As the sequence gets longer, the network forgets earlier words. *(Note: This often leads to upgrading to advanced architectures like LSTMs or GRUs).*

## 🛠️ Tech
