# Sigma NPL

## Submission for IgnitionHacks Sigma Division

View model.ipynb and submission.csv in Github

# Inspiration

The inspiration behind our project stems from a desire to learn about neural network architectures. We took on the classic problem statement of sentiment analysis and hoped to gain new skills and professional assets from the experience. The research we performed invoked a deeper understanding of neuron layers and we were inspired to innovate upon conventional network architectures. 

# What it does

The application analyzes positive and negative sentiment in text. The text is preprocessed and tokenized before being passed into our neural network. The neural network analyzes the sequences and searches for patterns using the weights from the training process before finally determining how positive/negative a piece of text is.  

# How we built it

The neural network was built in Google Colab using the Tensorflow libraries for neural networks. Preprocessing was done through a Python script and Regex libraries. The thought process behind our network architecture is outlined below:

## Our Model Architecture

Embedding - Converts words into vectors in transformed space to represent the data more meaningfully as opposed to a 'Bag of Words' where words are mapped to an ID.

Dropout - The dropout layer randomly sets inputs to 0, this helps introduce some randomness to prevent overfitting.

LSTM - Long Short-Term Memory is a layer specialized for taking into account the context from a sequence. This helps with tasks such as NLP, as language is very context dependant.

GlobalAveragePooling1D - Pooling layers are used to reduce the number of parameters in a model. This helps avoid
overfitting to the training data. We are performing binary classification so it is only 1-dimensional.

Dense - Dense layers represent a layer of neurons that is fully connected to the previous layer. The weights are adjusted during training as with all the other layers.

# Challenges we ran into

One of the issues we faced was creating a concise framework for sharing our code. We encountered issues with sharing on Github because of the large file size of our trained model. The common solution of using Github LFS helped us work around these issues, but raised some challenges of their own.

Github LFS has limited storage and bandwidth each month which eventually forced us to recreate our repo after we had maxed out the monthly limits. The experience taught us to be more conservative and precise with our usage of commits, as well as how to appropriately structure local save files to reduce storage usage.

We also faced challenges with inconsistent Tokenization, as we were fine-tuning our preprocessing script while the model was training. This led to inconsistencies with the training data and the cleaned data, but despite the adversity, we were able to salvage key elements and end up with a result that we are satisfied with.

# Accomplishments that we're proud of

We're proud of the presentation of our code. We believe that our concise code and commenting make it easily accessible to a wide array of audiences. Also, we are proud that we were able to apply new-found knowledge and techniques to fine-tune our algorithm.

## What we learned

The project taught us skills such as utilizing regex and a variety of data structures (NumPy, pandas, TensorFlow).

We learned a lot about the inner-workings of neural networks and have gained a more in-depth understanding of Tensorflow libraries. A skill we picked up was how to work with data pipelines. Initially, the large dataset gave us problems as we attempted to load it into the RAM for training. However, by setting up a data pipeline through Tensorflow Datasets we were able to pass our data in batches, preventing our RAM from being used up and streamlining the training in the process.

# What's next for Sigma NLP

Our hope with Sigma NLP is to create an interface for sentiment analysis that can be utilized by everyday users. Creating a user-friendly online experience is one of the sectors that we can see Sigma NLP helping to advance. Implementations could include creating filters against negative posts/tweets on social media, in a similar manner to parental controls.

In the future, we hope to increase the accuracy of Sigma NLP by utilizing industry-standard preprocessing techniques and further innovating upon the neural network architecture.
