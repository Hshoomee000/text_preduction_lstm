predictive text generator

Under the supervision of: Dr.Dalia Sameh  
Abstract:
In this project, we present a predictive text generator that leverages artificial intelligence to anticipate the next word in a sequence. The primary goal of this work is to assist users in writing text more efficiently by suggesting possible word continuations, among other useful features. To achieve this, key concepts from Natural Language Processing (NLP) were applied during the preprocessing stage, including tokenization and other text normalization techniques. Our model is capable of receiving an input sentence from the user and predicting the subsequent words, generating up to ten possible next words. The results demonstrate the model’s ability to significantly enhance typing speed and user experience by providing accurate and contextually relevant predictions.

Data Sets:
In this project, we utilized a dataset named Text Generator dataset, "Next Word Predictor, LLMs". According to its description, the dataset is well-suited for building models based on architectures such as RNN, LSTM, and even LLMs. The dataset consists of a collection of diverse text comprising approximately 4,994 words.
This dataset provides a sufficient foundation for training models to predict the next word in a sequence and supports the development of advanced text generation systems.

Preprocessing Pipeline:
In this phase, we prepare the raw data into a structured numerical format ready to be fed into our model (which will be discussed in the following section). The preprocessing steps are as follows:
1.	Data Cleaning:
The dataset was cleaned by removing unnecessary textual symbols such as #, $, %, &, (), and others.
2.	Tokenization:
We applied tokenization to split the sentences into individual words and assign a unique numerical identifier to each word.
3.	Generating Input Sequences:
From the tokenized data, we generated multiple input sequences by progressively removing one or more words from the end of each sentence.
This step helps the model learn to predict the next word based on partial input.
4.	Padding and Encoding:
Since the generated sequences vary in length, we applied padding to ensure uniform sequence length.
To avoid bias caused by word indices being treated as having different magnitudes (e.g., word 1 vs word 200), we used one-hot encoding to represent each word as a binary vector.
After completing these steps, the dataset became ready to be used as input for our predictive text model.

Model:
In this project, we used a Long Short-Term Memory (LSTM) model, a special type of Recurrent Neural Network (RNN) designed to handle sequences of text while preserving important information over long distances.
LSTM is particularly powerful in solving the common problem of forgetting long-term dependencies, making it ideal for tasks like text prediction.
The architecture of the model we built includes the following components:
•	An Embedding layer to convert words into dense vector representations.
•	A single LSTM layer containing 150 units (cells) to learn temporal dependencies in the text.
•	A Dense output layer with a softmax activation function to predict the probability distribution over the next possible word.
After training the model for 150 epochs, we achieved promising results:
•	Accuracy: approximately 90%
•	Loss: very low, indicating effective learning and good model convergence.
Furthermore, it is worth noting that the learning curve remained stable and well-balanced across all epochs, demonstrating that the model was learning effectively and efficiently without signs of overfitting or instability.
