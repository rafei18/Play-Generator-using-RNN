# Play Generator using RNN

In this project, I implemented a text generation model using TensorFlow/Keras to learn patterns from a dataset of Shakespeare's writings. The model architecture comprises an embedding layer, an LSTM layer, and a dense layer. During training, the model learns to predict the next character in a sequence of text based on the preceding characters.

This guide is based on the official TensorFlow tutorials.


- Importing the Dataset: The first step involves importing the dataset containing Shakespeare's writings.
- Encoding the Text: Each unique character in the dataset is encoded as a different integer to prepare the data for training.
- Creating Training Examples: Training examples are created by breaking the text data into shorter sequences. Each input sequence is of length 101, and the corresponding output sequence is the original sequence shifted one character to the right.
- Preparing the Dataset: The text data is converted into batches of desired length (101 characters) using TensorFlow dataset functionalities.
- Building the Model: The model architecture includes an embedding layer, an LSTM layer, and a dense layer. The dense layer provides a probability distribution over all nodes for each character.
- Creating a Custom Loss Function: A custom loss function is created to compare the expected output to the predicted output, considering the probability distribution output by the model.
- Compiling the Model: The model is compiled with the custom loss function and an optimizer.
- Training the Model: The model is trained on the dataset. In this instance, only 2 epochs are used for validation due to time constraints.