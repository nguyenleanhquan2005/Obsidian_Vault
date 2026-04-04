
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


Dưới đây là toàn bộ 55 câu hỏi trắc nghiệm đã được chuyển sang định dạng checkbox của Obsidian, kèm theo Callout ẩn đáp án và giải thích chi tiết. Bạn chỉ cần copy toàn bộ nội dung này dán vào file `.md` trong Obsidian.

---

### Multiple Choice Question 1

Which activation function is most appropriate for the output layer of a multi-label classification problem where an instance can belong to multiple classes simultaneously?

- [ ] A. Softmax
    
- [ ] B. ReLU
    
- [x] C. Sigmoid
    
- [ ] D. Tanh
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Trong multi-label classification (một vật thể có thể thuộc nhiều class cùng lúc), ta dùng Sigmoid cho layer cuối để xuất ra xác suất độc lập cho từng class. Softmax chỉ dùng cho multi-class (chỉ chọn 1 class duy nhất).

---

### Multiple Choice Question 2

How does L2 regularization (Ridge) help mitigate overfitting in a deep neural network?

- [ ] A. By randomly dropping neurons during the forward pass.
    
- [ ] B. By adding a penalty equivalent to the absolute value of the magnitude of weights.
    
- [x] C. By adding a penalty equivalent to the square of the magnitude of weights, forcing them to be small.
    
- [ ] D. By automatically stopping the training when the validation loss plateaus.
    

> [!success]- Đáp án: C
> 
> **Giải thích:** L2 Regularization (Ridge) cộng thêm một hình phạt bằng bình phương trọng số vào hàm loss, ép các trọng số (weights) của mạng tiến về gần 0, giúp mô hình bớt phức tạp và giảm overfitting.

---

### Multiple Choice Question 3

What is the primary difference between lemmatization and stemming in Natural Language Processing?

- [ ] A. Stemming uses a dictionary to find the root word, while lemmatization simply chops off the ends of words.
    
- [x] B. Lemmatization considers the context and converts the word to its meaningful base form, whereas stemming uses crude heuristic rules that may result in non-words.
    
- [ ] C. Stemming is strictly used for Chinese characters, while lemmatization is used for Latin-based languages.
    
- [ ] D. There is no difference; they are interchangeable terms in TensorFlow.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Lemmatization dùng từ điển và ngữ cảnh để đưa từ về dạng nguyên bản có nghĩa (ví dụ: better -> good). Stemming chỉ cắt bỏ hậu tố một cách máy móc (ví dụ: caring -> car) và có thể tạo ra từ vô nghĩa.

---

### Multiple Choice Question 4

When compiling a Keras model where your target labels are provided as integers (e.g., 0, 1, 2 for three classes), which loss function MUST you use?

- [ ] A. categorical_crossentropy
    
- [ ] B. binary_crossentropy
    
- [ ] C. mean_squared_error
    
- [x] D. sparse_categorical_crossentropy
    

> [!success]- Đáp án: D
> 
> **Giải thích:** Khi nhãn (labels) là các số nguyên (0, 1, 2...), ta phải dùng sparse_categorical_crossentropy. Nếu nhãn đã được one-hot encode (vd: [0, 0, 1]), ta mới dùng categorical_crossentropy.

---

### Multiple Choice Question 5

In time series forecasting, how can an upward or downward trend be addressed before applying a stationary statistical model?

- [ ] A. By applying a Word2Vec embedding.
    
- [x] B. By differencing the data (subtracting the previous observation from the current observation).
    
- [ ] C. By duplicating the dataset to increase volume.
    
- [ ] D. By applying a Softmax activation to the input window.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Differencing (Lấy sai phân) là kỹ thuật trừ giá trị hiện tại cho giá trị trước đó để loại bỏ xu hướng (trend), giúp chuỗi thời gian trở nên dừng (stationary) trước khi đưa vào mô hình thống kê.

---

### Multiple Choice Question 6

Which TensorFlow callback is specifically designed to halt the training process if the validation metric stops improving for a specified number of epochs?

- [ ] A. ReduceLROnPlateau
    
- [ ] B. ModelCheckpoint
    
- [ ] C. EarlyStopping
    
- [ ] D. TensorBoard
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Callback EarlyStopping theo dõi một metric (thường là val_loss) và sẽ tự động dừng quá trình train nếu metric đó không cải thiện sau một số epoch (tham số patience).

---

### Multiple Choice Question 7

What is the expected default input image resolution for the pre-trained VGG16 model in tf.keras.applications?

- [ ] A. 128x128
    
- [ ] B. 224x224
    
- [ ] C. 256x256
    
- [ ] D. 299x299
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Các mô hình kinh điển như VGG16, ResNet50 huấn luyện trên ImageNet đều mặc định nhận ảnh đầu vào có kích thước 224x224 pixel.

---

### Multiple Choice Question 8

When evaluating a model's learning curve, what does a consistently decreasing training loss accompanied by a sharply increasing validation loss strongly indicate?

- [ ] A. The model is underfitting.
    
- [ ] B. The learning rate is too small.
    
- [ ] C. The model is overfitting the training data.
    
- [ ] D. The model has perfectly converged.
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Loss trên tập train giảm nhưng loss trên tập validation tăng mạnh là dấu hiệu kinh điển của Overfitting (Mô hình học thuộc lòng dữ liệu train nhưng mất khả năng dự đoán trên dữ liệu mới).

---

### Multiple Choice Question 9

In the context of the tf.data API, what is the primary purpose of the shuffle(buffer_size) method?

- [ ] A. It changes the labels randomly to introduce noise.
    
- [ ] B. It fills a buffer with elements, randomly samples from it, and replaces the sampled elements with new ones to ensure independent and identically distributed batches.
    
- [ ] C. It reorganizes the dimensions of the input tensors.
    
- [ ] D. It repeats the dataset indefinitely.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** dataset.shuffle(buffer_size) tải trước một số lượng mẫu bằng buffer_size vào bộ nhớ, xáo trộn chúng, sau đó bốc ngẫu nhiên ra để tạo batch. Điều này đảm bảo tính ngẫu nhiên, rất quan trọng khi train Deep Learning.

---

### Multiple Choice Question 10

What is a key advantage of using subword tokenization algorithms like Byte-Pair Encoding (BPE) or WordPiece over standard word-level tokenization?

- [ ] A. They entirely eliminate the need for embedding layers.
    
- [ ] B. They process text faster by ignoring punctuation.
    
- [ ] C. They handle Out-Of-Vocabulary (OOV) words more effectively by breaking rare words into known subwords.
    
- [ ] D. They automatically translate text into multiple languages.
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Các thuật toán BPE hay WordPiece chia từ chưa biết (Out-Of-Vocabulary) thành các mảnh nhỏ hơn đã biết (subwords) thay vì gán nhãn `<UNK>`, giúp mô hình hiểu được cấu trúc từ mới.

### Multiple Choice Question 11

When using the pad_sequences utility in Keras to standardize sequence lengths, what is the default behavior if a sequence is longer than the specified maxlen?

- [ ]A. It raises an OutOfMemory error

- [ ] B. It truncates the sequence from the beginning (pre-truncating).
    
- [ ] C. It truncates the sequence from the end (post-truncating).
    
- [ ] D. It automatically increases the maxlen to fit the longest sequence.


> [!success]- Đáp án: B
>
> **Giải thích:** Theo mặc định của Keras pad_sequences, nếu chuỗi dài hơn maxlen, nó sẽ cắt bỏ các từ ở đầu chuỗi (pre-truncating).


---

### Multiple Choice Question 12

Given a 2D grayscale image tensor t of shape (28, 28), which TensorFlow operation correctly adds a channel dimension to make its shape (28, 28, 1)?

- [ ] A. tf.squeeze(t, axis=-1)
    
- [ ] B. tf.expand_dims(t, axis=-1)
    
- [ ] C. tf.concat(t, axis=1)
    
- [ ] D. tf.flatten(t)
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Hàm tf.expand_dims(t, axis=-1) sẽ thêm một chiều (dimension) vào cuối tensor, biến (28, 28) thành (28, 28, 1).

---

### Multiple Choice Question 13

When configuring data augmentation, what is the effect of the zoom_range=0.2 parameter?

- [ ] A. It changes the resolution of the image by exactly 20%.
    
- [ ] B. It randomly zooms inside the image by a factor between 0.8 and 1.2 during training.
    
- [ ] C. It crops the outer 20% of the image permanently.
    
- [ ] D. It moves the camera 20% closer to the object in 3D space.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** zoom_range=0.2 trong ImageDataGenerator sẽ thực hiện phóng to hoặc thu nhỏ bức ảnh một cách ngẫu nhiên trong khoảng [1 - 0.2, 1 + 0.2] tức là [0.8, 1.2].

---

### Multiple Choice Question 14

Why is it common practice to apply tf.keras.applications.resnet50.preprocess_input before feeding images to a ResNet50 model?

- [ ] A. To convert the images to text arrays.
    
- [ ] B. To center the pixel values around zero and scale them according to the specific way the original ResNet50 model was trained.
    
- [ ] C. To aggressively compress the image to save RAM.
    
- [ ] D. To automatically label the images if they are unannotated.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Hàm preprocess_input của ResNet50 sẽ chuẩn hóa ảnh đầu vào theo đúng chuẩn (thường là trừ đi mean RGB của ImageNet) giống hệt cách mô hình gốc đã được train, giúp transfer learning hiệu quả.

---

### Multiple Choice Question 15

Which statistical test is commonly employed to quantitatively determine if a time series dataset is stationary?

- [ ] A. Student's t-test
    
- [ ] B. Chi-square test
    
- [ ] C. Augmented Dickey-Fuller (ADF) test
    
- [ ] D. ANOVA
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Kiểm định Augmented Dickey-Fuller (ADF) là công cụ thống kê phổ biến nhất để kiểm tra tính dừng (stationarity) của chuỗi thời gian.

---

### Multiple Choice Question 16

What is the difference between padding='valid' and padding='same' in a Conv2D layer?

- [ ] A. 'valid' means no padding is applied, causing the output spatial dimensions to shrink; 'same' adds zeros so the output has the same spatial dimensions as the input.
    
- [ ] B. 'valid' pads with ones; 'same' pads with zeros.
    
- [ ] C. 'valid' ensures all pixels are between 0 and 1; 'same' ensures all images are the same size.
    
- [ ] D. There is no difference; they are aliases for the same operation.
    

> [!success]- Đáp án: A
> 
> **Giải thích:** 'Valid' tức là không làm gì cả, ảnh qua convolution sẽ bị nhỏ lại. 'Same' sẽ thêm các viền số 0 (zero-padding) xung quanh ảnh để output đầu ra giữ nguyên kích thước so với input.

---

### Multiple Choice Question 17

Which type of plot is most effective for visualizing the autocorrelation of a time series at various lags?

- [ ] A. Scatter plot
    
- [ ] B. Histogram
    
- [ ] C. Correlogram (ACF plot)
    
- [ ] D. Pie chart
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Biểu đồ ACF (Autocorrelation Function) vẽ hệ số tương quan của chuỗi thời gian với chính nó tại các độ trễ (lags) khác nhau.

---

### Multiple Choice Question 18

Which of the following code snippets correctly sets up an Adam optimizer with a custom learning rate of 0.001?

- [ ] A. optimizer = tf.keras.optimizers.Adam(lr=0.001)
    
- [ ] B. optimizer = tf.keras.optimizers.Adam(learning_rate=0.001)
    
- [ ] C. optimizer = 'adam(0.001)'
    
- [ ] D. optimizer = tf.train.Adam(0.001)
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Syntax hiện tại chuẩn nhất của Keras là tf.keras.optimizers.Adam(learning_rate=0.001). (Ở các bản TF cũ có thể dùng lr nhưng learning_rate là chuẩn mực hiện đại).

---

### Multiple Choice Question 19

What hardware accelerator, freely available in Google Colab, is specifically designed by Google for high-speed tensor operations and neural network training?

- [ ] A. CPU
    
- [ ] B. GPU
    
- [ ] C. TPU
    
- [ ] D. FPGA
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Tensor Processing Unit (TPU) là phần cứng chuyên dụng do Google phát triển để tăng tốc cực nhanh các phép toán ma trận của Deep Learning.

---

### Multiple Choice Question 20

What is the result of multiplying a matrix of shape (3, 4) by a matrix of shape (4, 2) using tf.matmul in TensorFlow?

- [ ] A. A matrix of shape (3, 2)
    
- [ ] B. A matrix of shape (4, 4)
    
- [ ] C. A vector of length 12
    
- [ ] D. An error will be thrown due to shape mismatch
    

> [!success]- Đáp án: A
> 
> **Giải thích:** Phép nhân ma trận (3, 4) x (4, 2) theo quy tắc đại số tuyến tính sẽ tạo ra một ma trận kết quả (3, 2).

---

### Multiple Choice Question 21

In tf.keras.preprocessing.text.Tokenizer, what is the function of the oov_token parameter?

- [ ] A. It defines a specific string to replace words that were not seen during the fit_on_texts phase, ensuring the sequence length is maintained.
    
- [ ] B. It automatically deletes out-of-vocabulary words.
    
- [ ] C. It triggers a web search to find the meaning of unknown words.
    
- [ ] D. It stands for "Only One Value" and forces the tokenizer to use a vocabulary size of 1.
    

> [!success]- Đáp án: A
> 
> **Giải thích:** Tham số oov_token=`<OOV>` đảm bảo những từ không có trong từ điển lúc train sẽ được thay bằng token này thay vì bị bỏ qua hoàn toàn, giúp giữ nguyên cấu trúc độ dài câu.

---

### Multiple Choice Question 22

If a dataset contains images of cars taken strictly during sunny days, which data augmentation technique would best help the model generalize to cloudy or night-time images?

- [ ] A. Random horizontal flipping
    
- [ ] B. Random brightness and contrast adjustments
    
- [ ] C. Random rotation by 90 degrees
    
- [ ] D. Random zooming
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Để ảnh chụp ban ngày có thể generalize (tổng quát hóa) ra điều kiện ban đêm hay nhiều mây, việc thay đổi ngẫu nhiên độ sáng (brightness) là Data Augmentation hợp lý nhất.

---

### Multiple Choice Question 23

In the context of sequence-to-sequence models and time series forecasting, what does the "horizon" refer to?

- [ ] A. The number of historical data points used as input.
    
- [ ] B. The number of future time steps the model is trained to predict.
    
- [ ] C. The horizontal axis of the loss graph.
    
- [ ] D. The baseline accuracy of the model.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** "Horizon" (Đường chân trời dự báo) là số lượng bước thời gian (time steps) trong tương lai mà mô hình cần phải dự báo.

---

### Multiple Choice Question 24

What is the primary function of a MaxPooling2D layer in a Convolutional Neural Network?

- [ ] A. To increase the number of channels/filters in the feature map.
    
- [ ] B. To reduce the spatial dimensions (width and height) of the feature map, thereby reducing parameters and computation while achieving translation invariance.
    
- [ ] C. To add padding to the image.
    
- [ ] D. To convert a 2D matrix into a 1D vector for the Dense layer.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** MaxPooling làm giảm kích thước chiều rộng/chiều cao của ảnh (downsampling), giữ lại những đặc trưng nổi bật nhất, từ đó giảm số lượng tính toán và chống nhiễu (translation invariance).

---

### Multiple Choice Question 25

In Transfer Learning, what does the term "fine-tuning" specifically refer to?

- [ ] A. Resizing the input images to match the base model.
    
- [ ] B. Unfreezing a few of the top layers of a frozen pre-trained base model and jointly training both the newly added classifier and these top layers at a very low learning rate.
    
- [ ] C. Adjusting the brightness of the training images.
    
- [ ] D. Deleting the pre-trained weights and training the entire architecture from scratch.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Fine-tuning không chỉ là trích xuất đặc trưng (feature extraction) mà còn là mở khóa (unfreeze) một vài layer cuối của model gốc và train lại chúng với learning rate cực nhỏ.

---

### Multiple Choice Question 26

Which hyperparameter is crucial to tune when deciding how far back in time an LSTM layer should look to make a prediction?

- [ ] A. Number of filters
    
- [ ] B. Pool size
    
- [ ] C. Window size (or time steps)
    
- [ ] D. Embedding dimension
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Window size (hay sequence length / look-back) xác định mô hình LSTM sẽ nhìn lại bao nhiêu bước thời gian trong quá khứ để đưa ra dự báo.

---

### Multiple Choice Question 27

What does the texts_to_sequences method of the Keras Tokenizer class return?

- [ ] A. A single string of concatenated words.
    
- [ ] B. A list of lists, where each inner list contains integers corresponding to the tokens in the original texts.
    
- [ ] C. A one-hot encoded 3D matrix.
    
- [ ] D. A dictionary mapping words to their frequency.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Method texts_to_sequences sẽ chuyển một danh sách các câu (string) thành một danh sách các mảng số nguyên, mỗi số tương ứng với index của từ trong từ điển.

---

### Multiple Choice Question 28

In an imbalanced dataset where detecting the minority class is critical (e.g., fraud detection), which evaluation metric is generally more informative than plain accuracy?

- [ ] A. Mean Absolute Error (MAE)
    
- [ ] B. Area Under the Precision-Recall Curve (AUC-PR) or F1-Score
    
- [ ] C. R-squared
    
- [ ] D. Cross-entropy loss
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Với tập dữ liệu mất cân bằng nghiêm trọng (imbalanced data), Accuracy là vô nghĩa (ví dụ đoán toàn bộ là "không lừa đảo" vẫn đúng 99%). F1-Score hoặc AUC-PR đánh giá chính xác hơn khả năng bắt được thiểu số.

---

### Multiple Choice Question 29

During training, if the loss function oscillates wildly (spiking up and down) instead of smoothly converging, what is the most likely cause?

- [ ] A. The learning rate is set too high.
    
- [ ] B. The batch size is exactly equal to the dataset size.
    
- [ ] C. The model has too few layers.
    
- [ ] D. The activation function is ReLU.
    

> [!success]- Đáp án: A
> 
> **Giải thích:** Khi loss function nhảy lên nhảy xuống liên tục (dao động mạnh), nguyên nhân chính thường do Learning Rate quá lớn khiến model bước qua điểm cực tiểu.

---

### Multiple Choice Question 30

When decomposing a time series, what does the "residual" (or noise) component represent?

- [ ] A. The long-term progression of the series.
    
- [ ] B. The repeating short-term cycle.
    
- [ ] C. The random, unpredictable variations left after extracting the trend and seasonality.
    
- [ ] D. The average value of the entire dataset.
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Trong phân rã chuỗi thời gian (Decomposition), thành phần Residual/Noise chứa các yếu tố nhiễu ngẫu nhiên còn sót lại sau khi đã tách Trend (xu hướng) và Seasonality (mùa vụ).

---

### Multiple Choice Question 31

Which of the following is a prominent challenge specifically associated with sentiment analysis in Natural Language Processing?

- [ ] A. Identifying nouns and verbs
    
- [ ] B. Detecting sarcasm and irony where positive words are used in a negative context
    
- [ ] C. Converting text to lowercase
    
- [ ] D. Removing white spaces
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Phát hiện châm biếm (Sarcasm) là thử thách cực lớn trong NLP vì ngôn từ mang nghĩa tích cực (ví dụ "Tuyệt vời quá nhỉ") nhưng lại ngụ ý tiêu cực.

---

### Multiple Choice Question 32

What is a common architectural strategy to reduce the complexity of a deep neural network to prevent overfitting?

- [ ] A. Using a smaller batch size.
    
- [ ] B. Increasing the number of epochs.
    
- [ ] C. Decreasing the number of hidden layers or the number of neurons per layer.
    
- [ ] D. Using one-hot encoding for all inputs.
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Để giảm độ phức tạp của model (giảm overfit), cách tiếp cận trực tiếp là làm mạng neural "nông" hơn hoặc "nhỏ" hơn bằng cách giảm số layer/số neuron.

---

### Multiple Choice Question 33

How does Dropout act as a form of regularization during the training of a neural network?

- [ ] A. It drops the learning rate when loss plateaus.
    
- [ ] B. It ignores misclassified examples.
    
- [ ] C. It randomly deactivates a fraction of neurons in a layer during each training step, preventing complex co-adaptations and forcing the network to learn robust features.
    
- [ ] D. It completely removes the validation set to focus only on training data.
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Dropout tắt ngẫu nhiên một phần các neuron trong quá trình train. Điều này ép các neuron còn lại phải tự học các đặc trưng mạnh mẽ thay vì dựa dẫm vào một vài neuron cụ thể.

---

### Multiple Choice Question 34

Why are Transformer architectures (like BERT or GPT) increasingly preferred over RNNs/LSTMs for long-sequence NLP tasks?

- [ ] A. Transformers process sequences strictly one word at a time, making them easier to debug.
    
- [ ] B. Transformers rely heavily on the vanishing gradient problem to filter out noise.
    
- [ ] C. Transformers use self-attention to process entire sequences in parallel, allowing for faster training and better capture of long-range dependencies.
    
- [ ] D. Transformers do not require any embeddings.
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Transformer dùng cơ chế Self-attention có khả năng xem xét toàn bộ các từ trong câu cùng lúc (parallel), vượt trội hơn RNN vốn phải đọc từng từ tuần tự và dễ bị quên chuỗi dài.

---

### Multiple Choice Question 35

How does tf.keras.utils.image_dataset_from_directory primarily differ from the older ImageDataGenerator.flow_from_directory?

- [ ] A. It cannot read images from subfolders.
    
- [ ] B. It returns a tf.data.Dataset object, which is highly optimized for performance, prefetching, and multi-threading compared to Python generators.
    
- [ ] C. It only supports grayscale images.
    
- [ ] D. It strictly requires the labels to be provided in a separate CSV file.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** image_dataset_from_directory là API mới của Keras, trả về đối tượng tf.data.Dataset hiện đại, tự động tối ưu hóa luồng I/O đa luồng, nhanh hơn nhiều so với ImageDataGenerator cũ.

---

### Multiple Choice Question 36

In an ARIMA(p,d,q) model for time series forecasting, what does the 'p' parameter represent?

- [ ] A. The order of differencing required to make the series stationary.
    
- [ ] B. The order of the moving average (MA) component.
    
- [ ] C. The order of the auto-regressive (AR) component, indicating the number of lag observations included.
    
- [ ] D. The period of the seasonality.
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Trong cấu trúc ARIMA(p,d,q), chữ 'p' đại diện cho Auto-Regressive (bậc tự hồi quy), chỉ định số lượng các giá trị trễ (lag) trong quá khứ được đưa vào mô hình.

---

### Multiple Choice Question 37

When instantiating a pre-trained base model like ResNet50 for transfer learning on a new dataset, why do we set include_top=False?

- [ ] A. To prevent the model from using the GPU.
    
- [ ] B. To exclude the final fully connected classification layers that were specific to the original ImageNet classes (e.g., 1000 categories).
    
- [ ] C. To remove the input layer.
    
- [ ] D. To disable all convolutional filters.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Lớp 'top' của ResNet50 là lớp Dense gồm 1000 nơ-ron để phân loại 1000 class của ImageNet. Khi dùng cho dữ liệu mới, ta phải bỏ lớp này (include_top=False) để thêm lớp phân loại của riêng ta.

---

### Multiple Choice Question 38

What is a major advantage of using dense, pre-trained word embeddings (like Word2Vec or GloVe) over sparse one-hot encoding?

- [ ] A. Dense embeddings take up infinitely more memory.
    
- [ ] B. Dense embeddings represent words as continuous vectors where semantic relationships and similarities between words are captured geometrically.
    
- [ ] C. Dense embeddings guarantee 100% accuracy in translation tasks.
    
- [ ] D. Dense embeddings represent every word as a single integer, saving space.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Dense embeddings (vector dày đặc) nhóm các từ có ý nghĩa tương đồng lại gần nhau trong không gian vector đa chiều, ưu việt hơn hẳn One-hot encoding thô sơ.

---

### Multiple Choice Question 39

What is the purpose of the save_best_only=True parameter in the ModelCheckpoint callback?

- [ ] A. It saves the code of the best layer.
    
- [ ] B. It ensures that the model weights are only saved to disk if the monitored metric (e.g., val_loss) has improved compared to the previous best epoch.
    
- [ ] C. It saves the dataset that produced the best results.
    
- [ ] D. It stops training as soon as the best accuracy is reached.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** save_best_only=True sẽ so sánh metric hiện tại với epoch tốt nhất trước đó. Nó chỉ ghi đè file model nếu mô hình thực sự học tốt hơn, giúp bạn luôn giữ được phiên bản model "đỉnh" nhất.

---

### Multiple Choice Question 40

When preparing images for a neural network, why might an engineer choose to convert RGB images to Grayscale?

- [ ] A. Grayscale images always contain more detailed information than RGB images.
    
- [ ] B. To reduce the input dimensionality and computational load when color is not a distinguishing feature for the classification task.
    
- [ ] C. Because CNNs cannot technically process tensors with 3 color channels.
    
- [ ] D. To automatically increase the resolution of the image.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Nếu bài toán không phụ thuộc vào màu sắc (vd: nhận diện chữ viết tay MNIST), chuyển sang ảnh Xám (Grayscale - 1 channel) giúp giảm 3 lần khối lượng tính toán so với RGB (3 channels).

---

### Multiple Choice Question 41

What specific problem does the Long Short-Term Memory (LSTM) architecture aim to solve compared to vanilla Recurrent Neural Networks (RNNs)?

- [ ] A. The inability to process text data.
    
- [ ] B. The vanishing gradient problem, which makes it difficult for standard RNNs to learn long-term dependencies in a sequence.
    
- [ ] C. The high memory consumption of Convolutional Neural Networks.
    
- [ ] D. The lack of a Softmax output layer.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** LSTM sinh ra với cấu trúc các "cổng" (gates) đặc biệt để giải quyết bài toán "Tiêu biến đạo hàm" (Vanishing gradient) - căn bệnh khiến RNN truyền thống không thể nhớ được dữ liệu ở xa.

---

### Multiple Choice Question 42

What is the effect of calling the .batch(32) method on a tf.data.Dataset object?

- [ ] A. It limits the entire dataset to only 32 elements.
    
- [ ] B. It trains the model for 32 epochs.
    
- [ ] C. It groups 32 consecutive elements of the dataset into a single batch tensor for parallel processing by the model.
    
- [ ] D. It shuffles the data using a seed of 32.
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Hàm .batch(32) sẽ gom 32 mẫu dữ liệu đơn lẻ lại thành một khối (tensor) duy nhất để đưa qua mạng nơ-ron trong 1 step.

---

### Multiple Choice Question 43

In the context of the bias-variance tradeoff, a model that is heavily underfitting the training data and failing to capture underlying patterns is said to have:

- [ ] A. High variance and low bias
    
- [ ] B. High bias and low variance
    
- [ ] C. Low bias and low variance
    
- [ ] D. High bias and high variance
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Underfitting xảy ra khi mô hình quá đơn giản, không học được quy luật. Trong thống kê, đây gọi là độ lệch cao (High Bias).

---

### Multiple Choice Question 44

While standard CNNs (like ResNet or MobileNet) are used primarily for image classification, which of the following architectures is designed specifically for Object Detection tasks (finding bounding boxes)?

- [ ] A. YOLO (You Only Look Once)
    
- [ ] B. LSTM
    
- [ ] C. Word2Vec
    
- [ ] D. ARIMA
    

> [!success]- Đáp án: A
> 
> **Giải thích:** YOLO là mạng nơ-ron cực kỳ nổi tiếng dành riêng cho việc vẽ bounding boxes và phân loại nhiều vật thể trong cùng một bức ảnh (Object Detection).

---

### Multiple Choice Question 45

In sequence-to-sequence translation models, what is the core mechanism of "Attention"?

- [ ] A. It sounds an alarm if the loss goes up.
    
- [ ] B. It forces the user to look at the screen during training.
    
- [ ] C. It allows the decoder to assign different weights (focus) to different parts of the input sequence for every single output step it generates.
    
- [ ] D. It acts as a dropout layer for recurrent units.
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Cơ chế Attention giúp mô hình khi sinh ra một từ ở đầu ra (decoder) có thể "liếc nhìn" và gán trọng số cao cho những từ quan trọng tương ứng ở chuỗi đầu vào.

---

### Multiple Choice Question 46

Which of the following data types is NOT a valid tf.DType in TensorFlow?

- [ ] A. tf.string
    
- [ ] B. tf.float32
    
- [ ] C. tf.array
    
- [ ] D. tf.int64
    

> [!success]- Đáp án: C
> 
> **Giải thích:** tf.float32, tf.string, tf.int64 đều là các dtype chuẩn của TensorFlow. tf.array không tồn tại (TensorFlow dùng khái niệm Tensor).

---

### Multiple Choice Question 47

In Computer Vision tasks like Image Segmentation, which evaluation metric is predominantly used to measure the overlap between the predicted mask and the ground truth mask?

- [ ] A. Mean Squared Error (MSE)
    
- [ ] B. Intersection over Union (IoU)
    
- [ ] C. Silhouette Score
    
- [ ] D. Bleu Score
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Intersection over Union (IoU) là tỷ lệ diện tích phần giao (đoán đúng) chia cho phần hợp, là metric tiêu chuẩn nhất để đo lường độ chính xác của bài toán Image Segmentation.

---

### Multiple Choice Question 48

What is a known limitation of the tf.keras.Sequential API when compared to the tf.keras.Model (Functional) API?

- [ ] A. The Sequential API cannot contain Dense layers.
    
- [ ] B. The Sequential API cannot handle models that require multiple distinct inputs or multiple distinct outputs.
    
- [ ] C. The Sequential API cannot be compiled.
    
- [ ] D. The Sequential API cannot be run on a GPU.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Sequential API rất dễ dùng nhưng chỉ cho phép xây dựng cấu trúc đường thẳng (1 đầu vào, 1 đầu ra). Để làm mạng phân nhánh phức tạp, phải dùng Functional API.

---

### Multiple Choice Question 49

In text preprocessing, what are "stop words"?

- [ ] A. Words that cause the training to stop.
    
- [x] B. Common words (like 'the', 'is', 'in') that appear frequently but carry little unique semantic meaning, often removed to reduce vocabulary size.
    
- [ ] C. Punctuation marks exclusively.
    
- [ ] D. Words that represent negative sentiment.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Stop words (Từ dừng) là những từ cực kỳ phổ biến (ví dụ tiếng Việt có: "thì", "là", "mà") nhưng không mang lại nhiều giá trị phân loại nội dung, nên thường bị xóa để tối ưu tốc độ.

---

### Multiple Choice Question 50

What is the purpose of applying a Moving Average to time series data during exploratory data analysis?

- [ ] A. To convert the data into categorical labels.
    
- [x] B. To smooth out short-term fluctuations and noise, helping to highlight longer-term underlying trends.
    
- [ ] C. To increase the variance of the dataset.
    
- [ ] D. To automatically generate a recurrent neural network.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Đường trung bình động (Moving Average) làm "mượt" các dao động lên xuống giật cục liên tục, giúp chuyên gia nhìn rõ được xu hướng tổng thể của chuỗi thời gian.

---

### Multiple Choice Question 51

What is the primary purpose of the Flatten() layer in a standard Convolutional Neural Network pipeline?

- [x] A. To convert 2D or 3D feature maps into a 1D vector so they can be fed into standard Fully Connected (Dense) layers.
    
- [ ] B. To reduce the number of channels to 1.
    
- [ ] C. To normalize the pixel values to be between 0 and 1.
    
- [ ] D. To compress the image into a JPEG format.
    

> [!success]- Đáp án: A
> 
> **Giải thích:** Sau khi trích xuất đặc trưng bằng Convolution (ra ma trận 2D/3D), ta phải dùng Flatten để duỗi thẳng nó thành mảng 1D, vì lớp Dense (Fully Connected) chỉ nhận đầu vào 1 chiều.

---

### Multiple Choice Question 52

Why is k-fold cross-validation typically preferred over a single train/test split when evaluating a model on a relatively small dataset?

- [ ] A. It trains the model k times faster.
    
- [ ] B. It provides a more robust and reliable estimate of model performance by ensuring every data point has a chance to be in the validation set, reducing evaluation variance.
    
- [ ] C. It automatically tunes hyperparameters without human intervention.
    
- [ ] D. It guarantees that the model will not overfit.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** K-fold cross validation chia nhỏ tập dữ liệu ra train/test nhiều lần luân phiên. Nó giúp đánh giá độ chính xác đáng tin cậy hơn trên dữ liệu nhỏ so với việc chỉ cắt tập train/test 1 lần ngẫu nhiên.

---

### Multiple Choice Question 53

When building a text generator, why is the CategoricalCrossentropy loss function often used over MeanSquaredError?

- [ ] A. Because text generation is inherently a regression problem.
    
- [ ] B. Because predicting the next word is treated as a multi-class classification problem across the entire vocabulary.
    
- [ ] C. Because MeanSquaredError cannot be calculated on GPUs.
    
- [ ] D. Because CategoricalCrossentropy automatically tokenizes the words.
    

> [!success]- Đáp án: B
> 
> **Giải thích:** Bài toán sinh chữ (Text Generation) thực chất là đoán "từ tiếp theo" từ một bộ từ vựng (ví dụ có 10,000 từ). Đây là bài toán phân loại đa lớp quy mô lớn, do đó phải dùng CategoricalCrossentropy.

---

### Multiple Choice Question 54

In TensorFlow, if you want to deploy a trained Keras model to a mobile device or a web browser, which ecosystem tool is specifically designed for this?

- [ ] A. TensorFlow Lite / TensorFlow.js
    
- [ ] B. TensorFlow Datasets
    
- [ ] C. TensorBoard
    
- [ ] D. TensorFlow Hub
    

> [!success]- Đáp án: A
> 
> **Giải thích:** TensorFlow Lite được tối ưu để nhúng vào Mobile/IoT, còn TensorFlow.js dùng để chạy thẳng mô hình trên trình duyệt web.

---

### Multiple Choice Question 55

Which of the following techniques is considered a "Data-Centric" approach to improving a deep learning model's performance, rather than a "Model-Centric" approach?

- [ ] A. Changing the activation function from ReLU to Leaky ReLU.
    
- [ ] B. Adding more layers to the neural network.
    
- [ ] C. Carefully cleaning mislabeled data and acquiring more high-quality samples for the minority class.
    
- [ ] D. Switching from Adam optimizer to SGD with momentum.
    

> [!success]- Đáp án: C
> 
> **Giải thích:** Cải thiện chất lượng dữ liệu, làm sạch nhãn sai (Cleaning mislabeled data) là cốt lõi của phong trào "Data-Centric AI", khác biệt so với Model-Centric (chỉ tập trung thay đổi kiến trúc layer, optimizer, loss).



Multiple Choice Question 50

How can you implement a learning rate schedule using callbacks in TensorFlow?

A. By using the ModelCheckpoint callback

B. By using the EarlyStopping callback

C. By using the ReduceLROnPlateau callback

D. Learning rate schedules cannot be implemented with callbacks

Multiple Choice Question 5

What is the purpose of stemming in text processing?

A. Expanding words to their full forms

B. Reducing words to their root or base form

C. Analyzing sentence structure

D. Identifying entities in text

Multiple Choice Question 4

In the context of creating a new model with a pre-trained model in TensorFlow, what is the benefit of transfer learning?

A. It avoids using pre-trained models altogether.

B. It allows the model to ignore the knowledge from the pre-trained model.

C. It transfers knowledge from the pre-trained model to improve performance on a new task.

D. Transfer learning has no impact on model performance.

Multiple Choice Question 3

How can seasonality be addressed in time series analysis?

A. By removing all time-dependent features

B. By using a rolling mean to smooth the data

C. By incorporating dummy variables for each season

D. By applying dimensionality reduction techniques

Multiple Choice Question 2

Which activation has range [0,∞)?

A. Tanh

B. Sigmoid

C. ReLU

D. Softsign

  

Multiple Choice Question 1

How is the softmax activation function typically used in next-word prediction models?

A. To normalize the output probabilities over multiple words

B. To apply non-linearity to the input sequences

C. To control the learning rate during training

D. To calculate the loss function

  

  

  

  

  

  

Query successful

Gemini said

  

Tiếp tục là nội dung văn bản của các câu hỏi tiếp theo mà bạn đã gửi:

  

Multiple Choice Question 11

How does increasing the size of the training dataset contribute to preventing overfitting?

A. It has no impact on overfitting.

B. It increases the risk of overfitting.

C. It helps the model generalize better to new data.

D. It makes the model more prone to memorizing noise.

Multiple Choice Question 10

What does the term "sequence length" refer to in the context of text-to-sequence conversion?

A. The length of each word in a document

B. The number of words in a sentence or document

C. The size of the vocabulary

D. The embedding dimension of the vectors

Multiple Choice Question 9

What is a potential use case for the SplitMergeTokenizer?

A. Tokenizing text into subword units for language modeling

B. Tokenizing multilingual text with different scripts

C. Tokenizing text into individual words based on whitespaces

D. Tokenizing text based on learned subword units for WordPiece models

Multiple Choice Question 8

What does the repeat method do when applied to a TensorFlow dataset?

A. It repeats the dataset multiple times during training.

B. It adds noise to the dataset.

C. It repeats the feature-label pairs within each batch.

D. It reshapes the dataset.

Multiple Choice Question 7

Typical input size for ImageNet-pretrained InceptionV3 is:

A. 224×224

B. 256×256

C. 299×299

D. 331×331

Multiple Choice Question 6

What is a typical representation of training and validation accuracies on a plot?

A. A single line indicating both training and validation accuracies

B. Two separate lines for training and validation accuracies

C. A bar chart comparing training and validation accuracies

D. A scatter plot showing individual data points

  

  

  

  

  

  

Query successful

Gemini said

  

Dưới đây là nội dung văn bản được trích xuất từ các hình ảnh mới mà bạn đã cung cấp:

  

Multiple Choice Question 20

What is the purpose of the Dropout layer in a ConvNet?

A. It drops neurons during training to prevent overfitting.

B. It adjusts the learning rate dynamically.

C. It adds random noise to the input data.

D. It reduces the spatial dimensions of the input.

Multiple Choice Question 19

Which type of padding preserves the spatial dimensions of the input in a convolutional layer?

A. Zero padding

B. Same padding

C. Valid padding

D. Symmetric padding

Multiple Choice Question 18

What is the benefit of using Google Colab for collaborative projects?

A. It restricts access to only one user at a time.

B. It allows real-time collaboration with multiple users on the same notebook.

C. It requires users to download and upload notebooks for sharing.

D. It only supports offline collaboration.

Multiple Choice Question 17

What is the purpose of the SplitMergeTokenizer in TensorFlow?

A. Tokenizing based on whitespace

B. Tokenizing using pre-trained models from TensorFlow Hub

C. Tokenizing using Sentencepiece

D. Tokenizing by splitting and merging text

Multiple Choice Question 16

What is Transfer Learning in the context of Computer Vision and TensorFlow?

A. Copying and pasting code from one project to another

B. Training a model on a specific task and then using it as a starting point for a different but related task

C. Moving data from one storage location to another

D. Adjusting the brightness and contrast of images during preprocessing

Multiple Choice Question 15

When creating a windowed dataset for time series prediction, what does the target window represent?

A. The window before the input window

B. The window after the input window

C. The window at the same time as the input window

D. The entire time series without windowing

Multiple Choice Question 14

Given a training dataset with exclusively left-facing individuals, what strategies can prevent overfitting when classifying right-facing individuals?

A. Use the 'horizontal_flip' parameter

B. Use the 'flip' parameter and set 'horizontal'

C. Use the 'flip_vertical' parameter around the Y axis

D. Use the 'flip' parameter

Multiple Choice Question 13

In a multiclass classification problem, how are categorical labels typically represented in TensorFlow?

A. As strings

B. As integer values

C. Using one-hot encoding

D. Using floating-point numbers

  

  

  

  

  

  

Query successful

Gemini said

  

Dưới đây là nội dung văn bản trích xuất từ loạt hình ảnh cuối cùng bạn đã gửi:

  

Multiple Choice Question 30

How can increasing the amount of training data help prevent overfitting?

A. By making the training process slower

B. By introducing more noise into the model

C. By improving the model's generalization to new data

D. Increasing data size has no effect on overfitting

Multiple Choice Question 29

Which Python library is commonly used for plotting training and validation accuracies in the context of evaluating model performance?

A. NumPy

B. Matplotlib

C. Scikit-learn

D. TensorFlow

Multiple Choice Question 28

How can you compile a sequential model with LSTM layers for classification in TensorFlow?

A. tf.keras.Sequential.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])

B. tf.keras.compile(model, optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])

C. tf.keras.Sequential().compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])

D. tf.keras.model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])(Lưu ý: Trong thực tế thường là model.compile(...) sau khi đã khởi tạo đối tượng model).

Multiple Choice Question 27

How can you visualize time series data effectively?

A. Scatter plots

B. Bar charts

C. Line charts

D. Pie charts

Multiple Choice Question 26

What is padding in the context of machine learning and TensorFlow?

A. A technique to remove unnecessary zeros from a dataset

B. Adding extra data to the input to ensure consistent dimensions

C. The process of smoothing out noisy data

D. Resizing images to a fixed size during preprocessing

Multiple Choice Question 25

What is stationarity in the context of time series data?

A. The absence of temporal patterns

B. The presence of seasonality in the data

C. The constancy of statistical properties over time

D. The rapid changes in the time series

Multiple Choice Question 24

Which method within the Image Generator performs image normalization?

A. rescale

B. normalize_image

C. normalize

D. rescale_image

Multiple Choice Question 23

When exploring the impact of image compression in TensorFlow, what metric is commonly used to measure the trade-off between compression and image quality?

A. Accuracy Score

B. Compression Ratio

C. Signal-to-Noise Ratio (SNR)

D. Learning Rate

Multiple Choice Question 22

What is the purpose of the "ImageDataGenerator" in TensorFlow's Computer Vision applications?

A. Generating random numbers for image pixel values

B. Preprocessing image data for model training

C. Creating animated GIFs from image sequences

D. Designing custom image filters

Multiple Choice Question 21

To reshape a vector v with length 12 into a 3x4 matrix in TensorFlow, which function should be used?

A. tf.reshape(v, (3, 4))

B. tf.resize(v, (3, 4))

C. tf.transform(v, (3, 4))

D. tf.matrixize(v, (3, 4))

  

  

  

  

  

  

Query successful

Gemini said

  

Dưới đây là nội dung văn bản trích xuất từ loạt hình ảnh bạn vừa gửi:

  

Multiple Choice Question 40

What role does the base model play when creating a new model with a pre-trained base in TensorFlow?

A. It serves as the output layer of the new model

B. It replaces the need for custom layers in the new model

C. It initializes the weights of the entire new model

D. It acts as a feature extractor for the new model

Multiple Choice Question 39

What is the result of adding two vectors of the same dimension in TensorFlow?

A. A scalar value

B. A matrix

C. Another vector

D. A higher-dimensional tensor

Multiple Choice Question 38

What happens if the num_words parameter is set in the Tokenizer class?

A. It defines the out-of-vocabulary token.

B. It determines the sequence length.

C. It controls the learning rate during training.

D. It limits the vocabulary size to a specified number of words.

Multiple Choice Question 37

Which of the following is a common transformation applied during image data augmentation?

A. Random rotation

B. Image compression

C. Grayscale conversion

D. Pixel normalization

Multiple Choice Question 36

What is the significance of convergence?

A. The process of getting very close to the correct answer.

B. A dramatic increase in loss.

C. A programming API for AI.

D. An analysis that corresponds too closely or exactly to a particular set of data.

Multiple Choice Question 35

What is the primary challenge in analyzing time series data?

A. Dealing with spatial variations

B. Managing high-dimensional features

C. Accounting for temporal dependencies

D. Handling categorical variables

Multiple Choice Question 34

What is the role of hyperparameter tuning in time series forecasting using machine learning?

A. To select the appropriate lag values

B. To optimize the learning rate of the model

C. To find the best model architecture

D. To identify the optimal time period for analysis

Multiple Choice Question 33

What does the tokenize method of the BertTokenizer return?

A. The original text without tokenization

B. A list of tokens obtained from the text

C. Token indices representing the text

D. A tokenized sequence in a matrix form

Multiple Choice Question 32

What is the purpose of using one-hot encoding for the target variable in a multi-class classification task?

A. To increase model complexity

B. To speed up training

C. To represent categorical labels as numerical vectors

D. One-hot encoding is not applicable for multi-class classification

Multiple Choice Question 31

Which statistical measure is commonly used to decompose a time series into trend, seasonality, and residual components?

A. Mean Absolute Deviation (MAD)

B. Mean Squared Error (MSE)

C. Autocorrelation Function (ACF)

D. Moving Average (MA)

  

  

  

  

  

  

Query successful

Gemini said

  

Dưới đây là nội dung văn bản trích xuất từ các hình ảnh câu hỏi trắc nghiệm mới nhất của bạn:

Multiple Choice Question 50

How can you implement a learning rate schedule using callbacks in TensorFlow?

A. By using the ModelCheckpoint callback

B. By using the EarlyStopping callback

C. By using the ReduceLROnPlateau callback

D. Learning rate schedules cannot be implemented with callbacks

Multiple Choice Question 49

How does reducing the complexity of a model contribute to preventing overfitting?

A. It increases the risk of overfitting.

B. It has no impact on overfitting.

C. It makes the model more prone to memorizing noise.

D. It encourages the model to capture general patterns rather than noise.

Multiple Choice Question 48

What does the F1 Score metric consider when evaluating the performance of a forecasting model?

A. The balance between precision and recall

B. The ratio of true positive predictions to total predicted positives

C. The overall accuracy of the model

D. The correlation between predicted and actual values

Multiple Choice Question 47

What is the goal of sentiment analysis in text understanding?

A. Identifying grammatical errors

B. Extracting meaning from text

C. Determining the emotional tone of the text

D. Summarizing the text content

Multiple Choice Question 46

How can you identify overfitting by examining a model's performance metrics?

A. If the training accuracy is high but the validation accuracy is low.

B. If both training and validation accuracies are high.

C. If the model has a low learning rate.

D. If the number of epochs is too small.

Multiple Choice Question 45

How does the lack of regularization contribute to overfitting in machine learning models?

A. Regularization has no impact on overfitting.

B. Lack of regularization allows the model to fit the training data too closely.

C. Regularization leads to underfitting rather than overfitting.

D. Lack of regularization increases the learning rate.

Multiple Choice Question 44

What does the rescale parameter in ImageDataGenerator do?

A. It resizes images to a specified shape.

B. It normalizes pixel values to a specified range.

C. It rotates images randomly during training.

D. It converts images to grayscale.

Multiple Choice Question 43

Which deep learning architecture is commonly used for predicting the next word in a sequence?

A. Convolutional Neural Network (CNN)

B. Recurrent Neural Network (RNN)

C. Support Vector Machine (SVM)

D. Decision Tree

Multiple Choice Question 42

What is the primary purpose of the ImageDataGenerator in TensorFlow?

A. Generating synthetic images for training

B. Resizing images to a fixed dimension

C. Preprocessing and augmenting image data for model training

D. Loading images from external URLs

Multiple Choice Question 41

How does autocorrelation play a role in time series analysis?

A. It measures the correlation between different time series.

B. It helps identify patterns within a single time series at different lags.

C. It calculates the average correlation across multiple time series.

D. It assesses the correlation between time series and external factors.