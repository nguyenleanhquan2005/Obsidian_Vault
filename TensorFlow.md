
end to end open source platform for machine learning, deep learning. it supports the following:
- multidimensional-array based numeric computation (similar to NumPy)
- GPU and distributed processing
- Automatic differentiation
- Model construction, training and export


**1. What is the difference between traditional programming and Machine Learning?**
- [ ] A. Machine learning identifies complex activities such as golf, while traditional programming is better suited to simpler activities such as walking.
- [x] B. In traditional programming, a programmer has to formulate or code rules manually, whereas, in Machine Learning, the algorithm automatically formulates the rules from the data.

**2. What do we call the process of telling the computer what the data represents (i.e. this data is for walking, this data is for running)?**
- [ ] A. Learning the Data
- [ ] B. Categorizing the Data
- [ ] C. Programming the Data
- [x] D. Labelling the Data

**3. What is a Dense layer?**
- [x] A. A layer of neurons fully connected to its adjacent layers
- [ ] B. An amount of mass occupying a volume
- [ ] C. A single neuron
- [ ] D. A layer of disconnected neurons

**4. How do you measure how good the current 'guess' is?**
- [ ] A. Training a neural network
- [ ] B. Figuring out if you win or lose
- [x] C. Using the Loss function

**5. What does the optimizer do?**
- [ ] A. Figures out how to efficiently compile your code
- [ ] B. Decides to stop training a neural network
- [ ] C. Measures how good the current guess is
- [x] D. Generates a new and improved guess

**6. What is Convergence?**
- [ ] A. A dramatic increase in loss
- [ ] B. A programming API for AI
- [ ] C. An analysis that corresponds too closely or exactly to a particular set of data.
- [x] D. The process of getting very close to the correct answer

**7. What does model.fit do?**
- [ ] A. It makes a model fit available memory
- [x] B. It trains the neural network to fit one set of values to another
- [ ] C. It determines if your activity is good for your body
- [ ] D. It optimizes an existing model

**8. What is the resolution of the 70,000 images from the Fashion MNIST dataset?**
- [ ] A. 82x82 Greyscale
- [ ] B. 100x100 Color
- [ ] C. 28x28 Color
- [x] D. 28x28 Greyscale

**9. Why are there 10 output neurons in the Neural Network used as an example for the Computer Vision Problem?**
- [x] A. There are 10 different labels
- [ ] B. Purely arbitrary
- [ ] C. To make it classify 10x faster
- [ ] D. To make it train 10x faster

**10. What does Relu do?**
- [ ] A. For a value x, it returns 1/x
- [ ] B. It only returns x if x is less than zero
- [x] C. It only returns x if x is greater than zero
- [ ] D. It returns the negative of x

**11. Why do you split data into training and test sets?**
- [ ] A. To make testing quicker
- [ ] B. To make training quicker
- [ ] C. To train a network with previously unseen data
- [x] D. To test a network with previously unseen data

**12. True or False: The on_epoch_end function sends a logs object with lots of great information about the current state of training at the start of every epoch**
- [ ] A. True
- [x] B. False

**13. Why do you set the callbacks= parameter in your fit function?**
- [ ] A. So that the training loops performs all epochs
- [ ] B. Because it accelerates the training
- [x] C. So, on every epoch you can call back to a code function

**14. How do Convolutions improve image recognition?**
- [ ] A. They make the image clearer
- [x] B. They isolate features in images
- [ ] C. They make processing of images faster
- [ ] D. They make the image smaller

**15. What does the Pooling technique do to the images?**
- [ ] A. Makes them sharper
- [ ] B. Combines them
- [x] C. Reduces information in them while maintaining some features
- [ ] D. Isolates features in them

**16. True or False. If you pass a 28x28 image through a 3x3 filter the output will be 26x26**
- [x] A. True
- [ ] B. False

**17. After max pooling a 26x26 image with a 2x2 filter, the output will be 56x56**
- [x] A. False
- [ ] B. True

**18. How does using Convolutions in our Deep neural network impact training?**
- [ ] A. It makes it faster
- [x] B. Its impact will depend on other factors.
- [ ] C. It makes it slower
- [ ] D. It does not affect training

**19. Using Image Generator, how do you label images?**
- [ ] A. TensorFlow figures it out from the contents
- [ ] B. You have to manually do it
- [x] C. It's based on the directory the image is contained in
- [ ] D. It's based on the file name

**20. What method on the Image Generator is used to normalize the image?**
- [ ] A. normalize_image
- [x] B. rescale
- [ ] C. normalize
- [ ] D. Rescale_image

**21. How did we specify the training size for the images?**
- [x] A. The target_size parameter on the training generator
- [ ] B. The target_size parameter on the validation generator
- [ ] C. The training_size parameter on the validation generator
- [ ] D. The training_size parameter on the training generator

**22. When we specify the input_shape to be (300, 300, 3), what does that mean?**
- [ ] A. There will be 300 horses and 300 humans, loaded in batches of 3
- [ ] B. Every Image will be 300x300 pixels, and there should be 3 Convolutional Layers
- [x] C. Every Image will be 300x300 pixels, with 3 bytes to define color
- [ ] D. There will be 300 images, each size 300, loaded in batches of 3

**23. If your training data is close to 1.000 accuracy, but your validation data isn't, what's the risk here?**
- [x] A. You're overfitting on your training data
- [ ] B. You're overfitting on your validation data
- [ ] C. No risk, that's a great result
- [ ] D. You're underfitting on your validation data

**24. Convolutional Neural Networks are better for classifying images like horses and humans because:**
- [ ] A. There's a wide variety of humans
- [ ] B. There's a wide variety of horses
- [x] C. In these images, the features may be in different parts of the frame

**25. After reducing the size of the images, the training results were different. Why?**
- [ ] A. There was more condensed information in the images
- [x] B. We removed some convolutions to handle the smaller images
- [ ] C. The training was faster
- [ ] D. There was less information in the images

**26. What does flow_from_directory give you on the ImageDataGenerator?**
- [ ] A. The ability to easily load images for training
- [ ] B. The ability to pick the size of training images
- [ ] C. The ability to automatically label images based on their directory name
- [x] D. All of the above

**27. If my Image is sized 150x150, and I pass a 3x3 Convolution over it, what size is the resulting image?**
- [ ] A. 153x153
- [x] B. 148x148
- [ ] C. 150x150
- [ ] D. 450x450

**28. If my data is sized 150x150, and I use Pooling of size 2x2, what size will the resulting image be?**
- [ ] A. 300x300
- [ ] B. 148x148
- [x] C. 75x75
- [ ] D. 149x149

**29. If I want to view the history of my training, how can I access it?**
- [x] A. Create a variable 'history' and assign it to the return of model.fit or model.fit_generator
- [ ] B. Pass the parameter 'history=true' to the model.fit
- [ ] C. Download the model and inspect it
- [ ] D. Use a model.fit_generator

**30. What's the name of the API that allows you to inspect the impact of convolutions on the images?**
- [ ] A. The model.images API
- [ ] B. The model.convolutions API
- [ ] C. The model.pools API
- [x] D. The model.layers API

**31. When exploring the graphs, the loss levelled out at about .75 after 2 epochs, but the accuracy climbed close to 1.0 after 15 epochs. What's the significance of this?**
- [ ] A. There was no point training after 2 epochs, as we overfit to the validation data
- [x] B. There was no point training after 2 epochs, as we overfit to the training data
- [ ] C. A bigger training set would give us better validation accuracy
- [ ] D. A bigger validation set would give us better training accuracy

**32. Why is the validation accuracy a better indicator of model performance than training accuracy?**
- [ ] A. It isn't, they're equally valuable
- [ ] B. There's no relationship between them
- [x] C. The validation accuracy is based on images that the model hasn't been trained with, and thus a better indicator of how the model will perform with new images.
- [ ] D. The validation dataset is smaller, and thus less accurate at measuring accuracy, so its performance isn't as important

**33. Why is overfitting more likely to occur on smaller datasets?**
- [ ] A. Because in a smaller dataset, your validation data is more likely to look like your training data
- [ ] B. Because there isn't enough data to activate all the convolutions or neurons
- [ ] C. Because with less data, the training will take place more quickly, and some features may be missed
- [x] D. Because there's less likelihood of all possible features being encountered in the training process.

**34. How do you use Image Augmentation in TensorFlow**
- [ ] A. With the tf.augment API
- [ ] B. You have to write a plugin to extend tf.layers
- [ ] C. With the keras.augment API
- [x] D. Using parameters to the ImageDataGenerator

**35. If my training data only has people facing left, but I want to classify people facing right, how would I avoid overfitting?**
- [ ] A. Use the 'flip' parameter and set 'horizontal'
- [x] B. Use the 'horizontal_flip' parameter
- [ ] C. Use the 'flip_vertical' parameter around the Y axis
- [ ] D. Use the 'flip' parameter

**36. After adding data augmentation and using the same batch size and steps per epoch, you noticed that each training epoch became a little slower than when you trained without it. Why?**
- [ ] A. Because there is more data to train on
- [x] B. Because the image preprocessing takes cycles
- [ ] C. Because the augmented data is bigger
- [ ] D. Because the training is making more mistakes

**37. What does the fill_mode parameter do?**
- [ ] A. There is no fill_mode parameter
- [ ] B. It creates random noise in the image
- [x] C. It attempts to recreate lost information after a transformation like a shear
- [ ] D. It masks the background of an image

**38. When using Image Augmentation with the ImageDataGenerator, what happens to your raw image data on-disk.**
- [ ] A. It gets overwritten, so be sure to make a backup
- [ ] B. A copy is made and the augmentation is done on the copy
- [x] C. Nothing, all augmentation is done in-memory
- [ ] D. It gets deleted

**39. How does Image Augmentation help solve overfitting?**
- [ ] A. It slows down the training process
- [x] B. It manipulates the training set to generate more scenarios for features in the images
- [ ] C. It manipulates the validation set to generate more scenarios for features in the images
- [ ] D. It automatically fits features to images by finding them through image processing techniques

**40. When using Image Augmentation my training gets...**
- [x] A. Slower
- [ ] B. Faster
- [ ] C. Stays the Same
- [ ] D. Much Faster

**41. Using Image Augmentation effectively simulates having a larger data set for training.**
- [ ] A. False
- [x] B. True

**42. If I put a dropout parameter of 0.2, how many nodes will I lose?**
- [x] A. 20% of them
- [ ] B. 2% of them
- [ ] C. 20% of the untrained ones
- [ ] D. 2% of the untrained ones

**43. Why is transfer learning useful?**
- [ ] A. Because I can use all of the data from the original training set
- [ ] B. Because I can use all of the data from the original validation set
- [x] C. Because I can use the features that were learned from large datasets that I may not have access to
- [ ] D. Because I can use the validation metadata from large datasets that I may not have access to

**44. How did you lock or freeze a layer from retraining?**
- [ ] A. tf.freeze(layer)
- [ ] B. tf.layer.frozen = true
- [ ] C. tf.layer.locked = true
- [x] D. layer.trainable = false

**45. How do you change the number of classes the model can classify when using transfer learning? (i.e. the original model handled 1000 classes, but yours handles just 2)**
- [ ] A. Ignore all the classes above yours (i.e. Numbers 2 onwards if I'm just classing 2)
- [ ] B. Use all classes but set their weights to 0
- [x] C. When you add your DNN at the bottom of the network, you specify your output layer with the number of classes you want
- [ ] D. Use dropouts to eliminate the unwanted classes

**46. Can you use Image Augmentation with Transfer Learning Models?**
- [ ] A. No, because you are using pre-set features
- [x] B. Yes, because you are adding new layers at the bottom of the network, and you can use image augmentation when training these

**47. Why do dropouts help avoid overfitting?**
- [x] A. Because neighbor neurons can have similar weights, and thus can skew the final training
- [ ] B. Having less neurons speeds up training

**48. What would the symptom of a Dropout rate being set too high?**
- [x] A. The network would lose specialization to the effect that it would be inefficient or ineffective at learning, driving accuracy down
- [ ] B. Training time would increase due to the extra calculations being required for higher dropout

**49. Which is the correct line of code for adding Dropout of 20% of neurons using TensorFlow**
- [ ] A. tf.keras.layers.Dropout(20)
- [ ] B. tf.keras.layers.DropoutNeurons(20),
- [x] C. tf.keras.layers.Dropout(0.2),
- [ ] D. tf.keras.layers.DropoutNeurons(0.2),

**50. The diagram for traditional programming had Rules and Data In, but what came out?**
- [x] A. Answers
- [ ] B. Binary
- [ ] C. Machine Learning
- [ ] D. Bugs

**51. Why does the DNN for Fashion MNIST have 10 output neurons?**
- [ ] A. To make it train 10x faster
- [ ] B. To make it classify 10x faster
- [ ] C. Purely Arbitrary
- [x] D. The dataset has 10 classes

**52. What is a Convolution?**
- [ ] A. A technique to make images smaller
- [ ] B. A technique to make images larger
- [x] C. A technique to extract features from an image
- [ ] D. A technique to remove unwanted images

**53. Applying Convolutions on top of a DNN will have what impact on training?**
- [ ] A. It will be slower
- [ ] B. It will be faster
- [ ] C. There will be no impact
- [x] D. It depends on many factors. It might make your training faster or slower, and a poorly designed Convolutional layer may even be less efficient than a plain DNN!

**54. What method on an ImageGenerator is used to normalize the image?**
- [ ] A. normalize
- [ ] B. flatten
- [ ] C. rezize()
- [x] D. rescale

**55. When using Image Augmentation with the ImageDataGenerator, what happens to your raw image data on-disk.**
- [ ] A. A copy will be made, and the copies are augmented
- [ ] B. A copy will be made, and the originals will be augmented
- [x] C. Nothing
- [ ] D. The images will be edited on disk, so be sure to have a backup

**56. Can you use Image augmentation with Transfer Learning?**
- [ ] A. No - because the layers are frozen so they can't be augmented
- [x] B. Yes. It's pre-trained layers that are frozen. So you can augment your images as you train the bottom layers of the DNN with them

**57. When training for multiple classes what is the Class Mode for Image Augmentation?**
- [ ] A. class_mode='multiple'
- [ ] B. class_mode='non_binary'
- [x] C. class_mode='categorical'
- [ ] D. class_mode='all'

**58. What is the name of the object used to tokenize sentences?**
- [ ] A. CharacterTokenizer
- [ ] B. TextTokenizer
- [ ] C. WordTokenizer
- [x] D. Tokenizer

**59. What is the name of the method used to tokenize a list of sentences?**
- [ ] A. tokenize(sentences)
- [ ] B. fit_to_text(sentences)
- [ ] C. tokenize_on_text(sentences)
- [x] D. fit_on_texts(sentences)

**60. Once you have the corpus tokenized, what's the method used to encode a list of sentences to use those tokens?**
- [x] A. texts_to_sequences(sentences)
- [ ] B. text_to_sequences(sentences)
- [ ] C. texts_to_tokens(sentences)
- [ ] D. text_to_tokens(sentences)

**61. When initializing the tokenizer, how do you specify a token to use for unknown words?**
- [x] A. oov_token=
- [ ] B. unknown_token=
- [ ] C. out_of_vocab=
- [ ] D. unknown_word=

**62. If you don't use a token for out of vocabulary words, what happens at encoding?**
- [ ] A. The word is replaced by the most common token
- [ ] B. The word isn't encoded, and the sequencing ends
- [x] C. The word isn't encoded, and is skipped in the sequence
- [ ] D. The word isn't encoded, and is replaced by a zero in the sequence

**63. If you have a number of sequences of different lengths, how do you ensure that they are understood when fed into a neural network?**
- [ ] A. Specify the input layer of the Neural Network to expect different sizes with dynamic_length
- [ ] B. Make sure that they are all the same length using the pad_sequences method of the tokenizer
- [ ] C. Process them on the input layer of the Neural Network using the pad_sequences property
- [x] D. Use the pad_sequences function from the tensorflow.keras.preprocessing.sequence namespace

**64. If you have a number of sequences of different length, and call pad_sequences on them, what's the default result?**
- [ ] A. Nothing, they'll remain unchanged
- [x] B. They'll get padded to the length of the longest sequence by adding zeros to the beginning of shorter ones
- [ ] C. They'll get cropped to the length of the shortest sequence
- [ ] D. They'll get padded to the length of the longest sequence by adding zeros to the end of shorter ones

**65. When padding sequences, if you want the padding to be at the end of the sequence, how do you do it?**
- [ ] A. Call the padding method of the pad_sequences object, passing it 'after'
- [x] B. Pass padding='post' to pad_sequences when initializing it
- [ ] C. Call the padding method of the pad_sequences object, passing it 'post'
- [ ] D. Pass padding='after' to pad_sequences when initializing it

**66. What is the name of the TensorFlow library containing common data that you can use to train and test neural networks?**
- [ ] A. TensorFlow Data
- [ ] B. TensorFlow Data Libraries
- [x] C. TensorFlow Datasets
- [ ] D. There is no library of common data sets, you have to use your own

**67. How many reviews are there in the IMDB dataset and how are they split?**
- [ ] A. 60,000 records, 80/20 train/test split
- [ ] B. 50,000 records, 80/20 train/test split
- [x] C. 50,000 records, 50/50 train/test split
- [ ] D. 60,000 records, 50/50 train/test split

**68. How are the labels for the IMDB dataset encoded?**
- [ ] A. Reviews encoded as a number 1-10
- [ ] B. Reviews encoded as a number 1-5
- [ ] C. Reviews encoded as a boolean true/false
- [x] D. Reviews encoded as a number 0-1

**69. What is the purpose of the embedding dimension?**
- [ ] A. It is the number of words to encode in the embedding
- [ ] B. It is the number of dimensions required to encode every word in the corpus
- [x] C. It is the number of dimensions for the vector representing the word encoding
- [ ] D. It is the number of letters in the word, denoting the size of the encoding

**70. When tokenizing a corpus, what does the num_words=n parameter do?**
- [ ] A. It specifies the maximum number of words to be tokenized, and picks the first 'n' words that were tokenized
- [ ] B. It errors out if there are more than n distinct words in the corpus
- [ ] C. It specifies the maximum number of words to be tokenized, and stops tokenizing when it reaches n
- [x] D. It specifies the maximum number of words to be tokenized, and picks the most common 'n-1' words

**71. To use word embeddings in TensorFlow, in a sequential layer, what is the name of the class?**
- [ ] A. tf.keras.layers.Word2Vector
- [ ] B. tf.keras.layers.WordEmbedding
- [ ] C. tf.keras.layers.Embed
- [x] D. tf.keras.layers.Embedding

**72. IMDB Reviews are either positive or negative. What type of loss function should be used in this scenario?**
- [ ] A. Binary Gradient descent
- [ ] B. Categorical crossentropy
- [x] C. Binary crossentropy
- [ ] D. Adam

**73. When using IMDB Sub Words dataset, our results in classification were poor. Why?**
- [ ] A. The sub words make no sense, so can't be classified
- [ ] B. We didn't train long enough
- [ ] C. Our neural network didn't have enough layers
- [x] D. Sequence becomes much more important when dealing with subwords, but we're ignoring word positions

**74. When predicting words to generate poetry, the more words predicted the more likely it will end up gibberish. Why?**
- [x] A. Because the probability that each word matches an existing phrase goes down the more words you create
- [ ] B. It doesn't, the likelihood of gibberish doesn't change
- [ ] C. Because you are more likely to hit words not in the training set
- [ ] D. Because the probability of prediction compounds, and thus increases overall

**75. What is a major drawback of word-based training for text generation instead of character-based generation?**
- [ ] A. Character based generation is more accurate because there are less characters to predict
- [ ] B. Word based generation is more accurate because there is a larger body of words to draw from
- [ ] C. There is no major drawback, it's always better to do word-based training
- [x] D. Because there are far more words in a typical corpus than characters, it is much more memory intensive

**76. What are the critical steps in preparing the input sequences for the prediction model?**
- [x] A. Generating subphrases from each line using n_gram_sequences.
- [x] B. Pre-padding the subphrases sequences.
- [ ] C. Converting the seed text to a token sequence using texts_to_sequences.
- [ ] D. Splitting the dataset into training and testing sentences.

**77. In natural language processing, predicting the next item in a sequence is a classification problem. Therefore, after creating inputs and labels from the subphrases, we one-hot encode the labels. What function do we use to create one-hot encoded arrays of the labels?**
- [ ] A. tf.keras.utils.SequenceEnqueuer
- [x] B. tf.keras.utils.to_categorical
- [ ] C. tf.keras.preprocessing.text.one_hot
- [ ] D. tf.keras.utils.img_to_array

**78. True or False: When building the model, we use a sigmoid activated Dense output layer with one neuron per word that lights up when we predict a given word.**
- [x] A. False
- [ ] B. True

**79. What is an example of a Univariate time series?**
- [ ] A. Hour by hour weather
- [ ] B. Fashion items
- [x] C. Hour by hour temperature
- [ ] D. Baseball scores

**80. What is an example of a Multivariate time series?**
- [ ] A. Hour by hour temperature
- [x] B. Hour by hour weather
- [ ] C. Fashion items
- [ ] D. Baseball scores

**81. What is imputed data?**
- [x] A. A projection of unknown (usually past or missing) data
- [ ] B. A good prediction of future data
- [ ] C. A bad prediction of future data
- [ ] D. Data that has been withheld for various reasons

**82. A sound wave is a good example of time series data**
- [x] A. True
- [ ] B. False

**83. What is Seasonality?**
- [ ] A. Data aligning to the 4 seasons of the calendar
- [x] B. A regular change in shape of the data
- [ ] C. Data that is only available at certain times of the year
- [ ] D. Weather data

**84. What is a trend?**
- [ ] A. An overall consistent flat direction for data
- [x] B. An overall direction for data regardless of direction
- [ ] C. An overall consistent upward direction for data
- [ ] D. An overall consistent downward direction for data

**85. In the context of time series, what is noise?**
- [ ] A. Sound waves forming a time series
- [ ] B. Data that doesn't have a trend
- [x] C. Unpredictable changes in time series data
- [ ] D. Data that doesn't have seasonality

**86. What is autocorrelation?**
- [ ] A. Data that automatically lines up in trends
- [x] B. Data that follows a predictable shape, even if the scale is different
- [ ] C. Data that automatically lines up seasonally
- [ ] D. Data that doesn't have noise

**87. What is a non-stationary time series?**
- [ ] A. One that moves seasonally.
- [ ] B. One that is consistent across all seasons.
- [ ] C. One that has a constructive event forming trend and seasonality.
- [x] D. One that has a disruptive event breaking trend and seasonality.

**88. What is a windowed dataset?**
- [ ] A. The time series aligned to a fixed shape
- [x] B. A fixed-size subset of a time series
- [ ] C. A consistent set of subsets of a time series
- [ ] D. There's no such thing

**89. What does 'drop_remainder=True' do?**
- [ ] A. It ensures that all data is used
- [ ] B. It ensures that all rows in the data window are the same length by adding data
- [x] C. It ensures that all rows in the data window are the same length by cropping data
- [ ] D. It ensures that the data is all the same shape

**90. What's the correct line of code to split an n column window into n-1 columns for features and 1 column for a label**
- [ ] A. dataset = dataset.map(lambda window: (window[n-1], window[1]))
- [x] B. dataset = dataset.map(lambda window: (window[:-1], window[-1:]))
- [ ] C. dataset = dataset.map(lambda window: (window[-1:], window[:-1]))
- [ ] D. dataset = dataset.map(lambda window: (window[n], window[1]))

**91. What does MSE stand for?**
- [ ] A. Mean Series error
- [x] B. Mean Squared error
- [ ] C. Mean Second error
- [ ] D. Mean Slight error

**92. What does MAE stand for?**
- [ ] A. Mean Average Error
- [ ] B. Mean Advanced Error
- [x] C. Mean Absolute Error
- [ ] D. Mean Active Error

**93. If time values are in time[], series values are in series[] and we want to split the series into training and validation at time split_time, what is the correct code?**
- [ ] A. time_train = time[:split_time] x_train = series[:split_time] time_valid = time[split_time] x_valid = series[split_time]
- [x] B. time_train = time[:split_time] x_train = series[:split_time] time_valid = time[split_time:] x_valid = series[split_time:]
- [ ] C. time_train = time[split_time] x_train = series[split_time] time_valid = time[split_time:] x_valid = series[split_time:]
- [ ] D. time_train = time[split_time] x_train = series[split_time] time_valid = time[split_time] x_valid = series[split_time]

**94. If you want to inspect the learned parameters in a layer after training, what's a good technique to use?**
- [x] A. Assign a variable to the layer and add it to the model using that variable. Inspect its properties after training.
- [ ] B. Run the model with unit data and inspect the output for that layer.
- [ ] C. Decompile the model and inspect the parameter set for that layer.
- [ ] D. Iterate through the layers dataset of the model to find the layer you want.

**95. How do you set the learning rate of the SGD optimizer?**
- [ ] A. Use the Rate property
- [ ] B. Use the RateOfLearning property
- [x] C. Use the learning_rate property
- [ ] D. You can't set it

**96. If you want to amend the learning rate of the optimizer on the fly, after each epoch. What do you do?**
- [ ] A. Use a LearningRateScheduler and pass it as a parameter to a callback
- [ ] B. Callback to a custom function and change the SGD property
- [x] C. Use a LearningRateScheduler object in the callbacks namespace and assign that to the callback
- [ ] D. You can't set it

**97. If X is the standard notation for the input to an RNN, what are the standard notations for the outputs?**
- [ ] A. Y
- [ ] B. H
- [x] C. Y(hat) and H
- [ ] D. H(hat) and Y

**98. What is a sequence to vector if an RNN has 30 cells numbered 0 to 29**
- [ ] A. The total Y(hat) for all cells
- [ ] B. The average Y(hat) for all 30 cells
- [x] C. The Y(hat) for the last cell
- [ ] D. The Y(hat) for the second cell

**99. What does a Lambda layer in a neural network do?**
- [ ] A. Pauses training without a callback
- [ ] B. Changes the shape of the input or output data
- [ ] C. There are no Lambda layers in a neural network
- [x] D. Allows you to execute arbitrary code while training

**100. What does the axis parameter of tf.expand_dims do?**
- [ ] A. Defines the axis around which to expand the dimensions
- [ ] B. Defines the dimension index to remove when you expand the tensor
- [ ] C. Defines if the tensor is X or Y
- [x] D. Defines the dimension index at which you will expand the shape of the tensor

**101. A new loss function was introduced in this module, named after a famous statistician. What is it called?**
- [ ] A. Hubble loss
- [ ] B. Hawking loss
- [ ] C. Hyatt loss
- [x] D. Huber loss

**102. What's the primary difference between a simple RNN and an LSTM**
- [ ] A. In addition to the H output, RNNs have a cell state that runs across all cells
- [x] B. In addition to the H output, LSTMs have a cell state that runs across all cells
- [ ] C. LSTMs have a single output, RNNs have multiple
- [ ] D. LSTMs have multiple outputs, RNNs have a single one

**103. If you want to clear out all temporary variables that tensorflow might have from previous sessions, what code do you run?**
- [x] A. tf.keras.backend.clear_session()
- [ ] B. tf.cache.backend.clear_session()
- [ ] C. tf.keras.clear_session
- [ ] D. tf.cache.clear_session()

**104. What happens if you define a neural network with these two layers? tf.keras.layers.Bidirectional(tf.keras.layers.LSTM(32)), tf.keras.layers.Bidirectional(tf.keras.layers.LSTM(32)), tf.keras.layers.Dense(1)**
- [ ] A. Your model will fail because you have the same number of cells in each LSTM
- [x] B. Your model will fail because you need return_sequences=True after the first LSTM layer
- [ ] C. Your model will fail because you need return_sequences=True after each LSTM layer
- [ ] D. Your model will compile and run correctly

**105. How do you add a 1 dimensional convolution to your model for predicting time series data?**
- [ ] A. Use a ConvolutionD1 layer type
- [ ] B. Use a 1DConvolution layer type
- [x] C. Use a Conv1D layer type
- [ ] D. Use a 1DConv layer type

**106. What's the input shape for a univariate time series to a Conv1D?**
- [x] A. [None, 1]
- [ ] B. []
- [ ] C. [1]
- [ ] D. [1, None]

**107. You used a sunspots dataset that was stored in CSV. What's the name of the Python library used to read CSVs?**
- [ ] A. CommaSeparatedValues
- [x] B. CSV
- [ ] C. PyCSV
- [ ] D. PyFiles

**108. If your CSV file has a header that you don't want to read into your dataset, what do you execute before iterating through the file using a 'reader' object?**
- [ ] A. reader.read(next)
- [ ] B. reader.next
- [x] C. next(reader)
- [ ] D. reader.ignore_header()

**109. When you read a row from a reader and want to cast column 2 to another data type, for example, a float, what's the correct syntax?**
- [ ] A. float f = row[2].read()
- [ ] B. You can't. It needs to be read into a buffer and a new float instantiated from the buffer
- [ ] C. Convert.toFloat(row[2])
- [x] D. float(row[2])

**110. What was the sunspot seasonality?**
- [ ] A. 22 years
- [ ] B. 4 times a year
- [ ] C. 11 years
- [x] D. 11 or 22 years depending on who you ask

**111. After studying this course, what neural network type do you think is best for predicting time series like our sunspots dataset?**
- [ ] A. DNN
- [ ] B. Convolutions
- [ ] C. RNN / LSTM
- [x] D. A combination of all other answers

**112. Why is MAE a good analytic for measuring accuracy of predictions for time series?**
- [ ] A. It punishes larger errors
- [x] B. It doesn't heavily punish larger errors like square errors do
- [ ] C. It only counts positive errors
- [ ] D. It biases towards small errors

**113. Why does sequence make a large difference when determining semantics of language?**
- [x] A. Because the order in which words appear dictate their impact on the meaning of the sentence
- [ ] B. Because the order of words doesn't matter
- [ ] C. It doesn't
- [ ] D. Because the order in which words appear dictate their meaning

**114. How do Recurrent Neural Networks help you understand the impact of sequence on meaning?**
- [ ] A. They don't
- [ ] B. They shuffle the words evenly
- [ ] C. They look at the whole sentence at a time
- [x] D. They carry meaning from one cell to the next

**115. How does an LSTM help understand meaning when words that qualify each other aren't necessarily beside each other in a sentence?**
- [x] A. Values from earlier words can be carried to later ones via a cell state
- [ ] B. They load all words into a cell state
- [ ] C. They shuffle the words randomly
- [ ] D. They don't

**116. What keras layer type allows LSTMs to look forward and backward in a sentence?**
- [ ] A. Bothdirection
- [ ] B. Bilateral
- [ ] C. Unilateral
- [x] D. Bidirectional

**117. What's the output shape of a bidirectional LSTM layer with 64 units?**
- [ ] A. (128,None)
- [ ] B. (128,1)
- [x] C. (None, 128)
- [ ] D. (None, 64)

**118. When stacking LSTMs, how do you instruct an LSTM to feed the next one in the sequence?**
- [ ] A. Do nothing, TensorFlow handles this automatically
- [ ] B. Ensure that they have the same number of units
- [x] C. Ensure that return_sequences is set to True only on units that feed to another LSTM
- [ ] D. Ensure that return_sequences is set to True on all units

**119. If a sentence has 120 tokens in it, and a Conv1D with 128 filters with a Kernal size of 5 is passed over it, what's the output shape?**
- [ ] A. (None, 120, 124)
- [ ] B. (None, 120, 128)
- [x] C. (None, 116, 128)
- [ ] D. (None, 116, 124)

**120. What's the best way to avoid overfitting in NLP datasets?**
- [ ] A. Use LSTMs
- [ ] B. Use GRUs
- [ ] C. Use Conv1D
- [x] D. None of the above

**121. Which type of boundary does the UnicodeCharTokenizer use to separate tokens?**
- [ ] A. Whitespace
- [x] B. Unicode script
- [ ] C. Special symbols
- [ ] D. Punctuation marks

**122. How can image augmentation be implemented in TensorFlow?**
- [ ] A. By manually modifying each image file
- [ ] B. By importing pre-augmented datasets
- [x] C. By using the ImageDataGenerator class
- [ ] D. By applying image transformations after model training

**123. What is a potential use case for the RegexSplitter?**
- [ ] A. Tokenizing text into subword units for language modeling
- [ ] B. Tokenizing multilingual text with different scripts
- [x] C. Tokenizing text into individual words based on custom regular expressions
- [ ] D. Tokenizing text based on learned subword units for WordPiece models

**124. What is the advantage of using a subword text encoder over a word-based encoder in TensorFlow?**
- [ ] A. Subword encoders are computationally faster
- [x] B. Subword encoders handle rare words more effectively
- [ ] C. Word-based encoders result in smaller vocabulary sizes
- [ ] D. Word-based encoders provide better semantic understanding.

**125. When might transfer learning be less effective in TensorFlow?**
- [ ] A. When the source and target tasks are similar.
- [ ] B. When there is a lack of pre-trained models available.
- [x] C. When the datasets for the source and target tasks are small and dissimilar.
- [ ] D. Transfer learning is always effective, regardless of the scenario.

**126. Which deep learning architecture is commonly used for predicting the next word in a sequence?**
- [ ] A. Convolutional Neural Network (CNN)
- [x] B. Recurrent Neural Network (RNN)
- [ ] C. Support Vector Machine (SVM)
- [ ] D. Decision Tree

**127. Which TensorFlow module is specifically designed for transferring knowledge from pre-trained models to new tasks in Computer Vision?**
- [ ] A. TensorFlow Estimator API
- [x] B. TensorFlow Hub
- [ ] C. TensorFlow Lite
- [ ] D. TensorFlow Extended (TFX)

**128. Which NLP technique involves breaking down a sentence into its individual components, such as words or phrases?**
- [x] A. Tokenization
- [ ] B. Clustering
- [ ] C. Dimensionality reduction
- [ ] D. Regularization

**129. Which TensorFlow function is commonly used to apply data augmentation to an image?**
- [ ] A. tf.image.transform()
- [ ] B. tf.data.augmentation.apply()
- [ ] C. tf.image.apply_image_augmentation()
- [x] D. tf.keras.preprocessing.image.random_transform()

**130. Which machine learning technique is suitable for handling complex patterns and nonlinear relationships in time series data?**
- [ ] A. Exponential Smoothing
- [x] B. Decision Trees
- [ ] C. Moving Averages
- [ ] D. Holt-Winters Method

**131. What is the purpose of the teacher forcing technique in training a next-word prediction model?**
- [x] A. To force the model to predict the ground truth at each step
- [ ] B. To increase the model's perplexity
- [ ] C. To decrease the influence of the previous words
- [ ] D. To speed up the training process

**132. What is the purpose of the batch method in a TensorFlow dataset?**
- [ ] A. To shuffle the dataset
- [x] B. To group consecutive elements into batches
- [ ] C. To split the dataset into training and validation sets
- [ ] D. To apply data augmentation to the dataset

**133. In a multiclass classifier, what is the role of the "softmax" activation function?**
- [ ] A. To introduce non-linearity to the model
- [ ] B. To calculate the mean of the predictions
- [x] C. To transform raw scores into probability distributions
- [ ] D. To increase the complexity of the output layer

**134. What function of ImageDataGenerator is commonly used for real-time data augmentation during training?**
- [x] A. flow_from_directory
- [ ] B. fit_genorator
- [ ] C. rescale
- [ ] D. random_transform

**135. Which technique can be used to prevent overfitting by randomly disabling a fraction of neurons during training?**
- [ ] A. Data augmentation
- [ ] B. Early stopping
- [ ] C. L2 regularization
- [x] D. Dropout

**136. In TensorFlow, what is the common approach for training only the added layers while keeping the pre-trained weights fixed?**
- [ ] A. Setting the learning rate to a very small value.
- [x] B. Freezing the layers of the pre-trained model.
- [ ] C. Using a high dropout rate.
- [ ] D. Training for a large number of epochs.

**137. How does a subword text encoder handle rare or infrequent words in TensorFlow?**
- [ ] A. By replacing them with a special token
- [ ] B. By discarding them during encoding
- [x] C. By merging them into larger subword units
- [ ] D. By assigning higher weights to them

**138. What is a typical task associated with a dog and cat dataset on Kaggle?**
- [ ] A. Sentiment analysis
- [x] B. Object detection
- [ ] C. Speech recognition
- [ ] D. Financial forecasting

**139. Which metric is commonly used to measure the accuracy of a forecasting model by comparing the absolute differences between predicted and actual values?**
- [ ] A. Mean Squared Error (MSE)
- [x] B. Mean Absolute Error (MAE)
- [ ] C. Root Mean Squared Error (RMSE)
- [ ] D. R-squared (R2)

**140. How does the SplitMergeTokenizer handle consecutive characters based on custom rules?**
- [x] A. It merges them into a single token.
- [ ] B. It treats each character as a separate token.
- [ ] C. It ignores them during tokenization.
- [ ] D. It replaces them with a special token.

**141. Why is padding necessary in neural networks?**
- [ ] A. To increase computational efficiency
- [ ] B. To reduce model complexity
- [x] C. To ensure all inputs have the same dimensions
- [ ] D. To speed up the training process

**142. Which of the following is a common image augmentation technique used in TensorFlow?**
- [ ] A. Image cropping
- [ ] B. Image binarization
- [ ] C. Image inversion
- [x] D. Image mirroring

**143. What is the purpose of setting the validation_split parameter in flow_from_directory when using ImageDataGenerator?**
- [ ] A. It controls the number of validation steps during training.
- [x] B. It defines the percentage of images used for validation.
- [ ] C. It specifies the validation loss function.
- [ ] D. It adjusts the learning rate during validation.

**144. Which TensorFlow module is commonly used for loading and preprocessing image datasets?**
- [ ] A. tf.keras.layers
- [ ] B. tf.datasets
- [ ] C. tf.image
- [x] D. tf.data

**145. In a multiclass classification problem, how are categorical labels typically represented in TensorFlow?**
- [ ] A. As strings
- [ ] B. As integer values
- [x] C. Using one-hot encoding
- [ ] D. Using floating-point numbers

**146. How can seasonality affect a time series?**
- [ ] A. By introducing random noise
- [ ] B. By creating long-term trends
- [x] C. By causing periodic fluctuations
- [ ] D. By removing outliers

**147. What is the purpose of the Conv2D layer in a computer vision neural network?**
- [ ] A. Handling sequence data
- [ ] B. Performing sequence data
- [x] C. Applying convolutional operations on image data
- [ ] D. Normalizing input features

**148. What does the term "early stopping" refer to in the context of preventing overfitting?**
- [ ] A. Terminating the training process when the model performs poorly on the training set
- [x] B. Halting training when the model's performance on a validation set plateaus
- [ ] C. Increasing the number of training epochs to ensure better convergence
- [ ] D. Initiating training earlier than planned to capture more patterns in the data

**149. What does the term "Exponential Smoothing" refer to in time series forecasting?**
- [ ] A. A technique for handling outliers in data
- [ ] B. A method for reducing the impact of seasonality
- [x] C. A weighted average approach that assigns exponentially decreasing weights to past observations
- [ ] D. A process of transforming time series data into a stationary format

**150. In a typical CNN architecture, what is the purpose of the fully connected (dense) layers?**
- [ ] A. Extracting features from input images
- [ ] B. Reducing spatial dimensions through pooling
- [ ] C. Normalizing the output of convolutional layers
- [x] D. Making predictions based on learned features

**151. How does the vocabulary size impact word-based encodings?**
- [x] A. A larger vocabulary size leads to longer encoding vectors
- [ ] B. A smaller vocabulary size increases the efficiency of encoding
- [ ] C. Vocabulary size has no impact on word-based encodings
- [ ] D. A larger vocabulary size reduces the model's ability to generalize

**152. What role does a "tensor" play in TensorFlow?**
- [ ] A. It's a graphical representation of a machine learning model
- [ ] B. It's a specific type of machine learning algorithm.
- [x] C. It's a fundamental data structure used for numerical computations.
- [ ] D. It's a module for handling natural language processing tasks.

**153. What is the common approach to loading textual data for a multi-class classification task in TensorFlow?**
- [ ] A. Using tf.keras.utils.image_dataset_from_directory
- [ ] B. Employing the tf.keras.datasets.load_text function
- [x] C. Utilizing tf.keras.preprocessing.text_dataset_from_directory
- [ ] D. Loading text data is not supported in TensorFlow

**154. Which TensorFlow layer is commonly used to add a convolutional layer to a CNN model?**
- [ ] A. Dense
- [x] B. Conv2D
- [ ] C. MaxPooling2D
- [ ] D. Flatten

**155. In TensorFlow, what is the role of the tf.data.Dataset.from_tensor_slices() function?**
- [ ] A. It creates a dataset from a list of strings.
- [x] B. It converts NumPy arrays into TensorFlow datasets.
- [ ] C. It generates slices of tensors from a given dataset.
- [ ] D. It defines the architecture of a neural network

**156. What is the purpose of the texts_to_matrix method in the Tokenizer class?**
- [ ] A. Converts sequences to text
- [ ] B. Adds padding to sequences
- [ ] C. Tokenizes words in a document
- [x] D. Converts text to numerical matices

**157. In time series forecasting using LSTMs, what does the term "sequence-to-sequence" refer to?**
- [ ] A. Predicting a single future data point from a single input data point
- [x] B. Predicting a sequence of future data points from a sequence of input data points
- [ ] C. Predicting multiple future data points from a single input data point
- [ ] D. Predicting a single future data point from a sequence of input data points

**158. What happens to leading and trailing characters with different Unicode scripts in the UnicodeScriptTokenizer?**
- [ ] A. They are removed from the tokens.
- [x] B. They are included as part of the tokens.
- [ ] C. They are replaced with special symbols.
- [ ] D. They are ignored during tokenization.

**159. How does the ImageDataGenerator handle the normalization of pixel values in ConvNet training?**
- [ ] A. It does not perform any normalization.
- [ ] B. It normalizes pixel values to be between 0 and 255.
- [ ] C. It automatically adjusts pixel values during training.
- [x] D. It scales pixel values to be between 0 and 1.

**160. How can the ModelCheckpoint callback be beneficial during training?**
- [ ] A. It logs training metrics for visualization.
- [x] B. It saves the model's weights at specified intervals.
- [ ] C. It adjusts the learning rate based on performance.
- [ ] D. It stops training when validation loss reaches a plateau.

**161. What function is typically used to load image data in TensorFlow?**
- [ ] A. load_image()
- [ ] B. read_image()
- [ ] C. tf.load_image()
- [x] D. tf.keras.preprocessing.image.load_img()

**162. When training an LSTM model for time series forecasting, why is it important to normalize the input data?**
- [ ] A. To make the data sationary
- [ ] B. To handle missing values in the time series
- [ ] C. To speed up the training process
- [x] D. To ensure consistent convergence during training

**163. How can you visualize time series data effectively?**
- [ ] A. Scatter plots
- [ ] B. Bar charts
- [x] C. Line charts
- [ ] D. Pie charts

**164. In word-based encodings, what is the advantage of using pretrained word embeddings?**
- [ ] A. They increase the vocabulary size.
- [ ] B. They reduce the dimensionality of the vectors.
- [x] C. They provide word representations learned from extensive data.
- [ ] D. They have no impact on the performance of the model.

**165. Which TensorFlow module is commonly used to load the Inception model for transfer learning?**
- [ ] A. tf.keras.preprocessing.image
- [ ] B. tf.keras.layers.Conv2D
- [x] C. tf.keras.applications.inception_v3
- [ ] D. tf.keras.optimizers.Adam

**166. How can you extract training and validation accuracies from the history object in TensorFlow?**
- [ ] A. By using the get_accuracy method
- [ ] B. By accessing the accuracy attribute directly
- [x] C. By using the history['accuracy'] and history['val_accuracy'] keys
- [ ] D. By applying the calculate_accuracy function

**167. What does the repeat method do when applied to a TensorFlow dataset?**
- [x] A. It repeats the dataset multiple times during training.
- [ ] B. It adds noise to the dataset.
- [ ] C. It repeats the feature-label pairs within each batch.
- [ ] D. It reshapes the dataset.

**168. How does the HubModuleTokenizer handle out-of-vocabulary words?**
- [ ] A. It replaces them with a special token.
- [ ] B. It ignores them during tokenization.
- [ ] C. It treats each charactoer as a separate token.
- [x] D. It splits them into subword units based on learned patterns.

**169. In transfer learning, what are the commonly used pre-trained models in TensorFlow?**
- [x] A. MobileNet and Inception
- [ ] B. LeNet and AlexNet
- [ ] C. Naive Bayes and Decision Trees
- [ ] D. Support Vector Machines and k-Nearest Neighbors

**170. What does the term "tokenization" refer to in the context of word-based encodings?**
- [ ] A. Creating a bag-of-words representation
- [ ] B. Reducing words to their root forms
- [x] C. Breaking down text into individual words or tokens
- [ ] D. Applying sentiment analysis to words

**171. Function to convert numpy array to tensor?**
- [ ] A. tf.convert_to_array()
- [x] B. tf.convert_to_tensor()
- [ ] C. tf.dtypes()
- [ ] D. tf.estimator()

**172. Which of the following evaluation metrics can be used to evaluate a model while modeling a continuous output variable?**
- [ ] A. AUC-ROC
- [ ] B. Accuracy
- [x] C. Mean-Squared-Error
- [ ] D. Log loss

**173. Mention the name of some methods to deal with the overfitting in TensorFlow?**
- [ ] A. Dropout Technique
- [ ] B. Regularization
- [ ] C. Batch Normalization
- [x] D. All of the above

**174. Function to find the version of tensorflow being used in python?**
- [ ] A. tf.version
- [ ] B. tf.version.VERSION
- [x] C. Both A & B
- [ ] D. None of the above

**175. Which is not a valid parameter in tf.keras.model.fit() function?**
- [ ] A. batch_size
- [ ] B. shuffle
- [ ] C. workers
- [x] D. loss

**176. Ways to optimize machine learning models for deployment and execution?**
- [ ] A. Overfitting
- [x] B. Quantization
- [ ] C. Regularization
- [ ] D. Underfitting

**177. Which of the following that a TensorFlow manager can not do?**
- [ ] A. Loading Servables
- [ ] B. Serving Servables
- [ ] C. Unloading Servables
- [x] D. Debugging Servables

**178. The TensorFlow Lite converter takes a TensorFlow model and generates a TensorFlow Lite model of what format, which identified by the .tflite file extension.**
- [ ] A. BufferStore
- [x] B. FlatBuffer
- [ ] C. WeightStore
- [ ] D. ModelFormat

**179. Which is not a module in tfx.components?**
- [ ] A. base
- [ ] B. bulk_inferrer
- [x] C. fit
- [ ] D. evaluator

**180. What is a Data Flow Graph?**
- [x] A. A representation of data dependencies between operations
- [ ] B. A cartesian (x,y) chart
- [ ] C. A graphics user interface
- [ ] D. A flowchart describing an algorithm
- [ ] E. None of the above

**181. For convolution, it is better to store images in TensorFlow Graph as:**
- [x] A. Placeholder
- [ ] B. CSV file
- [ ] C. Numpy array
- [ ] D. Variable
- [ ] E. None of the above

**182. Which of the subsequent declaration(s) effectively represents an actual neuron in TensorFlow?**
- [ ] A. A neuron has a single enter and a single output best
- [ ] B. A neuron has multiple inputs but a single output only
- [ ] C. A neuron has a single input, however, more than one outputs
- [ ] D. A neuron has multiple inputs and more than one outputs
- [x] E. All of the above statements are valid

**183. What are the stairs for the usage of a gradient descent algorithm in TensorFlow?**
1. Calculate error among the actual fee and the anticipated price
2. Reiterate until you find the excellent weights of the network
3. Pass an enter via the community and get values from the output layer
4. Initialize random weight and bias
5. Go to every neurons which contributes to the error and exchange its respective values to lessen the error
- [ ] A. 1, 2, 3, 4, 5
- [ ] B. 5, 4, 3, 2, 1
- [ ] C. 3, 2, 1, 5, 4
- [x] D. 4, 3, 1, 5, 2

**184. "Convolutional Neural Networks can carry out various forms of transformation (rotations or scaling) in an enter". Is the assertion correct true or false in TensorFlow?**
- [ ] True
- [x] False

**185. Which of the following techniques perform comparable operations as the dropout in a neural community in TensorFlow?**
- [x] A. Bagging
- [ ] B. Boosting
- [ ] C. Stacking
- [ ] D. None of those

**186. Which of the following is authentic approximately model capability (in which version capacity method the potential of the neural community to approximate complex capabilities) in TensorFlow?**
- [x] A. As range of hidden layers boom, model capability will increase
- [ ] B. As dropout ratio increases, version capacity increases
- [ ] C. As mastering charge will increase, model capacity will increase
- [ ] D. None of these

**187. In case you growth the range of hidden layers in a Multi-Layer Perceptron, the category errors of check facts always decreases in TensorFlow. Authentic or fake?**
- [ ] Authentic
- [x] Fake

**188. What's the series of the following duties in a perceptron in tensorflow?**
1. Initialize weights of perceptron randomly
2. Visit the subsequent batch of the dataset
3. If the prediction does no longer in shape the output, trade the weights
4. For a sample enter, compute an output
- [ ] A. 1, 2, 3, 4
- [ ] B. 4, 3, 2, 1
- [ ] C. 3, 1, 2, 4
- [x] D. 1, 4, 3, 2

**189. Suppose that you have to limit the value feature via converting the parameters. Which of the subsequent approach could be used for this in TensorFlow?**
- [ ] A. Exhaustive seek
- [ ] B. Random search
- [ ] C. Bayesian Optimization
- [x] D. Any of those

**190. Can a neural network model the characteristic (y=1/x) in TensorFlow?**
- [x] Sure
- [ ] No

**191. Wherein neural internet architecture, does weight sharing occur in TensorFlow?**
- [ ] A. Convolutional neural community
- [ ] B. Recurrent Neural community
- [ ] C. Fully related Neural community
- [x] D. Both a and b

**192. Batch Normalization is useful due to the fact?**
- [x] A. It normalizes (adjustments) all the input earlier than sending it to the subsequent layer
- [ ] B. It returns again the normalized mean and widespread deviation of weights
- [ ] C. It miles a very efficient backpropagation method
- [ ] D. None of those

**193. As opposed to trying to acquire absolute 0 error, we set a metric called Bayes blunders that's the error we hope to achieve. What may be the cause for the use of Bayes blunders in TensorFlow?**
- [ ] A. Input variables might not include entire statistics about the output variable
- [ ] B. Gadget (that creates input-output mapping) may be stochastic
- [ ] C. Constrained training facts
- [x] D. All of the above