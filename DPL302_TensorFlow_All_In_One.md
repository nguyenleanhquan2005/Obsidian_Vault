# 📘 DPL302 – Deep Learning & TensorFlow (Tài liệu ôn thi tổng hợp)

> [!note]
> This is a consolidated file merging previous separate notes to reduce redundancy. No information was removed.

## 📌 Table of Contents
1. [📚 I. Deep Learning – DPL302](#-i-deep-learning--dpl302)
   - [🔁 1. Ôn tập: Binary Classification & Logistic Regression](#-1-ôn-tập-binary-classification--logistic-regression)
   - [📝 2. Tóm tắt lý thuyết](#-2-tóm-tắt-lý-thuyết)
   - [🧪 3. Luyện tập](#-3-luyện-tập)
   - [📋 4. Đề thi cuối kỳ (Final Exam – FE)](#-4-đề-thi-cuối-kỳ-final-exam--fe)
     - [Mạng Nơ-ron Nông và Sâu](#mạng-nơ-ron-nông-và-sâu)
     - [Các khía cạnh thực tế của Học sâu](#các-khía-cạnh-thực-tế-của-học-sâu)
     - [Tối ưu hóa và Tinh chỉnh Siêu tham số](#tối-ưu-hóa-và-tinh-chỉnh-siêu-tham-so)
     - [Mạng Nơ-ron Tích chập (CNN)](#mạng-nơ-ron-tích-chập-cnn)
     - [Các Kiến trúc CNN kinh điển và Kỹ thuật Nâng cao](#các-kiến-trúc-cnn-kinh-điển-và-kỹ-thuật-nâng-cao)
     - [Các ứng dụng CNN Nâng cao](#các-ứng-dụng-cnn-nâng-cao)
     - [Mạng Nơ-ron Hồi quy (RNN)](#mạng-nơ-ron-hồi-quy-rnn)
     - [NLP, Mô hình Chuỗi, Attention và Transformer](#nlp-mô-hình-chuỗi-attention-và-transformer)
     - [Ôn tập bổ sung: Thiết lập Học sâu & Regularization (Coursera)](#ôn-tập-bổ-sung-thiết-lập-học-sâu--regularization-coursera)
     - [Ôn tập bổ sung: Thuật toán Tối ưu hóa & Batch Norm (Coursera)](#ôn-tập-bổ-sung-thuật-toán-tối-ưu-hóa--batch-norm-coursera)
2. [🔥 II. TensorFlow – Câu hỏi & Khái niệm](#-ii-tensorflow--câu-hỏi--khái-niệm)
   - [Masterclass Chuyên sâu](#masterclass-chuyên-sâu)

---

## 📚 I. Deep Learning – DPL302

### 🔁 1. Ôn tập: Binary Classification & Logistic Regression

**Câu 1:** Binary classification is a supervised learning algorithm that classifies input data into how many categories or classes?

- [x] a) One.
    
- [ ] b) Two.
    
- [ ] c) Three or more.
    
- [ ] d) Any number.
    

**Câu 2:** Which of the following is an example of a binary classification problem?

- [x] a) Predicting the price of a house.
    
- [ ] b) Distinguishing cats from dogs in images...
    
- [ ] c) Forecasting demand for retail sales.
    
- [ ] d) Predicting the length of stay for hospital patients.
    

**Câu 3:** Binary classification problems can be solved using which algorithm?

- [ ] a) Linear Regression.
    
- [x] b) Logistic Regression.
    
- [ ] c) K-means clustering.
    
- [ ] d) Principal Component Analysis.
    

**Câu 4:** In binary classification, the output of the algorithm is typically a binary decision, such as:

- [ ] a) A continuous number.
    
- [ ] b) A probability distribution over multiple classes.
    
- [x] c) Yes or no, true or false, 1 or 0.
    
- [ ] d) A ranking of options.
    

**Câu 5:** According to one source, classifying an email as spam or not spam is an example of what type of problem?

- [ ] a) Regression.
    
- [x] b) Binary classification.
    
- [ ] c) Clustering.
    
- [ ] d) Dimensionality reduction.
    

**Câu 6:** Another example of a binary classification problem mentioned is recognizing whether an image contains what?

- [ ] a) A specific object from a large set.
    
- [x] b) A cat or not.
    
- [ ] c) Multiple distinct objects.
    
- [ ] d) A handwritten digit.
    

**Câu 7:** In machine learning terminology, what refers to problems where we are interested only in hard assignments of examples to categories?

- [ ] a) Soft assignments.
    
- [x] b) Regression.
    
- [ ] c) Classification.
    
- [ ] d) Ranking.
    

**Câu 8:** What is the other subtly different problem that machine learning practitioners colloquially overload the word "classification" to describe, besides hard assignments?

- [ ] a) Ranking items.
    
- [ ] b) Predicting continuous values.
    
- [x] c) Making soft assignments, i.e., assessing the probability of each category.
    
- [ ] d) Clustering data points.
    

**Câu 9:** Even when the primary interest is in hard assignments in classification, models that make soft assignments are often used. Why does one source say this distinction tends to get blurred?

- [ ] a) Because soft assignments are always more accurate.
    
- [ ] b) Because hard assignments are computationally cheaper.
    
- [x] c) Because often, even when caring about hard assignments, models making soft assignments are used.
    
- [ ] d) Because the output is always interpreted as a probability.
    

---

### 📝 2. Tóm tắt lý thuyết

**Câu 1:** What is the gradient of a scalar function (f) with respect to a matrix (X)?

- [ ] a) A scalar.
    
- [ ] b) A vector.
    
- [ ] c) A matrix with the same dimensionality as (X).
    
- [ ] d) A tensor of higher order.
    

**Câu 2:** What process relies on the chain rule for transforming random variables and is used in generative models?

- [ ] a) Gradient Descent.
    
- [ ] b) Normalizing flows.
    
- [ ] c) Principal Component Analysis.
    
- [ ] d) K-means clustering.
    

**Câu 3:** In numerical optimization, what is a descent direction?

- [ ] a) A direction in which the function value increases.
    
- [ ] b) A direction in which the function value decreases.
    
- [ ] c) A direction orthogonal to the gradient.
    
- [ ] d) A direction parallel to the Hessian.
    

**Câu 4:** What is the Hessian matrix?

- [ ] a) A vector of first derivatives.
    
- [ ] b) A matrix of second derivatives.
    
- [ ] c) A scalar representing the magnitude of the gradient.
    
- [ ] d) A matrix of input features.
    

**Câu 5:** What is automatic differentiation?

- [ ] a) Manually computing derivatives for all parameters.
    
- [ ] b) Using numerical approximation to estimate derivatives.
    
- [ ] c) Algorithms that compute derivatives automatically.
    
- [ ] d) Ignoring derivatives and using a different optimization method.
    

**Câu 6:** What is the derivative of the Logistic Sigmoid function, according to one source?

- [ ] a) It is always 0.
    
- [ ] b) It is always 1.
    
- [ ] c) It vanishes for large positive and negative arguments.
    
- [ ] d) It is a constant value.
    

**Câu 7:** What are Newton's method and gradient descent methods for?

- [ ] a) Finding analytical solutions to optimization problems.
    
- [ ] b) Numerical optimization.
    
- [ ] c) Generating random data.
    
- [ ] d) Calculating the mean and variance of data.
    

---

### 🧪 3. Luyện tập

**Câu 1:** What activation function is defined as  $\max(a, 0) + \alpha \cdot \min(a, 0)$ ?

- [ ] a) ReLU.
    
- [x] b) Leaky ReLU.
    
- [ ] c) ELU.
    
- [ ] d) Swish.
    

**Câu 2:** What is the main learning objective when studying the basic building blocks of ResNets?

- [ ] a) Training a state-of-the-art neural network for image classification.
    
- [x] b) Implementing the basic building blocks of ResNets in a deep neural network using Keras.
    
- [ ] c) Preprocessing and augmenting data using the Keras Sequential API.
    
- [ ] d) Fine-tuning the final layers of a classifier to improve accuracy.
    

**Câu 3:** Why is it useful to review case studies of neural networks in computer vision research?

- [ ] a) They provide ready-made solutions for all computer vision tasks.
    
- [ ] b) They help create new datasets from a directory.
    
- [x] c) They provide useful insights and ideas for the learner's own work.
    
- [ ] d) They allow for fine-tuning the final layers of a classifier.
    

**Câu 4:** Which classic neural networks have been successful in computer vision and are used as models or starting points?

- [ ] a) MobileNet, EfficientNet, Transformer.
    
- [x] b) LeNet-5, AlexNet, VGG, ResNet, and Inception.
    
- [ ] c) GANs, Autoencoders, Reinforcement Learning.
    
- [ ] d) Only LeNet-5 and AlexNet.
    

**Câu 5:** What input image size was the LeNet-5 architecture designed to handle?

- [ ] a) 28x28x1.
    
- [x] b) 32x32x1.
    
- [ ] c) 14x14x6.
    
- [ ] d) 10x10x16.
    

**Câu 6:** Who proposed the VGG-16 network in 2014?

- [ ] a) Christian Szegedy at Google.
    
- [ ] b) Andrew G. Howard and colleagues at Google.
    
- [x] c) Karen Simonyan and Andrew Zisserman of the Visual Geometry Group Lab at the University of Oxford.
    
- [ ] d) Mingxing Tan and Quoc V. Le at Google.
    

**Câu 7:** How many total layers does VGG-16 consist of?

- [x] a) 13 convolutional layers and 3 fully connected layers.
    
- [ ] b) 16 layers, including 13 convolutional layers, 5 max-pooling layers, and 3 fully connected layers.
    
- [ ] c) 5 max-pooling layers and 3 fully connected layers.
    
- [ ] d) 13 convolutional layers and 5 max-pooling layers.
    

**Câu 8:** How did VGG-16 perform in the ImageNet Large Scale Visual Recognition Challenge?

- [ ] a) Average performance.
    
- [ ] b) Poor performance.
    
- [x] c) State-of-the-art performance.
    
- [ ] d) Performance only acceptable for simple images.
    

**Câu 9:** What is the purpose of a 1x1 convolution?

- [ ] a) To increase the spatial dimensions of the input image.
    
- [ ] b) To reduce the number of channels in an input volume.
    
- [ ] c) To apply a non-linear function without changing dimensions.
    
- [x] d) Both b and c.
    

**Câu 10:** Is the 1x1 convolution operation non-linear?

- [ ] a) Yes, and this allows it to learn a more complex function of the input volume.
    
- [x] b) No, it is just a linear transformation.
    
- [ ] c) Only when used in an Inception network.
    
- [ ] d) It depends on the size of the output channels.
    

**Câu 11:** For what purpose was the MobileNet convolutional neural network architecture designed?

- [ ] a) Efficient processing on mobile devices and embedded systems.
    
- [ ] b) Achieving the highest accuracy on large datasets.
    
- [ ] c) Natural language processing.
    
- [x] d) Real-time object detection on cloud servers.
    

**Câu 12:** What type of convolution does MobileNet use to reduce the number of computations and parameters?

- [ ] a) Normal convolution.
    
- [x] b) Depthwise separable convolutions.
    
- [ ] c) Transposed convolution.
    
- [ ] d) 3D convolution.
    

**Câu 13:** The computational cost of a normal convolution is proportional to which factors?

- [ ] a) The number of parameters of the filter.
    
- [ ] b) The number of filter positions.
    
- [ ] c) The number of filters.
    
- [x] d) All of the above.
    

**Câu 14:** Depthwise separable convolution can be used as a building block for which network architecture?

- [ ] a) LeNet.
    
- [ ] b) VGG.
    
- [x] c) MobileNet.
    
- [ ] d) AlexNet.
    

**Câu 15:** When performing a convolution on an RGB image, what happens with the filters and the output volume?

- [ ] a) Only one filter is used for the entire image.
    
- [x] b) Different filters are used to detect different features in the image, and the outputs of each filter can be stacked to form a 3D volume.
    
- [ ] c) The convolution is only applied to the red channel.
    
- [ ] d) The output volume is always 1x1.
    

**Câu 16:** In a layer of a convolutional neural network, which formula represents the forward propagation?

- [x] a) Z = W * X + b
    
- [ ] b) Z = Wa + b
    
- [ ] c) a = g(X)
    
- [ ] d) a = Z
    

**Câu 17:** If you have 10 filters of size 3x3x3 in one layer of a convolutional neural network, how many parameters does this layer have?

- [ ] a) 27 parameters.
    
- [ ] b) 28 parameters (27 filter parameters + 1 bias).
    
- [x] c) 280 parameters (28 * 10 filters).
    
- [ ] d) 10 parameters.
    

**Câu 18:** What are the main types of layers in a convolutional network?

- [ ] a) Input, Hidden, Output.
    
- [x] b) Convolution, Pooling, Fully connected.
    
- [ ] c) Encoder, Decoder, Attention.
    
- [ ] d) Recurrent, LSTM, GRU.
    

**Câu 19:** What is the main function of the pooling layer in a CNN?

- [ ] a) To increase the size of the representation.
    
- [x] b) To reduce the size of the representation and speed up computation.
    
- [ ] c) To add fully connected layers.
    
- [ ] d) To apply non-linear activation functions.
    

**Câu 20:** What is the advantage of a Pooling layer?

- [ ] a) Reduces data dimensionality and computational cost.
    
- [ ] b) Prevents overfitting.
    
- [ ] c) Helps achieve translation invariance.
    
- [x] d) All of the above.
    

**Câu 21:** What is the disadvantage of a Pooling layer?

- [ ] a) Information loss.
    
- [ ] b) Can cause over-smoothing.
    
- [ ] c) Introduces hyperparameters that need tuning.
    
- [x] d) All of the above.
    

**Câu 22:** What is convolution used to detect in an image?

- [ ] a) Only general features.
    
- [ ] b) Only specific features.
    
- [x] c) Edges in the image.
    
- [ ] d) None of the above.
    

**Câu 23:** What is the goal of Transpose Convolution?

- [ ] a) To reduce the input size.
    
- [x] b) To upsample a small input into a larger output, often used in semantic segmentation.
    
- [ ] c) To only apply a filter on the input regardless of position.
    
- [ ] d) To perform a simple matrix multiplication.
    

**Câu 24:** What is the key feature of One-shot learning in face recognition?

- [ ] a) It requires many images for each new person.
    
- [x] b) It recognizes a person from a single image.
    
- [ ] c) It uses the Euclidean distance function to compare faces.
    
- [ ] d) It does not require retraining the network when adding a new person to the database.
    

**Câu 25:** How do Siamese networks solve the one-shot learning problem in face recognition?

- [ ] a) By learning a direct classification function.
    
- [x] b) By learning a similarity function to measure the difference between images.
    
- [ ] c) By learning a cryptographic hash function.
    
- [ ] d) By learning a set of fully connected layers.
    

**Câu 26:** What loss function is used to define the objective function in a Siamese network?

- [ ] a) Cross-entropy loss.
    
- [ ] b) Mean squared error.
    
- [x] c) Triplet loss.
    
- [ ] d) Softmax loss.
    

---

### 📋 4. Đề thi cuối kỳ (Final Exam – FE)

#### Bài kiểm tra trắc nghiệm: Mạng Nơ-ron Nông và Sâu

**Câu 1:** **Một mạng nơ-ron "nông" (shallow) được định nghĩa là mạng có:**

- [ ] a) Không có lớp ẩn nào.
    
- [x] b) Một lớp ẩn.
    
- [ ] c) Hai lớp ẩn.
    
- [ ] d) Nhiều hơn hai lớp ẩn.
    

**Câu 2:** **Tại sao các lớp ẩn (hidden layers) lại được gọi là "ẩn"?**

- [ ] a) Vì chúng rất khó để lập trình.
    
- [x] b) Vì các giá trị kích hoạt của chúng không được quan sát trực tiếp trong tập dữ liệu.
    
- [ ] c) Vì chúng thực hiện các phép tính bí mật.
    
- [ ] d) Vì chúng luôn sử dụng hàm kích hoạt Sigmoid.
    

**Câu 3:** **Tại sao việc sử dụng các hàm kích hoạt phi tuyến (non-linear) trong các lớp ẩn lại quan trọng?**

- [ ] a) Vì chúng giúp tính toán nhanh hơn.
    
- [x] b) Vì nếu không có chúng, việc xếp chồng nhiều lớp cũng chỉ tương đương với một mô hình tuyến tính duy nhất.
    
- [ ] c) Vì chúng luôn cho ra kết quả trong khoảng [0, 1].
    
- [ ] d) Vì chúng giúp giảm số lượng tham số.
    

**Câu 4:** **Hàm kích hoạt nào thường được coi là lựa chọn mặc định tốt nhất cho các lớp ẩn hiện nay?**

- [ ] a) Sigmoid
    
- [ ] b) Tanh
    
- [x] c) ReLU (Rectified Linear Unit)
    
- [ ] d) Linear
    

**Câu 5:** **Hàm kích hoạt Tanh có ưu điểm gì so với Sigmoid trong các lớp ẩn?**

- [ ] a) Nó tính toán nhanh hơn.
    
- [x] b) Nó cho ra giá trị trung bình của các kích hoạt gần 0, giúp việc học ở lớp sau dễ dàng hơn.
    
- [ ] c) Nó không bao giờ bị bão hòa.
    
- [ ] d) Nó chỉ hoạt động với số nguyên.
    

**Câu 6:** **Nếu đầu vào `z = -5`, đầu ra của hàm ReLU là bao nhiêu?**

- [ ] a) -5
    
- [x] b) 0
    
- [ ] c) 1
    
- [ ] d) 0.01
    

**Câu 7:** **Đạo hàm của hàm ReLU tại `z = 10` là bao nhiêu?**

- [ ] a) 0
    
- [x] b) 1
    
- [ ] c) 10
    
- [ ] d) Không xác định.
    

**Câu 8:** **Mục đích của việc khởi tạo trọng số ngẫu nhiên (Random Initialization) là gì?**

- [ ] a) Để làm cho mô hình chạy nhanh hơn.
    
- [x] b) Để "phá vỡ tính đối xứng" (break symmetry), đảm bảo các nơ-ron trong cùng một lớp học các đặc trưng khác nhau.
    
- [ ] c) Để đảm bảo hàm chi phí luôn giảm.
    
- [ ] d) Để giảm số lượng tham số cần học.
    

**Câu 9:** **Điều gì sẽ xảy ra nếu tất cả các trọng số trong một mạng nơ-ron được khởi tạo bằng 0?**

- [ ] a) Mô hình sẽ hội tụ rất nhanh.
    
- [x] b) Tất cả các nơ-ron trong cùng một lớp sẽ học cùng một đặc trưng, khiến mạng không thể học được gì hữu ích.
    
- [ ] c) Hàm chi phí sẽ ngay lập tức bằng 0.
    
- [ ] d) Mô hình sẽ hoạt động tốt hơn.
    

**Câu 10:** **Trong một mạng nơ-ron 2 lớp (1 lớp ẩn, 1 lớp đầu ra), `a[1]` đại diện cho cái gì?**

- [ ] a) Các đặc trưng đầu vào.
    
- [x] b) Các kích hoạt (đầu ra) của lớp ẩn.
    
- [ ] c) Dự đoán cuối cùng của mạng.
    
- [ ] d) Các trọng số của lớp ẩn.
    

**Câu 11:** **Quá trình tính toán các đạo hàm `dW` và `db` được gọi là gì?**

- [ ] a) Lan truyền xuôi (Forward Propagation)
    
- [ ] b) Khởi tạo ngẫu nhiên (Random Initialization)
    
- [x] c) Lan truyền ngược (Backpropagation)
    
- [ ] d) Vector hóa (Vectorization)
    

**Câu 12:** **Trong công thức `Z[1] = W[1]X + b[1]`, `X` đại diện cho cái gì?**

- [ ] a) Ma trận trọng số.
    
- [x] b) Ma trận chứa tất cả các mẫu dữ liệu đầu vào.
    
- [ ] c) Vector độ lệch.
    
- [ ] d) Ma trận chứa các kích hoạt của lớp ẩn.
    

**Câu 13:** **Đâu là một biến thể của ReLU giúp giải quyết vấn đề "nơ-ron chết" (dying ReLU)?**

- [ ] a) Sigmoid
    
- [ ] b) Tanh
    
- [x] c) Leaky ReLU
    
- [ ] d) Softmax
    

**Câu 14:** **Đạo hàm của hàm Sigmoid `σ(z)` là gì?**

- [ ] a) `σ(z)`
    
- [ ] b) `1 - σ(z)²`
    
- [x] c) `σ(z) * (1 - σ(z))`
    
- [ ] d) `1`
    

**Câu 15:** **Một mạng nơ-ron có lớp đầu vào 10 nơ-ron, lớp ẩn có 5 nơ-ron và lớp đầu ra có 1 nơ-ron. Ma trận trọng số `W[1]` sẽ có kích thước là bao nhiêu?**

- [ ] a) (10, 5)
    
- [x] b) (5, 10)
    
- [ ] c) (5, 1)
    
- [ ] d) (1, 5)
    

**Câu 16:** **Một mạng nơ-ron được coi là "sâu" (deep) khi nào?**

- [ ] a) Khi nó có nhiều hơn 1000 nơ-ron.
    
- [x] b) Khi nó có nhiều hơn một lớp ẩn.
    
- [ ] c) Khi nó sử dụng hàm kích hoạt ReLU.
    
- [ ] d) Khi nó được huấn luyện trên một tập dữ liệu lớn.
    

**Câu 17:** **Lợi ích chính của việc sử dụng các kiến trúc sâu là gì?**

- [ ] a) Chúng luôn chạy nhanh hơn các mạng nông.
    
- [ ] b) Chúng có ít siêu tham số hơn.
    
- [x] c) Chúng có khả năng học các biểu diễn đặc trưng theo cấp bậc (hierarchical features), từ đơn giản đến phức tạp.
    
- [ ] d) Chúng không bao giờ bị overfitting.
    

**Câu 18:** **Trong một mạng nơ-ron sâu `L` lớp, `a[L]` đại diện cho cái gì?**

- [ ] a) Kích hoạt của lớp ẩn đầu tiên.
    
- [ ] b) Kích hoạt của lớp ẩn cuối cùng.
    
- [x] c) Dự đoán cuối cùng của mạng (`ŷ`).
    
- [ ] d) Dữ liệu đầu vào `X`.
    

**Câu 19:** **Trong lan truyền xuôi của một mạng sâu, đầu vào của lớp `l` là gì?**

- [ ] a) Dữ liệu gốc `X`.
    
- [ ] b) Kích hoạt của lớp `l+1` (`a[l+1]`).
    
- [x] c) Kích hoạt của lớp `l-1` (`a[l-1]`).
    
- [ ] d) Trọng số của lớp `l` (`W[l]`).
    

**Câu 20:** **Đâu là một ví dụ về "siêu tham số" (hyperparameter)?**

- [ ] a) Trọng số `W`.
    
- [ ] b) Độ lệch `b`.
    
- [x] c) Tốc độ học `α`.
    
- [ ] d) Kích hoạt `a`.
    

**Câu 21:** **Sự khác biệt chính giữa "tham số" (parameters) và "siêu tham số" (hyperparameters) là gì?**

- [x] a) Tham số được học từ dữ liệu, siêu tham số được người dùng thiết lập trước.
    
- [ ] b) Siêu tham số được học từ dữ liệu, tham số được người dùng thiết lập trước.
    
- [ ] c) Không có sự khác biệt.
    
- [ ] d) Tham số chỉ có trong mạng nông, siêu tham số chỉ có trong mạng sâu.
    

**Câu 22:** **Trong một mạng có `L=4` lớp, ma trận trọng số `W[3]` sẽ kết nối giữa hai lớp nào?**

- [x] a) Lớp 2 và lớp 3.
    
- [ ] b) Lớp 3 và lớp 4.
    
- [ ] c) Lớp 1 và lớp 2.
    
- [ ] d) Lớp 3 và lớp đầu vào.
    

**Câu 23:** **Tại sao việc kiểm tra kích thước của các ma trận (`W`, `b`, `Z`, `A`) lại là một công cụ gỡ lỗi hữu ích?**

- [ ] a) Vì nó giúp mô hình hội tụ nhanh hơn.
    
- [x] b) Vì nó đảm bảo các phép toán nhân ma trận được thực hiện đúng cách và giúp phát hiện lỗi trong quá trình lập trình.
    
- [ ] c) Vì nó giúp giảm overfitting.
    
- [ ] d) Vì nó giúp chọn đúng hàm kích hoạt.
    

**Câu 24:** **Trong bài toán nhận dạng khuôn mặt, lớp đầu tiên của một mạng nơ-ron sâu có khả năng học được đặc trưng gì?**

- [ ] a) Các khuôn mặt hoàn chỉnh.
    
- [ ] b) Các bộ phận như mắt, mũi, miệng.
    
- [x] c) Các cạnh và góc đơn giản.
    
- [ ] d) Tên của người trong ảnh.
    

**Câu 25:** **"Cache" trong quá trình lan truyền xuôi được sử dụng để làm gì?**

- [ ] a) Để lưu trữ dự đoán cuối cùng.
    
- [ ] b) Để tăng tốc độ lan truyền xuôi.
    
- [x] c) Để lưu trữ các giá trị trung gian (như `Z`) nhằm tái sử dụng trong quá trình lan truyền ngược.
    
- [ ] d) Để lưu trữ các siêu tham số.
    

**Câu 26:** **Câu khẳng định nào sau đây là đúng về mối quan hệ giữa mạng nơ-ron và bộ não?**

- [ ] a) Mạng nơ-ron là một bản sao chính xác của bộ não.
    
- [ ] b) Các nhà khoa học thần kinh đã chứng minh bộ não sử dụng thuật toán lan truyền ngược.
    
- [x] c) Mạng nơ-ron chỉ được lấy cảm hứng một cách lỏng lẻo từ bộ não và sự tương đồng này không hoàn toàn chính xác.
    
- [ ] d) Mạng nơ-ron hoạt động hiệu quả hơn bộ não trong mọi tác vụ.
    

**Câu 27:** **Một mạng nơ-ron có `n[l-1]` nơ-ron ở lớp trước và `n[l]` nơ-ron ở lớp hiện tại. Kích thước của ma trận trọng số `W[l]` là:**

- [ ] a) (`n[l-1]`, `n[l]`)
    
- [x] b) (`n[l]`, `n[l-1]`)
    
- [ ] c) (`n[l]`, 1)
    
- [ ] d) (`n[l-1]`, 1)
    

**Câu 28:** **Nếu bạn đang xây dựng một mạng nơ-ron và không chắc chắn về số lớp ẩn, một chiến lược tốt để bắt đầu là gì?**

- [ ] a) Bắt đầu với một mạng rất sâu (ví dụ: 50 lớp).
    
- [x] b) Bắt đầu với một mô hình đơn giản (như Hồi quy Logistic hoặc mạng 1 lớp ẩn) và tăng dần độ sâu nếu cần.
    
- [ ] c) Chọn một số ngẫu nhiên từ 1 đến 100.
    
- [ ] d) Luôn sử dụng 5 lớp ẩn.
    

**Câu 29:** **Trong lan truyền ngược của một mạng sâu, `da[l-1]` được tính toán dựa trên giá trị nào?**

- [ ] a) `da[l-2]`
    
- [x] b) `dz[l]`
    
- [ ] c) `a[l]`
    
- [ ] d) `W[l-1]`
    

**Câu 30:** **Lý thuyết mạch (Circuit theory) gợi ý rằng mạng sâu có thể hiệu quả hơn mạng nông vì:**

- [x] a) Mạng sâu có thể tính toán một số hàm phức tạp với số lượng nơ-ron ít hơn theo cấp số mũ so với mạng nông.
    
- [ ] b) Mạng sâu luôn cần nhiều dữ liệu hơn.
    
- [ ] c) Mạng sâu dễ lập trình hơn.
    
- [ ] d) Mạng sâu không cần hàm kích hoạt.
    

**Câu 31:** **Trong một mạng nơ-ron, "activation" (kích hoạt) của một nơ-ron là gì?**

- [ ] a) Giá trị đầu vào của nơ-ron đó.
    
- [x] b) Giá trị đầu ra của nơ-ron đó sau khi đi qua hàm kích hoạt.
    
- [ ] c) Trọng số kết nối đến nơ-ron đó.
    
- [ ] d) Độ lệch của nơ-ron đó.
    

**Câu 32:** **Quá trình lặp lại việc thực hiện lan truyền xuôi và lan truyền ngược được gọi là gì?**

- [ ] a) Một epoch.
    
- [x] b) Một bước của Gradient Descent.
    
- [ ] c) Một lần dự đoán.
    
- [ ] d) Khởi tạo.
    

**Câu 33:** **Đâu là một nhược điểm của hàm Sigmoid và Tanh?**

- [ ] a) Chúng không phải là hàm phi tuyến.
    
- [x] b) Chúng có thể gặp vấn đề "gradient biến mất" (vanishing gradient) khi đầu vào quá lớn hoặc quá nhỏ.
    
- [ ] c) Chúng chỉ có thể được sử dụng ở lớp đầu ra.
    
- [ ] d) Chúng rất khó để tính đạo hàm.
    

**Câu 34:** **Tại sao ReLU lại giúp giảm bớt vấn đề "gradient biến mất"?**

- [x] a) Vì đạo hàm của nó luôn bằng 1 đối với các đầu vào dương, giúp gradient không bị suy giảm khi lan truyền ngược.
    
- [ ] b) Vì nó là một hàm tuyến tính.
    
- [ ] c) Vì nó giới hạn đầu ra trong khoảng [0, 1].
    
- [ ] d) Vì nó có đạo hàm bằng 0 đối với các đầu vào âm.
    

**Câu 35:** **Ký hiệu `n[0]` thường dùng để chỉ điều gì?**

- [ ] a) Số nơ-ron ở lớp đầu ra.
    
- [ ] b) Số nơ-ron ở lớp ẩn đầu tiên.
    
- [x] c) Số đặc trưng đầu vào (`nₓ`).
    
- [ ] d) Luôn bằng 0.
    

**Câu 36:** **Trong các công thức lan truyền ngược, `g'(Z)` đại diện cho cái gì?**

- [ ] a) Giá trị của hàm kích hoạt.
    
- [x] b) Đạo hàm của hàm kích hoạt theo `Z`.
    
- [ ] c) Đầu vào của hàm kích hoạt.
    
- [ ] d) Một hằng số.
    

**Câu 37:** **Nếu bạn tăng số lượng lớp ẩn trong một mạng nơ-ron, điều gì có khả năng xảy ra?**

- [ ] a) Khả năng của mạng để học các hàm phức tạp sẽ tăng lên.
    
- [ ] b) Nguy cơ overfitting có thể tăng lên.
    
- [ ] c) Thời gian huấn luyện sẽ tăng lên.
    
- [x] d) Tất cả các câu trên đều đúng.
    

**Câu 38:** **"Forward propagation" và "Inference" (suy luận) có liên quan như thế nào?**

- [ ] a) Chúng hoàn toàn không liên quan.
    
- [x] b) Inference chính là quá trình thực hiện forward propagation trên dữ liệu mới để đưa ra dự đoán (sau khi mô hình đã được huấn luyện).
    
- [ ] c) Forward propagation là một phần của inference, nhưng không phải ngược lại.
    
- [ ] d) Inference là tên gọi khác của backpropagation.
    

**Câu 39:** **Việc chọn kiến trúc mạng (số lớp, số nơ-ron mỗi lớp) thuộc về quá trình nào?**

- [ ] a) Tối ưu hóa tham số.
    
- [x] b) Tinh chỉnh siêu tham số.
    
- [ ] c) Lan truyền ngược.
    
- [ ] d) Xử lý dữ liệu.
    

**Câu 40:** **Trong một mạng nơ-ron được huấn luyện tốt, các trọng số `W` thường có giá trị như thế nào?**

- [ ] a) Rất lớn.
    
- [ ] b) Rất nhỏ, gần 0.
    
- [x] c) Các giá trị được phân bổ hợp lý, không quá lớn cũng không quá nhỏ.
    
- [ ] d) Luôn bằng 1.
    

**Câu 41:** **Một mạng nơ-ron có 3 lớp ẩn sẽ được gọi là mạng mấy lớp?**

- [ ] a) 3 lớp.
    
- [x] b) 4 lớp (3 ẩn + 1 đầu ra).
    
- [ ] c) 5 lớp (1 đầu vào + 3 ẩn + 1 đầu ra).
    
- [ ] d) Tùy thuộc vào cách đếm.
    

**Câu 42:** **Mục đích của vector `b` (bias) trong một nơ-ron là gì?**

- [ ] a) Để làm cho phép tính phức tạp hơn.
    
- [x] b) Cung cấp thêm một mức độ linh hoạt, cho phép đường biên quyết định dịch chuyển lên/xuống.
    
- [ ] c) Để chuẩn hóa đầu vào.
    
- [ ] d) Để ngăn chặn overfitting.
    

**Câu 43:** **Đâu không phải là một hàm kích hoạt?**

- [ ] a) ReLU
    
- [ ] b) Tanh
    
- [ ] c) Sigmoid
    
- [x] d) Gradient Descent
    

**Câu 44:** **Quá trình tính toán `Z = W*A + b` là một phép biến đổi:**

- [x] a) Tuyến tính.
    
- [ ] b) Phi tuyến.
    
- [ ] c) Ngẫu nhiên.
    
- [ ] d) Logarit.
    

**Câu 45:** **Trong công thức `db[l] = (1/m) * np.sum(dZ[l], axis=1, keepdims=True)`, `np.sum` được sử dụng để làm gì?**

- [x] a) Tính tổng các sai số trên tất cả các mẫu trong mini-batch để có được đạo hàm của bias.
    
- [ ] b) Tính tổng các trọng số.
    
- [ ] c) Tính tổng các kích hoạt.
    
- [ ] d) Chuẩn hóa dữ liệu.
    

**Câu 46:** **Sự khác biệt chính giữa một mạng nơ-ron nông và một mạng sâu nằm ở:**

- [ ] a) Số lượng tham số.
    
- [ ] b) Tốc độ huấn luyện.
    
- [x] c) Độ sâu, tức là số lượng lớp ẩn.
    
- [ ] d) Loại dữ liệu chúng có thể xử lý.
    

**Câu 47:** **Nếu bạn có một mạng nơ-ron rất sâu, bạn có thể gặp phải vấn đề gì trong quá trình huấn luyện?**

- [ ] a) Gradient biến mất hoặc bùng nổ (Vanishing/Exploding Gradients).
    
- [ ] b) Overfitting.
    
- [ ] c) Thời gian huấn luyện lâu.
    
- [x] d) Tất cả các câu trên.
    

**Câu 48:** **Việc vector hóa giúp tăng tốc độ tính toán chủ yếu là do:**

- [ ] a) Python vốn dĩ rất nhanh.
    
- [x] b) Các thư viện như NumPy sử dụng các đoạn mã C/Fortran được tối ưu hóa cao và tận dụng tính toán song song của phần cứng.
    
- [ ] c) Nó làm giảm số lượng phép tính cần thực hiện.
    
- [ ] d) Nó làm giảm độ phức tạp của thuật toán.
    

**Câu 49:** **Trong một mạng nơ-ron, thông tin được truyền đi như thế nào?**

- [ ] a) Từ lớp đầu ra đến lớp đầu vào.
    
- [ ] b) Giữa các nơ-ron trong cùng một lớp.
    
- [x] c) Từ lớp này sang lớp tiếp theo, theo một chiều từ đầu vào đến đầu ra.
    
- [ ] d) Một cách ngẫu nhiên.
    

**Câu 50:** **Đâu là bước đầu tiên trong quá trình lan truyền ngược (backpropagation)?**

- [ ] a) Cập nhật trọng số của lớp đầu tiên.
    
- [x] b) Tính toán sai số giữa dự đoán và nhãn thật ở lớp đầu ra.
    
- [ ] c) Tính toán kích hoạt của lớp ẩn đầu tiên.
    
- [ ] d) Khởi tạo lại tất cả các trọng số.
    

#### Bài kiểm tra trắc nghiệm: Các khía cạnh thực tế của Học sâu

**Câu 1:** **Mục đích chính của tập phát triển (dev set) là gì?**

- [ ] a) Để huấn luyện mô hình.
    
- [ ] b) Để đưa ra đánh giá cuối cùng, không thiên vị về hiệu suất của mô hình.
    
- [x] c) Để tinh chỉnh các siêu tham số và đánh giá các ý tưởng khác nhau.
    
- [ ] d) Không có mục đích cụ thể.
    

**Câu 2:** **Trong thời đại Dữ liệu lớn (Big Data), tỷ lệ phân chia Train/Dev/Test nào sau đây là hợp lý nhất cho một tập dữ liệu có 1,000,000 mẫu?**

- [ ] a) 60% / 20% / 20%
    
- [ ] b) 70% / 30% / 0%
    
- [x] c) 98% / 1% / 1%
    
- [ ] d) 34% / 33% / 33%
    

**Câu 3:** **"High Bias" (Độ chệch cao) có nghĩa là gì?**

- [ ] a) Mô hình bị overfitting.
    
- [ ] b) Mô hình quá phức tạp.
    
- [x] c) Mô hình quá đơn giản và không khớp tốt với cả tập huấn luyện (underfitting).
    
- [ ] d) Mô hình hoạt động tốt trên tập huấn luyện nhưng kém trên tập dev.
    

**Câu 4:** **Nếu lỗi trên tập huấn luyện (Train error) là 1% và lỗi trên tập phát triển (Dev error) là 11%, mô hình của bạn đang gặp vấn đề gì?**

- [ ] a) High Bias (Độ chệch cao)
    
- [x] b) High Variance (Phương sai cao)
    
- [ ] c) Cả High Bias và High Variance
    
- [ ] d) Low Bias và Low Variance
    

**Câu 5:** **Nếu Train error là 14% và Dev error là 15% (giả sử lỗi tối ưu là ~0%), mô hình của bạn đang gặp vấn đề gì?**

- [x] a) High Bias (Độ chệch cao)
    
- [ ] b) High Variance (Phương sai cao)
    
- [ ] c) Cả High Bias và High Variance
    
- [ ] d) Low Bias và Low Variance
    

**Câu 6:** **Để giải quyết vấn đề High Variance, bạn nên thử phương pháp nào đầu tiên?**

- [ ] a) Huấn luyện một mạng lớn hơn.
    
- [x] b) Thêm dữ liệu hoặc sử dụng điều chuẩn hóa (regularization).
    
- [ ] c) Huấn luyện lâu hơn.
    
- [ ] d) Thử một thuật toán tối ưu hóa khác.
    

**Câu 7:** **Để giải quyết vấn đề High Bias, bạn nên thử phương pháp nào?**

- [ ] a) Thêm dữ liệu.
    
- [ ] b) Sử dụng Dropout.
    
- [x] c) Huấn luyện một mạng lớn hơn hoặc huấn luyện lâu hơn.
    
- [ ] d) Sử dụng L2 regularization.
    

**Câu 8:** **Tại sao tập dev và tập test nên đến từ cùng một phân phối dữ liệu?**

- [ ] a) Để quá trình huấn luyện nhanh hơn.
    
- [x] b) Để đảm bảo rằng việc tối ưu hóa trên tập dev sẽ dẫn đến hiệu suất tốt trên dữ liệu thực tế mà tập test đại diện.
    
- [ ] c) Đó chỉ là một quy ước không bắt buộc.
    
- [ ] d) Để giảm bộ nhớ sử dụng.
    

**Câu 9:** **Quy trình làm việc trong học máy có tính chất gì?**

- [ ] a) Tuyến tính, làm một lần là xong.
    
- [x] b) Lặp đi lặp lại (iterative): Lên ý tưởng -> Viết code -> Thử nghiệm -> Tinh chỉnh.
    
- [ ] c) Hoàn toàn ngẫu nhiên.
    
- [ ] d) Chỉ phụ thuộc vào việc viết code.
    

**Câu 10:** **Trong "công thức" cơ bản cho học máy, bước đầu tiên sau khi huấn luyện mô hình là gì?**

- [ ] a) Kiểm tra xem mô hình có bị High Variance không.
    
- [ ] b) Triển khai mô hình ngay lập tức.
    
- [x] c) Kiểm tra xem mô hình có bị High Bias không.
    
- [ ] d) Thu thập thêm dữ liệu.
    

**Câu 11:** **Mục đích chính của các kỹ thuật điều chuẩn hóa (regularization) là gì?**

- [ ] a) Để giải quyết vấn đề High Bias (underfitting).
    
- [ ] b) Để tăng tốc độ huấn luyện.
    
- [x] c) Để giải quyết vấn đề High Variance (overfitting).
    
- [ ] d) Để giảm số lượng lớp ẩn.
    

**Câu 12:** **L2 Regularization hoạt động bằng cách nào?**

- [x] a) Thêm một thành phần vào hàm chi phí để phạt các trọng số có giá trị lớn.
    
- [ ] b) Loại bỏ ngẫu nhiên các nơ-ron trong quá trình huấn luyện.
    
- [ ] c) Dừng quá trình huấn luyện sớm.
    
- [ ] d) Chuẩn hóa các đặc trưng đầu vào.
    

**Câu 13:** **Điều gì xảy ra với các trọng số `W` khi bạn tăng siêu tham số `λ` (lambda) trong L2 Regularization?**

- [ ] a) Các trọng số sẽ trở nên lớn hơn.
    
- [x] b) Các trọng số sẽ bị đẩy về gần 0.
    
- [ ] c) Các trọng số sẽ không thay đổi.
    
- [ ] d) Một nửa số trọng số sẽ bằng 0.
    

**Câu 14:** **Dropout Regularization hoạt động bằng cách nào?**

- [ ] a) Thêm nhiễu vào dữ liệu đầu vào.
    
- [x] b) Loại bỏ ngẫu nhiên một số nơ-ron và các kết nối của chúng trong mỗi lần lặp của quá trình huấn luyện.
    
- [ ] c) Giảm tốc độ học theo thời gian.
    
- [ ] d) Chỉ sử dụng một phần nhỏ của tập dữ liệu.
    

**Câu 15:** **Kỹ thuật "Inverted Dropout" thực hiện điều gì để giữ cho giá trị kỳ vọng của các kích hoạt không đổi?**

- [x] a) Chia các kích hoạt của các nơ-ron còn lại cho `keep_prob`.
    
- [ ] b) Nhân các kích hoạt của các nơ-ron còn lại với `keep_prob`.
    
- [ ] c) Thêm một giá trị bias mới.
    
- [ ] d) Không làm gì cả.
    

**Câu 16:** **Khi nào thì Dropout được áp dụng?**

- [x] a) Chỉ trong quá trình huấn luyện.
    
- [ ] b) Chỉ trong quá trình kiểm thử (test time).
    
- [ ] c) Cả trong quá trình huấn luyện và kiểm thử.
    
- [ ] d) Không bao giờ được áp dụng ở lớp đầu ra.
    

**Câu 17:** **Một trong những nhược điểm của Dropout là gì?**

- [ ] a) Nó làm tăng High Bias.
    
- [x] b) Nó làm cho hàm chi phí `J` không còn được định nghĩa rõ ràng, gây khó khăn cho việc gỡ lỗi.
    
- [ ] c) Nó chỉ hoạt động với hàm kích hoạt Sigmoid.
    
- [ ] d) Nó yêu cầu một lượng lớn bộ nhớ.
    

**Câu 18:** **"Data Augmentation" (Tăng cường dữ liệu) là một kỹ thuật điều chuẩn hóa bằng cách:**

- [ ] a) Mua thêm dữ liệu từ bên ngoài.
    
- [x] b) Tạo ra các mẫu huấn luyện mới bằng cách biến đổi các mẫu hiện có (ví dụ: lật ảnh, xoay ảnh).
    
- [ ] c) Lặp lại các mẫu dữ liệu hiện có nhiều lần.
    
- [ ] d) Giảm số lượng đặc trưng.
    

**Câu 19:** **"Early Stopping" (Dừng sớm) hoạt động dựa trên nguyên tắc nào?**

- [ ] a) Dừng huấn luyện sau một số lần lặp cố định.
    
- [ ] b) Dừng huấn luyện khi lỗi trên tập huấn luyện bắt đầu tăng.
    
- [x] c) Dừng huấn luyện khi lỗi trên tập phát triển (dev set) ngừng giảm và bắt đầu tăng.
    
- [ ] d) Dừng huấn luyện khi độ chính xác đạt 100%.
    

**Câu 20:** **Đâu là một nhược điểm của Early Stopping?**

- [ ] a) Nó không hiệu quả trong việc giảm overfitting.
    
- [x] b) Nó kết hợp hai nhiệm vụ: tối ưu hóa hàm chi phí và chống overfitting, làm cho việc tìm kiếm siêu tham số trở nên phức tạp hơn.
    
- [ ] c) Nó yêu cầu một mạng nơ-ron rất sâu.
    
- [ ] d) Nó chỉ hoạt động với L2 regularization.
    

**Câu 21:** **Mục đích của việc chuẩn hóa các đặc trưng đầu vào (Normalizing inputs) là gì?**

- [ ] a) Để làm cho dữ liệu khó hiểu hơn.
    
- [x] b) Để làm cho hàm chi phí có dạng đối xứng hơn (giống hình cái bát tròn), giúp Gradient Descent hội tụ nhanh hơn.
    
- [ ] c) Để tăng số lượng đặc trưng.
    
- [ ] d) Để loại bỏ các giá trị ngoại lai.
    

**Câu 22:** **Hai bước chính trong việc chuẩn hóa đầu vào là gì?**

- [ ] a) Trừ đi giá trị lớn nhất và chia cho giá trị nhỏ nhất.
    
- [x] b) Trừ đi trung bình và chia cho phương sai (hoặc độ lệch chuẩn).
    
- [ ] c) Lấy logarit và sau đó lấy căn bậc hai.
    
- [ ] d) Thêm một hằng số và nhân với một hằng số.
    

**Câu 23:** **"Vanishing Gradients" (Gradient biến mất) là hiện tượng gì?**

- [ ] a) Gradient trở nên rất lớn, gây ra sự bất ổn trong quá trình huấn luyện.
    
- [x] b) Gradient trở nên rất nhỏ (gần bằng 0) khi lan truyền ngược qua nhiều lớp, khiến việc học ở các lớp đầu tiên diễn ra rất chậm.
    
- [ ] c) Gradient biến mất khỏi bộ nhớ máy tính.
    
- [ ] d) Gradient luôn bằng 1.
    

**Câu 24:** **"Exploding Gradients" (Gradient bùng nổ) là hiện tượng gì?**

- [x] a) Gradient trở nên rất lớn khi lan truyền ngược, gây ra các bước cập nhật quá lớn và làm cho mô hình phân kỳ.
    
- [ ] b) Gradient trở nên rất nhỏ.
    
- [ ] c) Gradient chỉ xuất hiện ở lớp cuối cùng.
    
- [ ] d) Gradient được lưu vào một file riêng.
    

**Câu 25:** **Phương pháp khởi tạo trọng số nào được đề xuất để sử dụng với hàm kích hoạt ReLU?**

- [ ] a) Khởi tạo bằng 0.
    
- [ ] b) Khởi tạo Xavier/Glorot.
    
- [x] c) Khởi tạo He.
    
- [ ] d) Khởi tạo bằng 1.
    

**Câu 26:** **Công thức khởi tạo He cho trọng số `W[l]` sử dụng phương sai là bao nhiêu? (với `n[l-1]` là số nơ-ron ở lớp trước)**

- [ ] a) `1 / n[l-1]`
    
- [x] b) `2 / n[l-1]`
    
- [ ] c) `1 / n[l]`
    
- [ ] d) `2 / n[l]`
    

**Câu 27:** **Tại sao việc khởi tạo tất cả các trọng số bằng 0 lại là một ý tưởng tồi?**

- [ ] a) Vì nó gây ra lỗi chia cho 0.
    
- [x] b) Vì nó tạo ra vấn đề "đối xứng", khiến tất cả các nơ-ron trong một lớp học cùng một thứ.
    
- [ ] c) Vì nó làm cho quá trình huấn luyện quá nhanh.
    
- [ ] d) Vì nó chỉ hoạt động với mạng nông.
    

**Câu 28:** **Nếu bạn sử dụng hàm kích hoạt `tanh`, phương pháp khởi tạo trọng số nào thường được khuyên dùng?**

- [ ] a) Khởi tạo He
    
- [ ] b) Khởi tạo bằng 0
    
- [x] c) Khởi tạo Xavier
    
- [ ] d) Khởi tạo bằng 1
    

**Câu 29:** **Việc chuẩn hóa đầu vào có thể giúp giảm thiểu vấn đề gradient biến mất/bùng nổ không?**

- [x] a) Có, vì nó giúp giữ cho các giá trị đầu vào ở một quy mô hợp lý.
    
- [ ] b) Không, nó hoàn toàn không liên quan.
    
- [ ] c) Nó chỉ làm cho vấn đề tồi tệ hơn.
    
- [ ] d) Nó chỉ giải quyết được vấn đề gradient biến mất.
    

**Câu 30:** **Việc lựa chọn phương pháp khởi tạo trọng số phù hợp phụ thuộc chủ yếu vào yếu tố nào?**

- [ ] a) Số lượng lớp trong mạng.
    
- [ ] b) Kích thước của tập dữ liệu.
    
- [x] c) Loại hàm kích hoạt được sử dụng.
    
- [ ] d) Tốc độ học.
    

**Câu 31:** **"Gradient Checking" là một kỹ thuật được sử dụng để làm gì?**

- [ ] a) Để tăng tốc độ của Gradient Descent.
    
- [x] b) Để kiểm tra xem việc triển khai thuật toán lan truyền ngược (backpropagation) có đúng hay không.
    
- [ ] c) Để tự động chọn tốc độ học.
    
- [ ] d) Để điều chuẩn hóa mô hình.
    

**Câu 32:** **Gradient Checking hoạt động bằng cách nào?**

- [x] a) So sánh gradient tính bằng lan truyền ngược với gradient được ước tính bằng phương pháp số (xấp xỉ hai phía).
    
- [ ] b) Chạy Gradient Descent hai lần và so sánh kết quả.
    
- [ ] c) Kiểm tra xem hàm chi phí có giảm sau mỗi lần lặp hay không.
    
- [ ] d) So sánh các trọng số trước và sau khi cập nhật.
    

**Câu 33:** **Bạn có nên sử dụng Gradient Checking trong quá trình huấn luyện không?**

- [ ] a) Có, trong mỗi lần lặp.
    
- [x] b) Không, nó chỉ nên được sử dụng để gỡ lỗi và sau đó tắt đi vì nó rất chậm về mặt tính toán.
    
- [ ] c) Chỉ khi mô hình bị overfitting.
    
- [ ] d) Chỉ khi mô hình bị underfitting.
    

**Câu 34:** **Gradient Checking có hoạt động với Dropout không?**

- [ ] a) Có, nó hoạt động hoàn hảo.
    
- [x] b) Không, vì Dropout đưa vào tính ngẫu nhiên, làm cho hàm chi phí thay đổi trong mỗi lần chạy, khiến việc kiểm tra gradient trở nên khó khăn.
    
- [ ] c) Chỉ hoạt động với `keep_prob` = 1.
    
- [ ] d) Chỉ hoạt động với `keep_prob` = 0.5.
    

**Câu 35:** **Nếu kết quả của Gradient Checking cho ra một sự khác biệt lớn (ví dụ: `10⁻²`), điều đó có nghĩa là gì?**

- [ ] a) Việc triển khai lan truyền ngược của bạn có khả năng cao là đúng.
    
- [x] b) Việc triển khai lan truyền ngược của bạn có khả năng cao là sai.
    
- [ ] c) Tốc độ học của bạn quá lớn.
    
- [ ] d) Mô hình của bạn đang học rất tốt.
    

**Câu 36:** **"Bias" và "Variance" có mối quan hệ "trade-off" (đánh đổi) trong học máy cổ điển. Điều này có còn đúng trong học sâu không?**

- [ ] a) Có, hoàn toàn đúng.
    
- [x] b) Không hẳn, trong học sâu, việc tăng kích thước mạng và thêm dữ liệu thường có thể giảm cả bias và variance (hoặc giảm một cái mà không làm tăng cái kia nhiều).
    
- [ ] c) Trong học sâu chỉ có bias, không có variance.
    
- [ ] d) Trong học sâu chỉ có variance, không có bias.
    

**Câu 37:** **Đâu không phải là một phương pháp điều chuẩn hóa?**

- [ ] a) L2 Regularization
    
- [ ] b) Dropout
    
- [x] c) Gradient Descent
    
- [ ] d) Data Augmentation
    

**Câu 38:** **Việc thêm điều chuẩn hóa L2 vào hàm chi phí tương đương với việc đặt một prior (tiên nghiệm) nào lên các trọng số?**

- [ ] a) Prior phân phối Laplace.
    
- [x] b) Prior phân phối Gaussian với trung bình 0.
    
- [ ] c) Prior phân phối đều.
    
- [ ] d) Không tương đương với bất kỳ prior nào.
    

**Câu 39:** **Tại sao Dropout có thể được coi là một dạng của L2 regularization?**

- [x] a) Vì nó buộc các nơ-ron phải học các trọng số nhỏ hơn và phân tán hơn, không phụ thuộc vào bất kỳ đặc trưng nào.
    
- [ ] b) Vì công thức toán học của chúng giống hệt nhau.
    
- [ ] c) Vì chúng đều làm cho quá trình huấn luyện chậm lại.
    
- [ ] d) Chúng không liên quan đến nhau.
    

**Câu 40:** **Việc chuẩn hóa đầu vào sử dụng trung bình và phương sai được tính từ tập dữ liệu nào?**

- [ ] a) Chỉ từ tập test.
    
- [ ] b) Chỉ từ tập dev.
    
- [x] c) Chỉ từ tập huấn luyện (train set).
    
- [ ] d) Từ toàn bộ dữ liệu (train + dev + test).
    

**Câu 41:** **Khi áp dụng chuẩn hóa cho tập dev/test, bạn nên làm gì?**

- [ ] a) Tính lại trung bình và phương sai mới từ tập dev/test.
    
- [x] b) Sử dụng cùng một giá trị trung bình và phương sai đã được tính từ tập huấn luyện.
    
- [ ] c) Không cần chuẩn hóa tập dev/test.
    
- [ ] d) Trộn tập train và dev/test lại rồi tính trung bình và phương sai.
    

**Câu 42:** **Trong thực tế, khi nào bạn nên lo lắng về vấn đề High Bias?**

- [ ] a) Khi lỗi trên tập dev rất cao.
    
- [x] b) Khi lỗi trên tập huấn luyện cao hơn đáng kể so với hiệu suất của con người (hoặc lỗi Bayes).
    
- [ ] c) Khi lỗi trên tập huấn luyện thấp nhưng lỗi trên tập dev cao.
    
- [ ] d) Khi mô hình huấn luyện rất nhanh.
    

**Câu 43:** **"Orthogonalization" (Trực giao hóa) trong học máy là ý tưởng về việc:**

- [ ] a) Sử dụng các vector trực giao để khởi tạo trọng số.
    
- [x] b) Đảm bảo rằng mỗi "nút vặn" (kỹ thuật) bạn sử dụng chỉ ảnh hưởng đến một khía cạnh duy nhất của hiệu suất mô hình (ví dụ: một nút cho bias, một nút khác cho variance).
    
- [ ] c) Làm cho các lớp trong mạng nơ-ron độc lập với nhau.
    
- [ ] d) Luôn sử dụng ma trận vuông.
    

**Câu 44:** **Nếu mô hình của bạn có High Variance, nhưng bạn không thể thu thập thêm dữ liệu, lựa chọn tốt nhất tiếp theo là gì?**

- [ ] a) Tăng kích thước mạng.
    
- [x] b) Tăng cường các kỹ thuật điều chuẩn hóa (tăng `λ`, giảm `keep_prob`).
    
- [ ] c) Huấn luyện lâu hơn nữa.
    
- [ ] d) Giảm tốc độ học.
    

**Câu 45:** **Trong "inverted dropout", tại sao chúng ta không cần phải làm gì thêm ở bước kiểm thử (test time)?**

- [ ] a) Vì ở bước kiểm thử chúng ta cũng áp dụng dropout.
    
- [x] b) Vì việc chia cho `keep_prob` trong quá trình huấn luyện đã đảm bảo rằng đầu ra ở bước kiểm thử không cần phải thay đổi tỷ lệ.
    
- [ ] c) Vì bước kiểm thử không quan trọng.
    
- [ ] d) Vì chúng ta nhân với `keep_prob` ở bước kiểm thử.
    

**Câu 46:** **Kỹ thuật nào giúp giải quyết vấn đề "internal covariate shift" (sự thay đổi hiệp phương sai nội bộ)?**

- [ ] a) L2 Regularization
    
- [ ] b) Dropout
    
- [ ] c) Batch Normalization (Sẽ học ở bài sau, nhưng là một khái niệm liên quan)
    
- [x] d) Chuẩn hóa đầu vào (Input Normalization).
    

**Câu 47:** **Nếu bạn đang gỡ lỗi cho việc triển khai backpropagation, bạn nên kiểm tra thành phần nào trước tiên?**

- [ ] a) Đạo hàm của hàm chi phí.
    
- [ ] b) Đạo hàm của hàm kích hoạt.
    
- [ ] c) Phép nhân ma trận.
    
- [x] d) Tất cả các thành phần, bắt đầu từ lớp cuối cùng và đi ngược lại.
    

**Câu 48:** **Việc huấn luyện một mạng nơ-ron là một quá trình có tính chất gì?**

- [ ] a) Có thể dự đoán chính xác kết quả ngay từ đầu.
    
- [x] b) Mang tính thực nghiệm cao, đòi hỏi nhiều lần thử và sai.
    
- [ ] c) Luôn luôn hội tụ đến điểm tối ưu toàn cục.
    
- [ ] d) Chỉ cần một lần lặp là đủ.
    

**Câu 49:** **L1 regularization khác L2 regularization ở điểm nào?**

- [x] a) L1 có xu hướng đẩy các trọng số về 0, tạo ra các mô hình thưa (sparse), trong khi L2 chỉ làm chúng nhỏ lại.
    
- [ ] b) L2 có xu hướng đẩy các trọng số về 0, tạo ra các mô hình thưa (sparse), trong khi L1 chỉ làm chúng nhỏ lại.
    
- [ ] c) L1 chỉ dùng cho mạng nông, L2 chỉ dùng cho mạng sâu.
    
- [ ] d) Không có sự khác biệt.
    

**Câu 50:** **Đâu là lý do chính khiến các mạng nơ-ron sâu dễ bị overfitting hơn các mô hình đơn giản?**

- [ ] a) Vì chúng có ít tham số hơn.
    
- [x] b) Vì chúng có rất nhiều tham số, cho phép chúng học được cả nhiễu trong dữ liệu huấn luyện.
    
- [ ] c) Vì chúng huấn luyện chậm hơn.
    
- [ ] d) Vì chúng không thể sử dụng các kỹ thuật điều chuẩn hóa.
    

#### Bài kiểm tra trắc nghiệm: Tối ưu hóa và Tinh chỉnh Siêu tham số

**Câu 1:** **Sự khác biệt chính giữa Batch Gradient Descent và Mini-batch Gradient Descent là gì?**

- [ ] a) Batch GD nhanh hơn Mini-batch GD.
    
- [ ] b) Batch GD cập nhật tham số sau mỗi mẫu dữ liệu, còn Mini-batch GD cập nhật sau mỗi lô nhỏ.
    
- [x] c) Batch GD cập nhật tham số sau khi xử lý toàn bộ tập huấn luyện, còn Mini-batch GD cập nhật sau mỗi lô nhỏ (subset).
    
- [ ] d) Mini-batch GD luôn hội tụ tốt hơn.
    

**Câu 2:** **Một "epoch" có nghĩa là gì?**

- [ ] a) Một lần cập nhật các tham số.
    
- [x] b) Một lần thuật toán đi qua toàn bộ tập dữ liệu huấn luyện.
    
- [ ] c) Kích thước của một mini-batch.
    
- [ ] d) Số lượng lớp trong mạng nơ-ron.
    

**Câu 3:** **Nếu bạn có 5,000,000 mẫu huấn luyện và kích thước mini-batch là 1000, có bao nhiêu lần lặp (iterations) trong một epoch?**

- [ ] a) 1000
    
- [ ] b) 5,000,000
    
- [x] c) 5000
    
- [ ] d) 1
    

**Câu 4:** **Ưu điểm của Mini-batch Gradient Descent so với Stochastic Gradient Descent (SGD) là gì?**

- [x] a) Mini-batch GD ít "nhiễu" hơn và có thể tận dụng lợi thế của vector hóa để tính toán nhanh hơn.
    
- [ ] b) Mini-batch GD luôn tìm ra điểm tối ưu toàn cục tốt hơn.
    
- [ ] c) Mini-batch GD không cần thiết lập tốc độ học.
    
- [ ] d) SGD luôn nhanh hơn Mini-batch GD.
    

**Câu 5:** **Trong công thức tính Trung bình trọng số mũ (EWA), `Vt = β * Vt-1 + (1-β) * θt`, nếu `β` được đặt gần bằng 1 (ví dụ: 0.98), đường cong trung bình sẽ như thế nào?**

- [ ] a) Rất nhiễu và bám sát vào các điểm dữ liệu.
    
- [x] b) Mượt hơn và phản ứng chậm hơn với sự thay đổi.
    
- [ ] c) Gần như là một đường thẳng.
    
- [ ] d) Luôn đi qua điểm dữ liệu đầu tiên.
    

**Câu 6:** **Mục đích của "Bias correction" trong EWA là gì?**

- [ ] a) Để làm cho thuật toán chạy nhanh hơn.
    
- [x] b) Để hiệu chỉnh ước tính ban đầu, vốn bị chệch về phía 0, đặc biệt là trong giai đoạn đầu.
    
- [ ] c) Để ngăn chặn overfitting.
    
- [ ] d) Để tăng giá trị của `β`.
    

**Câu 7:** **Gradient Descent with Momentum được thiết kế để giải quyết vấn đề gì?**

- [x] a) Giảm thiểu dao động theo chiều dọc và tăng tốc độ hội tụ theo chiều ngang trong các hàm chi phí có dạng "thung lũng hẹp".
    
- [ ] b) Chỉ để làm cho code phức tạp hơn.
    
- [ ] c) Giảm thiểu High Bias.
    
- [ ] d) Tự động tìm kích thước mini-batch tốt nhất.
    

**Câu 8:** **Thuật toán RMSprop (Root Mean Square prop) điều chỉnh tốc độ học cho mỗi tham số bằng cách nào?**

- [ ] a) Dựa trên tổng của các gradient.
    
- [ ] b) Dựa trên trung bình trọng số mũ của các gradient.
    
- [x] c) Dựa trên trung bình trọng số mũ của bình phương các gradient.
    
- [ ] d) Dựa trên một giá trị ngẫu nhiên.
    

**Câu 9:** **Thuật toán Adam (Adaptive Moment Estimation) là sự kết hợp của hai thuật toán nào?**

- [ ] a) Batch GD và Stochastic GD.
    
- [x] b) Momentum và RMSprop.
    
- [ ] c) L2 Regularization và Dropout.
    
- [ ] d) EWA và Bias Correction.
    

**Câu 10:** **Mục đích của việc sử dụng "Learning Rate Decay" là gì?**

- [ ] a) Để tăng tốc độ học khi quá trình huấn luyện diễn ra.
    
- [x] b) Để giảm dần tốc độ học khi tiến gần đến điểm tối ưu, giúp mô hình hội tụ một cách tinh vi hơn và tránh dao động quanh điểm tối ưu.
    
- [ ] c) Để giữ cho tốc độ học không đổi trong suốt quá trình huấn luyện.
    
- [ ] d) Để ngăn chặn gradient biến mất.
    

**Câu 11:** **Trong các mạng nơ-ron sâu và không gian nhiều chiều, hầu hết các điểm có gradient bằng 0 là gì?**

- [ ] a) Điểm cực tiểu toàn cục (Global optima).
    
- [ ] b) Điểm cực tiểu cục bộ (Local optima).
    
- [x] c) Điểm yên ngựa (Saddle points).
    
- [ ] d) Điểm cực đại (Maxima).
    

**Câu 12:** **Hiện tượng "plateau" (vùng phẳng) trong hàm chi phí gây ra vấn đề gì?**

- [x] a) Làm cho quá trình học bị chậm lại đáng kể vì gradient rất gần 0.
    
- [ ] b) Gây ra hiện tượng gradient bùng nổ.
    
- [ ] c) Khiến mô hình bị overfitting.
    
- [ ] d) Làm cho bộ nhớ bị đầy.
    

**Câu 13:** **Giá trị `β₁` trong thuật toán Adam thường được đặt mặc định là bao nhiêu và nó kiểm soát thành phần nào?**

- [ ] a) 0.999, kiểm soát RMSprop.
    
- [x] b) 0.9, kiểm soát Momentum.
    
- [ ] c) 0.5, kiểm soát tốc độ học.
    
- [ ] d) 10⁻⁸, kiểm soát epsilon.
    

**Câu 14:** **Khi chọn kích thước mini-batch, tại sao các con số lũy thừa của 2 (ví dụ: 64, 128, 512) lại được ưa chuộng?**

- [ ] a) Vì chúng là các số đẹp.
    
- [x] b) Vì chúng phù hợp với cách tổ chức bộ nhớ của CPU/GPU, giúp tính toán hiệu quả hơn.
    
- [ ] c) Vì chúng giúp giảm overfitting.
    
- [ ] d) Đây chỉ là một quy ước ngẫu nhiên.
    

**Câu 15:** **Nếu bạn có một tập dữ liệu nhỏ (ví dụ: < 2000 mẫu), bạn nên chọn kích thước mini-batch là bao nhiêu?**

- [ ] a) 1 (Stochastic GD).
    
- [ ] b) 64.
    
- [x] c) Bằng kích thước của toàn bộ tập dữ liệu (Batch GD).
    
- [ ] d) 128.
    

**Câu 16:** **Đâu là siêu tham số (hyperparameter) thường được coi là quan trọng nhất cần tinh chỉnh?**

- [ ] a) Số lớp ẩn.
    
- [x] b) Tốc độ học `α`.
    
- [ ] c) `β` trong Momentum.
    
- [ ] d) Kích thước mini-batch.
    

**Câu 17:** **Tại sao tìm kiếm ngẫu nhiên (Random Search) thường hiệu quả hơn tìm kiếm theo lưới (Grid Search) để tinh chỉnh siêu tham số?**

- [ ] a) Vì nó luôn nhanh hơn.
    
- [x] b) Vì nó cho phép khám phá nhiều giá trị hơn cho các siêu tham số quan trọng, trong khi một số siêu tham số khác có thể ít ảnh hưởng hơn.
    
- [ ] c) Vì nó dễ lập trình hơn.
    
- [ ] d) Vì nó đảm bảo tìm ra điểm tối ưu toàn cục.
    

**Câu 18:** **Khi tinh chỉnh tốc độ học `α`, tại sao nên sử dụng thang đo logarit (logarithmic scale)?**

- [ ] a) Vì tốc độ học luôn là một số dương.
    
- [x] b) Vì sự thay đổi từ 0.001 đến 0.01 có tác động lớn hơn nhiều so với sự thay đổi từ 0.9 đến 0.91. Thang đo logarit giúp khám phá các khoảng giá trị nhỏ hiệu quả hơn.
    
- [ ] c) Để làm cho biểu đồ đẹp hơn.
    
- [ ] d) Vì `α` không thể lớn hơn 1.
    

**Câu 19:** **Chiến lược "Caviar" trong tinh chỉnh siêu tham số ám chỉ điều gì?**

- [ ] a) Huấn luyện một mô hình duy nhất và theo dõi, tinh chỉnh nó một cách cẩn thận.
    
- [x] b) Huấn luyện song song nhiều mô hình với các bộ siêu tham số khác nhau và chọn ra mô hình tốt nhất.
    
- [ ] c) Chỉ sử dụng các siêu tham số mặc định.
    
- [ ] d) Sử dụng các thuật toán di truyền để tìm siêu tham số.
    

**Câu 20:** **Batch Normalization (Batch Norm) thực hiện việc chuẩn hóa trên cái gì?**

- [ ] a) Dữ liệu đầu vào `X`.
    
- [x] b) Các giá trị kích hoạt `A` hoặc các giá trị tiền kích hoạt `Z` của các lớp ẩn.
    
- [ ] c) Các trọng số `W`.
    
- [ ] d) Các nhãn `Y`.
    

**Câu 21:** **Hai tham số có thể học được trong Batch Norm, `γ` (gamma) và `β` (beta), có vai trò gì?**

- [ ] a) Chúng là tốc độ học và momentum.
    
- [x] b) Chúng cho phép mạng học một giá trị trung bình và phương sai tối ưu cho các kích hoạt, thay vì bị ép buộc phải có trung bình 0 và phương sai 1.
    
- [ ] c) Chúng là các tham số điều chuẩn hóa.
    
- [ ] d) Chúng được dùng để khởi tạo trọng số.
    

**Câu 22:** **Một trong những lợi ích chính của Batch Norm là gì?**

- [ ] a) Nó làm cho mạng nơ-ron trở nên sâu hơn.
    
- [x] b) Nó cho phép sử dụng tốc độ học cao hơn và làm cho quá trình huấn luyện ổn định hơn, ít nhạy cảm với việc khởi tạo trọng số.
    
- [ ] c) Nó loại bỏ hoàn toàn nhu cầu về các hàm kích hoạt.
    
- [ ] d) Nó chỉ hoạt động với bài toán hồi quy.
    

**Câu 23:** **Batch Norm có tác dụng điều chuẩn hóa (regularization) nhẹ vì:**

- [ ] a) Nó thêm một thành phần phạt vào hàm chi phí.
    
- [ ] b) Nó loại bỏ các nơ-ron một cách ngẫu nhiên.
    
- [x] c) Trung bình và phương sai được tính trên từng mini-batch mang một chút nhiễu, và nhiễu này được đưa vào các kích hoạt của lớp ẩn.
    
- [ ] d) Nó làm cho các trọng số nhỏ hơn.
    

**Câu 24:** **Trong quá trình dự đoán (test time), trung bình và phương sai cho Batch Norm được tính như thế nào?**

- [ ] a) Chúng được tính lại trên từng mẫu dữ liệu test.
    
- [ ] b) Chúng được tính trên toàn bộ tập test.
    
- [x] c) Một ước tính (ví dụ: trung bình trọng số mũ) của trung bình và phương sai từ các mini-batch trong quá trình huấn luyện được sử dụng.
    
- [ ] d) Luôn được đặt bằng 0 và 1.
    

**Câu 25:** **Hàm kích hoạt Softmax thường được sử dụng ở lớp đầu ra cho loại bài toán nào?**

- [ ] a) Hồi quy.
    
- [ ] b) Phân loại nhị phân.
    
- [x] c) Phân loại nhiều lớp (Multi-class classification).
    
- [ ] d) Phân cụm.
    

**Câu 26:** **Đầu ra của lớp Softmax có đặc điểm gì?**

- [ ] a) Là một vector chứa các số thực bất kỳ.
    
- [ ] b) Là một số duy nhất trong khoảng (0, 1).
    
- [x] c) Là một vector các xác suất có tổng bằng 1.
    
- [ ] d) Là một vector các số nguyên.
    

**Câu 27:** **Nếu lớp đầu ra của một mạng Softmax có 4 nơ-ron, điều đó có nghĩa là gì?**

- [ ] a) Mạng có 4 lớp ẩn.
    
- [ ] b) Bài toán có 4 đặc trưng đầu vào.
    
- [x] c) Bài toán phân loại có 4 lớp.
    
- [ ] d) Kích thước mini-batch là 4.
    

**Câu 28:** **TensorFlow là gì?**

- [ ] a) Một ngôn ngữ lập trình.
    
- [ ] b) Một hệ điều hành.
    
- [x] c) Một framework mã nguồn mở cho học máy và học sâu.
    
- [ ] d) Một thuật toán tối ưu hóa.
    

**Câu 29:** **Trong TensorFlow, "placeholder" (trước TF 2.x) hoặc `tf.function` với `input_signature` được dùng để làm gì?**

- [ ] a) Để lưu trữ các trọng số đã được huấn luyện.
    
- [x] b) Để định nghĩa một biến sẽ được cung cấp dữ liệu sau (ví dụ: dữ liệu đầu vào từ mini-batch).
    
- [ ] c) Để tính toán hàm chi phí.
    
- [ ] d) Để khởi tạo các biến.
    

**Câu 30:** **Một ưu điểm lớn của việc sử dụng các framework học sâu như TensorFlow là gì?**

- [ ] a) Bạn phải tự viết code cho lan truyền ngược.
    
- [x] b) Chúng tự động tính toán các đạo hàm cho lan truyền ngược, bạn chỉ cần định nghĩa lan truyền xuôi.
    
- [ ] c) Chúng chỉ chạy được trên CPU.
    
- [ ] d) Chúng không yêu cầu dữ liệu.
    

**Câu 31:** **Tại sao Mini-batch GD thường được ưa chuộng hơn Batch GD trong thực tế?**

- [ ] a) Vì nó hội tụ mượt mà hơn.
    
- [ ] b) Vì việc tính toán gradient trên toàn bộ tập dữ liệu (đặc biệt là dữ liệu lớn) rất tốn kém và chậm chạp.
    
- [ ] c) Vì nó yêu cầu bộ nhớ ít hơn Batch GD.
    
- [x] d) Cả b và c đều đúng.
    

**Câu 32:** **Giá trị `β` trong EWA xấp xỉ trung bình trên bao nhiêu ngày?**

- [ ] a) `1 / β`
    
- [x] b) `1 / (1 - β)`
    
- [ ] c) `β / (1 - β)`
    
- [ ] d) `1 - β`
    

**Câu 33:** **Thuật toán Momentum giúp "tích lũy đà" theo hướng có gradient nhất quán, điều này có ý nghĩa gì?**

- [x] a) Nó làm cho thuật toán di chuyển nhanh hơn theo các hướng mà gradient liên tục chỉ về một phía.
    
- [ ] b) Nó làm cho thuật toán dừng lại.
    
- [ ] c) Nó chỉ hoạt động trên các hàm lồi.
    
- [ ] d) Nó làm giảm tốc độ học.
    

**Câu 34:** **Tại sao thuật toán Adam lại được gọi là "thích ứng" (Adaptive)?**

- [ ] a) Vì nó thích ứng với kích thước của tập dữ liệu.
    
- [x] b) Vì nó tính toán một tốc độ học riêng biệt, thích ứng cho từng tham số.
    
- [ ] c) Vì nó có thể thay đổi kiến trúc mạng.
    
- [ ] d) Vì nó chỉ hoạt động trên CPU.
    

**Câu 35:** **Đâu không phải là một phương pháp learning rate decay?**

- [ ] a) Exponential decay.
    
- [ ] b) Step decay.
    
- [x] c) Random decay.
    
- [ ] d) `1 / (1 + decay_rate * epoch_num)`.
    

**Câu 36:** **Trong không gian nhiều chiều, tại sao các điểm yên ngựa (saddle points) lại phổ biến hơn các điểm cực tiểu cục bộ (local optima)?**

- [x] a) Vì để là một điểm cực tiểu cục bộ, hàm chi phí phải cong lên ở tất cả các chiều, một điều kiện rất khó xảy ra.
    
- [ ] b) Vì các thuật toán tối ưu hóa có xu hướng tránh các điểm cực tiểu cục bộ.
    
- [ ] c) Vì các hàm chi phí trong học sâu luôn là hàm lồi.
    
- [ ] d) Đây là một nhận định sai.
    

**Câu 37:** **Đâu là một siêu tham số của thuật toán Adam?**

- [ ] a) `keep_prob`
    
- [ ] b) `λ` (lambda)
    
- [x] c) `β₁`, `β₂`, `ε`
    
- [ ] d) Số lượng epoch.
    

**Câu 38:** **Việc tinh chỉnh siêu tham số là một quá trình mang tính:**

- [ ] a) Lý thuyết và có thể tính toán chính xác.
    
- [x] b) Thực nghiệm, đòi hỏi nhiều lần thử và sai.
    
- [ ] c) Tự động hoàn toàn.
    
- [ ] d) Chỉ cần thực hiện một lần duy nhất.
    

**Câu 39:** **Batch Norm giúp giải quyết vấn đề "Internal Covariate Shift". Vấn đề này là gì?**

- [ ] a) Sự thay đổi trong phân phối của dữ liệu đầu vào.
    
- [x] b) Sự thay đổi trong phân phối của các kích hoạt ở các lớp ẩn khi các lớp trước đó cập nhật tham số.
    
- [ ] c) Sự khác biệt giữa tập train và tập test.
    
- [ ] d) Sự thay đổi trong tốc độ học.
    

**Câu 40:** **Bạn nên đặt lớp Batch Norm ở đâu trong một tầng của mạng nơ-ron?**

- [ ] a) Trước phép tính tuyến tính (`Z`).
    
- [x] b) Giữa phép tính tuyến tính (`Z`) và hàm kích hoạt (`A`).
    
- [ ] c) Sau hàm kích hoạt (`A`).
    
- [ ] d) Chỉ ở lớp đầu ra.
    

**Câu 41:** **Nếu bạn sử dụng Batch Norm, tham số `b` (bias) trong phép tính `Z = W*A + b` có còn cần thiết không?**

- [ ] a) Có, nó rất quan trọng.
    
- [x] b) Không, vì tác dụng của nó sẽ bị loại bỏ bởi bước trừ đi trung bình trong Batch Norm.
    
- [ ] c) Chỉ cần thiết ở lớp đầu ra.
    
- [ ] d) Chỉ cần thiết nếu không dùng hàm kích hoạt.
    

**Câu 42:** **Softmax là một dạng tổng quát hóa của hàm nào cho trường hợp nhiều lớp?**

- [ ] a) ReLU
    
- [ ] b) Tanh
    
- [x] c) Sigmoid
    
- [ ] d) Linear
    

**Câu 43:** **Nếu một trong các giá trị đầu vào của Softmax rất lớn so với các giá trị khác, xác suất đầu ra tương ứng sẽ như thế nào?**

- [ ] a) Gần 0.
    
- [ ] b) Gần 0.5.
    
- [x] c) Gần 1.
    
- [ ] d) Không thể xác định.
    

**Câu 44:** **"Tuning process" (Quá trình tinh chỉnh) trong học sâu thường bắt đầu bằng việc:**

- [ ] a) Thử nghiệm với một kiến trúc mạng rất phức tạp.
    
- [x] b) Tìm ra tốc độ học tốt nhất trước tiên, vì nó là siêu tham số quan trọng nhất.
    
- [ ] c) Thu thập càng nhiều dữ liệu càng tốt.
    
- [ ] d) Chọn một thuật toán tối ưu hóa ngẫu nhiên.
    

**Câu 45:** **Tại sao việc theo dõi đường cong học tập (learning curve - cost theo số lần lặp) lại quan trọng?**

- [ ] a) Để đảm bảo code không có lỗi cú pháp.
    
- [x] b) Để chẩn đoán các vấn đề như tốc độ học quá lớn/quá nhỏ, hoặc mô hình có đang học hay không.
    
- [ ] c) Để tính toán số lượng tham số.
    
- [ ] d) Chỉ để tạo ra các biểu đồ đẹp.
    

**Câu 46:** **So với Batch GD, đường cong chi phí của Mini-batch GD có đặc điểm gì?**

- [ ] a) Mượt mà và luôn đi xuống.
    
- [x] b) Có nhiều "nhiễu" (dao động) nhưng có xu hướng chung là đi xuống.
    
- [ ] c) Luôn đi lên.
    
- [ ] d) Là một đường thẳng.
    

**Câu 47:** **Trong công thức của Momentum, `β` thường được đặt giá trị là bao nhiêu?**

- [x] a) 0.9
    
- [ ] b) 0.999
    
- [ ] c) 0.5
    
- [ ] d) 1.0
    

**Câu 48:** **Việc sử dụng các framework như TensorFlow/PyTorch giúp các nhà nghiên cứu và kỹ sư tập trung vào đâu?**

- [ ] a) Tối ưu hóa các phép toán ma trận ở mức độ thấp.
    
- [x] b) Xây dựng kiến trúc mô hình và thử nghiệm các ý tưởng mới.
    
- [ ] c) Viết driver cho GPU.
    
- [ ] d) Quản lý bộ nhớ.
    

**Câu 49:** **Trong bài toán phân loại có 3 lớp (A, B, C), nếu đầu ra của lớp Softmax là `[0.1, 0.8, 0.1]`, dự đoán của mô hình là gì?**

- [ ] a) Lớp A
    
- [x] b) Lớp B
    
- [ ] c) Lớp C
    
- [ ] d) Không thể xác định.
    

**Câu 50:** **Đâu là một lý do khiến Batch Norm có thể làm cho mạng nơ-ron ít nhạy cảm hơn với việc khởi tạo trọng số?**

- [x] a) Vì nó chuẩn hóa các kích hoạt, giảm bớt ảnh hưởng của các trọng số ban đầu không tốt.
    
- [ ] b) Vì nó tự động khởi tạo các trọng số.
    
- [ ] c) Vì nó loại bỏ một nửa số trọng số.
    
- [ ] d) Vì nó làm cho tất cả các trọng số bằng nhau.
    

#### Bài kiểm tra trắc nghiệm: Mạng Nơ-ron Tích chập (CNN)

**Câu 1:** **Tại sao mạng nơ-ron truyền thẳng (fully-connected) thông thường không phù hợp với các hình ảnh có kích thước lớn?**

- [ ] a) Vì chúng không thể học được các đặc trưng phức tạp.
    
- [x] b) Vì số lượng tham số sẽ trở nên cực kỳ lớn, dễ gây overfitting và tốn kém về mặt tính toán.
    
- [ ] c) Vì chúng chỉ hoạt động với ảnh xám.
    
- [ ] d) Vì chúng yêu cầu phải có lớp pooling.
    

**Câu 2:** **Hai ưu điểm chính của Mạng Nơ-ron Tích chập (CNN) so với mạng nơ-ron thông thường là gì?**

- [ ] a) Vector hóa và Tốc độ học cao.
    
- [x] b) Chia sẻ tham số (Parameter sharing) và Kết nối thưa (Sparsity of connections).
    
- [ ] c) Lớp ẩn và Lớp đầu ra.
    
- [ ] d) Điều chuẩn hóa L2 và Dropout.
    

**Câu 3:** **"Parameter sharing" (Chia sẻ tham số) trong CNN có nghĩa là gì?**

- [ ] a) Mỗi nơ-ron trong một lớp có một bộ trọng số riêng.
    
- [x] b) Một bộ lọc (filter) với cùng một bộ trọng số được sử dụng để quét qua các vùng khác nhau của ảnh.
    
- [ ] c) Các lớp khác nhau chia sẻ cùng một bộ trọng số.
    
- [ ] d) Giảm số lượng tham số bằng cách chia sẻ chúng với một mô hình khác.
    

**Câu 4:** **"Sparsity of connections" (Kết nối thưa) trong CNN có nghĩa là gì?**

- [ ] a) Mỗi nơ-ron đầu ra chỉ kết nối với tất cả các nơ-ron đầu vào.
    
- [x] b) Mỗi nơ-ron đầu ra chỉ phụ thuộc vào một vùng nhỏ (local region) của các nơ-ron đầu vào.
    
- [ ] c) Một số kết nối bị loại bỏ ngẫu nhiên.
    
- [ ] d) Mạng có rất ít lớp.
    

**Câu 5:** **Mục đích chính của phép tích chập (convolution operation) trong CNN là gì?**

- [ ] a) Để giảm kích thước của ảnh.
    
- [ ] b) Để tăng độ sáng của ảnh.
    
- [x] c) Để trích xuất các đặc trưng (features) từ ảnh, chẳng hạn như các cạnh, góc, hoặc các hoa văn.
    
- [ ] d) Để phân loại ảnh.
    

**Câu 6:** **Trong một phép tích chập, "filter" (bộ lọc) hay "kernel" là gì?**

- [ ] a) Là ảnh đầu ra sau khi tích chập.
    
- [x] b) Là một ma trận các trọng số nhỏ được học để phát hiện một đặc trưng cụ thể.
    
- [ ] c) Là kích thước của ảnh đầu vào.
    
- [ ] d) Là một hàm kích hoạt.
    

**Câu 7:** **Lớp đầu tiên của một CNN thường học được các đặc trưng ở cấp độ nào?**

- [ ] a) Các đối tượng hoàn chỉnh như khuôn mặt, xe hơi.
    
- [ ] b) Các bộ phận của đối tượng như mắt, bánh xe.
    
- [x] c) Các đặc trưng đơn giản như các cạnh, góc, và màu sắc.
    
- [ ] d) Các câu văn hoàn chỉnh.
    

**Câu 8:** **Đầu ra của một phép tích chập được gọi là gì?**

- [ ] a) Vector trọng số.
    
- [ ] b) Lớp ẩn.
    
- [x] c) Bản đồ đặc trưng (Feature Map) hoặc Bản đồ kích hoạt (Activation Map).
    
- [ ] d) Lớp pooling.
    

**Câu 9:** **Một bộ lọc `[[1, 0, -1], [1, 0, -1], [1, 0, -1]]` được thiết kế để phát hiện loại đặc trưng nào?**

- [ ] a) Các cạnh ngang.
    
- [x] b) Các cạnh dọc.
    
- [ ] c) Các góc.
    
- [ ] d) Các vùng màu đỏ.
    

**Câu 10:** **Các giá trị trong các bộ lọc của CNN được xác định như thế nào?**

- [ ] a) Chúng được thiết lập thủ công bởi người lập trình.
    
- [x] b) Chúng được học tự động thông qua quá trình huấn luyện (sử dụng backpropagation).
    
- [ ] c) Chúng luôn là các số 0 và 1.
    
- [ ] d) Chúng được lấy ngẫu nhiên và không thay đổi.
    

**Câu 11:** **"Padding" trong CNN được sử dụng để giải quyết vấn đề gì?**

- [ ] a) Làm cho ảnh đầu vào lớn hơn.
    
- [ ] b) Giảm số lượng kênh màu.
    
- [x] c) Ngăn chặn việc kích thước đầu ra bị thu nhỏ và mất thông tin ở các cạnh của ảnh.
    
- [ ] d) Tăng tốc độ tính toán.
    

**Câu 12:** **"Valid Padding" có nghĩa là gì?**

- [ ] a) Thêm padding để kích thước đầu ra bằng kích thước đầu vào.
    
- [x] b) Không sử dụng padding (`p=0`).
    
- [ ] c) Chỉ thêm padding ở các cạnh hợp lệ.
    
- [ ] d) Thêm padding bằng các giá trị ngẫu nhiên.
    

**Câu 13:** **"Same Padding" có nghĩa là gì?**

- [ ] a) Không sử dụng padding.
    
- [x] b) Thêm một lượng padding sao cho kích thước chiều cao và chiều rộng của đầu ra bằng với đầu vào.
    
- [ ] c) Sử dụng cùng một giá trị padding cho tất cả các lớp.
    
- [ ] d) Sử dụng cùng một bộ lọc cho tất cả các lớp.
    

**Câu 14:** **"Stride" (bước nhảy) trong phép tích chập là gì?**

- [ ] a) Kích thước của bộ lọc.
    
- [x] b) Số lượng pixel mà bộ lọc dịch chuyển qua ảnh trong mỗi bước.
    
- [ ] c) Số lượng lớp trong mạng.
    
- [ ] d) Kích thước của padding.
    

**Câu 15:** **Nếu bạn thực hiện tích chập trên một ảnh màu RGB (có 3 kênh), chiều sâu (số kênh) của bộ lọc phải là bao nhiêu?**

- [ ] a) 1
    
- [x] b) 3
    
- [ ] c) Tùy ý.
    
- [ ] d) Bằng kích thước của bộ lọc (ví dụ: 3x3 thì chiều sâu là 3).
    

**Câu 16:** **Nếu bạn áp dụng 16 bộ lọc khác nhau vào một ảnh đầu vào, chiều sâu (số kênh) của bản đồ đặc trưng đầu ra sẽ là bao nhiêu?**

- [ ] a) 1
    
- [ ] b) 3
    
- [x] c) 16
    
- [ ] d) Bằng chiều sâu của ảnh đầu vào.
    

**Câu 17:** **Mục đích chính của lớp Pooling là gì?**

- [ ] a) Để tăng độ phân giải của bản đồ đặc trưng.
    
- [x] b) Để giảm kích thước không gian (chiều cao và rộng) của bản đồ đặc trưng, giúp giảm tính toán và kiểm soát overfitting.
    
- [ ] c) Để thêm các đặc trưng mới.
    
- [ ] d) Để học các bộ lọc.
    

**Câu 18:** **Max Pooling hoạt động như thế nào?**

- [ ] a) Lấy giá trị trung bình của các pixel trong một vùng.
    
- [x] b) Lấy giá trị lớn nhất của các pixel trong một vùng.
    
- [ ] c) Lấy giá trị nhỏ nhất của các pixel trong một vùng.
    
- [ ] d) Tính tổng các pixel trong một vùng.
    

**Câu 19:** **Lớp Pooling có các tham số cần học (như trọng số) không?**

- [ ] a) Có, nó có cả trọng số và độ lệch.
    
- [ ] b) Chỉ có trọng số.
    
- [x] c) Không, nó không có tham số nào để học.
    
- [ ] d) Chỉ có độ lệch.
    

**Câu 20:** **Đâu là các siêu tham số của một lớp Pooling?**

- [x] a) Kích thước bộ lọc (`f`) và bước nhảy (`s`).
    
- [ ] b) Tốc độ học và momentum.
    
- [ ] c) Số lượng lớp và số nơ-ron.
    
- [ ] d) Hàm kích hoạt và hàm chi phí.
    

**Câu 21:** **Ba loại lớp phổ biến nhất trong một kiến trúc CNN điển hình là gì?**

- [ ] a) Input, Hidden, Output.
    
- [x] b) Convolutional, Pooling, Fully Connected.
    
- [ ] c) ReLU, Sigmoid, Tanh.
    
- [ ] d) Adam, RMSprop, Momentum.
    

**Câu 22:** **Lớp Fully Connected (FC) thường được đặt ở đâu trong một CNN và có vai trò gì?**

- [ ] a) Ở đầu mạng, để tiền xử lý ảnh.
    
- [ ] b) Ở giữa các lớp CONV, để tăng tính phi tuyến.
    
- [x] c) Ở cuối mạng, để thực hiện việc phân loại cuối cùng dựa trên các đặc trưng đã được trích xuất.
    
- [ ] d) Nó không được sử dụng trong CNN.
    

**Câu 23:** **Khi đi sâu hơn vào một mạng CNN, kích thước không gian (chiều cao, rộng) và chiều sâu (số kênh) của các bản đồ đặc trưng thường thay đổi như thế nào?**

- [ ] a) Kích thước không gian tăng, chiều sâu giảm.
    
- [x] b) Kích thước không gian giảm, chiều sâu tăng.
    
- [ ] c) Cả hai đều tăng.
    
- [ ] d) Cả hai đều giảm.
    

**Câu 24:** **Một lớp CONV có 10 bộ lọc, mỗi bộ lọc có kích thước 3x3x3. Lớp này có bao nhiêu tham số (chỉ tính trọng số, không tính bias)?**

- [ ] a) 90
    
- [ ] b) 27
    
- [x] c) 270
    
- [ ] d) 30
    

**Câu 25:** **Tiếp câu 24, nếu mỗi bộ lọc có thêm 1 tham số bias, tổng số tham số có thể học được trong lớp đó là bao nhiêu?**

- [x] a) 280
    
- [ ] b) 271
    
- [ ] c) 100
    
- [ ] d) 37
    

**Câu 26:** **Cho ảnh đầu vào 7x7, bộ lọc 3x3, padding `p=0`, stride `s=1`. Kích thước đầu ra là bao nhiêu?**

- [ ] a) 7x7
    
- [ ] b) 6x6
    
- [x] c) 5x5
    
- [ ] d) 4x4
    

**Câu 27:** **Cho ảnh đầu vào 7x7, bộ lọc 3x3, padding `p=0`, stride `s=2`. Kích thước đầu ra là bao nhiêu?**

- [x] a) 3x3
    
- [ ] b) 4x4
    
- [ ] c) 2x2
    
- [ ] d) 5x5
    

**Câu 28:** **Cho ảnh đầu vào 10x10, bộ lọc 5x5, stride `s=1`. Cần padding `p` bằng bao nhiêu để có "Same Padding"?**

- [ ] a) 0
    
- [ ] b) 1
    
- [x] c) 2
    
- [ ] d) 3
    

**Câu 29:** **Một bản đồ đặc trưng 4x4 được đưa vào một lớp Max Pooling 2x2 với stride `s=2`. Kích thước đầu ra là bao nhiêu?**

- [ ] a) 4x4
    
- [ ] b) 3x3
    
- [x] c) 2x2
    
- [ ] d) 1x1
    

**Câu 30:** **Một lớp CONV có đầu vào là 14x14x6, sử dụng 16 bộ lọc 5x5 với stride `s=1` và padding `p=0`. Kích thước đầu ra là bao nhiêu?**

- [x] a) 10x10x16
    
- [ ] b) 14x14x16
    
- [ ] c) 10x10x6
    
- [ ] d) 9x9x16
    

**Câu 31:** **Tại sao CNN có khả năng bất biến với sự dịch chuyển (translation invariance) ở một mức độ nào đó?**

- [ ] a) Vì nó sử dụng hàm kích hoạt ReLU.
    
- [x] b) Vì các đặc trưng được phát hiện bởi một bộ lọc không phụ thuộc vào vị trí của chúng trên ảnh, và lớp pooling giúp làm mờ đi các khác biệt nhỏ về vị trí.
    
- [ ] c) Vì nó luôn chuẩn hóa dữ liệu đầu vào.
    
- [ ] d) Vì nó có các lớp fully connected.
    

**Câu 32:** **Trong các thư viện học sâu, phép toán "convolution" thực chất thường là phép toán nào trong xử lý tín hiệu?**

- [ ] a) Tích chập (Convolution).
    
- [x] b) Tương quan chéo (Cross-correlation).
    
- [ ] c) Biến đổi Fourier.
    
- [ ] d) Phép cộng.
    

**Câu 33:** **Lớp tích chập 1x1 (1x1 Convolution) thường được sử dụng để làm gì?**

- [ ] a) Để phát hiện các cạnh.
    
- [ ] b) Chỉ để giảm chiều cao và rộng.
    
- [x] c) Để thay đổi số lượng kênh (chiều sâu) của bản đồ đặc trưng một cách hiệu quả về mặt tính toán.
    
- [ ] d) Nó không có tác dụng gì.
    

**Câu 34:** **Hàm kích hoạt (ví dụ: ReLU) được đặt ở đâu trong một lớp CONV?**

- [ ] a) Trước phép tích chập.
    
- [x] b) Sau phép tích chập và sau khi cộng bias.
    
- [ ] c) Chỉ ở lớp cuối cùng.
    
- [ ] d) Thay thế cho lớp pooling.
    

**Câu 35:** **Đâu là một nhược điểm của lớp Pooling?**

- [ ] a) Tăng số lượng tham số.
    
- [x] b) Gây mất mát thông tin không gian.
    
- [ ] c) Làm cho quá trình huấn luyện chậm lại.
    
- [ ] d) Không tương thích với lớp CONV.
    

**Câu 36:** **Tại sao việc xếp chồng nhiều lớp với bộ lọc nhỏ (ví dụ: hai lớp 3x3) thường tốt hơn một lớp với bộ lọc lớn (ví dụ: một lớp 5x5)?**

- [x] a) Nó có ít tham số hơn và có thể học được các hàm phức tạp hơn do có nhiều lớp phi tuyến hơn.
    
- [ ] b) Nó có nhiều tham số hơn.
    
- [ ] c) Nó chạy nhanh hơn.
    
- [ ] d) Nó dễ lập trình hơn.
    

**Câu 37:** **"Flattening" một lớp trong CNN có nghĩa là gì?**

- [ ] a) Làm cho các giá trị trong lớp bằng 0.
    
- [x] b) Chuyển đổi một bản đồ đặc trưng đa chiều (ví dụ: 7x7x40) thành một vector phẳng (1D) để đưa vào lớp Fully Connected.
    
- [ ] c) Áp dụng một bộ lọc làm mờ.
    
- [ ] d) Giảm số lượng kênh.
    

**Câu 38:** **Ngoài phân loại ảnh, CNN còn có thể được sử dụng cho tác vụ nào khác?**

- [ ] a) Phát hiện vật thể (Object Detection).
    
- [ ] b) Phân đoạn ảnh (Image Segmentation).
    
- [ ] c) Xử lý ngôn ngữ tự nhiên (trên dữ liệu văn bản 1D).
    
- [x] d) Tất cả các câu trên.
    

**Câu 39:** **Mối quan hệ giữa kích thước bộ lọc, padding, stride và kích thước đầu ra được mô tả bằng công thức nào?**

- [x] a) `output_size = (n + 2p - f) / s + 1`
    
- [ ] b) `output_size = (n - 2p + f) / s + 1`
    
- [ ] c) `output_size = (n + p - f) / s`
    
- [ ] d) `output_size = n - f + 1`
    

**Câu 40:** **Sự khác biệt chính giữa Max Pooling và Average Pooling là gì?**

- [x] a) Max Pooling giữ lại đặc trưng nổi bật nhất (mạnh nhất), trong khi Average Pooling giữ lại thông tin trung bình của đặc trưng.
    
- [ ] b) Max Pooling nhanh hơn Average Pooling.
    
- [ ] c) Average Pooling có các tham số cần học.
    
- [ ] d) Không có sự khác biệt đáng kể.
    

**Câu 41:** **Nếu bạn tăng số lượng bộ lọc trong một lớp CONV, điều gì sẽ xảy ra?**

- [ ] a) Số lượng tham số trong lớp đó sẽ tăng.
    
- [ ] b) Chiều sâu của bản đồ đặc trưng đầu ra sẽ tăng.
    
- [ ] c) Khả năng của lớp đó để học nhiều loại đặc trưng khác nhau sẽ tăng.
    
- [x] d) Tất cả các câu trên đều đúng.
    

**Câu 42:** **Lớp cuối cùng của một CNN cho bài toán phân loại 10 chữ số (0-9) thường là gì?**

- [ ] a) Một lớp CONV với 10 bộ lọc.
    
- [ ] b) Một lớp Max Pooling.
    
- [x] c) Một lớp Fully Connected với 10 nơ-ron và hàm kích hoạt Softmax.
    
- [ ] d) Một lớp Fully Connected với 1 nơ-ron và hàm kích hoạt Sigmoid.
    

**Câu 43:** **Tại sao CNN lại đặc biệt phù hợp với dữ liệu hình ảnh?**

- [ ] a) Vì ảnh có thể được biểu diễn dưới dạng số.
    
- [x] b) Vì CNN có khả năng bảo toàn và tận dụng các mối quan hệ không gian giữa các pixel (tính cục bộ).
    
- [ ] c) Vì CNN luôn cho độ chính xác 100%.
    
- [ ] d) Vì CNN yêu cầu ít dữ liệu hơn các mô hình khác.
    

**Câu 44:** **Trong một kiến trúc CNN, lớp nào chịu trách nhiệm chính cho việc học các đặc trưng?**

- [ ] a) Lớp Pooling.
    
- [ ] b) Lớp Fully Connected.
    
- [x] c) Lớp Convolutional.
    
- [ ] d) Lớp Input.
    

**Câu 45:** **Trong một kiến trúc CNN, lớp nào chịu trách nhiệm chính cho việc giảm kích thước?**

- [x] a) Lớp Pooling và các lớp CONV có stride > 1.
    
- [ ] b) Lớp Fully Connected.
    
- [ ] c) Lớp Convolutional có stride = 1.
    
- [ ] d) Lớp Input.
    

**Câu 46:** **"Receptive field" (trường tiếp nhận) của một nơ-ron trong CNN là gì?**

- [ ] a) Toàn bộ ảnh đầu vào.
    
- [x] b) Vùng trên ảnh đầu vào mà nơ-ron đó "nhìn thấy" hoặc bị ảnh hưởng bởi.
    
- [ ] c) Kích thước của bộ lọc.
    
- [ ] d) Số lượng nơ-ron trong lớp.
    

**Câu 47:** **Nếu bạn xếp chồng hai lớp CONV 3x3 (stride 1), trường tiếp nhận của một nơ-ron ở lớp thứ hai sẽ có kích thước bao nhiêu trên đầu vào của lớp đầu tiên?**

- [ ] a) 3x3
    
- [ ] b) 4x4
    
- [x] c) 5x5
    
- [ ] d) 6x6
    

**Câu 48:** **Đâu không phải là một siêu tham số của một lớp CONV?**

- [ ] a) Kích thước bộ lọc (`f`).
    
- [ ] b) Số lượng bộ lọc (`nC`).
    
- [ ] c) Bước nhảy (`s`).
    
- [x] d) Ma trận trọng số (`W`).
    

**Câu 49:** **Trong TensorFlow Keras, lớp nào được sử dụng để tạo một lớp tích chập 2D?**

- [ ] a) `tf.keras.layers.Dense`
    
- [x] b) `tf.keras.layers.Conv2D`
    
- [ ] c) `tf.keras.layers.MaxPooling2D`
    
- [ ] d) `tf.keras.layers.Flatten`
    

**Câu 50:** **Đâu là một kiến trúc CNN nổi tiếng?**

- [ ] a) Logistic Regression
    
- [ ] b) Support Vector Machine
    
- [x] c) LeNet-5, AlexNet, VGG
    
- [ ] d) K-Means
    

#### Bài kiểm tra trắc nghiệm: Các Kiến trúc CNN kinh điển và Kỹ thuật Nâng cao

**Câu 1:** **Kiến trúc LeNet-5 ban đầu được thiết kế cho tác vụ chính nào?**

- [ ] a) Nhận dạng vật thể trong ảnh màu.
    
- [x] b) Nhận dạng chữ số viết tay.
    
- [ ] c) Phân đoạn ảnh y tế.
    
- [ ] d) Dịch máy.
    

**Câu 2:** **Đặc điểm nào sau đây không phải của LeNet-5?**

- [ ] a) Sử dụng các lớp tích chập và pooling xen kẽ.
    
- [ ] b) Có khoảng 60,000 tham số.
    
- [x] c) Sử dụng hàm kích hoạt ReLU trong tất cả các lớp.
    
- [ ] d) Chiều cao và rộng của ảnh giảm dần khi đi sâu vào mạng.
    

**Câu 3:** **AlexNet đã mang lại cải tiến đột phá nào so với các kiến trúc trước đó?**

- [ ] a) Sử dụng hàm kích hoạt Sigmoid/tanh.
    
- [ ] b) Là mạng nơ-ron nông đầu tiên.
    
- [x] c) Sử dụng hàm kích hoạt ReLU và kỹ thuật Dropout để chống overfitting.
    
- [ ] d) Có ít tham số hơn LeNet-5.
    

**Câu 4:** **Kiến trúc VGG-16 nổi tiếng với đặc điểm nào?**

- [ ] a) Sử dụng nhiều kích thước bộ lọc khác nhau trong cùng một lớp.
    
- [ ] b) Rất nông nhưng có nhiều tham số.
    
- [ ] c) Sử dụng các kết nối tắt (skip connections).
    
- [x] d) Sử dụng một kiến trúc rất đồng nhất, chủ yếu là các lớp tích chập 3x3 được xếp chồng lên nhau.
    

**Câu 5:** **Tại sao việc xếp chồng hai lớp CONV 3x3 lại được ưa chuộng trong VGG thay vì một lớp CONV 5x5?**

- [ ] a) Nó có nhiều tham số hơn, giúp học tốt hơn.
    
- [x] b) Nó có ít tham số hơn và tăng độ sâu phi tuyến của mạng.
    
- [ ] c) Nó chỉ hoạt động với ảnh xám.
    
- [ ] d) Nó tính toán nhanh hơn đáng kể.
    

**Câu 6:** **Số lượng tham số của AlexNet so với LeNet-5 như thế nào?**

- [ ] a) Ít hơn đáng kể.
    
- [ ] b) Tương đương nhau.
    
- [x] c) Nhiều hơn đáng kể (khoảng 60 triệu so với 60 nghìn).
    
- [ ] d) Gấp đôi.
    

**Câu 7:** **Trong AlexNet, Dropout được sử dụng ở các lớp nào?**

- [ ] a) Các lớp tích chập.
    
- [ ] b) Các lớp pooling.
    
- [x] c) Các lớp fully-connected.
    
- [ ] d) Lớp đầu vào.
    

**Câu 8:** **Thứ tự các loại lớp trong LeNet-5 là gì?**

- [ ] a) CONV -> CONV -> POOL -> POOL -> FC -> FC
    
- [x] b) CONV -> POOL -> CONV -> POOL -> FC -> FC
    
- [ ] c) FC -> FC -> CONV -> POOL -> CONV -> POOL
    
- [ ] d) CONV -> FC -> POOL -> CONV -> FC -> POOL
    

**Câu 9:** **VGG-16 có bao nhiêu lớp có trọng số (convolutional và fully-connected)?**

- [ ] a) 8
    
- [x] b) 16
    
- [ ] c) 19
    
- [ ] d) 22
    

**Câu 10:** **Điểm chung của LeNet-5, AlexNet, và VGG là gì?**

- [ ] a) Tất cả đều sử dụng kết nối tắt (skip connections).
    
- [x] b) Cấu trúc chung là các lớp CONV/POOL xếp chồng lên nhau, theo sau là các lớp FC để phân loại.
    
- [ ] c) Tất cả đều được thiết kế cho các thiết bị di động.
    
- [ ] d) Tất cả đều có ít hơn 1 triệu tham số.
    

**Câu 11:** **Vấn đề chính mà Mạng Residual (ResNet) được thiết kế để giải quyết là gì?**

- [ ] a) Tốc độ tính toán chậm.
    
- [x] b) Vấn đề gradient biến mất (vanishing gradients) trong các mạng rất sâu.
    
- [ ] c) Overfitting trong các mạng nông.
    
- [ ] d) Thiếu dữ liệu huấn luyện.
    

**Câu 12:** **Cơ chế cốt lõi của một khối Residual (Residual Block) là gì?**

- [ ] a) Sử dụng các bộ lọc 1x1.
    
- [x] b) Sử dụng một kết nối tắt (skip connection) để cộng đầu vào của khối với đầu ra của nó.
    
- [ ] c) Loại bỏ ngẫu nhiên các nơ-ron.
    
- [ ] d) Sử dụng nhiều kích thước bộ lọc song song.
    

**Câu 13:** **Tại sao ResNet có thể huấn luyện các mạng cực kỳ sâu (hơn 100 lớp) mà không làm tăng lỗi huấn luyện?**

- [ ] a) Vì nó có ít tham số hơn.
    
- [x] b) Vì kết nối tắt giúp các lớp dễ dàng học một hàm đồng nhất (identity function), đảm bảo việc thêm lớp mới không làm giảm hiệu suất.
    
- [ ] c) Vì nó chỉ sử dụng các bộ lọc 1x1.
    
- [ ] d) Vì nó không sử dụng backpropagation.
    

**Câu 14:** **Mục đích của việc sử dụng các lớp tích chập 1x1 trong kiến trúc "Network in Network" và Inception là gì?**

- [ ] a) Để tăng kích thước không gian của bản đồ đặc trưng.
    
- [x] b) Để giảm số lượng kênh (chiều sâu) một cách hiệu quả, hoạt động như một "bottleneck" để giảm chi phí tính toán.
    
- [ ] c) Chỉ để phát hiện các cạnh dọc.
    
- [ ] d) Để thay thế hoàn toàn các lớp pooling.
    

**Câu 15:** **Ý tưởng chính đằng sau mạng Inception là gì?**

- [ ] a) Chỉ sử dụng các lớp 3x3 để đơn giản hóa kiến trúc.
    
- [ ] b) Xếp chồng các khối residual lên nhau.
    
- [x] c) Thực hiện song song nhiều phép tích chập với các kích thước bộ lọc khác nhau (1x1, 3x3, 5x5) và cả pooling trong cùng một module, sau đó ghép kết quả lại.
    
- [ ] d) Sử dụng một mạng rất nông để tăng tốc độ.
    

**Câu 16:** **Mạng MobileNet được thiết kế để tối ưu cho môi trường nào?**

- [ ] a) Các siêu máy tính.
    
- [x] b) Các thiết bị di động và nhúng có tài nguyên tính toán hạn chế.
    
- [ ] c) Chỉ cho các bài toán xử lý văn bản.
    
- [ ] d) Các máy chủ đám mây với GPU mạnh mẽ.
    

**Câu 17:** **Kỹ thuật cốt lõi được sử dụng trong MobileNet để giảm chi phí tính toán là gì?**

- [ ] a) Kết nối tắt (Skip connections).
    
- [x] b) Tích chập tách biệt theo chiều sâu (Depthwise Separable Convolutions).
    
- [ ] c) Dropout.
    
- [ ] d) Data Augmentation.
    

**Câu 18:** **Một phép tích chập tách biệt theo chiều sâu bao gồm hai bước nào?**

- [x] a) Depthwise Convolution và 1x1 Pointwise Convolution.
    
- [ ] b) Max Pooling và Average Pooling.
    
- [ ] c) Convolution và Deconvolution.
    
- [ ] d) Forward Propagation và Backward Propagation.
    

**Câu 19:** **Kiến trúc MobileNetV2 đã cải tiến MobileNetV1 bằng cách thêm vào yếu tố nào?**

- [ ] a) Các bộ lọc 7x7.
    
- [x] b) Các khối bottleneck ngược với kết nối residual.
    
- [ ] c) Loại bỏ tất cả các lớp 1x1.
    
- [ ] d) Chỉ sử dụng hàm kích hoạt Sigmoid.
    

**Câu 20:** **Ý tưởng chính của EfficientNet là gì?**

- [ ] a) Chỉ tăng độ sâu của mạng.
    
- [ ] b) Chỉ tăng độ rộng của mạng.
    
- [x] c) Sử dụng một phương pháp "compound scaling" để cân bằng và tăng đồng thời cả độ sâu, độ rộng và độ phân giải của mạng.
    
- [ ] d) Sử dụng một kiến trúc hoàn toàn khác so với các CNN trước đó.
    

**Câu 21:** **"Transfer Learning" (Học chuyển giao) là kỹ thuật gì?**

- [ ] a) Huấn luyện một mô hình từ đầu trên một tập dữ liệu mới.
    
- [x] b) Sử dụng kiến thức (các trọng số đã được huấn luyện) từ một mô hình đã được huấn luyện trên một tác vụ lớn để áp dụng cho một tác vụ mới, thường có ít dữ liệu hơn.
    
- [ ] c) Chuyển đổi một mô hình từ TensorFlow sang PyTorch.
    
- [ ] d) Chỉ sử dụng các lớp cuối cùng của một mạng đã được huấn luyện.
    

**Câu 22:** **Khi nào thì Transfer Learning có khả năng hoạt động hiệu quả nhất?**

- [ ] a) Khi tác vụ nguồn có ít dữ liệu hơn tác vụ đích.
    
- [ ] b) Khi hai tác vụ có cùng một đầu vào (ví dụ: cùng là ảnh) và tác vụ nguồn có lượng dữ liệu lớn hơn nhiều.
    
- [x] c) Khi hai tác vụ hoàn toàn không liên quan đến nhau.
    
- [ ] d) Khi bạn không có GPU.
    

**Câu 23:** **Trong Transfer Learning, "fine-tuning" (tinh chỉnh) có nghĩa là gì?**

- [ ] a) Chỉ huấn luyện lớp đầu ra mới và giữ nguyên tất cả các lớp khác.
    
- [ ] b) Huấn luyện lại toàn bộ mạng với tốc độ học rất lớn.
    
- [x] c) "Rã đông" (unfreeze) một vài lớp cuối của mô hình đã được huấn luyện trước và tiếp tục huấn luyện chúng với tốc độ học nhỏ trên dữ liệu mới.
    
- [ ] d) Thay đổi kiến trúc của mô hình.
    

**Câu 24:** **"Data Augmentation" (Tăng cường dữ liệu) được sử dụng để làm gì?**

- [ ] a) Để giảm số lượng dữ liệu huấn luyện.
    
- [ ] b) Để tăng tốc độ huấn luyện.
    
- [x] c) Để tạo ra các mẫu dữ liệu huấn luyện mới một cách nhân tạo, giúp mô hình khái quát hóa tốt hơn và giảm overfitting.
    
- [ ] d) Để gán nhãn cho dữ liệu.
    

**Câu 25:** **Đâu là một kỹ thuật Data Augmentation phổ biến cho dữ liệu hình ảnh?**

- [ ] a) Lật ảnh theo chiều ngang (Mirroring).
    
- [ ] b) Cắt xén ngẫu nhiên (Random Cropping).
    
- [ ] c) Thay đổi màu sắc (Color shifting).
    
- [x] d) Tất cả các câu trên.
    

**Câu 26:** **"Ensembling" là kỹ thuật gì để cải thiện hiệu suất?**

- [ ] a) Sử dụng một mô hình duy nhất nhưng rất sâu.
    
- [x] b) Huấn luyện nhiều mô hình độc lập và lấy trung bình kết quả dự đoán của chúng.
    
- [ ] c) Tăng cường dữ liệu huấn luyện.
    
- [ ] d) Sử dụng một thuật toán tối ưu hóa khác.
    

**Câu 27:** **"Multi-crop at test time" là gì?**

- [x] a) Áp dụng data augmentation cho tập test (ví dụ: tạo nhiều phiên bản cắt xén của ảnh test) và lấy trung bình dự đoán để có kết quả cuối cùng ổn định hơn.
    
- [ ] b) Chỉ huấn luyện mô hình trên các ảnh đã được cắt xén.
    
- [ ] c) Cắt bỏ các phần không quan trọng của ảnh test.
    
- [ ] d) Sử dụng nhiều tập test khác nhau.
    

**Câu 28:** **Khi bạn có một tập dữ liệu rất nhỏ cho tác vụ của mình, chiến lược nào sau đây là hiệu quả nhất?**

- [ ] a) Huấn luyện một mạng rất lớn từ đầu.
    
- [x] b) Sử dụng Transfer Learning từ một mô hình đã được huấn luyện trước (pre-trained model).
    
- [ ] c) Chỉ sử dụng các mô hình tuyến tính.
    
- [ ] d) Không sử dụng lớp ẩn nào.
    

**Câu 29:** **Tại sao Data Augmentation lại giúp chống overfitting?**

- [ ] a) Vì nó làm cho mô hình trở nên phức tạp hơn.
    
- [ ] b) Vì nó làm cho tập dữ liệu huấn luyện trở nên đa dạng hơn, buộc mô hình phải học các đặc trưng bất biến và khái quát hơn.
    
- [x] c) Vì nó giảm số lượng tham số.
    
- [ ] d) Vì nó làm giảm tốc độ học.
    

**Câu 30:** **Khi thực hiện Transfer Learning, bạn thường thay thế phần nào của mạng đã được huấn luyện trước?**

- [ ] a) Các lớp tích chập đầu tiên.
    
- [x] b) Lớp đầu ra (ví dụ: lớp Softmax).
    
- [ ] c) Các lớp pooling.
    
- [ ] d) Tất cả các lớp.
    

**Câu 31:** **Tại sao việc nghiên cứu các "case studies" (các kiến trúc đã thành công) lại quan trọng?**

- [ ] a) Để sao chép y hệt code của người khác.
    
- [x] b) Để có được những ý tưởng và trực giác về cách kết hợp các khối xây dựng (CONV, POOL, FC) một cách hiệu quả.
    
- [ ] c) Vì không có cách nào khác để xây dựng một mạng nơ-ron.
    
- [ ] d) Chỉ để biết về lịch sử của học sâu.
    

**Câu 32:** **Đặc điểm chung của các kiến trúc CNN hiện đại (VGG, ResNet, Inception) là gì?**

- [ ] a) Chúng rất nông.
    
- [x] b) Chúng có xu hướng ngày càng sâu hơn.
    
- [ ] c) Chúng không sử dụng lớp fully-connected.
    
- [ ] d) Chúng chỉ hoạt động trên ảnh xám.
    

**Câu 33:** **Trong một khối residual, nếu kích thước của đầu vào và đầu ra khác nhau, bạn cần làm gì với kết nối tắt?**

- [ ] a) Không thể sử dụng kết nối tắt.
    
- [x] b) Thêm một lớp tích chập 1x1 (hoặc một phép chiếu tuyến tính) vào kết nối tắt để làm cho kích thước khớp nhau.
    
- [ ] c) Thêm padding vào đầu vào.
    
- [ ] d) Sử dụng Average Pooling.
    

**Câu 34:** **Trong MobileNet, "pointwise convolution" thực chất là loại tích chập nào?**

- [ ] a) Tích chập 3x3.
    
- [ ] b) Tích chập 5x5.
    
- [x] c) Tích chập 1x1.
    
- [ ] d) Max Pooling.
    

**Câu 35:** **"Depthwise convolution" khác với tích chập tiêu chuẩn như thế nào?**

- [ ] a) Nó áp dụng một bộ lọc duy nhất cho tất cả các kênh đầu vào.
    
- [x] b) Nó áp dụng một bộ lọc riêng cho từng kênh đầu vào một cách độc lập.
    
- [ ] c) Nó không có trọng số.
    
- [ ] d) Nó chỉ hoạt động trên dữ liệu 1D.
    

**Câu 36:** **Trong các tác vụ Thị giác máy tính (Computer Vision), nguồn kiến thức của một thuật toán học máy đến từ đâu?**

- [ ] a) Chỉ từ dữ liệu được gán nhãn.
    
- [ ] b) Chỉ từ các đặc trưng được thiết kế thủ công.
    
- [x] c) Cả từ dữ liệu được gán nhãn và từ các kiến trúc/thành phần được thiết kế thủ công.
    
- [ ] d) Từ các siêu tham số.
    

**Câu 37:** **Khi lượng dữ liệu có sẵn rất lớn, xu hướng trong thiết kế mô hình là gì?**

- [ ] a) Dựa nhiều hơn vào các đặc trưng được thiết kế thủ công.
    
- [x] b) Sử dụng các kiến trúc đơn giản hơn và để "dữ liệu tự lên tiếng".
    
- [ ] c) Sử dụng các mô hình nhỏ hơn.
    
- [ ] d) Giảm số lượng lớp.
    

**Câu 38:** **Đâu là một lý do khiến MobileNet hiệu quả hơn về mặt tính toán so với một CNN tiêu chuẩn?**

- [ ] a) Nó sâu hơn.
    
- [x] b) Tích chập tách biệt theo chiều sâu tách một phép tích chập lớn thành hai phép tích chập nhỏ hơn, làm giảm đáng kể tổng số phép tính.
    
- [ ] c) Nó sử dụng nhiều lớp fully-connected hơn.
    
- [ ] d) Nó không sử dụng hàm kích hoạt.
    

**Câu 39:** **Kiến trúc nào giới thiệu khái niệm "bottleneck layer" sử dụng tích chập 1x1 để giảm chiều dữ liệu trước khi thực hiện các phép tích chập tốn kém hơn?**

- [ ] a) LeNet-5
    
- [ ] b) AlexNet
    
- [x] c) Inception
    
- [ ] d) VGG
    

**Câu 40:** **"Fine-tuning" một mô hình thường hiệu quả hơn huấn luyện từ đầu khi nào?**

- [ ] a) Khi bạn có một tập dữ liệu cực lớn.
    
- [x] b) Khi bạn có một tập dữ liệu nhỏ và tác vụ của bạn tương tự như tác vụ mà mô hình đã được huấn luyện trước đó.
    
- [ ] c) Khi bạn có rất nhiều tài nguyên tính toán.
    
- [ ] d) Khi bạn muốn tạo ra một kiến trúc hoàn toàn mới.
    

**Câu 41:** **Trong kiến trúc ResNet, hàm kích hoạt ReLU thường được đặt ở đâu trong một khối residual?**

- [ ] a) Chỉ ở đầu khối.
    
- [ ] b) Chỉ ở cuối khối.
    
- [x] c) Sau mỗi lớp tích chập và sau phép cộng của kết nối tắt.
    
- [ ] d) Không sử dụng ReLU.
    

**Câu 42:** **Tại sao các mô hình CNN hiện đại thường loại bỏ hoặc giảm thiểu số lượng các lớp fully-connected lớn ở cuối?**

- [ ] a) Vì các lớp FC không thể học được gì.
    
- [x] b) Vì các lớp FC chứa một lượng lớn tham số, dễ gây overfitting và làm tăng kích thước mô hình.
    
- [ ] c) Vì các lớp CONV có thể thực hiện việc phân loại.
    
- [ ] d) Vì các lớp FC quá nhanh.
    

**Câu 43:** **Đâu là một ví dụ về việc "cross-fertilizing" ý tưởng trong học sâu?**

- [ ] a) Chỉ sử dụng các ý tưởng từ lĩnh vực thị giác máy tính cho các bài toán thị giác máy tính.
    
- [x] b) Áp dụng các ý tưởng từ kiến trúc CNN (như ResNet) cho các mô hình trong xử lý ngôn ngữ tự nhiên (như Transformer).
    
- [ ] c) Chỉ sử dụng một kiến trúc duy nhất cho mọi bài toán.
    
- [ ] d) Luôn huấn luyện mô hình từ đầu.
    

**Câu 44:** **Khi thực hiện data augmentation, điều quan trọng cần đảm bảo là gì?**

- [ ] a) Các phép biến đổi phải làm thay đổi hoàn toàn đối tượng trong ảnh.
    
- [x] b) Các phép biến đổi phải giữ nguyên nhãn của ảnh (ví dụ: lật ảnh một con mèo vẫn phải là một con mèo).
    
- [ ] c) Chỉ áp dụng một loại biến đổi duy nhất.
    
- [ ] d) Áp dụng các phép biến đổi cho cả tập train và tập test.
    

**Câu 45:** **Trong MobileNetV2, lớp "expansion" có vai trò gì?**

- [ ] a) Giảm số lượng kênh.
    
- [x] b) Tăng số lượng kênh bằng tích chập 1x1 trước khi thực hiện depthwise convolution.
    
- [ ] c) Thực hiện max pooling.
    
- [ ] d) Thay thế hàm kích hoạt.
    

**Câu 46:** **Đâu là một thách thức khi so sánh hiệu suất của các kiến trúc CNN khác nhau?**

- [ ] a) Số lượng tham số.
    
- [ ] b) Tốc độ suy luận (inference speed).
    
- [ ] c) Độ chính xác trên một tập dữ liệu chuẩn.
    
- [x] d) Tất cả các yếu tố trên đều cần được xem xét.
    

**Câu 47:** **Tên gọi "Inception" được lấy cảm hứng từ đâu?**

- [ ] a) Tên của nhà khoa học đã phát minh ra nó.
    
- [x] b) Một bộ phim khoa học viễn tưởng.
    
- [ ] c) Một thuật ngữ toán học.
    
- [ ] d) Tên của một công ty.
    

**Câu 48:** **Việc sử dụng các mô hình đã được huấn luyện trước (pre-trained models) từ các kho mã nguồn mở có lợi ích gì?**

- [ ] a) Tiết kiệm thời gian và tài nguyên tính toán.
    
- [ ] b) Tận dụng được các kiến trúc đã được chứng minh là hiệu quả.
    
- [ ] c) Cung cấp một điểm khởi đầu tốt cho các tác vụ với dữ liệu hạn chế.
    
- [x] d) Tất cả các câu trên.
    

**Câu 49:** **Kiến trúc nào sau đây không sử dụng kết nối tắt (skip connection)?**

- [ ] a) ResNet
    
- [ ] b) MobileNetV2
    
- [x] c) VGG-16
    
- [ ] d) EfficientNet
    

**Câu 50:** **Xu hướng chung trong các kiến trúc CNN từ LeNet đến EfficientNet là gì?**

- [ ] a) Mạng ngày càng nông và rộng hơn.
    
- [x] b) Mạng ngày càng sâu hơn, phức tạp hơn nhưng cũng hiệu quả hơn về mặt tính toán.
    
- [ ] c) Mạng ngày càng có nhiều lớp fully-connected hơn.
    
- [ ] d) Mạng ngày càng ít sử dụng các lớp tích chập hơn.
    

#### Bài kiểm tra trắc nghiệm: Các ứng dụng CNN Nâng cao

**Câu 1:** **Sự khác biệt chính giữa "Image Classification" và "Classification with Localization" là gì?**

- [ ] a) Classification chỉ cho biết có đối tượng hay không, còn Localization cho biết có bao nhiêu đối tượng.
    
- [x] b) Classification chỉ dự đoán lớp của đối tượng, còn Localization còn dự đoán thêm một hộp giới hạn (bounding box) xung quanh đối tượng.
    
- [ ] c) Localization nhanh hơn Classification.
    
- [ ] d) Chúng là hai tên gọi khác nhau cho cùng một bài toán.
    

**Câu 2:** **Một hộp giới hạn (bounding box) thường được tham số hóa bởi những giá trị nào?**

- [ ] a) Tọa độ góc trên bên trái (x1, y1) và góc dưới bên phải (x2, y2).
    
- [x] b) Tọa độ điểm trung tâm (bx, by), chiều cao (bh), và chiều rộng (bw).
    
- [ ] c) Chỉ chiều cao và chiều rộng.
    
- [ ] d) Tên của đối tượng bên trong hộp.
    

**Câu 3:** **"Landmark detection" (Phát hiện điểm mốc) là bài toán gì?**

- [ ] a) Phát hiện các địa danh nổi tiếng trong ảnh.
    
- [x] b) Xác định các điểm chính, quan trọng trên một đối tượng (ví dụ: các góc mắt, chóp mũi trên khuôn mặt).
    
- [ ] c) Vẽ một hộp giới hạn xung quanh đối tượng.
    
- [ ] d) Phân loại đối tượng.
    

**Câu 4:** **Thuật toán "Sliding Windows Detection" hoạt động như thế nào?**

- [ ] a) Phóng to các cửa sổ trong ảnh để xem chi tiết.
    
- [x] b) Trượt một cửa sổ (vùng chữ nhật) qua toàn bộ ảnh và dùng một bộ phân loại để xác định xem có đối tượng trong cửa sổ đó không.
    
- [ ] c) Chỉ nhìn vào trung tâm của ảnh.
    
- [ ] d) Chia ảnh thành các vùng ngẫu nhiên.
    

**Câu 5:** **Nhược điểm chính của thuật toán Sliding Windows truyền thống là gì?**

- [ ] a) Độ chính xác thấp.
    
- [x] b) Chi phí tính toán rất cao do phải chạy bộ phân loại trên rất nhiều cửa sổ.
    
- [ ] c) Chỉ hoạt động với ảnh xám.
    
- [ ] d) Không thể phát hiện các đối tượng nhỏ.
    

**Câu 6:** **Làm thế nào để biến một lớp Fully Connected (FC) thành một lớp Tích chập (CONV)?**

- [ ] a) Không thể làm được.
    
- [x] b) Bằng cách sử dụng một bộ lọc có cùng kích thước với đầu vào của lớp FC đó (ví dụ: đầu vào 5x5x16 thì dùng bộ lọc 5x5x16).
    
- [ ] c) Bằng cách sử dụng một bộ lọc 1x1.
    
- [ ] d) Bằng cách thêm một lớp pooling.
    

**Câu 7:** **Ưu điểm của việc triển khai Sliding Windows bằng phép tích chập là gì?**

- [ ] a) Tăng độ chính xác của hộp giới hạn.
    
- [x] b) Cho phép chia sẻ một lượng lớn các phép tính giữa các cửa sổ chồng chéo, giúp tăng tốc độ đáng kể.
    
- [ ] c) Giảm số lượng lớp trong mạng.
    
- [ ] d) Không cần dữ liệu huấn luyện.
    

**Câu 8:** **"Intersection over Union" (IoU) được sử dụng để làm gì?**

- [ ] a) Để đo lường tốc độ của thuật toán.
    
- [x] b) Để đo lường mức độ chồng chéo giữa hai hộp giới hạn (thường là hộp dự đoán và hộp thực tế).
    
- [ ] c) Để tính toán hàm chi phí.
    
- [ ] d) Để chọn kích thước của anchor box.
    

**Câu 9:** **Nếu IoU giữa hộp dự đoán và hộp thực tế là 0.9, điều đó có nghĩa là gì?**

- [ ] a) Hai hộp hầu như không chồng lên nhau.
    
- [ ] b) Hộp dự đoán hoàn toàn sai.
    
- [x] c) Hộp dự đoán có độ trùng khớp rất cao với hộp thực tế.
    
- [ ] d) Không thể kết luận.
    

**Câu 10:** **Mục đích của "Non-max Suppression" (NMS) là gì?**

- [ ] a) Để tăng số lượng hộp giới hạn được dự đoán.
    
- [x] b) Để loại bỏ các hộp giới hạn dư thừa, chồng chéo cho cùng một đối tượng và chỉ giữ lại hộp tốt nhất.
    
- [ ] c) Để tăng tốc độ lan truyền ngược.
    
- [ ] d) Để chọn ra các đặc trưng quan trọng nhất.
    

**Câu 11:** **YOLO là viết tắt của cụm từ gì?**

- [ ] a) You Only Learn Once
    
- [x] b) You Only Look Once
    
- [ ] c) You Observe Local Objects
    
- [ ] d) You Omit Lots of Objects
    

**Câu 12:** **Ý tưởng cốt lõi của thuật toán YOLO là gì?**

- [x] a) Chia ảnh thành một lưới (grid), và mỗi ô lưới (grid cell) chịu trách nhiệm dự đoán đối tượng có tâm nằm trong ô đó.
    
- [ ] b) Chạy thuật toán sliding windows trên toàn bộ ảnh.
    
- [ ] c) Chỉ nhìn vào các góc của ảnh.
    
- [ ] d) Sử dụng nhiều mạng nơ-ron khác nhau cho mỗi đối tượng.
    

**Câu 13:** **"Anchor boxes" được sử dụng để giải quyết vấn đề gì trong YOLO?**

- [x] a) Giúp mỗi ô lưới có thể phát hiện nhiều đối tượng có hình dạng khác nhau và chồng chéo lên nhau.
    
- [ ] b) Giảm chi phí tính toán.
    
- [ ] c) Cố định kích thước của các hộp giới hạn.
    
- [ ] d) Tăng số lượng lớp trong mạng.
    

**Câu 14:** **Trong YOLO, nếu một đối tượng có tâm nằm trong ô lưới (i, j), ô lưới nào sẽ chịu trách nhiệm dự đoán đối tượng đó?**

- [ ] a) Tất cả các ô lưới.
    
- [x] b) Chỉ ô lưới (i, j).
    
- [ ] c) Các ô lưới lân cận của (i, j).
    
- [ ] d) Một ô lưới được chọn ngẫu nhiên.
    

**Câu 15:** **Đâu không phải là một thành phần trong vector đầu ra của một ô lưới trong YOLO?**

- [ ] a) `Pc` (xác suất có đối tượng).
    
- [ ] b) `bx, by, bh, bw` (tọa độ hộp giới hạn).
    
- [ ] c) `c1, c2, c3,...` (xác suất các lớp).
    
- [x] d) `IoU` (giá trị Intersection over Union).
    

**Câu 16:** **"Semantic Segmentation" (Phân đoạn theo ngữ nghĩa) khác với Object Detection như thế nào?**

- [ ] a) Semantic Segmentation nhanh hơn.
    
- [ ] b) Semantic Segmentation chỉ hoạt động với ảnh y tế.
    
- [x] c) Thay vì chỉ vẽ một hộp giới hạn, Semantic Segmentation phân loại cho từng pixel trong ảnh.
    
- [ ] d) Object Detection chính xác hơn.
    

**Câu 17:** **Kiến trúc U-Net được đặt tên như vậy vì lý do gì?**

- [ ] a) Nó được phát minh bởi một người tên U.
    
- [x] b) Sơ đồ kiến trúc của nó có hình dạng giống chữ U.
    
- [ ] c) Nó là viết tắt của "Ultimate Network".
    
- [ ] d) Nó chỉ có thể phân loại chữ U.
    

**Câu 18:** **Thành phần nào trong U-Net được sử dụng để tăng kích thước (upsample) của bản đồ đặc trưng ở nhánh giải mã (decoder)?**

- [ ] a) Max Pooling
    
- [x] b) Tích chập chuyển vị (Transpose Convolution).
    
- [ ] c) Lớp Fully Connected.
    
- [ ] d) Anchor Box.
    

**Câu 19:** **Các "skip connections" trong kiến trúc U-Net có vai trò gì?**

- [ ] a) Để làm cho mạng sâu hơn.
    
- [x] b) Để kết hợp thông tin đặc trưng chi tiết từ nhánh mã hóa (encoder) với thông tin ngữ cảnh từ nhánh giải mã, giúp việc định vị chính xác hơn.
    
- [ ] c) Để giảm số lượng tham số.
    
- [ ] d) Để tăng tốc độ huấn luyện.
    

**Câu 20:** **Đâu là một ứng dụng phổ biến của U-Net?**

- [ ] a) Dịch máy.
    
- [x] b) Phân đoạn ảnh y tế (ví dụ: xác định khối u).
    
- [ ] c) Nhận dạng giọng nói.
    
- [ ] d) Dự báo giá cổ phiếu.
    

**Câu 21:** **Sự khác biệt giữa "Face Verification" (Xác minh khuôn mặt) và "Face Recognition" (Nhận dạng khuôn mặt) là gì?**

- [x] a) Verification là bài toán 1:1 ("Đây có phải là người X không?"), còn Recognition là bài toán 1:N ("Đây là ai trong số N người?").
    
- [ ] b) Recognition là bài toán 1:1, còn Verification là bài toán 1:N.
    
- [ ] c) Chúng là hai tên gọi cho cùng một bài toán.
    
- [ ] d) Verification chỉ hoạt động với ảnh tĩnh, Recognition hoạt động với video.
    

**Câu 22:** **"One-shot learning" trong nhận dạng khuôn mặt là vấn đề gì?**

- [ ] a) Chỉ cần một lần lặp để huấn luyện mô hình.
    
- [x] b) Mô hình phải có khả năng nhận dạng một người chỉ từ một hình ảnh duy nhất của người đó.
    
- [ ] c) Chỉ có một người trong cơ sở dữ liệu.
    
- [ ] d) Mô hình chỉ đưa ra một dự đoán duy nhất.
    

**Câu 23:** **Tại sao việc huấn luyện một mạng Softmax tiêu chuẩn không hiệu quả cho bài toán one-shot learning?**

- [ ] a) Vì Softmax không thể xử lý ảnh.
    
- [x] b) Vì tập huấn luyện cho mỗi người quá nhỏ (chỉ 1 ảnh) và việc thêm người mới đòi hỏi phải huấn luyện lại toàn bộ mạng.
    
- [ ] c) Vì Softmax quá chậm.
    
- [ ] d) Vì Softmax chỉ hoạt động với bài toán nhị phân.
    

**Câu 24:** **Kiến trúc Siamese Network hoạt động dựa trên nguyên tắc nào?**

- [x] a) Sử dụng hai mạng nơ-ron giống hệt nhau để học một hàm "đo độ tương tự" (similarity function) giữa hai ảnh đầu vào.
    
- [ ] b) Sử dụng một mạng duy nhất để phân loại nhiều người.
    
- [ ] c) Kết hợp nhiều mô hình khác nhau.
    
- [ ] d) Chỉ sử dụng các lớp fully-connected.
    

**Câu 25:** **Mục tiêu của việc huấn luyện Siamese Network là gì?**

- [ ] a) Tối đa hóa khoảng cách giữa các embedding của cùng một người.
    
- [ ] b) Tối thiểu hóa khoảng cách giữa các embedding của những người khác nhau.
    
- [x] c) Học một hàm embedding sao cho khoảng cách giữa các ảnh của cùng một người thì nhỏ, và khoảng cách giữa các ảnh của những người khác nhau thì lớn.
    
- [ ] d) Phân loại ảnh thành các nhóm.
    

**Câu 26:** **Hàm mất mát Triplet Loss yêu cầu một bộ ba (triplet) gồm những ảnh nào?**

- [ ] a) Ba ảnh của cùng một người.
    
- [ ] b) Ba ảnh của ba người khác nhau.
    
- [x] c) Một ảnh mỏ neo (Anchor), một ảnh dương tính (Positive - cùng người với anchor), và một ảnh âm tính (Negative - khác người với anchor).
    
- [ ] d) Một ảnh gốc, một ảnh đã qua augmentation, và một ảnh nhiễu.
    

**Câu 27:** **Công thức của Triplet Loss, `max(||f(A)-f(P)||² - ||f(A)-f(N)||² + α, 0)`, nhằm mục đích gì?**

- [x] a) Đảm bảo khoảng cách từ Anchor đến Negative lớn hơn khoảng cách từ Anchor đến Positive ít nhất một khoảng `α`.
    
- [ ] b) Đảm bảo khoảng cách từ Anchor đến Positive lớn hơn khoảng cách từ Anchor đến Negative.
    
- [ ] c) Làm cho tất cả các khoảng cách bằng nhau.
    
- [ ] d) Tối đa hóa tổng các khoảng cách.
    

**Câu 28:** **Tham số `α` (alpha) trong Triplet Loss được gọi là gì?**

- [ ] a) Tốc độ học.
    
- [ ] b) Tham số điều chuẩn hóa.
    
- [x] c) Lề (Margin).
    
- [ ] d) Ngưỡng (Threshold).
    

**Câu 29:** **Tại sao việc chọn các "hard triplets" lại quan trọng trong quá trình huấn luyện?**

- [ ] a) Vì chúng dễ học nhất.
    
- [x] b) Vì việc học trên các triplet quá dễ không giúp mô hình cải thiện, nên cần chọn các triplet mà mô hình dễ bị nhầm lẫn để tập trung học.
    
- [ ] c) Để làm cho quá trình huấn luyện chậm lại.
    
- [ ] d) Vì chúng chiếm phần lớn trong tập dữ liệu.
    

**Câu 30:** **Một cách tiếp cận khác để giải quyết bài toán Face Verification là coi nó như một bài toán:**

- [ ] a) Hồi quy.
    
- [x] b) Phân loại nhị phân (dự đoán 2 ảnh có phải cùng một người hay không).
    
- [ ] c) Phân cụm.
    
- [ ] d) One-shot learning.
    

**Câu 31:** **"Neural Style Transfer" (Chuyển đổi phong cách bằng mạng nơ-ron) là kỹ thuật gì?**

- [ ] a) Sao chép phong cách của một người và áp dụng cho người khác.
    
- [x] b) Kết hợp "nội dung" của một ảnh với "phong cách" của một ảnh khác để tạo ra một ảnh mới.
    
- [ ] c) Chuyển đổi một mạng nơ-ron từ TensorFlow sang PyTorch.
    
- [ ] d) Dạy cho mạng nơ-ron vẽ tranh.
    

**Câu 32:** **Trong Neural Style Transfer, hàm chi phí tổng hợp `J(G)` bao gồm hai thành phần nào?**

- [ ] a) Chi phí huấn luyện và chi phí kiểm thử.
    
- [x] b) Chi phí nội dung (Content cost) và Chi phí phong cách (Style cost).
    
- [ ] c) Chi phí L1 và chi phí L2.
    
- [ ] d) Chi phí của ảnh gốc và chi phí của ảnh phong cách.
    

**Câu 33:** **Chi phí nội dung `J_content(C, G)` được tính như thế nào?**

- [ ] a) Bằng cách so sánh trực tiếp các pixel của ảnh nội dung (C) và ảnh được tạo ra (G).
    
- [x] b) Bằng cách so sánh các kích hoạt của một lớp ẩn sâu trong một mạng CNN đã được huấn luyện trước cho cả hai ảnh C và G.
    
- [ ] c) Bằng cách đo độ tương phản của hai ảnh.
    
- [ ] d) Bằng cách so sánh biểu đồ màu của hai ảnh.
    

**Câu 34:** **Tại sao lại sử dụng một lớp ẩn sâu để đo lường "nội dung"?**

- [x] a) Vì các lớp sâu nắm bắt được các đặc trưng ngữ nghĩa, cấp cao của đối tượng trong ảnh.
    
- [ ] b) Vì các lớp nông tính toán nhanh hơn.
    
- [ ] c) Vì các lớp sâu có ít nơ-ron hơn.
    
- [ ] d) Đây là một lựa chọn ngẫu nhiên.
    

**Câu 35:** **"Phong cách" của một ảnh trong Neural Style Transfer được định nghĩa là gì?**

- [ ] a) Bảng màu được sử dụng trong ảnh.
    
- [x] b) Mức độ tương quan giữa các kích hoạt trên các kênh khác nhau trong một lớp của CNN.
    
- [ ] c) Các đối tượng có trong ảnh.
    
- [ ] d) Độ phân giải của ảnh.
    

**Câu 36:** **Ma trận phong cách (Style Matrix), hay ma trận Gram, đo lường điều gì?**

- [ ] a) Giá trị trung bình của các kích hoạt.
    
- [x] b) Mức độ mà các đặc trưng cấp thấp (như màu sắc, hoa văn) có xu hướng xuất hiện cùng nhau.
    
- [ ] c) Kích thước của ảnh.
    
- [ ] d) Số lượng đối tượng trong ảnh.
    

**Câu 37:** **Tại sao lại sử dụng nhiều lớp (cả nông và sâu) để tính toán chi phí phong cách?**

- [ ] a) Để làm cho việc tính toán phức tạp hơn.
    
- [x] b) Để nắm bắt được các đặc trưng phong cách ở nhiều quy mô khác nhau, từ các hoa văn nhỏ đến các cấu trúc lớn hơn.
    
- [ ] c) Vì không thể sử dụng một lớp duy nhất.
    
- [ ] d) Để giảm thời gian huấn luyện.
    

**Câu 38:** **Quá trình tạo ra ảnh trong Neural Style Transfer hoạt động như thế nào?**

- [ ] a) Huấn luyện một mạng nơ-ron mới từ đầu.
    
- [x] b) Bắt đầu với một ảnh nhiễu ngẫu nhiên và sử dụng Gradient Descent để cập nhật các pixel của ảnh đó nhằm tối thiểu hóa hàm chi phí tổng hợp.
    
- [ ] c) Trộn lẫn các pixel của ảnh nội dung và ảnh phong cách.
    
- [ ] d) Tìm một ảnh tương tự trên internet.
    

**Câu 39:** **Mạng nơ-ron tích chập có thể được tổng quát hóa cho dữ liệu 1D không?**

- [ ] a) Không, nó chỉ hoạt động với dữ liệu 2D (ảnh).
    
- [x] b) Có, bằng cách sử dụng các bộ lọc 1D, nó có thể được áp dụng cho dữ liệu chuỗi thời gian hoặc văn bản.
    
- [ ] c) Chỉ có thể tổng quát hóa cho dữ liệu 3D.
    
- [ ] d) Chỉ khi dữ liệu 1D được chuyển đổi thành ảnh.
    

**Câu 40:** **Đâu là một ví dụ về dữ liệu 3D mà CNN có thể được áp dụng?**

- [ ] a) Một đoạn văn bản.
    
- [x] b) Dữ liệu quét y tế (như CT scan) hoặc video.
    
- [ ] c) Một tín hiệu âm thanh.
    
- [ ] d) Một bức ảnh đen trắng.
    

**Câu 41:** **Trong thuật toán YOLO, nếu hai anchor box khác nhau trong cùng một ô lưới đều có IoU cao với cùng một đối tượng, đối tượng đó sẽ được gán cho anchor box nào?**

- [ ] a) Cả hai.
    
- [x] b) Anchor box có IoU cao hơn.
    
- [ ] c) Một anchor box được chọn ngẫu nhiên.
    
- [ ] d) Không gán cho cái nào.
    

**Câu 42:** **Trong Non-max Suppression, nếu hai hộp giới hạn có IoU cao hơn một ngưỡng nhất định, hộp nào sẽ bị loại bỏ?**

- [ ] a) Hộp có xác suất `Pc` cao hơn.
    
- [x] b) Hộp có xác suất `Pc` thấp hơn.
    
- [ ] c) Cả hai.
    
- [ ] d) Hộp có kích thước lớn hơn.
    

**Câu 43:** **"Face encoding" hay "face embedding" là gì?**

- [ ] a) Là ảnh gốc của khuôn mặt.
    
- [x] b) Là một vector số (thường là 128 chiều) biểu diễn các đặc trưng của một khuôn mặt, được tạo ra bởi một mạng nơ-ron.
    
- [ ] c) Là tên của người đó.
    
- [ ] d) Là một hộp giới hạn quanh khuôn mặt.
    

**Câu 44:** **Thuật toán R-CNN (Regions with CNN) hoạt động như thế nào?**

- [ ] a) Chạy một mạng CNN trên toàn bộ ảnh một lần.
    
- [x] b) Đầu tiên đề xuất các "vùng có khả năng chứa đối tượng", sau đó chạy một bộ phân loại CNN trên từng vùng đó.
    
- [ ] c) Chia ảnh thành một lưới cố định.
    
- [ ] d) Chỉ phân đoạn ảnh.
    

**Câu 45:** **Tại sao các thuật toán như Fast R-CNN và Faster R-CNN lại nhanh hơn R-CNN?**

- [ ] a) Vì chúng sử dụng mạng nông hơn.
    
- [x] b) Vì chúng sử dụng các kỹ thuật tích chập để chia sẻ tính toán giữa các vùng đề xuất, thay vì chạy CNN trên từng vùng một cách độc lập.
    
- [ ] c) Vì chúng sử dụng ít dữ liệu hơn.
    
- [ ] d) Vì chúng không cần gán nhãn dữ liệu.
    

**Câu 46:** **Trong Neural Style Transfer, chúng ta tối ưu hóa cái gì?**

- [ ] a) Các trọng số của mạng nơ-ron.
    
- [ ] b) Các siêu tham số.
    
- [x] c) Các pixel của ảnh được tạo ra (G).
    
- [ ] d) Các pixel của ảnh nội dung (C).
    

**Câu 47:** **Để huấn luyện một hệ thống nhận dạng khuôn mặt, bạn cần một tập dữ liệu như thế nào?**

- [ ] a) Một vài ảnh của một người duy nhất.
    
- [x] b) Nhiều ảnh của nhiều người khác nhau.
    
- [ ] c) Chỉ cần các ảnh không có khuôn mặt.
    
- [ ] d) Các ảnh đã được chuyển đổi phong cách.
    

**Câu 48:** **Đâu là một thách thức của bài toán "one-shot learning"?**

- [x] a) Mô hình rất dễ bị overfitting vào một ví dụ duy nhất.
    
- [ ] b) Cần rất nhiều dữ liệu.
    
- [ ] c) Thời gian huấn luyện rất lâu.
    
- [ ] d) Không thể sử dụng GPU.
    

**Câu 49:** **Trong U-Net, nhánh bên trái (nhánh đi xuống) có vai trò gì?**

- [ ] a) Tăng kích thước ảnh.
    
- [x] b) Hoạt động như một bộ mã hóa (encoder), trích xuất các đặc trưng ngữ nghĩa và giảm kích thước không gian.
    
- [ ] c) Phân loại các pixel.
    
- [ ] d) Chỉ để sao chép dữ liệu.
    

**Câu 50:** **Đâu là một ứng dụng mà CNN 1D có thể hữu ích?**

- [ ] a) Phân tích tín hiệu EKG (điện tâm đồ).
    
- [ ] b) Phân loại văn bản.
    
- [ ] c) Nhận dạng giọng nói.
    
- [x] d) Tất cả các câu trên.
    

#### Bài kiểm tra trắc nghiệm: Mạng Nơ-ron Hồi quy (RNN)

**Câu 1:** **Tại sao các mạng nơ-ron tiêu chuẩn (không phải RNN) không phù hợp cho các bài toán xử lý chuỗi (sequence tasks)?**

- [ ] a) Vì chúng không thể xử lý các đầu vào và đầu ra có độ dài thay đổi.
    
- [ ] b) Vì chúng không chia sẻ các đặc trưng đã học được qua các vị trí khác nhau trong chuỗi.
    
- [x] c) Cả A và B đều đúng.
    
- [ ] d) Vì chúng quá chậm.
    

**Câu 2:** **Trong ký hiệu của mô hình chuỗi, `x<t>` đại diện cho điều gì?**

- [ ] a) Toàn bộ chuỗi đầu vào.
    
- [x] b) Đầu vào tại bước thời gian (time step) thứ `t`.
    
- [ ] c) Mẫu dữ liệu huấn luyện thứ `t`.
    
- [ ] d) Lớp thứ `t` của mạng.
    

**Câu 3:** **Đặc điểm kiến trúc cốt lõi của một Mạng Nơ-ron Hồi quy (RNN) là gì?**

- [ ] a) Nó có nhiều lớp ẩn hơn các mạng khác.
    
- [x] b) Nó có một vòng lặp, cho phép thông tin (trạng thái kích hoạt) từ bước thời gian trước được truyền đến bước thời gian hiện tại.
    
- [ ] c) Nó chỉ sử dụng hàm kích hoạt tuyến tính.
    
- [ ] d) Nó không có tham số trọng số.
    

**Câu 4:** **Trong một RNN cơ bản, các tham số trọng số (`W_aa`, `W_ax`, `W_ya`) có đặc điểm gì?**

- [ ] a) Chúng thay đổi ở mỗi bước thời gian.
    
- [x] b) Chúng được chia sẻ (sử dụng chung) qua tất cả các bước thời gian.
    
- [ ] c) Chúng chỉ được sử dụng ở bước thời gian cuối cùng.
    
- [ ] d) Chúng được khởi tạo bằng 0.
    

**Câu 5:** **Trong bài toán Nhận dạng Thực thể có tên (Named-Entity Recognition), nếu đầu vào và đầu ra đều có cùng độ dài (`Tx = Ty`), đây là loại kiến trúc RNN nào?**

- [ ] a) Many-to-one
    
- [ ] b) One-to-many
    
- [x] c) Many-to-many
    
- [ ] d) One-to-one
    

**Câu 6:** **Phân tích cảm xúc (sentiment classification) của một câu văn (ví dụ: đánh giá phim) là một ví dụ của loại kiến trúc RNN nào?**

- [x] a) Many-to-one
    
- [ ] b) One-to-many
    
- [ ] c) Many-to-many (`Tx = Ty`)
    
- [ ] d) Many-to-many (`Tx != Ty`)
    

**Câu 7:** **Tạo ra một bản nhạc (music generation) từ một nốt nhạc đầu vào là một ví dụ của loại kiến trúc RNN nào?**

- [ ] a) Many-to-one
    
- [x] b) One-to-many
    
- [ ] c) Many-to-many
    
- [ ] d) One-to-one
    

**Câu 8:** **Trong công thức tính kích hoạt của RNN, `a<t> = g(W_aa * a<t-1> + W_ax * x<t> + b_a)`, thành phần `a<t-1>` đại diện cho điều gì?**

- [ ] a) Đầu vào hiện tại.
    
- [x] b) "Bộ nhớ" hay thông tin từ bước thời gian trước đó.
    
- [ ] c) Dự đoán của bước thời gian trước.
    
- [ ] d) Nhãn đúng của bước thời gian trước.
    

**Câu 9:** **Để biểu diễn một từ trong một câu cho máy tính, phương pháp phổ biến là gì?**

- [ ] a) Sử dụng chính chuỗi ký tự đó.
    
- [ ] b) Sử dụng một số nguyên duy nhất.
    
- [x] c) Sử dụng mã hóa one-hot dựa trên một bộ từ điển (vocabulary).
    
- [ ] d) Sử dụng mã ASCII của từ đó.
    

**Câu 10:** **Token `<UNK>` được sử dụng để làm gì trong mô hình ngôn ngữ?**

- [ ] a) Để biểu thị sự kết thúc của một câu.
    
- [x] b) Để biểu thị một từ không có trong từ điển.
    
- [ ] c) Để biểu thị một từ là tên riêng.
    
- [ ] d) Để bắt đầu một câu mới.
    

**Câu 11:** **Thuật toán được sử dụng để huấn luyện RNN được gọi là gì?**

- [ ] a) Gradient Descent
    
- [ ] b) Adam
    
- [ ] c) Backpropagation
    
- [x] d) Backpropagation Through Time (BPTT)
    

**Câu 12:** **Tại sao thuật toán huấn luyện RNN lại có tên "Through Time" (Xuyên thời gian)?**

- [ ] a) Vì nó mất rất nhiều thời gian để huấn luyện.
    
- [x] b) Vì quá trình lan truyền ngược lỗi diễn ra từ bước thời gian cuối cùng ngược về các bước thời gian đầu tiên.
    
- [ ] c) Vì nó có thể dự đoán tương lai.
    
- [ ] d) Vì nó chỉ hoạt động với dữ liệu chuỗi thời gian.
    

**Câu 13:** **Mục tiêu của một mô hình ngôn ngữ (language model) là gì?**

- [ ] a) Dịch một câu từ ngôn ngữ này sang ngôn ngữ khác.
    
- [ ] b) Đếm số từ trong một câu.
    
- [x] c) Ước tính xác suất của một chuỗi các từ.
    
- [ ] d) Phân loại cảm xúc của một câu.
    

**Câu 14:** **Khi tạo ra một chuỗi mới (ví dụ: văn bản) bằng RNN, đầu vào cho bước thời gian `t` là gì?**

- [ ] a) Một từ được chọn ngẫu nhiên từ từ điển.
    
- [x] b) Đầu ra (từ được dự đoán) của bước thời gian `t-1`.
    
- [ ] c) Luôn là một vector zero.
    
- [ ] d) Toàn bộ câu đã được tạo ra trước đó.
    

**Câu 15:** **Sự khác biệt chính giữa mô hình ngôn ngữ cấp độ từ (word-level) và cấp độ ký tự (character-level) là gì?**

- [x] a) Mô hình cấp độ ký tự không bao giờ gặp phải từ không xác định (`<UNK>`).
    
- [ ] b) Mô hình cấp độ từ thường tạo ra các chuỗi dài hơn.
    
- [ ] c) Mô hình cấp độ ký tự yêu cầu một từ điển lớn hơn.
    
- [ ] d) Mô hình cấp độ từ luôn chính xác hơn.
    

**Câu 16:** **Trong BPTT, hàm chi phí tổng hợp (`L`) cho toàn bộ chuỗi được tính như thế nào?**

- [ ] a) Là giá trị chi phí ở bước thời gian cuối cùng.
    
- [ ] b) Là giá trị chi phí trung bình của tất cả các bước thời gian.
    
- [x] c) Là tổng của các hàm chi phí tại mỗi bước thời gian.
    
- [ ] d) Là giá trị chi phí lớn nhất trong tất cả các bước thời gian.
    

**Câu 17:** **Trong một RNN cơ bản, dự đoán `ŷ<t>` tại một bước thời gian phụ thuộc vào những thông tin nào?**

- [ ] a) Chỉ đầu vào `x<t>`.
    
- [ ] b) Chỉ kích hoạt `a<t-1>`.
    
- [x] c) Cả đầu vào `x<t>` và tất cả các đầu vào trước đó (`x<1>`, ..., `x<t-1>`) thông qua `a<t-1>`.
    
- [ ] d) Chỉ các đầu vào trong tương lai.
    

**Câu 18:** **Dịch máy từ một câu có độ dài `Tx` sang một câu có độ dài `Ty` (với `Tx != Ty`) là một ví dụ của loại kiến trúc RNN nào?**

- [ ] a) Many-to-one
    
- [ ] b) One-to-many
    
- [ ] c) Many-to-many (`Tx = Ty`)
    
- [x] d) Many-to-many (`Tx != Ty`), thường sử dụng kiến trúc Encoder-Decoder.
    

**Câu 19:** **Nhược điểm của mô hình ngôn ngữ cấp độ ký tự là gì?**

- [ ] a) Nó không thể học được cấu trúc ngữ pháp.
    
- [x] b) Nó có xu hướng tạo ra các chuỗi rất dài và khó nắm bắt các phụ thuộc xa.
    
- [ ] c) Nó không thể xử lý dấu câu.
    
- [ ] d) Nó yêu cầu một GPU rất mạnh.
    

**Câu 20:** **Trong quá trình "sampling" một chuỗi mới, điều gì quyết định từ/ký tự nào sẽ được chọn ở mỗi bước?**

- [ ] a) Luôn chọn từ có xác suất cao nhất.
    
- [ ] b) Lấy mẫu từ phân phối xác suất được tạo ra bởi lớp softmax.
    
- [ ] c) Chọn một từ ngẫu nhiên.
    
- [x] d) Cả A và B đều là các chiến lược có thể sử dụng.
    

**Câu 21:** **Vấn đề "Vanishing Gradients" (Gradient biến mất) trong RNN gây ra khó khăn gì?**

- [ ] a) Làm cho mô hình học quá nhanh.
    
- [x] b) Khiến cho lỗi từ các bước thời gian sau khó lan truyền ngược lại để cập nhật các trọng số ở các bước thời gian đầu, làm cho RNN khó học các phụ thuộc xa (long-range dependencies).
    
- [ ] c) Gây ra hiện tượng overfitting.
    
- [ ] d) Chỉ xảy ra với các chuỗi ngắn.
    

**Câu 22:** **Vấn đề "Exploding Gradients" (Gradient bùng nổ) là gì?**

- [ ] a) Gradient trở nên rất nhỏ.
    
- [x] b) Gradient trở nên cực kỳ lớn, gây ra các bước cập nhật không ổn định và dẫn đến giá trị `NaN`.
    
- [ ] c) Hàm chi phí không bao giờ giảm.
    
- [ ] d) Mô hình dự đoán cùng một giá trị cho mọi đầu vào.
    

**Câu 23:** **Kỹ thuật nào thường được sử dụng để giải quyết vấn đề Exploding Gradients?**

- [ ] a) Dropout
    
- [x] b) Gradient Clipping (Xén Gradient).
    
- [ ] c) Batch Normalization
    
- [ ] d) Khởi tạo He.
    

**Câu 24:** **Mục đích chính của các đơn vị GRU (Gated Recurrent Unit) và LSTM (Long Short-Term Memory) là gì?**

- [ ] a) Để làm cho RNN chạy nhanh hơn.
    
- [x] b) Để giải quyết vấn đề gradient biến mất và giúp RNN học các phụ thuộc xa tốt hơn.
    
- [ ] c) Để giảm số lượng tham số.
    
- [ ] d) Để chỉ hoạt động với dữ liệu hình ảnh.
    

**Câu 25:** **Thành phần nào trong GRU và LSTM hoạt động như một "bộ nhớ" để lưu trữ thông tin qua các bước thời gian?**

- [ ] a) Trạng thái kích hoạt (activation state) `a<t>`.
    
- [x] b) Trạng thái ô nhớ (memory cell) `c<t>`.
    
- [ ] c) Các cổng (gates).
    
- [ ] d) Vector đầu vào `x<t>`.
    

**Câu 26:** **"Cổng" (gate) trong GRU/LSTM có vai trò gì?**

- [x] a) Nó là một mạng nơ-ron nhỏ (thường có hàm kích hoạt sigmoid) quyết định lượng thông tin nào được phép đi qua.
    
- [ ] b) Nó là một hằng số cố định.
    
- [ ] c) Nó chỉ cho phép thông tin đi qua nếu giá trị lớn hơn 1.
    
- [ ] d) Nó chặn tất cả thông tin.
    

**Câu 27:** **GRU có bao nhiêu cổng?**

- [ ] a) 1 (Update gate)
    
- [x] b) 2 (Update gate và Relevance gate)
    
- [ ] c) 3 (Update gate, Forget gate, và Output gate)
    
- [ ] d) 4
    

**Câu 28:** **LSTM có bao nhiêu cổng?**

- [ ] a) 1
    
- [ ] b) 2
    
- [x] c) 3 (Update gate, Forget gate, và Output gate)
    
- [ ] d) 4
    

**Câu 29:** **Cổng nào trong LSTM có nhiệm vụ quyết định thông tin nào từ ô nhớ cũ (`c<t-1>`) cần được loại bỏ?**

- [ ] a) Update gate
    
- [ ] b) Relevance gate
    
- [ ] c) Output gate
    
- [x] d) Forget gate
    

**Câu 30:** **So với LSTM, GRU có ưu điểm gì?**

- [ ] a) Nó luôn chính xác hơn.
    
- [x] b) Nó có kiến trúc đơn giản hơn và ít tham số hơn, giúp tính toán nhanh hơn và dễ dàng xây dựng các mô hình lớn hơn.
    
- [ ] c) Nó có nhiều cổng hơn.
    
- [ ] d) Nó không bao giờ gặp vấn đề gradient biến mất.
    

**Câu 31:** **Tại sao một RNN đơn hướng (unidirectional) lại có hạn chế?**

- [ ] a) Vì nó không thể xử lý các chuỗi dài.
    
- [x] b) Vì tại một bước thời gian `t`, dự đoán chỉ có thể sử dụng thông tin từ các bước trước đó (`1` đến `t-1`), không sử dụng được thông tin từ tương lai.
    
- [ ] c) Vì nó quá phức tạp.
    
- [ ] d) Vì nó chỉ có thể được huấn luyện bằng BPTT.
    

**Câu 32:** **Mạng RNN hai chiều (Bidirectional RNN - BRNN) giải quyết hạn chế của RNN đơn hướng bằng cách nào?**

- [ ] a) Bằng cách thêm nhiều lớp ẩn hơn.
    
- [x] b) Bằng cách xử lý chuỗi theo cả hai hướng (từ trái sang phải và từ phải sang trái) và kết hợp kết quả.
    
- [ ] c) Bằng cách sử dụng một tốc độ học lớn hơn.
    
- [ ] d) Bằng cách loại bỏ các kết nối hồi quy.
    

**Câu 33:** **BRNN đặc biệt hữu ích cho các tác vụ nào?**

- [x] a) Các tác vụ mà việc dự đoán tại một điểm cần ngữ cảnh từ cả quá khứ và tương lai, ví dụ như Named-Entity Recognition.
    
- [ ] b) Các tác vụ tạo văn bản thời gian thực.
    
- [ ] c) Các tác vụ có chuỗi đầu vào rất ngắn.
    
- [ ] d) Các tác vụ không yêu cầu bộ nhớ.
    

**Câu 34:** **Một nhược điểm của BRNN là gì?**

- [ ] a) Nó chậm hơn RNN đơn hướng.
    
- [x] b) Nó yêu cầu toàn bộ chuỗi đầu vào phải có sẵn trước khi có thể đưa ra dự đoán.
    
- [ ] c) Nó có nhiều khả năng bị overfitting hơn.
    
- [ ] d) Nó khó triển khai hơn.
    

**Câu 35:** **Một Mạng RNN sâu (Deep RNN) được tạo ra bằng cách nào?**

- [ ] a) Tăng số lượng bước thời gian.
    
- [x] b) Xếp chồng nhiều lớp RNN lên nhau, trong đó đầu ra của lớp `l` tại thời điểm `t` là đầu vào cho lớp `l+1` tại cùng thời điểm `t`.
    
- [ ] c) Sử dụng một vector kích hoạt có kích thước lớn hơn.
    
- [ ] d) Kết hợp RNN với CNN.
    

**Câu 36:** **Lợi ích của việc sử dụng Deep RNN là gì?**

- [x] a) Cho phép học các đặc trưng phức tạp hơn ở mỗi bước thời gian.
    
- [ ] b) Luôn chạy nhanh hơn RNN nông.
    
- [ ] c) Không bao giờ gặp vấn đề gradient biến mất.
    
- [ ] d) Yêu cầu ít dữ liệu hơn.
    

**Câu 37:** **Trong một Deep RNN 3 lớp, đầu vào của lớp thứ 2 tại bước thời gian `t` (`a[2]<t>`) là gì?**

- [ ] a) `x<t>`
    
- [x] b) `a[1]<t>`
    
- [ ] c) `a[2]<t-1>`
    
- [ ] d) `a[3]<t>`
    

**Câu 38:** **Trong thực tế, các kiến trúc RNN sâu thường có bao nhiêu lớp?**

- [ ] a) Hàng trăm lớp.
    
- [x] b) Thường không quá sâu (ví dụ, 3 lớp đã được coi là khá sâu) do chi phí tính toán.
    
- [ ] c) Luôn chỉ có 1 lớp.
    
- [ ] d) Hàng nghìn lớp.
    

**Câu 39:** **Bạn có thể xây dựng một Deep Bidirectional RNN không?**

- [ ] a) Không, hai kiến trúc này không tương thích.
    
- [x] b) Có, bằng cách xếp chồng các lớp BRNN lên nhau.
    
- [ ] c) Chỉ khi sử dụng GRU.
    
- [ ] d) Chỉ khi sử dụng LSTM.
    

**Câu 40:** **Trong các ứng dụng thực tế, loại đơn vị hồi quy nào thường được sử dụng làm lựa chọn mặc định?**

- [ ] a) RNN cơ bản.
    
- [ ] b) GRU.
    
- [ ] c) LSTM.
    
- [x] d) Cả GRU và LSTM đều là những lựa chọn mạnh mẽ.
    

**Câu 41:** **Trong RNN, "trạng thái ẩn" (hidden state) là gì?**

- [ ] a) Là đầu ra cuối cùng của mạng.
    
- [x] b) Là một vector mang thông tin tóm tắt về những gì đã xảy ra trong chuỗi cho đến bước thời gian hiện tại.
    
- [ ] c) Là các trọng số của mạng.
    
- [ ] d) Là một siêu tham số.
    

**Câu 42:** **Tại sao việc chia sẻ tham số lại quan trọng trong RNN?**

- [ ] a) Nó làm giảm đáng kể tổng số tham số cần học.
    
- [ ] b) Nó cho phép mô hình áp dụng cùng một quy tắc/đặc trưng đã học cho các phần khác nhau của chuỗi.
    
- [x] c) Cả A và B đều đúng.
    
- [ ] d) Nó làm cho mô hình phức tạp hơn.
    

**Câu 43:** **"Unfolding" một RNN có nghĩa là gì?**

- [x] a) Biến đổi kiến trúc vòng lặp của RNN thành một mạng truyền thẳng rất sâu, trong đó mỗi bước thời gian là một lớp.
    
- [ ] b) Làm phẳng vector đầu ra.
    
- [ ] c) Giảm số lượng lớp.
    
- [ ] d) Tăng tốc độ học.
    

**Câu 44:** **Cổng cập nhật (update gate) trong GRU có chức năng tương tự như sự kết hợp của hai cổng nào trong LSTM?**

- [ ] a) Cổng quên và cổng đầu ra.
    
- [x] b) Cổng quên và cổng cập nhật (đầu vào).
    
- [ ] c) Cổng cập nhật và cổng đầu ra.
    
- [ ] d) Không có sự tương đồng.
    

**Câu 45:** **Trong công thức của LSTM, `c<t> = Γu * c̃<t> + Γf * c<t-1>`, `Γf` là đầu ra của cổng nào?**

- [ ] a) Cổng cập nhật (Update gate).
    
- [x] b) Cổng quên (Forget gate).
    
- [ ] c) Cổng đầu ra (Output gate).
    
- [ ] d) Cổng liên quan (Relevance gate).
    

**Câu 46:** **Đâu là một ví dụ về dữ liệu chuỗi (sequence data)?**

- [ ] a) Giá cổ phiếu theo thời gian.
    
- [ ] b) Một câu văn.
    
- [ ] c) Một đoạn âm thanh.
    
- [x] d) Tất cả các câu trên.
    

**Câu 47:** **Nếu bạn đang xây dựng một hệ thống nhận dạng giọng nói, tại sao BRNN lại hữu ích?**

- [x] a) Vì việc nhận dạng một âm vị có thể phụ thuộc vào các âm vị đứng cả trước và sau nó.
    
- [ ] b) Vì giọng nói luôn được xử lý từ trái sang phải.
    
- [ ] c) Vì BRNN yêu cầu ít dữ liệu hơn.
    
- [ ] d) Vì BRNN không bị ảnh hưởng bởi nhiễu.
    

**Câu 48:** **Trong một Deep RNN, các kết nối được hình thành như thế nào?**

- [ ] a) Chỉ theo chiều ngang (qua thời gian).
    
- [ ] b) Chỉ theo chiều dọc (qua các lớp).
    
- [x] c) Cả theo chiều ngang (qua thời gian) và chiều dọc (qua các lớp).
    
- [ ] d) Một cách ngẫu nhiên.
    

**Câu 49:** **Peephole connection là một biến thể của kiến trúc nào?**

- [ ] a) GRU
    
- [ ] b) RNN cơ bản
    
- [x] c) LSTM
    
- [ ] d) BRNN
    

**Câu 50:** **Đâu không phải là một ứng dụng của mô hình chuỗi?**

- [ ] a) Nhận dạng hoạt động trong video.
    
- [x] b) Phân loại ảnh tĩnh (ví dụ: ảnh mèo và chó).
    
- [ ] c) Phân tích chuỗi DNA.
    
- [ ] d) Dịch máy.
    

#### Bài kiểm tra trắc nghiệm: NLP, Mô hình Chuỗi, Attention và Transformer

**Câu 1:** **Ưu điểm chính của Word Embeddings so với biểu diễn One-hot là gì?**

- [ ] a) Word Embeddings yêu cầu ít bộ nhớ hơn cho mỗi vector.
    
- [x] b) Word Embeddings cho phép mô hình khái quát hóa mối quan hệ giữa các từ (ví dụ: "cam" và "táo" đều là trái cây).
    
- [ ] c) One-hot luôn tốt hơn cho các bài toán NLP.
    
- [ ] d) Word Embeddings dễ tính toán hơn.
    

**Câu 2:** **Trong bài toán loại suy "Man is to Woman as King is to ___", word embeddings giải quyết bằng cách nào?**

- [ ] a) Tìm kiếm trên Google.
    
- [x] b) Tìm từ `w` sao cho vector `e_w` gần nhất với `e_king - e_man + e_woman`.
    
- [ ] c) So sánh độ dài của các từ.
    
- [ ] d) Sử dụng một mạng nơ-ron riêng để giải bài toán loại suy.
    

**Câu 3:** **Hàm tương tự Cosine (Cosine Similarity) được dùng để làm gì?**

- [ ] a) Để đo khoảng cách Euclid giữa hai vector từ.
    
- [x] b) Để đo góc giữa hai vector từ, qua đó xác định mức độ tương đồng về ngữ nghĩa.
    
- [ ] c) Để tính toán hàm chi phí.
    
- [ ] d) Để chuẩn hóa các vector từ.
    

**Câu 4:** **Trong mô hình Word2Vec Skip-gram, nhiệm vụ học có giám sát được tạo ra là gì?**

- [x] a) Từ một từ mục tiêu (target), dự đoán các từ ngữ cảnh (context) xung quanh nó.
    
- [ ] b) Từ các từ ngữ cảnh, dự đoán một từ mục tiêu ở giữa.
    
- [ ] c) Phân loại cảm xúc của một câu.
    
- [ ] d) Dịch một câu.
    

**Câu 5:** **Kỹ thuật "Negative Sampling" được phát triển để giải quyết vấn đề gì trong Word2Vec?**

- [ ] a) Vấn đề từ không có trong từ điển.
    
- [x] b) Chi phí tính toán rất cao của lớp Softmax trên toàn bộ từ điển.
    
- [ ] c) Vấn đề thiên vị giới tính trong word embeddings.
    
- [ ] d) Vấn đề gradient biến mất.
    

**Câu 6:** **Thuật toán GloVe (Global Vectors for Word Representation) học word embeddings dựa trên thông tin nào?**

- [ ] a) Chỉ dựa vào các cặp từ ngữ cảnh-mục tiêu cục bộ.
    
- [x] b) Dựa trên ma trận đồng xuất hiện (co-occurrence matrix) của các từ trên toàn bộ kho văn bản.
    
- [ ] c) Dựa trên cảm xúc của câu.
    
- [ ] d) Dựa trên một mạng nơ-ron sâu.
    

**Câu 7:** **Một phương pháp đơn giản để phân loại cảm xúc của một câu sử dụng word embeddings là gì?**

- [ ] a) Chỉ sử dụng embedding của từ cuối cùng.
    
- [x] b) Lấy trung bình hoặc tổng các vector embedding của tất cả các từ trong câu và đưa vào một bộ phân loại Softmax.
    
- [ ] c) Đếm số lượng từ tích cực và tiêu cực.
    
- [ ] d) Sử dụng one-hot encoding.
    

**Câu 8:** **Tại sao word embeddings có thể chứa đựng các thiên vị (bias) xã hội?**

- [ ] a) Do lỗi trong thuật toán.
    
- [x] b) Vì chúng học từ các kho văn bản lớn do con người tạo ra, vốn đã chứa đựng các thiên vị đó.
    
- [ ] c) Do khởi tạo ngẫu nhiên.
    
- [ ] d) Do hàm chi phí không phù hợp.
    

**Câu 9:** **Một trong các bước để giảm thiểu thiên vị (debiasing) trong word embeddings là gì?**

- [ ] a) Huấn luyện lại mô hình với dữ liệu ít hơn.
    
- [x] b) Xác định "chiều thiên vị" (ví dụ: chiều giới tính) và chiếu các từ không mang tính định nghĩa ra khỏi chiều đó.
    
- [ ] c) Tăng kích thước của vector embedding.
    
- [ ] d) Chỉ sử dụng các từ trung tính.
    

**Câu 10:** **Trong mô hình Word2Vec CBOW (Continuous Bag-of-Words), nhiệm vụ học là gì?**

- [ ] a) Từ một từ mục tiêu, dự đoán các từ ngữ cảnh.
    
- [x] b) Từ các từ ngữ cảnh xung quanh, dự đoán từ mục tiêu ở giữa.
    
- [ ] c) Dự đoán từ tiếp theo trong câu.
    
- [ ] d) Dịch từ sang ngôn ngữ khác.
    

**Câu 11:** **Ma trận embedding `E` thường có kích thước là bao nhiêu?**

- [ ] a) (số chiều embedding, số chiều embedding)
    
- [ ] b) (kích thước từ điển, số lượng câu)
    
- [ ] c) (số chiều embedding, kích thước từ điển)
    
- [x] d) (kích thước từ điển, số chiều embedding)
    

**Câu 12:** **"Transfer learning" trong NLP thường được thực hiện như thế nào?**

- [ ] a) Huấn luyện một mô hình từ đầu cho mọi tác vụ.
    
- [ ] b) Sử dụng một mô hình đã huấn luyện trên tác vụ A để huấn luyện cho tác vụ B.
    
- [x] c) Tải về một bộ word embeddings đã được huấn luyện trước trên một kho văn bản lớn và sử dụng nó cho tác vụ của mình.
    
- [ ] d) Chia sẻ các siêu tham số giữa các mô hình.
    

**Câu 13:** **Đâu không phải là một ứng dụng của word embeddings?**

- [ ] a) Nhận dạng thực thể có tên (Named Entity Recognition).
    
- [ ] b) Phân loại cảm xúc.
    
- [ ] c) Tóm tắt văn bản.
    
- [x] d) Phân đoạn ảnh.
    

**Câu 14:** **Khi tạo các cặp (context, target) trong Word2Vec, "window size" (kích thước cửa sổ) có ý nghĩa gì?**

- [ ] a) Kích thước của toàn bộ câu.
    
- [x] b) Số lượng từ ngữ cảnh được xem xét ở bên trái và bên phải của từ mục tiêu.
    
- [ ] c) Số chiều của vector embedding.
    
- [ ] d) Số lượng ví dụ âm (negative examples).
    

**Câu 15:** **Trong Negative Sampling, tại sao chúng ta không lấy mẫu các từ âm một cách ngẫu nhiên đều?**

- [ ] a) Vì làm vậy quá chậm.
    
- [x] b) Vì các từ phổ biến (như "the", "a") sẽ được chọn quá thường xuyên. Thay vào đó, một heuristic được sử dụng để cân bằng giữa các từ phổ biến và ít phổ biến.
    
- [ ] c) Vì làm vậy sẽ khiến mô hình không hội tụ.
    
- [ ] d) Vì các từ âm không quan trọng.
    

**Câu 16:** **Kiến trúc Encoder-Decoder trong các mô hình sequence-to-sequence có vai trò gì?**

- [x] a) Encoder nén chuỗi đầu vào thành một vector biểu diễn, Decoder tạo ra chuỗi đầu ra từ vector đó.
    
- [ ] b) Encoder tạo ra chuỗi đầu ra, Decoder nén chuỗi đầu vào.
    
- [ ] c) Cả hai đều cùng tạo ra chuỗi đầu ra.
    
- [ ] d) Chúng được dùng để phân loại từ.
    

**Câu 17:** **Một nhược điểm lớn của kiến trúc Encoder-Decoder cơ bản khi xử lý các câu dài là gì?**

- [ ] a) Nó quá nhanh.
    
- [x] b) Nó phải nén toàn bộ thông tin của câu dài vào một vector ngữ cảnh có kích thước cố định, gây ra hiện tượng "thắt cổ chai thông tin".
    
- [ ] c) Nó chỉ hoạt động với các câu ngắn.
    
- [ ] d) Nó yêu cầu quá nhiều bộ nhớ.
    

**Câu 18:** **Thuật toán tìm kiếm nào chọn ra từ có xác suất cao nhất ở mỗi bước để tạo ra câu dịch?**

- [ ] a) Beam Search
    
- [ ] b) Breadth-First Search
    
- [x] c) Greedy Search
    
- [ ] d) Depth-First Search
    

**Câu 19:** **Tại sao Greedy Search thường không phải là thuật toán tốt nhất để dịch máy?**

- [ ] a) Vì nó quá chậm.
    
- [x] b) Vì việc chọn từ tốt nhất ở mỗi bước có thể dẫn đến một câu hoàn chỉnh không tối ưu về mặt tổng thể.
    
- [ ] c) Vì nó không thể xử lý các từ không có trong từ điển.
    
- [ ] d) Vì nó yêu cầu beam width lớn.
    

**Câu 20:** **Beam Search với beam width `B=1` tương đương với thuật toán nào?**

- [ ] a) Random Search
    
- [x] b) Greedy Search
    
- [ ] c) Breadth-First Search
    
- [ ] d) Không có thuật toán nào.
    

**Câu 21:** **Trong Beam Search, tham số `B` (beam width) có ý nghĩa gì?**

- [ ] a) Số lượng câu dịch cuối cùng được tạo ra.
    
- [x] b) Số lượng giả thuyết (lựa chọn) tốt nhất được giữ lại ở mỗi bước.
    
- [ ] c) Kích thước tối đa của câu dịch.
    
- [ ] d) Tốc độ học.
    

**Câu 22:** **Mục đích của việc chuẩn hóa độ dài (Length Normalization) trong Beam Search là gì?**

- [ ] a) Để ưu tiên các câu dịch ngắn hơn, vốn có tích các xác suất cao hơn.
    
- [x] b) Để phạt các câu dịch quá dài bằng cách chia log của xác suất cho độ dài câu.
    
- [ ] c) Để đảm bảo tất cả các câu dịch có cùng độ dài.
    
- [ ] d) Để tăng tốc độ tìm kiếm.
    

**Câu 23:** **Chỉ số BLEU (Bilingual Evaluation Understudy) được dùng để làm gì?**

- [ ] a) Để đo tốc độ của một mô hình dịch máy.
    
- [x] b) Để đánh giá chất lượng của một câu dịch máy bằng cách so sánh nó với một hoặc nhiều câu dịch tham khảo của con người.
    
- [ ] c) Để tính toán hàm chi phí trong quá trình huấn luyện.
    
- [ ] d) Để chọn ra beam width tốt nhất.
    

**Câu 24:** **Cơ chế chú ý (Attention Mechanism) giải quyết vấn đề câu dài của mô hình Encoder-Decoder bằng cách nào?**

- [ ] a) Bằng cách tăng kích thước của vector ngữ cảnh.
    
- [x] b) Cho phép Decoder ở mỗi bước tạo từ, "nhìn lại" và tập trung vào các phần khác nhau, phù hợp của câu đầu vào.
    
- [ ] c) Bằng cách sử dụng một mạng nơ-ron lớn hơn.
    
- [ ] d) Bằng cách cắt các câu dài thành nhiều câu ngắn.
    

**Câu 25:** **Trong mô hình Attention, trọng số chú ý `α<t, t'>` cho biết điều gì?**

- [ ] a) Mức độ quan trọng của từ đầu vào thứ `t` đối với từ đầu ra thứ `t'`.
    
- [ ] b) Mức độ quan trọng của từ đầu ra thứ `t` đối với từ đầu vào thứ `t'`.
    
- [x] c) Mức độ quan trọng của từ đầu vào thứ `t'` khi tạo ra từ đầu ra thứ `t`.
    
- [ ] d) Xác suất của từ đầu ra thứ `t`.
    

**Câu 26:** **Trong bài toán chú thích ảnh (Image Captioning), vai trò của Encoder thường được đảm nhiệm bởi kiến trúc nào?**

- [ ] a) Một mạng RNN.
    
- [ ] b) Một mạng Transformer.
    
- [x] c) Một mạng CNN đã được huấn luyện trước (ví dụ: VGG, ResNet).
    
- [ ] d) Một mô hình tuyến tính.
    

**Câu 27:** **Hàm chi phí CTC (Connectionist Temporal Classification) hữu ích cho bài toán nào?**

- [ ] a) Dịch máy.
    
- [ ] b) Phân loại cảm xúc.
    
- [x] c) Nhận dạng giọng nói, nơi không có sự căn chỉnh chính xác giữa chuỗi âm thanh đầu vào và chuỗi văn bản đầu ra.
    
- [ ] d) Tạo văn bản.
    

**Câu 28:** **Trong một hệ thống phát hiện từ kích hoạt (trigger word detection), nhãn của dữ liệu thường được gán như thế nào?**

- [ ] a) Gán nhãn 1 cho toàn bộ đoạn âm thanh nếu có từ kích hoạt.
    
- [x] b) Gán nhãn 1 cho các khung thời gian ngay sau khi từ kích hoạt được nói xong.
    
- [ ] c) Gán nhãn 1 cho các khung thời gian trước khi từ kích hoạt được nói.
    
- [ ] d) Không cần gán nhãn.
    

**Câu 29:** **Nếu lỗi dịch máy của bạn chủ yếu là do Beam Search, bạn nên làm gì? (dựa trên phân tích lỗi)**

- [x] a) Tăng beam width `B`.
    
- [ ] b) Huấn luyện lại mô hình RNN.
    
- [ ] c) Thu thập thêm dữ liệu.
    
- [ ] d) Giảm beam width `B`.
    

**Câu 30:** **Nếu lỗi dịch máy của bạn chủ yếu là do mô hình RNN, bạn nên làm gì?**

- [ ] a) Tăng beam width `B`.
    
- [x] b) Thử một kiến trúc RNN khác, thêm điều chuẩn hóa, hoặc thu thập thêm dữ liệu.
    
- [ ] c) Giảm beam width `B`.
    
- [ ] d) Chỉ cần chạy lại Beam Search.
    

**Câu 31:** **Động lực chính đằng sau việc phát minh ra kiến trúc Transformer là gì?**

- [ ] a) Để tạo ra một mô hình có ít tham số hơn RNN.
    
- [x] b) Để khắc phục hạn chế về xử lý tuần tự của RNN và cho phép xử lý song song toàn bộ chuỗi, giúp nắm bắt các phụ thuộc xa tốt hơn.
    
- [ ] c) Để chuyên biệt hóa cho các bài toán thị giác máy tính.
    
- [ ] d) Để sử dụng ít dữ liệu hơn.
    

**Câu 32:** **Cơ chế cốt lõi của Transformer là gì?**

- [ ] a) Các kết nối hồi quy.
    
- [ ] b) Các lớp tích chập.
    
- [x] c) Tự chú ý (Self-Attention).
    
- [ ] d) Các cổng (gates) như trong LSTM.
    

**Câu 33:** **Trong Self-Attention, ba vector Query (Q), Key (K), và Value (V) được tạo ra từ đâu?**

- [ ] a) Từ ba nguồn dữ liệu khác nhau.
    
- [x] b) Chúng được tạo ra bằng cách nhân vector embedding của cùng một từ đầu vào với ba ma trận trọng số khác nhau (`W_Q`, `W_K`, `W_V`).
    
- [ ] c) Chúng là các hằng số cố định.
    
- [ ] d) Chúng được lấy ngẫu nhiên.
    

**Câu 34:** **Vai trò của Query, Key, và Value trong Self-Attention là gì?**

- [ ] a) Query hỏi, Key trả lời, Value cung cấp thông tin.
    
- [x] b) Query đại diện cho từ hiện tại, nó so khớp với tất cả các Key (đại diện cho các từ khác) để tìm ra trọng số chú ý, sau đó các trọng số này được dùng để tính tổng có trọng số của các Value.
    
- [ ] c) Chúng không có vai trò cụ thể.
    
- [ ] d) Cả ba đều được dùng để tính toán hàm chi phí.
    

**Câu 35:** **Mục đích của "Multi-Head Attention" là gì?**

- [ ] a) Để làm cho mô hình phức tạp hơn một cách không cần thiết.
    
- [x] b) Cho phép mô hình cùng lúc chú ý đến các thông tin từ các không gian con biểu diễn khác nhau (ví dụ: một "đầu" có thể tập trung vào quan hệ cú pháp, một "đầu" khác tập trung vào quan hệ ngữ nghĩa).
    
- [ ] c) Để xử lý nhiều ngôn ngữ cùng lúc.
    
- [ ] d) Để giảm số lượng tham số.
    

**Câu 36:** **Tại sao Transformer cần "Positional Encoding" (Mã hóa vị trí)?**

- [x] a) Vì cơ chế self-attention không có tính tuần tự, nó xử lý tất cả các từ như một tập hợp. Positional Encoding được thêm vào để cung cấp thông tin về vị trí của các từ trong chuỗi.
    
- [ ] b) Để tăng số chiều của vector embedding.
    
- [ ] c) Để giảm số chiều của vector embedding.
    
- [ ] d) Nó không thực sự cần thiết.
    

**Câu 37:** **Trong khối Decoder của Transformer, "Masked Multi-Head Attention" có tác dụng gì?**

- [ ] a) Che đi một số từ ngẫu nhiên để điều chuẩn hóa.
    
- [x] b) Ngăn chặn việc một vị trí có thể "nhìn thấy" các vị trí trong tương lai của chuỗi đầu ra, đảm bảo rằng dự đoán tại bước `t` chỉ phụ thuộc vào các đầu ra đã biết trước đó.
    
- [ ] c) Che đi các từ không quan trọng trong câu đầu vào.
    
- [ ] d) Chỉ được sử dụng trong quá trình inference.
    

**Câu 38:** **Thành phần "Add & Norm" trong Transformer bao gồm những gì?**

- [ ] a) Phép cộng và phép nhân.
    
- [x] b) Một kết nối tắt (residual connection) và một lớp chuẩn hóa lớp (Layer Normalization).
    
- [ ] c) Data augmentation và chuẩn hóa dữ liệu.
    
- [ ] d) Phép cộng và hàm Softmax.
    

**Câu 39:** **Đâu là một mô hình nổi tiếng được xây dựng dựa trên kiến trúc Transformer?**

- [ ] a) Word2Vec
    
- [ ] b) GloVe
    
- [ ] c) LSTM
    
- [x] d) BERT, GPT
    

**Câu 40:** **So với RNN, Transformer có ưu điểm gì về mặt tính toán?**

- [ ] a) Nó luôn yêu cầu ít bộ nhớ hơn.
    
- [x] b) Các phép tính trong nó có thể được song song hóa cao độ, giúp tận dụng tốt GPU và huấn luyện nhanh hơn trên các chuỗi dài.
    
- [ ] c) Nó không cần backpropagation.
    
- [ ] d) Nó có ít tham số hơn.
    

**Câu 41:** **Trong mô hình Encoder-Decoder với Attention, vector ngữ cảnh `c<t>` được tính như thế nào?**

- [ ] a) Là trạng thái ẩn cuối cùng của Encoder.
    
- [x] b) Là tổng có trọng số của các trạng thái ẩn của Encoder, với trọng số là các trọng số chú ý.
    
- [ ] c) Là trạng thái ẩn đầu tiên của Encoder.
    
- [ ] d) Là trung bình của tất cả các trạng thái ẩn của Encoder.
    

**Câu 42:** **Trong Self-Attention, tại sao lại chia cho `sqrt(d_k)` trong công thức `softmax(QKᵀ / sqrt(d_k))`?**

- [ ] a) Để làm cho kết quả là số nguyên.
    
- [x] b) Để ổn định gradient, ngăn chặn việc tích vô hướng trở nên quá lớn khi số chiều `d_k` lớn.
    
- [ ] c) Đây là một tham số có thể học được.
    
- [ ] d) Để chuẩn hóa độ dài của vector.
    

**Câu 43:** **Kiến trúc Transformer có các kết nối hồi quy (recurrent connections) không?**

- [ ] a) Có, giống hệt như RNN.
    
- [x] b) Không, nó hoàn toàn dựa vào cơ chế self-attention.
    
- [ ] c) Chỉ có ở khối Encoder.
    
- [ ] d) Chỉ có ở khối Decoder.
    

**Câu 44:** **"Fine-tuning" một mô hình Transformer đã được huấn luyện trước (như BERT) cho một tác vụ cụ thể (như NER) thường bao gồm bước nào?**

- [ ] a) Huấn luyện lại toàn bộ mô hình từ đầu trên dữ liệu mới.
    
- [x] b) Giữ nguyên phần lớn mô hình và chỉ thêm/huấn luyện một vài lớp phân loại ở trên cùng.
    
- [ ] c) Chỉ sử dụng các positional encodings.
    
- [ ] d) Loại bỏ cơ chế attention.
    

**Câu 45:** **Trong bài toán Question Answering (QA), mô hình Transformer thường được huấn luyện để làm gì?**

- [ ] a) Tạo ra một câu trả lời hoàn toàn mới.
    
- [x] b) Dự đoán vị trí bắt đầu và kết thúc của câu trả lời trong một đoạn văn bản cho trước.
    
- [ ] c) Dịch câu hỏi sang một ngôn ngữ khác.
    
- [ ] d) Tóm tắt đoạn văn bản.
    

**Câu 46:** **Sự khác biệt chính giữa khối Encoder và Decoder trong Transformer là gì?**

- [ ] a) Encoder không có self-attention.
    
- [x] b) Decoder có thêm một lớp "Masked Multi-Head Attention" và một lớp multi-head attention thứ hai để chú ý đến đầu ra của Encoder.
    
- [ ] c) Decoder không có lớp Feed Forward.
    
- [ ] d) Không có sự khác biệt nào.
    

**Câu 47:** **Đâu là một nhược điểm của Transformer so với RNN?**

- [ ] a) Khó nắm bắt các phụ thuộc xa.
    
- [x] b) Chi phí tính toán và bộ nhớ tăng theo bậc hai với độ dài chuỗi.
    
- [ ] c) Không thể xử lý song song.
    
- [ ] d) Không thể áp dụng cho các bài toán NLP.
    

**Câu 48:** **"Positional Encoding" trong Transformer thường được tạo ra bằng cách nào?**

- [ ] a) Bằng một mạng nơ-ron nhỏ.
    
- [x] b) Bằng cách sử dụng các hàm sin và cos ở các tần số khác nhau.
    
- [ ] c) Là các vector có thể học được.
    
- [ ] d) Bằng cách gán một số nguyên cho mỗi vị trí.
    

**Câu 49:** **Trong Word2Vec, tại sao Negative Sampling lại hiệu quả hơn Hierarchical Softmax?**

- [ ] a) Về mặt lý thuyết, Hierarchical Softmax tốt hơn.
    
- [x] b) Trong thực tế, Negative Sampling đơn giản hóa bài toán thành nhiều bài toán phân loại nhị phân độc lập, thường cho kết quả tốt hơn và dễ triển khai hơn.
    
- [ ] c) Negative Sampling yêu cầu ít dữ liệu hơn.
    
- [ ] d) Hierarchical Softmax không thể học được các từ hiếm.
    

**Câu 50:** **Mô hình nào sau đây không phải là mô hình sequence-to-sequence?**

- [ ] a) Dịch máy.
    
- [ ] b) Tóm tắt văn bản.
    
- [x] c) Phân loại cảm xúc (sử dụng RNN many-to-one).
    
- [ ] d) Tạo chú thích ảnh.
    

**Câu 51:** **Trong BLEU score, "brevity penalty" (phạt độ ngắn) được dùng để làm gì?**

- [ ] a) Để phạt các câu dịch máy quá dài so với câu tham khảo.
    
- [x] b) Để phạt các câu dịch máy quá ngắn so với câu tham khảo, tránh trường hợp mô hình chỉ dịch một từ đúng để có precision cao.
    
- [ ] c) Để thưởng cho các câu dịch ngắn.
    
- [ ] d) Để đo lường tốc độ dịch.
    

**Câu 52:** **Lớp "Feed Forward Network" trong mỗi khối của Transformer có đặc điểm gì?**

- [ ] a) Nó là một mạng RNN.
    
- [ ] b) Nó là một mạng tích chập (CNN).
    
- [x] c) Nó là một mạng nơ-ron truyền thẳng (fully-connected) đơn giản, được áp dụng độc lập cho từng vị trí.
    
- [ ] d) Nó chia sẻ trọng số giữa tất cả các vị trí.
    

**Câu 53:** **Trong bài toán Question Answering, fine-tuning mô hình Transformer thường yêu cầu đầu vào là gì?**

- [ ] a) Chỉ câu hỏi.
    
- [ ] b) Chỉ đoạn văn.
    
- [x] c) Cặp (câu hỏi, đoạn văn).
    
- [ ] d) Chỉ câu trả lời.
    

**Câu 54:** **"Scaled Dot-Product Attention" là tên gọi của cơ chế nào?**

- [ ] a) Toàn bộ kiến trúc Transformer.
    
- [x] b) Cơ chế self-attention cụ thể được sử dụng trong Transformer.
    
- [ ] c) Lớp Feed Forward Network.
    
- [ ] d) Lớp Positional Encoding.
    

**Câu 55:** **Kiến trúc Transformer được giới thiệu lần đầu tiên trong bài báo nào?**

- [ ] a) "Deep Residual Learning for Image Recognition"
    
- [ ] b) "GloVe: Global Vectors for Word Representation"
    
- [x] c) "Attention Is All You Need"
    
- [ ] d) "BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding"
    

**Câu 56:** **Tại sao Attention có thể được xem là một cơ chế "mềm" (soft)?**

- [ ] a) Vì nó dễ lập trình.
    
- [x] b) Vì nó gán một trọng số (một giá trị mềm) cho mỗi từ đầu vào, thay vì chọn "cứng" một từ duy nhất để tập trung vào.
    
- [ ] c) Vì nó không yêu cầu nhiều bộ nhớ.
    
- [ ] d) Vì nó sử dụng hàm kích hoạt Softmax.
    

**Câu 57:** **Trong khối Decoder của Transformer, lớp Multi-Head Attention thứ hai nhận Key (K) và Value (V) từ đâu?**

- [ ] a) Từ lớp Masked Multi-Head Attention ngay trước đó.
    
- [x] b) Từ đầu ra của khối Encoder.
    
- [ ] c) Từ các positional encodings.
    
- [ ] d) Từ dữ liệu đầu vào gốc.
    

**Câu 58:** **Đâu là một hạn chế của chỉ số BLEU?**

- [x] a) Nó không xem xét đến ý nghĩa hoặc cấu trúc ngữ pháp của câu.
    
- [ ] b) Nó quá chậm để tính toán.
    
- [ ] c) Nó yêu cầu nhiều GPU.
    
- [ ] d) Nó chỉ hoạt động với các câu ngắn.
    

**Câu 59:** **"Extractive Question Answering" có nghĩa là gì?**

- [ ] a) Mô hình tự tạo ra câu trả lời.
    
- [x] b) Mô hình trích xuất một đoạn văn bản từ ngữ cảnh cho trước để làm câu trả lời.
    
- [ ] c) Mô hình chỉ trả lời "có" hoặc "không".
    
- [ ] d) Mô hình dịch câu hỏi.
    

**Câu 60:** **So với RNN, Transformer có khả năng nắm bắt các phụ thuộc xa tốt hơn là do:**

- [ ] a) Nó có nhiều lớp hơn.
    
- [x] b) Đường đi trực tiếp giữa hai từ bất kỳ trong cơ chế self-attention có độ dài là O(1), không phụ thuộc vào khoảng cách giữa chúng trong chuỗi.
    
- [ ] c) Nó sử dụng hàm kích hoạt ReLU.
    
- [ ] d) Nó có kết nối hồi quy.
    

---

#### Ôn tập bổ sung: Thiết lập Học sâu & Regularization (Coursera)

**Câu 1:** If you have 10,000 examples, how would you split the train/dev/test set? Choose the best option.

- [ ] a) 33% train. 33% dev. 33% test.
    
- [ ] b) 60% train. 20% dev. 20% test.
    
- [x] c) 98% train. 1% dev. 1% test.
    

> [!success]- Giải thích
> Yes. This might be considered a small data set, not in the range of big data. Thus a more classical (old) best practice should be used.

**Câu 2:** In a personal experiment, an M.L. student decides to not use a test set, only train-dev sets. In this case which of the following is true?

- [x] a) He might be overfitting to the dev set.
    
- [ ] b) He won't be able to measure the variance of the model.
    
- [ ] c) He won't be able to measure the bias of the model.
    
- [ ] d) Not having a test set is unacceptable under any circumstance.
    

> [!success]- Giải thích
> No. Although not recommended if a more accurate measure of the performance is not necessary, it is ok to not use a test set. However, this might cause an overfit to the dev set.

**Câu 3:** If your Neural Network model seems to have high variance, what of the following would be promising things to try?

- [ ] a) Make the Neural Network deeper
    
- [x] b) Get more training data
    
- [x] c) Add regularization
    
- [ ] d) Increase the number of units in each hidden layer
    
- [ ] e) Get more test data
    

**Câu 4:** You are working on an automated check-out kiosk for a supermarket and are building a classifier for apples, bananas, and oranges. Suppose your classifier obtains a training set error of 19% and a development set error of 21%. Which of the following is the most promising strategy to improve your classifier? (Assume the human error is approximately 0%)

- [ ] a) Get more training data.
    
- [ ] b) Increase the regularization parameter lambda.
    
- [x] c) Use a bigger network.
    

> [!success]- Giải thích
> A larger network can reduce bias by enabling the model to learn more complex patterns.

**Câu 5:** In every case it is a good practice to use dropout when training a deep neural network because it can help to prevent overfitting. True/False?

- [x] a) False
    
- [ ] b) True
    

> [!success]- Giải thích
> Correct. In most cases, it is recommended to not use dropout if there is no overfit. Although in computer vision, due to the nature of the data, it is the default practice.

**Câu 6:** To reduce high variance, the regularization hyperparameter lambda must be increased. True or False?

- [x] a) True
    
- [ ] b) False
    

> [!success]- Giải thích
> Correct. By increasing the regularization parameter the magnitude of the weight parameters is reduced. This helps reduce the variance.

**Câu 7:** Which of the following are true about dropout?

- [x] a) In practice, it eliminates units of each layer with a probability of 1 - keep_prob.
    
- [x] b) It helps to reduce overfitting.
    
- [ ] c) In practice, it eliminates units of each layer with a probability of keep_prob.
    
- [ ] d) It helps to reduce the bias of a model.
    

> [!success]- Giải thích
> Correct. The probability that dropout doesn't eliminate a neuron is keep_prob.
> The dropout is a regularization technique and thus helps to reduce the overfit.

**Câu 8:** Increasing the parameter keep_prob from (say) 0.5 to 0.6 will likely cause the following: (Check the two that apply)

- [ ] a) Increasing the regularization effect
    
- [x] b) Reducing the regularization effect
    
- [ ] c) Causing the neural network to end up with a higher training set error
    
- [x] d) Causing the neural network to end up with a lower training set error
    

**Câu 9:** Which of these techniques are useful for reducing variance (reducing overfitting)? (Check all that apply.)

- [x] a) Dropout
    
- [ ] b) Xavier initialization
    
- [x] c) L2 regularization
    
- [ ] d) Exploding gradient
    
- [x] e) Data augmentation
    
- [ ] f) Vanishing gradient
    
- [ ] g) Gradient Checking
    

**Câu 10:** Suppose that a model uses, as one feature, the total number of kilometers walked by a person during a year, and another feature is the height of the person in meters. What is the most likely effect of normalization of the input data?

- [ ] a) It won't have any positive or negative effects.
    
- [ ] b) It will make the data easier to visualize.
    
- [x] c) It will make the training faster.
    
- [ ] d) It will increase the variance of the model.
    
#### Ôn tập bổ sung: Thuật toán Tối ưu hóa & Batch Norm (Coursera)

**Câu 1:** **What is a primary learning objective related to optimization methods according to the sources?**

- [ ] a) To only apply Stochastic Gradient Descent
    
- [ ] b) To avoid using random minibatches to prevent convergence
    
- [x] c) To apply optimization methods such as Stochastic Gradient Descent, Momentum, RMSProp, and Adam
    
- [ ] d) To ignore the benefits of learning rate decay in optimization
    

**Câu 2:** **What does "mini-batch gradient descent" primarily accelerate in deep learning?**

- [ ] a) Data preprocessing only
    
- [ ] b) Deep learning training on large datasets
    
- [ ] c) Model deployment
    
- [x] d) Hyperparameter tuning
    

**Câu 3:** **What is a key difference between Batch Gradient Descent and Mini-Batch Gradient Descent regarding updates?**

- [ ] a) Batch Gradient Descent makes quick updates, while Mini-Batch Gradient Descent makes smooth updates
    
- [ ] b) Batch Gradient Descent considers the entire training data for a single update, while Mini-Batch Gradient Descent uses a subset
    
- [ ] c) Mini-Batch Gradient Descent always results in noisier updates than Batch Gradient Descent
    
- [ ] d) Batch Gradient Descent is faster than Mini-Batch Gradient Descent for large datasets
    

**Câu 4:** **In the context of mini-batch gradient descent, what does "an epoch" mean?**

- [ ] a) A single iteration through a mini-batch
    
- [ ] b) The total number of training samples
    
- [x] c) Passing each sample of the training set one time through the network to update the parameters
    
- [ ] d) The size of a mini-batch
    

**Câu 5:** **Given a dataset with n=2000 samples and mini-batch size b=4, how many iterations correspond to one epoch in mini-batch gradient descent?**

- [ ] a) 2000 iterations
    
- [ ] b) 1 iteration
    
- [ ] c) 500 iterations
    
- [ ] d) 4 iterations
    

**Câu 6:** **What is one of the main advantages of using random minibatches?**

- [ ] a) It simplifies data collection
    
- [ ] b) It accelerates convergence and improves optimization
    
- [ ] c) It reduces the need for bias correction
    
- [ ] d) It guarantees finding the global optima
    

**Câu 7:** **How does the cost function typically behave during mini-batch gradient descent, compared to batch gradient descent?**

- [ ] a) It decreases smoothly on every iteration, just like batch gradient descent
    
- [ ] b) It is noisier with mini-batch iterations but still decreases over time
    
- [ ] c) It always increases due to the small sample size
    
- [ ] d) It remains constant due to the iterative updates
    

**Câu 8:** **What is a general guideline for choosing a mini-batch size when the training set is small (m < 2000)?**

- [ ] a) Always use the entire training set (mini-batch size = m)
    
- [ ] b) Select a mini-batch size of 64, 128, 256, or 512
    
- [ ] c) Use a mini-batch size of 1 for stochastic gradient descent
    
- [ ] d) The mini-batch size does not affect training for small datasets
    

**Câu 9:** **Mini-batch gradient descent accelerates training on large datasets by employing a loop to iterate through each mini-batch. What technique is crucial for efficient computation on m examples?**

- [ ] a) Normalization
    
- [ ] b) Regularization
    
- [ ] c) Vectorization
    
- [ ] d) Initialization
    

**Câu 10:** What is the primary purpose of Exponentially Weighted Averages (EWAs)?

- [ ] a) To compute a simple average of data points
    
- [ ] b) To compute a moving average of a sequence of data points that assigns exponentially decreasing weights to previous values
    
- [ ] c) To apply bias correction to raw data
    
- [ ] d) To randomly select data points for averaging
    

**Câu 11:** In the EWA formula (Vt​=βVt−1​+(1−β)θt​), what does the parameter β control?

- [ ] a) The number of data points
    
- [ ] b) The weight given to the current data point
    
- [ ] c) The weight given to the previous average, often referred to as the smoothing factor
    
- [ ] d) The overall magnitude of the average
    

**Câu 12:** What is the effect of choosing a higher β value (closer to 1) in Exponentially Weighted Averages?

- [ ] a) It leads to a more responsive but volatile sequence
    
- [ ] b) It leads to a smoother sequence with slower adaptation to changes
    
- [ ] c) It completely disregards older data points
    
- [ ] d) It causes overfitting of the data
    

**Câu 13:** Exponentially Weighted Averages are widely used in which fields?

- [ ] a) Only in financial market analysis
    
- [ ] b) Time series analysis, finance, and machine learning
    
- [ ] c) Image processing and natural language understanding only
    
- [ ] d) Database management and network security
    

**Câu 14:** Why is bias correction sometimes applied in Exponentially Weighted Averages, especially during the initial phase of learning?

- [ ] a) The initial Vt​ values are too high
    
- [ ] b) The moving average can underestimate the true value of the parameter due to a small number of initial values
    
- [ ] c) It overestimates the parameter values during the initial phase
    
- [ ] d) It causes the algorithm to diverge
    

**Câu 15:** What is the main goal of applying bias correction in exponentially weighted averages?

- [ ] a) To increase computational costs
    
- [ ] b) To normalize the estimate and account for fewer initial values, providing a more accurate parameter estimate
    
- [ ] c) To make initial bias acceptable
    
- [ ] d) To simplify the overall algorithm
    

**Câu 16:** What is the primary benefit of using "gradient descent with momentum" compared to the standard gradient descent algorithm?

- [ ] a) It always uses a smaller learning rate
    
- [ ] b) It works faster and reduces oscillations, especially in vertical directions
    
- [ ] c) It focuses only on horizontal movement in the cost function
    
- [ ] d) It prevents reaching the global minima
    

**Câu 17:** In gradient descent with momentum, which terms resemble acceleration and friction?

- [ ] a) Only the learning rate, α
    
- [ ] b) (1−β) resembles acceleration, and β acts as friction
    
- [ ] c) dw and db
    
- [ ] d) Vdw​ and Vdb​
    

**Câu 18:** What is the main function of the RMSprop optimization algorithm?

- [ ] a) To maintain a constant learning rate throughout training
    
- [ ] b) To solely reduce horizontal oscillations
    
- [ ] c) To adjust the learning rate for each parameter during the update step by keeping an exponentially weighted average of the squares of the derivatives
    
- [ ] d) To ensure the function is sloped more steeply
    

**Câu 19:** How does RMSprop effectively reduce oscillations in the vertical direction?

- [ ] a) By increasing the update for each parameter
    
- [ ] b) By dividing the update for each parameter by a larger number in the vertical direction
    
- [ ] c) By adding epsilon to the numerator
    
- [ ] d) By using a simple average of the derivatives
    

**Câu 20:** What is the purpose of adding a very small epsilon value to the denominator in the RMSprop algorithm's weight update rule?

- [ ] a) To increase the learning rate
    
- [ ] b) To ensure numerical stability and prevent division by zero or very small numbers
    
- [ ] c) To make the oscillations larger
    
- [ ] d) To simplify the calculation of derivatives
    

**Câu 21:** What is the Adam optimization algorithm (Adaptive Moment Estimation) known for?

- [ ] a) It's a standard gradient descent algorithm with no additional features
    
- [ ] b) It combines the effects of gradient descent with momentum and gradient descent with RMSProp
    
- [ ] c) It is exclusively used for very small datasets
    
- [ ] d) It only adjusts the learning rate for the bias terms
    

**Câu 22:** What are the recommended default values for the hyperparameters β1​ and β2​ in the Adam optimization algorithm?

- [ ] a) β1​=0.5,β2​=0.9
    
- [ ] b) β1​=0.9,β2​=0.999
    
- [ ] c) β1​=0.1,β2​=0.9
    
- [ ] d) β1​=0.999,β2​=0.9
    

**Câu 23:** What is the primary intuition behind using learning rate decay?

- [ ] a) To make learning approaches converge slower
    
- [ ] b) To allow for smaller and more precise steps towards the minimum instead of oscillating around it
    
- [ ] c) To increase training speed and allow for larger steps
    
- [ ] d) To prevent the algorithm from reaching the global minima
    

**Câu 24:** A benefit of using learning rate decay is that initially, when the learning rate is not very small, training will be faster. What happens when the learning rate is slowly reduced?

- [ ] a) It increases the chance of getting stuck in local optima
    
- [ ] b) It leads to larger, less precise steps
    
- [ ] c) There is a higher chance of coming close to the global minima
    
- [ ] d) It causes the model to overfit more quickly
    

**Câu 25:** In the context of modern deep learning, what is the current understanding of the "problem of local optima"?

- [ ] a) It is the primary obstacle to training deep neural networks
    
- [ ] b) Most points of zero gradient in a cost function are not local optima but saddle points
    
- [ ] c) Deep learning algorithms are highly likely to get stuck in bad local optima
    
- [ ] d) The problem has become more severe with advanced deep learning
    

**Câu 26:** In high-dimensional spaces, what are common challenges in optimization for neural networks, where the derivative remains near zero?

- [ ] a) Only global optima
    
- [ ] b) Saddle points and plateaus
    
- [ ] c) Convex light functions
    
- [ ] d) Perfect convergence
    

**Câu 27:** Why is tuning hyperparameters effectively important in deep neural networks?

- [ ] a) It simplifies the network architecture
    
- [ ] b) It can lead to a massive improvement in performance
    
- [ ] c) It eliminates the need for large datasets
    
- [ ] d) It reduces computational costs to zero
    

**Câu 28:** Among the listed hyperparameters (learning rate, momentum, Adam's parameters, number of hidden layers/units, learning rate decay, mini-batch size), which one is typically considered the most important to tune?

- [ ] a) Mini-batch size
    
- [ ] b) Number of hidden units
    
- [ ] c) Learning rate (α)
    
- [ ] d) Momentum (β)
    

**Câu 29:** When tuning hyperparameters, why might randomly selecting values from a uniform distribution be preferable for certain hyperparameters like learning rate (alpha) or beta in exponentially weighted averages?

- [ ] a) It guarantees finding the optimal values
    
- [ ] b) Small changes in these parameters can significantly impact results, and random search is often more effective than grid search
    
- [ ] c) It reduces the need for careful tuning
    
- [ ] d) It only works for a small number of hyperparameters
    

**Câu 30:** For hyperparameters like the learning rate (alpha) or beta in exponentially weighted averages, what kind of scale is often recommended for sampling values?

- [ ] a) Linear scale
    
- [ ] b) Exponential scale
    
- [ ] c) Logarithmic scale
    
- [ ] d) Discrete scale
    

**Câu 31:** What is the "Panda" approach to hyperparameter tuning in practice?

- [ ] a) Training multiple models in parallel with diverse hyperparameters
    
- [ ] b) Carefully adjusting a single model's learning rate by babysitting it
    
- [ ] c) Using grid search for all hyperparameters
    
- [ ] d) Focusing on a fixed set of hyperparameters
    

**Câu 32:** What is the primary purpose of Batch Normalization in deep neural networks?

- [ ] a) To increase the complexity of the network
    
- [ ] b) To normalize mean and variance of hidden unit values to speed up learning
    
- [ ] c) To solely adjust the output layer activations
    
- [ ] d) To prevent the network from converging
    

**Câu 33:** In which part of the neural network is batch normalization typically applied?

- [ ] a) After the activation function
    
- [ ] b) Before the input layer
    
- [ ] c) After calculating the Z-value and before the activation function
    
- [ ] d) Only on the output layer
    

**Câu 34:** How does Batch Normalization contribute to enhancing the efficiency of training in networks with multiple hidden layers?

- [ ] a) It makes the input features less similar
    
- [ ] b) It enhances the efficiency by normalizing mean and variance of hidden unit values
    
- [ ] c) It removes the need for any regularization
    
- [ ] d) It forces the network to learn slower
    

**Câu 35:** Besides speeding up learning, how else can Batch Normalization act as a form of regularization?

- [ ] a) By explicitly adding L2 penalties
    
- [ ] b) By adding some noise to the scaled hidden unit values, similar to dropout
    
- [ ] c) By increasing the batch size significantly
    
- [ ] d) By completely eliminating the need for other regularization techniques
    

**Câu 36:** For what type of classification problem is Softmax regression primarily employed?

- [ ] a) Binary classification (two classes)
    
- [ ] b) Multi-class classification (more than two classes)
    
- [ ] c) Regression problems with continuous outputs
    
- [ ] d) Anomaly detection
    

**Câu 37:** What do the units in the output layer of a Softmax regression network represent?

- [ ] a) The raw linear outputs only
    
- [ ] b) The total number of hidden layers
    
- [ ] c) Probabilities of the input belonging to each specific class
    
- [ ] d) The activation function values directly
    

**Câu 38:** How does the Softmax layer transform its linear output into probabilities?

- [ ] a) By applying a sigmoid function
    
- [ ] b) By directly converting values to percentages
    
- [ ] c) By exponentiating and normalizing the values
    
- [ ] d) By summing the values and taking the average
    

**Câu 39:** What is a key reason for using a Machine Learning Strategy?

- [ ] a) To minimize data collection efforts
    
- [ ] b) To choose the wrong idea and waste time and effort
    
- [ ] c) To determine the most promising ideas and effectively build and ship deep learning products
    
- [ ] d) To avoid experimenting with different algorithms
    

**Câu 40:** What does "orthogonalization" refer to in machine learning?

- [ ] a) Combining all components into a single, complex module
    
- [ ] b) Separating the concerns of a machine learning system into distinct and independent modules or components
    
- [ ] c) Ensuring that modules heavily depend on each other
    
- [ ] d) Applying the same function across all layers of a network
    

> [!success]- Giải thích
> project-root/
> ├── game-client/                # C# (Unity/Godot)
> │   ├── Assets/                 # UI (phong cách Japandi), Models, Scenes
> │   ├── Scripts/                # C# Scripts (áp dụng async/await, Task Parallel Library)
> │   │   ├── Core/               # Logic nền tảng, Object Pooling
> │   │   └── Network/            # Gọi API an toàn với try-catch toàn diện
> │   └── Packages/               # NuGet và các thư viện quản lý qua Package Manager
> ├── backend-services/           # Go (gRPC/HTTP API Gateway & Logic)
> │   ├── cmd/                    # Entry points (hàm main)
> │   ├── internal/               # Logic nghiệp vụ bảo mật (không export ra ngoài)
> │   ├── pkg/                    # Các thư viện dùng chung (O(N log N) algorithms, Utils)
> │   ├── Dockerfile              # Multi-stage build cho Go
> │   └── go.mod
> ├── ai-inference/               # Python (FastAPI xử lý Deep Learning)
> │   ├── app/                    # Các async endpoints xử lý yêu cầu
> │   ├── models/                 # Chứa trọng số và logic suy luận (YOLO, CDCN, Audio)
> │   ├── core/                   # Cấu hình, logging tập trung, và error handling
> │   ├── tests/                  # Pytest cho validation
> │   ├── requirements.txt        # Quản lý dependencies (ưu tiên thư viện có sẵn)
> │   └── Dockerfile              # Môi trường chạy suy luận được tối ưu hóa
> ├── infrastructure/             # DevOps & Quản lý Đám mây
> │   ├── terraform/              # Infrastructure as Code (AWS VPC, EKS, RDS)
> │   ├── helm-charts/            # Cấu hình Kubernetes cho toàn bộ dịch vụ
> │   └── scripts/                # Các shell script hỗ trợ tự động hóa
> ├── .github/                    # CI/CD Workflows (GitHub Actions)
> │   └── workflows/
> │       ├── go-ci.yml
> │       ├── python-mlops.yml
> │       └── unity-build.yml
> └── README.md                   # Tài liệu kiến trúc học thuật và hướng dẫn setup

---

## 🔥 II. TensorFlow – Câu hỏi & Khái niệm

> [!info]
> **TensorFlow** là nền tảng mã nguồn mở end-to-end cho Machine Learning và Deep Learning. Hỗ trợ: tính toán đa chiều (NumPy-style), GPU/distributed processing, automatic differentiation, và model construction/training/export.

**Câu 1:** What is the difference between traditional programming and Machine Learning?

- [ ] a) Machine learning identifies complex activities such as golf, while traditional programming is better suited to simpler activities such as walking.
    
- [x] b) In traditional programming, a programmer has to formulate or code rules manually, whereas, in Machine Learning, the algorithm automatically formulates the rules from the data.
    

**Câu 2:** What do we call the process of telling the computer what the data represents (i.e. this data is for walking, this data is for running)?

- [ ] a) Learning the Data
    
- [ ] b) Categorizing the Data
    
- [ ] c) Programming the Data
    
- [x] d) Labelling the Data
    

**Câu 3:** What is a Dense layer?

- [x] a) A layer of neurons fully connected to its adjacent layers
    
- [ ] b) An amount of mass occupying a volume
    
- [ ] c) A single neuron
    
- [ ] d) A layer of disconnected neurons
    

**Câu 4:** How do you measure how good the current 'guess' is?

- [ ] a) Training a neural network
    
- [ ] b) Figuring out if you win or lose
    
- [x] c) Using the Loss function
    

**Câu 5:** What does the optimizer do?

- [ ] a) Figures out how to efficiently compile your code
    
- [ ] b) Decides to stop training a neural network
    
- [ ] c) Measures how good the current guess is
    
- [x] d) Generates a new and improved guess
    

**Câu 6:** What is Convergence?

- [ ] a) A dramatic increase in loss
    
- [ ] b) A programming API for AI
    
- [ ] c) An analysis that corresponds too closely or exactly to a particular set of data.
    
- [x] d) The process of getting very close to the correct answer
    

**Câu 7:** What does model.fit do?

- [ ] a) It makes a model fit available memory
    
- [x] b) It trains the neural network to fit one set of values to another
    
- [ ] c) It determines if your activity is good for your body
    
- [ ] d) It optimizes an existing model
    

**Câu 8:** What is the resolution of the 70,000 images from the Fashion MNIST dataset?

- [ ] a) 82x82 Greyscale
    
- [ ] b) 100x100 Color
    
- [ ] c) 28x28 Color
    
- [x] d) 28x28 Greyscale
    

**Câu 9:** Why are there 10 output neurons in the Neural Network used as an example for the Computer Vision Problem?

- [x] a) There are 10 different labels
    
- [ ] b) Purely arbitrary
    
- [ ] c) To make it classify 10x faster
    
- [ ] d) To make it train 10x faster
    

**Câu 10:** What does Relu do?

- [ ] a) For a value x, it returns 1/x
    
- [ ] b) It only returns x if x is less than zero
    
- [x] c) It only returns x if x is greater than zero
    
- [ ] d) It returns the negative of x
    

**Câu 11:** Why do you split data into training and test sets?

- [ ] a) To make testing quicker
    
- [ ] b) To make training quicker
    
- [ ] c) To train a network with previously unseen data
    
- [x] d) To test a network with previously unseen data
    

**Câu 12:** True or False: The on_epoch_end function sends a logs object with lots of great information about the current state of training at the start of every epoch

- [ ] a) True
    
- [x] b) False
    

**Câu 13:** Why do you set the callbacks= parameter in your fit function?

- [ ] a) So that the training loops performs all epochs
    
- [ ] b) Because it accelerates the training
    
- [x] c) So, on every epoch you can call back to a code function
    

**Câu 14:** How do Convolutions improve image recognition?

- [ ] a) They make the image clearer
    
- [x] b) They isolate features in images
    
- [ ] c) They make processing of images faster
    
- [ ] d) They make the image smaller
    

**Câu 15:** What does the Pooling technique do to the images?

- [ ] a) Makes them sharper
    
- [ ] b) Combines them
    
- [x] c) Reduces information in them while maintaining some features
    
- [ ] d) Isolates features in them
    

**Câu 16:** True or False. If you pass a 28x28 image through a 3x3 filter the output will be 26x26

- [x] a) True
    
- [ ] b) False
    

**Câu 17:** After max pooling a 26x26 image with a 2x2 filter, the output will be 56x56

- [x] a) False
    
- [ ] b) True
    

**Câu 18:** How does using Convolutions in our Deep neural network impact training?

- [ ] a) It makes it faster
    
- [x] b) Its impact will depend on other factors.
    
- [ ] c) It makes it slower
    
- [ ] d) It does not affect training
    

**Câu 19:** Using Image Generator, how do you label images?

- [ ] a) TensorFlow figures it out from the contents
    
- [ ] b) You have to manually do it
    
- [x] c) It's based on the directory the image is contained in
    
- [ ] d) It's based on the file name
    

**Câu 20:** What method on the Image Generator is used to normalize the image?

- [ ] a) normalize_image
    
- [x] b) rescale
    
- [ ] c) normalize
    
- [ ] d) Rescale_image
    

**Câu 21:** How did we specify the training size for the images?

- [x] a) The target_size parameter on the training generator
    
- [ ] b) The target_size parameter on the validation generator
    
- [ ] c) The training_size parameter on the validation generator
    
- [ ] d) The training_size parameter on the training generator
    

**Câu 22:** When we specify the input_shape to be (300, 300, 3), what does that mean?

- [ ] a) There will be 300 horses and 300 humans, loaded in batches of 3
    
- [ ] b) Every Image will be 300x300 pixels, and there should be 3 Convolutional Layers
    
- [x] c) Every Image will be 300x300 pixels, with 3 bytes to define color
    
- [ ] d) There will be 300 images, each size 300, loaded in batches of 3
    

**Câu 23:** If your training data is close to 1.000 accuracy, but your validation data isn't, what's the risk here?

- [x] a) You're overfitting on your training data
    
- [ ] b) You're overfitting on your validation data
    
- [ ] c) No risk, that's a great result
    
- [ ] d) You're underfitting on your validation data
    

**Câu 24:** Convolutional Neural Networks are better for classifying images like horses and humans because:

- [ ] a) There's a wide variety of humans
    
- [ ] b) There's a wide variety of horses
    
- [x] c) In these images, the features may be in different parts of the frame
    

**Câu 25:** After reducing the size of the images, the training results were different. Why?

- [ ] a) There was more condensed information in the images
    
- [x] b) We removed some convolutions to handle the smaller images
    
- [ ] c) The training was faster
    
- [ ] d) There was less information in the images
    

**Câu 26:** What does flow_from_directory give you on the ImageDataGenerator?

- [ ] a) The ability to easily load images for training
    
- [ ] b) The ability to pick the size of training images
    
- [ ] c) The ability to automatically label images based on their directory name
    
- [x] d) All of the above
    

**Câu 27:** If my Image is sized 150x150, and I pass a 3x3 Convolution over it, what size is the resulting image?

- [ ] a) 153x153
    
- [x] b) 148x148
    
- [ ] c) 150x150
    
- [ ] d) 450x450
    

**Câu 28:** If my data is sized 150x150, and I use Pooling of size 2x2, what size will the resulting image be?

- [ ] a) 300x300
    
- [ ] b) 148x148
    
- [x] c) 75x75
    
- [ ] d) 149x149
    

**Câu 29:** If I want to view the history of my training, how can I access it?

- [x] a) Create a variable 'history' and assign it to the return of model.fit or model.fit_generator
    
- [ ] b) Pass the parameter 'history=true' to the model.fit
    
- [ ] c) Download the model and inspect it
    
- [ ] d) Use a model.fit_generator
    

**Câu 30:** What's the name of the API that allows you to inspect the impact of convolutions on the images?

- [ ] a) The model.images API
    
- [ ] b) The model.convolutions API
    
- [ ] c) The model.pools API
    
- [x] d) The model.layers API
    

**Câu 31:** When exploring the graphs, the loss levelled out at about .75 after 2 epochs, but the accuracy climbed close to 1.0 after 15 epochs. What's the significance of this?

- [ ] a) There was no point training after 2 epochs, as we overfit to the validation data
    
- [x] b) There was no point training after 2 epochs, as we overfit to the training data
    
- [ ] c) A bigger training set would give us better validation accuracy
    
- [ ] d) A bigger validation set would give us better training accuracy
    

**Câu 32:** Why is the validation accuracy a better indicator of model performance than training accuracy?

- [ ] a) It isn't, they're equally valuable
    
- [ ] b) There's no relationship between them
    
- [x] c) The validation accuracy is based on images that the model hasn't been trained with, and thus a better indicator of how the model will perform with new images.
    
- [ ] d) The validation dataset is smaller, and thus less accurate at measuring accuracy, so its performance isn't as important
    

**Câu 33:** Why is overfitting more likely to occur on smaller datasets?

- [ ] a) Because in a smaller dataset, your validation data is more likely to look like your training data
    
- [ ] b) Because there isn't enough data to activate all the convolutions or neurons
    
- [ ] c) Because with less data, the training will take place more quickly, and some features may be missed
    
- [x] d) Because there's less likelihood of all possible features being encountered in the training process.
    

**Câu 34:** How do you use Image Augmentation in TensorFlow

- [ ] a) With the tf.augment API
    
- [ ] b) You have to write a plugin to extend tf.layers
    
- [ ] c) With the keras.augment API
    
- [x] d) Using parameters to the ImageDataGenerator
    

**Câu 35:** If my training data only has people facing left, but I want to classify people facing right, how would I avoid overfitting?

- [ ] a) Use the 'flip' parameter and set 'horizontal'
    
- [x] b) Use the 'horizontal_flip' parameter
    
- [ ] c) Use the 'flip_vertical' parameter around the Y axis
    
- [ ] d) Use the 'flip' parameter
    

**Câu 36:** After adding data augmentation and using the same batch size and steps per epoch, you noticed that each training epoch became a little slower than when you trained without it. Why?

- [ ] a) Because there is more data to train on
    
- [x] b) Because the image preprocessing takes cycles
    
- [ ] c) Because the augmented data is bigger
    
- [ ] d) Because the training is making more mistakes
    

**Câu 37:** What does the fill_mode parameter do?

- [ ] a) There is no fill_mode parameter
    
- [ ] b) It creates random noise in the image
    
- [x] c) It attempts to recreate lost information after a transformation like a shear
    
- [ ] d) It masks the background of an image
    

**Câu 38:** When using Image Augmentation with the ImageDataGenerator, what happens to your raw image data on-disk.

- [ ] a) It gets overwritten, so be sure to make a backup
    
- [ ] b) A copy is made and the augmentation is done on the copy
    
- [x] c) Nothing, all augmentation is done in-memory
    
- [ ] d) It gets deleted
    

**Câu 39:** How does Image Augmentation help solve overfitting?

- [ ] a) It slows down the training process
    
- [x] b) It manipulates the training set to generate more scenarios for features in the images
    
- [ ] c) It manipulates the validation set to generate more scenarios for features in the images
    
- [ ] d) It automatically fits features to images by finding them through image processing techniques
    

**Câu 40:** When using Image Augmentation my training gets...

- [x] a) Slower
    
- [ ] b) Faster
    
- [ ] c) Stays the Same
    
- [ ] d) Much Faster
    

**Câu 41:** Using Image Augmentation effectively simulates having a larger data set for training.

- [ ] a) False
    
- [x] b) True
    

**Câu 42:** If I put a dropout parameter of 0.2, how many nodes will I lose?

- [x] a) 20% of them
    
- [ ] b) 2% of them
    
- [ ] c) 20% of the untrained ones
    
- [ ] d) 2% of the untrained ones
    

**Câu 43:** Why is transfer learning useful?

- [ ] a) Because I can use all of the data from the original training set
    
- [ ] b) Because I can use all of the data from the original validation set
    
- [x] c) Because I can use the features that were learned from large datasets that I may not have access to
    
- [ ] d) Because I can use the validation metadata from large datasets that I may not have access to
    

**Câu 44:** How did you lock or freeze a layer from retraining?

- [ ] a) tf.freeze(layer)
    
- [ ] b) tf.layer.frozen = true
    
- [ ] c) tf.layer.locked = true
    
- [x] d) layer.trainable = false
    

**Câu 45:** How do you change the number of classes the model can classify when using transfer learning? (i.e. the original model handled 1000 classes, but yours handles just 2)

- [ ] a) Ignore all the classes above yours (i.e. Numbers 2 onwards if I'm just classing 2)
    
- [ ] b) Use all classes but set their weights to 0
    
- [x] c) When you add your DNN at the bottom of the network, you specify your output layer with the number of classes you want
    
- [ ] d) Use dropouts to eliminate the unwanted classes
    

**Câu 46:** Can you use Image Augmentation with Transfer Learning Models?

- [ ] a) No, because you are using pre-set features
    
- [x] b) Yes, because you are adding new layers at the bottom of the network, and you can use image augmentation when training these
    

**Câu 47:** Why do dropouts help avoid overfitting?

- [x] a) Because neighbor neurons can have similar weights, and thus can skew the final training
    
- [ ] b) Having less neurons speeds up training
    

**Câu 48:** What would the symptom of a Dropout rate being set too high?

- [x] a) The network would lose specialization to the effect that it would be inefficient or ineffective at learning, driving accuracy down
    
- [ ] b) Training time would increase due to the extra calculations being required for higher dropout
    

**Câu 49:** Which is the correct line of code for adding Dropout of 20% of neurons using TensorFlow

- [ ] a) tf.keras.layers.Dropout(20)
    
- [ ] b) tf.keras.layers.DropoutNeurons(20),
    
- [x] c) tf.keras.layers.Dropout(0.2),
    
- [ ] d) tf.keras.layers.DropoutNeurons(0.2),
    

**Câu 50:** The diagram for traditional programming had Rules and Data In, but what came out?

- [x] a) Answers
    
- [ ] b) Binary
    
- [ ] c) Machine Learning
    
- [ ] d) Bugs
    

**Câu 51:** Why does the DNN for Fashion MNIST have 10 output neurons?

- [ ] a) To make it train 10x faster
    
- [ ] b) To make it classify 10x faster
    
- [ ] c) Purely Arbitrary
    
- [x] d) The dataset has 10 classes
    

**Câu 52:** What is a Convolution?

- [ ] a) A technique to make images smaller
    
- [ ] b) A technique to make images larger
    
- [x] c) A technique to extract features from an image
    
- [ ] d) A technique to remove unwanted images
    

**Câu 53:** Applying Convolutions on top of a DNN will have what impact on training?

- [ ] a) It will be slower
    
- [ ] b) It will be faster
    
- [ ] c) There will be no impact
    
- [x] d) It depends on many factors. It might make your training faster or slower, and a poorly designed Convolutional layer may even be less efficient than a plain DNN!
    

**Câu 54:** What method on an ImageGenerator is used to normalize the image?

- [ ] a) normalize
    
- [ ] b) flatten
    
- [ ] c) rezize()
    
- [x] d) rescale
    

**Câu 55:** When using Image Augmentation with the ImageDataGenerator, what happens to your raw image data on-disk.

- [ ] a) A copy will be made, and the copies are augmented
    
- [ ] b) A copy will be made, and the originals will be augmented
    
- [x] c) Nothing
    
- [ ] d) The images will be edited on disk, so be sure to have a backup
    

**Câu 56:** Can you use Image augmentation with Transfer Learning?

- [ ] a) No - because the layers are frozen so they can't be augmented
    
- [x] b) Yes. It's pre-trained layers that are frozen. So you can augment your images as you train the bottom layers of the DNN with them
    

**Câu 57:** When training for multiple classes what is the Class Mode for Image Augmentation?

- [ ] a) class_mode='multiple'
    
- [ ] b) class_mode='non_binary'
    
- [x] c) class_mode='categorical'
    
- [ ] d) class_mode='all'
    

**Câu 58:** What is the name of the object used to tokenize sentences?

- [ ] a) CharacterTokenizer
    
- [ ] b) TextTokenizer
    
- [ ] c) WordTokenizer
    
- [x] d) Tokenizer
    

**Câu 59:** What is the name of the method used to tokenize a list of sentences?

- [ ] a) tokenize(sentences)
    
- [ ] b) fit_to_text(sentences)
    
- [ ] c) tokenize_on_text(sentences)
    
- [x] d) fit_on_texts(sentences)
    

**Câu 60:** Once you have the corpus tokenized, what's the method used to encode a list of sentences to use those tokens?

- [x] a) texts_to_sequences(sentences)
    
- [ ] b) text_to_sequences(sentences)
    
- [ ] c) texts_to_tokens(sentences)
    
- [ ] d) text_to_tokens(sentences)
    

**Câu 61:** When initializing the tokenizer, how do you specify a token to use for unknown words?

- [x] a) oov_token=
    
- [ ] b) unknown_token=
    
- [ ] c) out_of_vocab=
    
- [ ] d) unknown_word=
    

**Câu 62:** If you don't use a token for out of vocabulary words, what happens at encoding?

- [ ] a) The word is replaced by the most common token
    
- [ ] b) The word isn't encoded, and the sequencing ends
    
- [x] c) The word isn't encoded, and is skipped in the sequence
    
- [ ] d) The word isn't encoded, and is replaced by a zero in the sequence
    

**Câu 63:** If you have a number of sequences of different lengths, how do you ensure that they are understood when fed into a neural network?

- [ ] a) Specify the input layer of the Neural Network to expect different sizes with dynamic_length
    
- [ ] b) Make sure that they are all the same length using the pad_sequences method of the tokenizer
    
- [ ] c) Process them on the input layer of the Neural Network using the pad_sequences property
    
- [x] d) Use the pad_sequences function from the tensorflow.keras.preprocessing.sequence namespace
    

**Câu 64:** If you have a number of sequences of different length, and call pad_sequences on them, what's the default result?

- [ ] a) Nothing, they'll remain unchanged
    
- [x] b) They'll get padded to the length of the longest sequence by adding zeros to the beginning of shorter ones
    
- [ ] c) They'll get cropped to the length of the shortest sequence
    
- [ ] d) They'll get padded to the length of the longest sequence by adding zeros to the end of shorter ones
    

**Câu 65:** When padding sequences, if you want the padding to be at the end of the sequence, how do you do it?

- [ ] a) Call the padding method of the pad_sequences object, passing it 'after'
    
- [x] b) Pass padding='post' to pad_sequences when initializing it
    
- [ ] c) Call the padding method of the pad_sequences object, passing it 'post'
    
- [ ] d) Pass padding='after' to pad_sequences when initializing it
    

**Câu 66:** What is the name of the TensorFlow library containing common data that you can use to train and test neural networks?

- [ ] a) TensorFlow Data
    
- [ ] b) TensorFlow Data Libraries
    
- [x] c) TensorFlow Datasets
    
- [ ] d) There is no library of common data sets, you have to use your own
    

**Câu 67:** How many reviews are there in the IMDB dataset and how are they split?

- [ ] a) 60,000 records, 80/20 train/test split
    
- [ ] b) 50,000 records, 80/20 train/test split
    
- [x] c) 50,000 records, 50/50 train/test split
    
- [ ] d) 60,000 records, 50/50 train/test split
    

**Câu 68:** How are the labels for the IMDB dataset encoded?

- [ ] a) Reviews encoded as a number 1-10
    
- [ ] b) Reviews encoded as a number 1-5
    
- [ ] c) Reviews encoded as a boolean true/false
    
- [x] d) Reviews encoded as a number 0-1
    

**Câu 69:** What is the purpose of the embedding dimension?

- [ ] a) It is the number of words to encode in the embedding
    
- [ ] b) It is the number of dimensions required to encode every word in the corpus
    
- [x] c) It is the number of dimensions for the vector representing the word encoding
    
- [ ] d) It is the number of letters in the word, denoting the size of the encoding
    

**Câu 70:** When tokenizing a corpus, what does the num_words=n parameter do?

- [ ] a) It specifies the maximum number of words to be tokenized, and picks the first 'n' words that were tokenized
    
- [ ] b) It errors out if there are more than n distinct words in the corpus
    
- [ ] c) It specifies the maximum number of words to be tokenized, and stops tokenizing when it reaches n
    
- [x] d) It specifies the maximum number of words to be tokenized, and picks the most common 'n-1' words
    

**Câu 71:** To use word embeddings in TensorFlow, in a sequential layer, what is the name of the class?

- [ ] a) tf.keras.layers.Word2Vector
    
- [ ] b) tf.keras.layers.WordEmbedding
    
- [ ] c) tf.keras.layers.Embed
    
- [x] d) tf.keras.layers.Embedding
    

**Câu 72:** IMDB Reviews are either positive or negative. What type of loss function should be used in this scenario?

- [ ] a) Binary Gradient descent
    
- [ ] b) Categorical crossentropy
    
- [x] c) Binary crossentropy
    
- [ ] d) Adam
    

**Câu 73:** When using IMDB Sub Words dataset, our results in classification were poor. Why?

- [ ] a) The sub words make no sense, so can't be classified
    
- [ ] b) We didn't train long enough
    
- [ ] c) Our neural network didn't have enough layers
    
- [x] d) Sequence becomes much more important when dealing with subwords, but we're ignoring word positions
    

**Câu 74:** When predicting words to generate poetry, the more words predicted the more likely it will end up gibberish. Why?

- [x] a) Because the probability that each word matches an existing phrase goes down the more words you create
    
- [ ] b) It doesn't, the likelihood of gibberish doesn't change
    
- [ ] c) Because you are more likely to hit words not in the training set
    
- [ ] d) Because the probability of prediction compounds, and thus increases overall
    

**Câu 75:** What is a major drawback of word-based training for text generation instead of character-based generation?

- [ ] a) Character based generation is more accurate because there are less characters to predict
    
- [ ] b) Word based generation is more accurate because there is a larger body of words to draw from
    
- [ ] c) There is no major drawback, it's always better to do word-based training
    
- [x] d) Because there are far more words in a typical corpus than characters, it is much more memory intensive
    

**Câu 76:** What are the critical steps in preparing the input sequences for the prediction model?

- [x] a) Generating subphrases from each line using n_gram_sequences.
    
- [x] b) Pre-padding the subphrases sequences.
    
- [ ] c) Converting the seed text to a token sequence using texts_to_sequences.
    
- [ ] d) Splitting the dataset into training and testing sentences.
    

**Câu 77:** In natural language processing, predicting the next item in a sequence is a classification problem. Therefore, after creating inputs and labels from the subphrases, we one-hot encode the labels. What function do we use to create one-hot encoded arrays of the labels?

- [ ] a) tf.keras.utils.SequenceEnqueuer
    
- [x] b) tf.keras.utils.to_categorical
    
- [ ] c) tf.keras.preprocessing.text.one_hot
    
- [ ] d) tf.keras.utils.img_to_array
    

**Câu 78:** True or False: When building the model, we use a sigmoid activated Dense output layer with one neuron per word that lights up when we predict a given word.

- [x] a) False
    
- [ ] b) True
    

**Câu 79:** What is an example of a Univariate time series?

- [ ] a) Hour by hour weather
    
- [ ] b) Fashion items
    
- [x] c) Hour by hour temperature
    
- [ ] d) Baseball scores
    

**Câu 80:** What is an example of a Multivariate time series?

- [ ] a) Hour by hour temperature
    
- [x] b) Hour by hour weather
    
- [ ] c) Fashion items
    
- [ ] d) Baseball scores
    

**Câu 81:** What is imputed data?

- [x] a) A projection of unknown (usually past or missing) data
    
- [ ] b) A good prediction of future data
    
- [ ] c) A bad prediction of future data
    
- [ ] d) Data that has been withheld for various reasons
    

**Câu 82:** A sound wave is a good example of time series data

- [x] a) True
    
- [ ] b) False
    

**Câu 83:** What is Seasonality?

- [ ] a) Data aligning to the 4 seasons of the calendar
    
- [x] b) A regular change in shape of the data
    
- [ ] c) Data that is only available at certain times of the year
    
- [ ] d) Weather data
    

**Câu 84:** What is a trend?

- [ ] a) An overall consistent flat direction for data
    
- [x] b) An overall direction for data regardless of direction
    
- [ ] c) An overall consistent upward direction for data
    
- [ ] d) An overall consistent downward direction for data
    

**Câu 85:** In the context of time series, what is noise?

- [ ] a) Sound waves forming a time series
    
- [ ] b) Data that doesn't have a trend
    
- [x] c) Unpredictable changes in time series data
    
- [ ] d) Data that doesn't have seasonality
    

**Câu 86:** What is autocorrelation?

- [ ] a) Data that automatically lines up in trends
    
- [x] b) Data that follows a predictable shape, even if the scale is different
    
- [ ] c) Data that automatically lines up seasonally
    
- [ ] d) Data that doesn't have noise
    

**Câu 87:** What is a non-stationary time series?

- [ ] a) One that moves seasonally.
    
- [ ] b) One that is consistent across all seasons.
    
- [ ] c) One that has a constructive event forming trend and seasonality.
    
- [x] d) One that has a disruptive event breaking trend and seasonality.
    

**Câu 88:** What is a windowed dataset?

- [ ] a) The time series aligned to a fixed shape
    
- [x] b) A fixed-size subset of a time series
    
- [ ] c) A consistent set of subsets of a time series
    
- [ ] d) There's no such thing
    

**Câu 89:** What does 'drop_remainder=True' do?

- [ ] a) It ensures that all data is used
    
- [ ] b) It ensures that all rows in the data window are the same length by adding data
    
- [x] c) It ensures that all rows in the data window are the same length by cropping data
    
- [ ] d) It ensures that the data is all the same shape
    

**Câu 90:** What's the correct line of code to split an n column window into n-1 columns for features and 1 column for a label

- [ ] a) dataset = dataset.map(lambda window: (window[n-1], window[1]))
    
- [x] b) dataset = dataset.map(lambda window: (window[:-1], window[-1:]))
    
- [ ] c) dataset = dataset.map(lambda window: (window[-1:], window[:-1]))
    
- [ ] d) dataset = dataset.map(lambda window: (window[n], window[1]))
    

**Câu 91:** What does MSE stand for?

- [ ] a) Mean Series error
    
- [x] b) Mean Squared error
    
- [ ] c) Mean Second error
    
- [ ] d) Mean Slight error
    

**Câu 92:** What does MAE stand for?

- [ ] a) Mean Average Error
    
- [ ] b) Mean Advanced Error
    
- [x] c) Mean Absolute Error
    
- [ ] d) Mean Active Error
    

**Câu 93:** If time values are in time[], series values are in series[] and we want to split the series into training and validation at time split_time, what is the correct code?

- [ ] a) time_train = time[:split_time] x_train = series[:split_time] time_valid = time[split_time] x_valid = series[split_time]
    
- [x] b) time_train = time[:split_time] x_train = series[:split_time] time_valid = time[split_time:] x_valid = series[split_time:]
    
- [ ] c) time_train = time[split_time] x_train = series[split_time] time_valid = time[split_time:] x_valid = series[split_time:]
    
- [ ] d) time_train = time[split_time] x_train = series[split_time] time_valid = time[split_time] x_valid = series[split_time]
    

**Câu 94:** If you want to inspect the learned parameters in a layer after training, what's a good technique to use?

- [x] a) Assign a variable to the layer and add it to the model using that variable. Inspect its properties after training.
    
- [ ] b) Run the model with unit data and inspect the output for that layer.
    
- [ ] c) Decompile the model and inspect the parameter set for that layer.
    
- [ ] d) Iterate through the layers dataset of the model to find the layer you want.
    

**Câu 95:** How do you set the learning rate of the SGD optimizer?

- [ ] a) Use the Rate property
    
- [ ] b) Use the RateOfLearning property
    
- [x] c) Use the learning_rate property
    
- [ ] d) You can't set it
    

**Câu 96:** If you want to amend the learning rate of the optimizer on the fly, after each epoch. What do you do?

- [ ] a) Use a LearningRateScheduler and pass it as a parameter to a callback
    
- [ ] b) Callback to a custom function and change the SGD property
    
- [x] c) Use a LearningRateScheduler object in the callbacks namespace and assign that to the callback
    
- [ ] d) You can't set it
    

**Câu 97:** If X is the standard notation for the input to an RNN, what are the standard notations for the outputs?

- [ ] a) Y
    
- [ ] b) H
    
- [x] c) Y(hat) and H
    
- [ ] d) H(hat) and Y
    

**Câu 98:** What is a sequence to vector if an RNN has 30 cells numbered 0 to 29

- [ ] a) The total Y(hat) for all cells
    
- [ ] b) The average Y(hat) for all 30 cells
    
- [x] c) The Y(hat) for the last cell
    
- [ ] d) The Y(hat) for the second cell
    

**Câu 99:** What does a Lambda layer in a neural network do?

- [ ] a) Pauses training without a callback
    
- [ ] b) Changes the shape of the input or output data
    
- [ ] c) There are no Lambda layers in a neural network
    
- [x] d) Allows you to execute arbitrary code while training
    

**Câu 100:** What does the axis parameter of tf.expand_dims do?

- [ ] a) Defines the axis around which to expand the dimensions
    
- [ ] b) Defines the dimension index to remove when you expand the tensor
    
- [ ] c) Defines if the tensor is X or Y
    
- [x] d) Defines the dimension index at which you will expand the shape of the tensor
    

**Câu 101:** A new loss function was introduced in this module, named after a famous statistician. What is it called?

- [ ] a) Hubble loss
    
- [ ] b) Hawking loss
    
- [ ] c) Hyatt loss
    
- [x] d) Huber loss
    

**Câu 102:** What's the primary difference between a simple RNN and an LSTM

- [ ] a) In addition to the H output, RNNs have a cell state that runs across all cells
    
- [x] b) In addition to the H output, LSTMs have a cell state that runs across all cells
    
- [ ] c) LSTMs have a single output, RNNs have multiple
    
- [ ] d) LSTMs have multiple outputs, RNNs have a single one
    

**Câu 103:** If you want to clear out all temporary variables that tensorflow might have from previous sessions, what code do you run?

- [x] a) tf.keras.backend.clear_session()
    
- [ ] b) tf.cache.backend.clear_session()
    
- [ ] c) tf.keras.clear_session
    
- [ ] d) tf.cache.clear_session()
    

**Câu 104:** What happens if you define a neural network with these two layers? tf.keras.layers.Bidirectional(tf.keras.layers.LSTM(32)), tf.keras.layers.Bidirectional(tf.keras.layers.LSTM(32)), tf.keras.layers.Dense(1)

- [ ] a) Your model will fail because you have the same number of cells in each LSTM
    
- [x] b) Your model will fail because you need return_sequences=True after the first LSTM layer
    
- [ ] c) Your model will fail because you need return_sequences=True after each LSTM layer
    
- [ ] d) Your model will compile and run correctly
    

**Câu 105:** How do you add a 1 dimensional convolution to your model for predicting time series data?

- [ ] a) Use a ConvolutionD1 layer type
    
- [ ] b) Use a 1DConvolution layer type
    
- [x] c) Use a Conv1D layer type
    
- [ ] d) Use a 1DConv layer type
    

**Câu 106:** What's the input shape for a univariate time series to a Conv1D?

- [x] a) [None, 1]
    
- [ ] b) []
    
- [ ] c) [1]
    
- [ ] d) [1, None]
    

**Câu 107:** You used a sunspots dataset that was stored in CSV. What's the name of the Python library used to read CSVs?

- [ ] a) CommaSeparatedValues
    
- [x] b) CSV
    
- [ ] c) PyCSV
    
- [ ] d) PyFiles
    

**Câu 108:** If your CSV file has a header that you don't want to read into your dataset, what do you execute before iterating through the file using a 'reader' object?

- [ ] a) reader.read(next)
    
- [ ] b) reader.next
    
- [x] c) next(reader)
    
- [ ] d) reader.ignore_header()
    

**Câu 109:** When you read a row from a reader and want to cast column 2 to another data type, for example, a float, what's the correct syntax?

- [ ] a) float f = row[2].read()
    
- [ ] b) You can't. It needs to be read into a buffer and a new float instantiated from the buffer
    
- [ ] c) Convert.toFloat(row[2])
    
- [x] d) float(row[2])
    

**Câu 110:** What was the sunspot seasonality?

- [ ] a) 22 years
    
- [ ] b) 4 times a year
    
- [ ] c) 11 years
    
- [x] d) 11 or 22 years depending on who you ask
    

**Câu 111:** After studying this course, what neural network type do you think is best for predicting time series like our sunspots dataset?

- [ ] a) DNN
    
- [ ] b) Convolutions
    
- [ ] c) RNN / LSTM
    
- [x] d) A combination of all other answers
    

**Câu 112:** Why is MAE a good analytic for measuring accuracy of predictions for time series?

- [ ] a) It punishes larger errors
    
- [x] b) It doesn't heavily punish larger errors like square errors do
    
- [ ] c) It only counts positive errors
    
- [ ] d) It biases towards small errors
    

**Câu 113:** Why does sequence make a large difference when determining semantics of language?

- [x] a) Because the order in which words appear dictate their impact on the meaning of the sentence
    
- [ ] b) Because the order of words doesn't matter
    
- [ ] c) It doesn't
    
- [ ] d) Because the order in which words appear dictate their meaning
    

**Câu 114:** How do Recurrent Neural Networks help you understand the impact of sequence on meaning?

- [ ] a) They don't
    
- [ ] b) They shuffle the words evenly
    
- [ ] c) They look at the whole sentence at a time
    
- [x] d) They carry meaning from one cell to the next
    

**Câu 115:** How does an LSTM help understand meaning when words that qualify each other aren't necessarily beside each other in a sentence?

- [x] a) Values from earlier words can be carried to later ones via a cell state
    
- [ ] b) They load all words into a cell state
    
- [ ] c) They shuffle the words randomly
    
- [ ] d) They don't
    

**Câu 116:** What keras layer type allows LSTMs to look forward and backward in a sentence?

- [ ] a) Bothdirection
    
- [ ] b) Bilateral
    
- [ ] c) Unilateral
    
- [x] d) Bidirectional
    

**Câu 117:** What's the output shape of a bidirectional LSTM layer with 64 units?

- [ ] a) (128,None)
    
- [ ] b) (128,1)
    
- [x] c) (None, 128)
    
- [ ] d) (None, 64)
    

**Câu 118:** When stacking LSTMs, how do you instruct an LSTM to feed the next one in the sequence?

- [ ] a) Do nothing, TensorFlow handles this automatically
    
- [ ] b) Ensure that they have the same number of units
    
- [x] c) Ensure that return_sequences is set to True only on units that feed to another LSTM
    
- [ ] d) Ensure that return_sequences is set to True on all units
    

**Câu 119:** If a sentence has 120 tokens in it, and a Conv1D with 128 filters with a Kernal size of 5 is passed over it, what's the output shape?

- [ ] a) (None, 120, 124)
    
- [ ] b) (None, 120, 128)
    
- [x] c) (None, 116, 128)
    
- [ ] d) (None, 116, 124)
    

**Câu 120:** What's the best way to avoid overfitting in NLP datasets?

- [ ] a) Use LSTMs
    
- [ ] b) Use GRUs
    
- [ ] c) Use Conv1D
    
- [x] d) None of the above
    

**Câu 121:** Which type of boundary does the UnicodeCharTokenizer use to separate tokens?

- [ ] a) Whitespace
    
- [x] b) Unicode script
    
- [ ] c) Special symbols
    
- [ ] d) Punctuation marks
    

**Câu 122:** How can image augmentation be implemented in TensorFlow?

- [ ] a) By manually modifying each image file
    
- [ ] b) By importing pre-augmented datasets
    
- [x] c) By using the ImageDataGenerator class
    
- [ ] d) By applying image transformations after model training
    

**Câu 123:** What is a potential use case for the RegexSplitter?

- [ ] a) Tokenizing text into subword units for language modeling
    
- [ ] b) Tokenizing multilingual text with different scripts
    
- [x] c) Tokenizing text into individual words based on custom regular expressions
    
- [ ] d) Tokenizing text based on learned subword units for WordPiece models
    

**Câu 124:** What is the advantage of using a subword text encoder over a word-based encoder in TensorFlow?

- [ ] a) Subword encoders are computationally faster
    
- [x] b) Subword encoders handle rare words more effectively
    
- [ ] c) Word-based encoders result in smaller vocabulary sizes
    
- [ ] d) Word-based encoders provide better semantic understanding.
    

**Câu 125:** When might transfer learning be less effective in TensorFlow?

- [ ] a) When the source and target tasks are similar.
    
- [ ] b) When there is a lack of pre-trained models available.
    
- [x] c) When the datasets for the source and target tasks are small and dissimilar.
    
- [ ] d) Transfer learning is always effective, regardless of the scenario.
    

**Câu 126:** Which deep learning architecture is commonly used for predicting the next word in a sequence?

- [ ] a) Convolutional Neural Network (CNN)
    
- [x] b) Recurrent Neural Network (RNN)
    
- [ ] c) Support Vector Machine (SVM)
    
- [ ] d) Decision Tree
    

**Câu 127:** Which TensorFlow module is specifically designed for transferring knowledge from pre-trained models to new tasks in Computer Vision?

- [ ] a) TensorFlow Estimator API
    
- [x] b) TensorFlow Hub
    
- [ ] c) TensorFlow Lite
    
- [ ] d) TensorFlow Extended (TFX)
    

**Câu 128:** Which NLP technique involves breaking down a sentence into its individual components, such as words or phrases?

- [x] a) Tokenization
    
- [ ] b) Clustering
    
- [ ] c) Dimensionality reduction
    
- [ ] d) Regularization
    

**Câu 129:** Which TensorFlow function is commonly used to apply data augmentation to an image?

- [ ] a) tf.image.transform()
    
- [ ] b) tf.data.augmentation.apply()
    
- [ ] c) tf.image.apply_image_augmentation()
    
- [x] d) tf.keras.preprocessing.image.random_transform()
    

**Câu 130:** Which machine learning technique is suitable for handling complex patterns and nonlinear relationships in time series data?

- [ ] a) Exponential Smoothing
    
- [x] b) Decision Trees
    
- [ ] c) Moving Averages
    
- [ ] d) Holt-Winters Method
    

**Câu 131:** What is the purpose of the teacher forcing technique in training a next-word prediction model?

- [x] a) To force the model to predict the ground truth at each step
    
- [ ] b) To increase the model's perplexity
    
- [ ] c) To decrease the influence of the previous words
    
- [ ] d) To speed up the training process
    

**Câu 132:** What is the purpose of the batch method in a TensorFlow dataset?

- [ ] a) To shuffle the dataset
    
- [x] b) To group consecutive elements into batches
    
- [ ] c) To split the dataset into training and validation sets
    
- [ ] d) To apply data augmentation to the dataset
    

**Câu 133:** In a multiclass classifier, what is the role of the "softmax" activation function?

- [ ] a) To introduce non-linearity to the model
    
- [ ] b) To calculate the mean of the predictions
    
- [x] c) To transform raw scores into probability distributions
    
- [ ] d) To increase the complexity of the output layer
    

**Câu 134:** What function of ImageDataGenerator is commonly used for real-time data augmentation during training?

- [x] a) flow_from_directory
    
- [ ] b) fit_genorator
    
- [ ] c) rescale
    
- [ ] d) random_transform
    

**Câu 135:** Which technique can be used to prevent overfitting by randomly disabling a fraction of neurons during training?

- [ ] a) Data augmentation
    
- [ ] b) Early stopping
    
- [ ] c) L2 regularization
    
- [x] d) Dropout
    

**Câu 136:** In TensorFlow, what is the common approach for training only the added layers while keeping the pre-trained weights fixed?

- [ ] a) Setting the learning rate to a very small value.
    
- [x] b) Freezing the layers of the pre-trained model.
    
- [ ] c) Using a high dropout rate.
    
- [ ] d) Training for a large number of epochs.
    

**Câu 137:** How does a subword text encoder handle rare or infrequent words in TensorFlow?

- [ ] a) By replacing them with a special token
    
- [ ] b) By discarding them during encoding
    
- [x] c) By merging them into larger subword units
    
- [ ] d) By assigning higher weights to them
    

**Câu 138:** What is a typical task associated with a dog and cat dataset on Kaggle?

- [ ] a) Sentiment analysis
    
- [x] b) Object detection
    
- [ ] c) Speech recognition
    
- [ ] d) Financial forecasting
    

**Câu 139:** Which metric is commonly used to measure the accuracy of a forecasting model by comparing the absolute differences between predicted and actual values?

- [ ] a) Mean Squared Error (MSE)
    
- [x] b) Mean Absolute Error (MAE)
    
- [ ] c) Root Mean Squared Error (RMSE)
    
- [ ] d) R-squared (R2)
    

**Câu 140:** How does the SplitMergeTokenizer handle consecutive characters based on custom rules?

- [x] a) It merges them into a single token.
    
- [ ] b) It treats each character as a separate token.
    
- [ ] c) It ignores them during tokenization.
    
- [ ] d) It replaces them with a special token.
    

**Câu 141:** Why is padding necessary in neural networks?

- [ ] a) To increase computational efficiency
    
- [ ] b) To reduce model complexity
    
- [x] c) To ensure all inputs have the same dimensions
    
- [ ] d) To speed up the training process
    

**Câu 142:** Which of the following is a common image augmentation technique used in TensorFlow?

- [ ] a) Image cropping
    
- [ ] b) Image binarization
    
- [ ] c) Image inversion
    
- [x] d) Image mirroring
    

**Câu 143:** What is the purpose of setting the validation_split parameter in flow_from_directory when using ImageDataGenerator?

- [ ] a) It controls the number of validation steps during training.
    
- [x] b) It defines the percentage of images used for validation.
    
- [ ] c) It specifies the validation loss function.
    
- [ ] d) It adjusts the learning rate during validation.
    

**Câu 144:** Which TensorFlow module is commonly used for loading and preprocessing image datasets?

- [ ] a) tf.keras.layers
    
- [ ] b) tf.datasets
    
- [ ] c) tf.image
    
- [x] d) tf.data
    

**Câu 145:** In a multiclass classification problem, how are categorical labels typically represented in TensorFlow?

- [ ] a) As strings
    
- [ ] b) As integer values
    
- [x] c) Using one-hot encoding
    
- [ ] d) Using floating-point numbers
    

**Câu 146:** How can seasonality affect a time series?

- [ ] a) By introducing random noise
    
- [ ] b) By creating long-term trends
    
- [x] c) By causing periodic fluctuations
    
- [ ] d) By removing outliers
    

**Câu 147:** What is the purpose of the Conv2D layer in a computer vision neural network?

- [ ] a) Handling sequence data
    
- [ ] b) Performing sequence data
    
- [x] c) Applying convolutional operations on image data
    
- [ ] d) Normalizing input features
    

**Câu 148:** What does the term "early stopping" refer to in the context of preventing overfitting?

- [ ] a) Terminating the training process when the model performs poorly on the training set
    
- [x] b) Halting training when the model's performance on a validation set plateaus
    
- [ ] c) Increasing the number of training epochs to ensure better convergence
    
- [ ] d) Initiating training earlier than planned to capture more patterns in the data
    

**Câu 149:** What does the term "Exponential Smoothing" refer to in time series forecasting?

- [ ] a) A technique for handling outliers in data
    
- [ ] b) A method for reducing the impact of seasonality
    
- [x] c) A weighted average approach that assigns exponentially decreasing weights to past observations
    
- [ ] d) A process of transforming time series data into a stationary format
    

**Câu 150:** In a typical CNN architecture, what is the purpose of the fully connected (dense) layers?

- [ ] a) Extracting features from input images
    
- [ ] b) Reducing spatial dimensions through pooling
    
- [ ] c) Normalizing the output of convolutional layers
    
- [x] d) Making predictions based on learned features
    

**Câu 151:** How does the vocabulary size impact word-based encodings?

- [x] a) A larger vocabulary size leads to longer encoding vectors
    
- [ ] b) A smaller vocabulary size increases the efficiency of encoding
    
- [ ] c) Vocabulary size has no impact on word-based encodings
    
- [ ] d) A larger vocabulary size reduces the model's ability to generalize
    

**Câu 152:** What role does a "tensor" play in TensorFlow?

- [ ] a) It's a graphical representation of a machine learning model
    
- [ ] b) It's a specific type of machine learning algorithm.
    
- [x] c) It's a fundamental data structure used for numerical computations.
    
- [ ] d) It's a module for handling natural language processing tasks.
    

**Câu 153:** What is the common approach to loading textual data for a multi-class classification task in TensorFlow?

- [ ] a) Using tf.keras.utils.image_dataset_from_directory
    
- [ ] b) Employing the tf.keras.datasets.load_text function
    
- [x] c) Utilizing tf.keras.preprocessing.text_dataset_from_directory
    
- [ ] d) Loading text data is not supported in TensorFlow
    

**Câu 154:** Which TensorFlow layer is commonly used to add a convolutional layer to a CNN model?

- [ ] a) Dense
    
- [x] b) Conv2D
    
- [ ] c) MaxPooling2D
    
- [ ] d) Flatten
    

**Câu 155:** In TensorFlow, what is the role of the tf.data.Dataset.from_tensor_slices() function?

- [ ] a) It creates a dataset from a list of strings.
    
- [x] b) It converts NumPy arrays into TensorFlow datasets.
    
- [ ] c) It generates slices of tensors from a given dataset.
    
- [ ] d) It defines the architecture of a neural network
    

**Câu 156:** What is the purpose of the texts_to_matrix method in the Tokenizer class?

- [ ] a) Converts sequences to text
    
- [ ] b) Adds padding to sequences
    
- [ ] c) Tokenizes words in a document
    
- [x] d) Converts text to numerical matices
    

**Câu 157:** In time series forecasting using LSTMs, what does the term "sequence-to-sequence" refer to?

- [ ] a) Predicting a single future data point from a single input data point
    
- [x] b) Predicting a sequence of future data points from a sequence of input data points
    
- [ ] c) Predicting multiple future data points from a single input data point
    
- [ ] d) Predicting a single future data point from a sequence of input data points
    

**Câu 158:** What happens to leading and trailing characters with different Unicode scripts in the UnicodeScriptTokenizer?

- [ ] a) They are removed from the tokens.
    
- [x] b) They are included as part of the tokens.
    
- [ ] c) They are replaced with special symbols.
    
- [ ] d) They are ignored during tokenization.
    

**Câu 159:** How does the ImageDataGenerator handle the normalization of pixel values in ConvNet training?

- [ ] a) It does not perform any normalization.
    
- [ ] b) It normalizes pixel values to be between 0 and 255.
    
- [ ] c) It automatically adjusts pixel values during training.
    
- [x] d) It scales pixel values to be between 0 and 1.
    

**Câu 160:** How can the ModelCheckpoint callback be beneficial during training?

- [ ] a) It logs training metrics for visualization.
    
- [x] b) It saves the model's weights at specified intervals.
    
- [ ] c) It adjusts the learning rate based on performance.
    
- [ ] d) It stops training when validation loss reaches a plateau.
    

**Câu 161:** What function is typically used to load image data in TensorFlow?

- [ ] a) load_image()
    
- [ ] b) read_image()
    
- [ ] c) tf.load_image()
    
- [x] d) tf.keras.preprocessing.image.load_img()
    

**Câu 162:** When training an LSTM model for time series forecasting, why is it important to normalize the input data?

- [ ] a) To make the data sationary
    
- [ ] b) To handle missing values in the time series
    
- [ ] c) To speed up the training process
    
- [x] d) To ensure consistent convergence during training
    

**Câu 163:** How can you visualize time series data effectively?

- [ ] a) Scatter plots
    
- [ ] b) Bar charts
    
- [x] c) Line charts
    
- [ ] d) Pie charts
    

**Câu 164:** In word-based encodings, what is the advantage of using pretrained word embeddings?

- [ ] a) They increase the vocabulary size.
    
- [ ] b) They reduce the dimensionality of the vectors.
    
- [x] c) They provide word representations learned from extensive data.
    
- [ ] d) They have no impact on the performance of the model.
    

**Câu 165:** Which TensorFlow module is commonly used to load the Inception model for transfer learning?

- [ ] a) tf.keras.preprocessing.image
    
- [ ] b) tf.keras.layers.Conv2D
    
- [x] c) tf.keras.applications.inception_v3
    
- [ ] d) tf.keras.optimizers.Adam
    

**Câu 166:** How can you extract training and validation accuracies from the history object in TensorFlow?

- [ ] a) By using the get_accuracy method
    
- [ ] b) By accessing the accuracy attribute directly
    
- [x] c) By using the history['accuracy'] and history['val_accuracy'] keys
    
- [ ] d) By applying the calculate_accuracy function
    

**Câu 167:** What does the repeat method do when applied to a TensorFlow dataset?

- [x] a) It repeats the dataset multiple times during training.
    
- [ ] b) It adds noise to the dataset.
    
- [ ] c) It repeats the feature-label pairs within each batch.
    
- [ ] d) It reshapes the dataset.
    

**Câu 168:** How does the HubModuleTokenizer handle out-of-vocabulary words?

- [ ] a) It replaces them with a special token.
    
- [ ] b) It ignores them during tokenization.
    
- [ ] c) It treats each charactoer as a separate token.
    
- [x] d) It splits them into subword units based on learned patterns.
    

**Câu 169:** In transfer learning, what are the commonly used pre-trained models in TensorFlow?

- [x] a) MobileNet and Inception
    
- [ ] b) LeNet and AlexNet
    
- [ ] c) Naive Bayes and Decision Trees
    
- [ ] d) Support Vector Machines and k-Nearest Neighbors
    

**Câu 170:** What does the term "tokenization" refer to in the context of word-based encodings?

- [ ] a) Creating a bag-of-words representation
    
- [ ] b) Reducing words to their root forms
    
- [x] c) Breaking down text into individual words or tokens
    
- [ ] d) Applying sentiment analysis to words
    

**Câu 171:** Function to convert numpy array to tensor?

- [ ] a) tf.convert_to_array()
    
- [x] b) tf.convert_to_tensor()
    
- [ ] c) tf.dtypes()
    
- [ ] d) tf.estimator()
    

**Câu 172:** Which of the following evaluation metrics can be used to evaluate a model while modeling a continuous output variable?

- [ ] a) AUC-ROC
    
- [ ] b) Accuracy
    
- [x] c) Mean-Squared-Error
    
- [ ] d) Log loss
    

**Câu 173:** Mention the name of some methods to deal with the overfitting in TensorFlow?

- [ ] a) Dropout Technique
    
- [ ] b) Regularization
    
- [ ] c) Batch Normalization
    
- [x] d) All of the above
    

**Câu 174:** Function to find the version of tensorflow being used in python?

- [ ] a) tf.version
    
- [ ] b) tf.version.VERSION
    
- [x] c) Both A & B
    
- [ ] d) None of the above
    

**Câu 175:** Which is not a valid parameter in tf.keras.model.fit() function?

- [ ] a) batch_size
    
- [ ] b) shuffle
    
- [ ] c) workers
    
- [x] d) loss
    

**Câu 176:** Ways to optimize machine learning models for deployment and execution?

- [ ] a) Overfitting
    
- [x] b) Quantization
    
- [ ] c) Regularization
    
- [ ] d) Underfitting
    

**Câu 177:** Which of the following that a TensorFlow manager can not do?

- [ ] a) Loading Servables
    
- [ ] b) Serving Servables
    
- [ ] c) Unloading Servables
    
- [x] d) Debugging Servables
    

**Câu 178:** The TensorFlow Lite converter takes a TensorFlow model and generates a TensorFlow Lite model of what format, which identified by the .tflite file extension.

- [ ] a) BufferStore
    
- [x] b) FlatBuffer
    
- [ ] c) WeightStore
    
- [ ] d) ModelFormat
    

**Câu 179:** Which is not a module in tfx.components?

- [ ] a) base
    
- [ ] b) bulk_inferrer
    
- [x] c) fit
    
- [ ] d) evaluator
    

**Câu 180:** What is a Data Flow Graph?

- [x] a) A representation of data dependencies between operations
    
- [ ] b) A cartesian (x,y) chart
    
- [ ] c) A graphics user interface
    
- [ ] d) A flowchart describing an algorithm
    
- [ ] e) None of the above
    

**Câu 181:** For convolution, it is better to store images in TensorFlow Graph as:

- [x] a) Placeholder
    
- [ ] b) CSV file
    
- [ ] c) Numpy array
    
- [ ] d) Variable
    
- [ ] e) None of the above
    

**Câu 182:** Which of the subsequent declaration(s) effectively represents an actual neuron in TensorFlow?

- [ ] a) A neuron has a single enter and a single output best
    
- [ ] b) A neuron has multiple inputs but a single output only
    
- [ ] c) A neuron has a single input, however, more than one outputs
    
- [ ] d) A neuron has multiple inputs and more than one outputs
    
- [x] e) All of the above statements are valid
    

> [!success]- Giải thích
> 183. What are the stairs for the usage of a gradient descent algorithm in TensorFlow?
> 1. Calculate error among the actual fee and the anticipated price
> 2. Reiterate until you find the excellent weights of the network
> 3. Pass an enter via the community and get values from the output layer
> 4. Initialize random weight and bias

**Câu 183:** Go to every neurons which contributes to the error and exchange its respective values to lessen the error

- [ ] a) 1, 2, 3, 4, 5
    
- [ ] b) 5, 4, 3, 2, 1
    
- [ ] c) 3, 2, 1, 5, 4
    
- [x] d) 4, 3, 1, 5, 2
    

**Câu 184:** "Convolutional Neural Networks can carry out various forms of transformation (rotations or scaling) in an enter". Is the assertion correct true or false in TensorFlow?

- [ ] a) True
    
- [x] b) False
    

**Câu 185:** Which of the following techniques perform comparable operations as the dropout in a neural community in TensorFlow?

- [x] a) Bagging
    
- [ ] b) Boosting
    
- [ ] c) Stacking
    
- [ ] d) None of those
    

**Câu 186:** Which of the following is authentic approximately model capability (in which version capacity method the potential of the neural community to approximate complex capabilities) in TensorFlow?

- [x] a) As range of hidden layers boom, model capability will increase
    
- [ ] b) As dropout ratio increases, version capacity increases
    
- [ ] c) As mastering charge will increase, model capacity will increase
    
- [ ] d) None of these
    

**Câu 187:** In case you growth the range of hidden layers in a Multi-Layer Perceptron, the category errors of check facts always decreases in TensorFlow. Authentic or fake?

- [ ] a) Authentic
    
- [x] b) Fake
    

> [!success]- Giải thích
> 188. What's the series of the following duties in a perceptron in tensorflow?
> 1. Initialize weights of perceptron randomly
> 2. Visit the subsequent batch of the dataset
> 3. If the prediction does no longer in shape the output, trade the weights

**Câu 188:** For a sample enter, compute an output

- [ ] a) 1, 2, 3, 4
    
- [ ] b) 4, 3, 2, 1
    
- [ ] c) 3, 1, 2, 4
    
- [x] d) 1, 4, 3, 2
    

**Câu 189:** Suppose that you have to limit the value feature via converting the parameters. Which of the subsequent approach could be used for this in TensorFlow?

- [ ] a) Exhaustive seek
    
- [ ] b) Random search
    
- [ ] c) Bayesian Optimization
    
- [x] d) Any of those
    

**Câu 190:** Can a neural network model the characteristic (y=1/x) in TensorFlow?

- [x] a) Sure
    
- [ ] b) No
    

**Câu 191:** Wherein neural internet architecture, does weight sharing occur in TensorFlow?

- [ ] a) Convolutional neural community
    
- [ ] b) Recurrent Neural community
    
- [ ] c) Fully related Neural community
    
- [x] d) Both a and b
    

**Câu 192:** Batch Normalization is useful due to the fact?

- [x] a) It normalizes (adjustments) all the input earlier than sending it to the subsequent layer
    
- [ ] b) It returns again the normalized mean and widespread deviation of weights
    
- [ ] c) It miles a very efficient backpropagation method
    
- [ ] d) None of those
    

**Câu 193:** As opposed to trying to acquire absolute 0 error, we set a metric called Bayes blunders that's the error we hope to achieve. What may be the cause for the use of Bayes blunders in TensorFlow?

- [ ] a) Input variables might not include entire statistics about the output variable
    
- [ ] b) Gadget (that creates input-output mapping) may be stochastic
    
- [ ] c) Constrained training facts
    
- [x] d) All of the above
    

> [!success]- Giải thích
> Dưới đây là toàn bộ 55 câu hỏi trắc nghiệm đã được chuyển sang định dạng checkbox của Obsidian, kèm theo Callout ẩn đáp án và giải thích chi tiết. Bạn chỉ cần copy toàn bộ nội dung này dán vào file `.md` trong Obsidian.

---

## Masterclass Chuyên sâu

### 📖 BỘ TÀI LIỆU ÔN TẬP CHUYÊN SÂU (PHẦN 2): TỪ DỮ LIỆU ĐẾN KHẢ NĂNG TỔNG QUÁT HÓA

### CHUYÊN ĐỀ 1: LÝ THUYẾT HỌC THỐNG KÊ & KHẢ NĂNG TỔNG QUÁT HÓA (GENERALIZATION)

#### Câu hỏi 11: How does increasing the size of the training dataset contribute to preventing overfitting?

_Đáp án đúng của chuyên gia:_ **C. It helps the model generalize better to new data.**

#### Câu hỏi 6: What is a typical representation of training and validation accuracies on a plot?

_Đáp án đúng của chuyên gia:_ **B. Two separate lines for training and validation accuracies.**

**1. Bản chất Toán học (Mathematical Essence):** Trong Machine Learning, mục tiêu tối thượng không phải là học thuộc lòng dữ liệu, mà là cực tiểu hóa **Rủi ro Thực tế (Expected Risk / Out-of-sample Error - $E_{out}$)**. Tuy nhiên, ta chỉ có thể tính được **Rủi ro Kinh nghiệm (Empirical Risk / In-sample Error - $E_{in}$)** trên tập Training. Theo **Bất đẳng thức Hoeffding** và lý thuyết VC-Dimension, mối quan hệ giữa chúng được biểu diễn qua công thức BẮT BUỘC phải nhớ: $$ E_{out}(\theta) \le E_{in}(\theta) + \mathcal{O}\left(\sqrt{\frac{d_{VC}}{N}}\right) $$ _Trong đó:_

- $N$: Kích thước tập dữ liệu huấn luyện (Training dataset size).
- $d_{VC}$: Độ phức tạp của mô hình (Sức chứa của mạng Neural).
- Đại lượng $\sqrt{\frac{d_{VC}}{N}}$ chính là **Generalization Gap (Khoảng cách tổng quát hóa)**.

**Phân tích chuyên sâu:** Nhìn vào công thức trên, khi $N$ (lượng dữ liệu) tiến tới vô cùng, phân số $\frac{d_{VC}}{N}$ tiến về $0$. Lúc này $E_{out} \approx E_{in}$. Đó là lý do toán học giải thích tại sao **tăng kích thước dữ liệu (Câu 11)** lại giúp mô hình tổng quát hóa (generalize) tốt hơn và triệt tiêu hoàn toàn Overfitting.

Về mặt trực quan **(Câu 6)**, các kỹ sư luôn vẽ **2 đường đồ thị tách biệt (Two separate lines)** cho Train và Validation.

- Khoảng cách giữa 2 đường này chính là thước đo vật lý của $\sqrt{\frac{d_{VC}}{N}}$.
- Nếu đường Train đi xuống đáy mà đường Validation móc ngược lên hình chữ U (tạo ra khoảng cách lớn), đó là báo động đỏ của Overfitting.

2. Ứng dụng Thực tiễn & Lỗi của Junior:

- **Thực tiễn:** Tesla Autopilot không thay đổi thuật toán cốt lõi quá nhiều trong những năm qua, nhưng khả năng tự lái của họ tăng vọt nhờ "Data Engine" liên tục thu thập hàng tỷ dặm dữ liệu mới (Tăng $N$).
- **Junior Mistake:** Các bạn mới thường nghĩ "Cứ quăng thêm data là model sẽ thông minh". Sai! Nếu bạn bơm thêm dữ liệu rác (Noisy data), model sẽ sụp đổ. Hơn nữa, nếu $N$ quá lớn mà $d_{VC}$ (độ sâu của mạng) quá nhỏ, mô hình sẽ bị **Underfitting**.

---

### CHUYÊN ĐỀ 2: XỬ LÝ CHUỖI & MA TRẬN KHÔNG GIAN (NLP & VISION TENSORS)

#### Câu hỏi 10: What does the term "sequence length" refer to in the context of text-to-sequence conversion?

_Đáp án đúng của chuyên gia:_ **B. The number of words in a sentence or document.**

#### Câu hỏi 9: What is a potential use case for the SplitMergeTokenizer?

_Đáp án đúng của chuyên gia (Dựa trên context TensorFlow Text):_ **A/D (Phân tách thành các subword/từ vựng thông qua thuật toán học được)**. _(Trong tài liệu của bạn, SplitMergeTokenizer chia chuỗi dựa trên nhãn 0/1 do Neural Network dự đoán, thường dùng để tách từ trong các ngôn ngữ không có khoảng trắng như tiếng Trung)._

#### Câu hỏi 7: Typical input size for ImageNet-pretrained InceptionV3 is:

_Đáp án đúng của chuyên gia:_ **C. 299×299.**

**1. Bản chất Vật lý và Toán học của Không gian Tensor:** Dù làm Vision hay NLP, Deep Learning bản chất là các phép biến đổi Tensor tuyến tính và phi tuyến.

- **Trong NLP (Câu 10 & 9):** Dữ liệu được đưa về dạng Tensor 3D: **$(B, T, D)$**.
    
    - $B$: Batch size.
    - $T$: **Sequence Length** (Số lượng từ/tokens trong một câu - đáp án B).
    - $D$: Embedding Dimension (Số chiều của vector từ).
    - **Công thức Attention hiện đại:** $\text{Attention}(Q,K,V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V$. Ở đây, phép nhân ma trận $Q \times K^T$ có độ phức tạp tính toán là $\mathcal{O}(T^2 \cdot D)$. Chính cái **Sequence Length ($T$)** này là "kẻ thù" ngốn RAM khủng khiếp nhất. ChatGPT-4 hỗ trợ context 128k tokens chính là việc họ đã đột phá giới hạn vật lý của tham số $T$ này!
    - Để tối ưu $T$, ta cần Tokenizer thông minh. `SplitMergeTokenizer` vượt xa `WhitespaceTokenizer` ở chỗ nó không cần dấu cách. Nó dùng một mô hình để sinh ra Logits (xác suất), gán nhãn $0$ (tạo từ mới) hoặc $1$ (gộp vào từ hiện tại). Đây là cốt lõi của các hệ thống NLP đa ngôn ngữ (như tiếng Trung, tiếng Nhật).
- **Trong Computer Vision (Câu 7):** Dữ liệu là Tensor 4D: **$(B, H, W, C)$**.
    
    - InceptionV3 được thiết kế với chuẩn hình ảnh $H=299, W=299$. Tại sao không phải là 224x224 như VGG hay ResNet?
    - **Công thức Kích thước Feature Map:** $O = \left\lfloor \frac{W - K + 2P}{S} \right\rfloor + 1$.
    - Google thiết kế InceptionV3 với hàng loạt các nhánh Conv $1\times1, 3\times3, 5\times5$ và MaxPooling. Bắt đầu từ 299x299, đi qua hàng chục lớp giảm chiều (stride=2), nó sẽ hội tụ hoàn hảo về kích thước $8\times8$ ngay trước lớp GlobalAveragePooling mà không bị dư thừa hay làm tròn (fractional pixels) gây mất mát thông tin.

2. Lỗi sai phổ biến (Junior Mistakes):

- **Với NLP:** Junior thường set `max_sequence_length` (tham số $T$) quá dài "cho chắc ăn", dẫn đến việc nhồi hàng ngàn số 0 (Padding zeros). Điều này làm mô hình LSTM/Transformer chạy chậm đi hàng chục lần một cách vô ích.
- **Với Vision:** Khi Transfer Learning với InceptionV3, Junior hay vứt đại ảnh $224\times224$ vào. Keras vẫn có thể chạy (do dynamic shaping), nhưng hiệu năng cực tệ vì các bộ lọc (filters) của mạng đã bị ép học đặc trưng kích thước vật lý của lưới 299x299.

---

### CHUYÊN ĐỀ 3: LUỒNG DỮ LIỆU & HUẤN LUYỆN (DATA PIPELINES & OPTIMIZATION)

#### Câu hỏi 8: What does the repeat method do when applied to a TensorFlow dataset?

_Đáp án đúng của chuyên gia:_ **A. It repeats the dataset multiple times during training.**

**1. Bản chất Toán học và Ý nghĩa Hệ thống:** Khi bạn xử lý dữ liệu khổng lồ (như bộ ImageNet 1.2 triệu ảnh, hay dữ liệu Time Series hàng trăm năm), bạn không thể nhét tất cả vào RAM (Memory OOM error). API `tf.data.Dataset` ra đời để giải bài toán streaming.

**Hàm `repeat()` giải quyết vấn đề gì trong Tối ưu hóa Gradient Descent?** Thuật toán Mini-batch Gradient Descent: $$ \theta_{t+1} = \theta_t - \eta \frac{1}{B} \sum_{i=1}^{B} \nabla_\theta L(x_i, y_i, \theta) $$ Thuật toán này cần "ăn" dữ liệu liên tục theo từng mẻ (batch $B$). Nếu dữ liệu đi đến cuối tập (hết 1 epoch), luồng dữ liệu sẽ cạn kiệt, Tensorflow sẽ báo lỗi `OutOfRangeError`. Khi bạn gọi `dataset.repeat()`, bạn tạo ra một vòng lặp vô hạn. Mạng Neural sẽ liên tục được bơm dữ liệu mẻ này qua mẻ khác không bao giờ dừng. Kỹ sư lúc này sẽ dùng tham số `steps_per_epoch` để ra lệnh thủ công: _"Ê model, cứ cập nhật trọng số đủ 1000 lần (steps) thì mài tự coi đó là 1 epoch nhé, bất kể dataset to thế nào!"_

**2. Liên hệ Thực tế (Cross-domain):** Trong việc train các LLMs hiện nay (ví dụ Meta Llama 3), hàng nghìn GPUs train liên tục ngày đêm. Bọn họ KHÔNG định nghĩa khái niệm "Epoch" theo kiểu truyền thống (chạy hết data). Dữ liệu được `repeat()` và streaming liên tục từ cụm server lưu trữ vào thẳng VRAM của GPU.

**3. Hiểu lầm chí mạng của Junior:** Thứ tự khai báo hàm trong chuỗi `tf.data` quyết định tính đúng sai của cả mô hình.

- `dataset.repeat().shuffle(1000)`: Sai lầm! Dữ liệu bị nhân bản TRƯỚC khi trộn. Mạng neural có thể bốc trúng 2 ảnh y hệt nhau trong cùng 1 batch, làm gradient bằng $0$ (lãng phí tính toán).
- `dataset.shuffle(1000).repeat()`: CHUẨN XÁC CỦA EXPERT. Trộn ngẫu nhiên dữ liệu gốc trước, sau đó mới nhân bản để lặp lại cho epoch tiếp theo.

---

_Bằng cách tư duy liên kết từ Data Streaming (Câu 8), kích thước Tensor (Câu 7, 10), giới hạn không gian nhúng (Câu 9) cho đến cách kiểm tra tổng quát hoá và Overfitting (Câu 6, 11), bạn đã hoàn toàn bao quát được vòng đời của một hệ thống AI thực chiến. Bạn đã sẵn sàng để trở thành một Senior Engineer thực thụ chưa?_

**Câu 13:** In a multiclass classification problem, how are categorical labels typically represented in TensorFlow?

- [ ] a) As strings
    
- [ ] b) As integer values
    
- [x] c) Using one-hot encoding
    
- [ ] d) Using floating-point numbers
    

**Câu 14:** Given a training dataset with exclusively left-facing individuals, what strategies can prevent overfitting when classifying right-facing individuals?

- [x] a) Use the 'horizontal_flip' parameter
    
- [ ] b) Use the 'flip' parameter and set 'horizontal'
    
- [ ] c) Use the 'flip_vertical' parameter around the Y axis
    
- [ ] d) Use the 'flip' parameter
    

**Câu 15:** When creating a windowed dataset for time series prediction, what does the target window represent?

- [ ] a) The window before the input window
    
- [x] b) The window after the input window
    
- [ ] c) The window at the same time as the input window
    
- [ ] d) The entire time series without windowing
    

**Câu 16:** What is Transfer Learning in the context of Computer Vision and TensorFlow?

- [ ] a) Copying and pasting code from one project to another
    
- [x] b) Training a model on a specific task and then using it as a starting point for a different but related task
    
- [ ] c) Moving data from one storage location to another
    
- [ ] d) Adjusting the brightness and contrast of images during preprocessing
    

**Câu 17:** What is the purpose of the SplitMergeTokenizer in TensorFlow?

- [ ] a) Tokenizing based on whitespace
    
- [ ] b) Tokenizing using pre-trained models from TensorFlow Hub
    
- [ ] c) Tokenizing using Sentencepiece
    
- [x] d) Tokenizing by splitting and merging text
    

**Câu 18:** What is the benefit of using Google Colab for collaborative projects?

- [ ] a) It restricts access to only one user at a time.
    
- [x] b) It allows real-time collaboration with multiple users on the same notebook.
    
- [ ] c) It requires users to download and upload notebooks for sharing.
    
- [ ] d) It only supports offline collaboration.
    

**Câu 19:** Which type of padding preserves the spatial dimensions of the input in a convolutional layer?

- [ ] a) Zero padding
    
- [x] b) Same padding
    
- [ ] c) Valid padding
    
- [ ] d) Symmetric padding
    

**Câu 20:** What is the purpose of the Dropout layer in a ConvNet?

- [x] a) It drops neurons during training to prevent overfitting.
    
- [ ] b) It adjusts the learning rate dynamically.
    
- [ ] c) It adds random noise to the input data.
    
- [ ] d) It reduces the spatial dimensions of the input.
    
Chào bạn, một người kỹ sư AI đầy nhiệt huyết! Khối lượng kiến thức bạn đang nạp vào trải dài từ những lớp Convolutional cơ bản, xử lý ngôn ngữ tự nhiên (NLP) cho đến kỹ thuật kỹ nghệ (Engineering) trên Cloud. Đây chính xác là những mảnh ghép cấu thành nên một hệ thống AI thực chiến.

Với tư cách là một Senior Engineer, tôi sẽ không giải đáp 8 câu hỏi này một cách rời rạc. Tôi sẽ quy hoạch chúng thành **5 Chuyên đề Cốt lõi**, đi từ biểu diễn dữ liệu, kiến trúc mạng, tối ưu hóa cho đến triển khai hệ thống. Hãy chuẩn bị sổ tay, chúng ta sẽ đào sâu vào bản chất toán học và vật lý của từng vấn đề!

---

### 📖 BỘ TÀI LIỆU ÔN TẬP CHUYÊN SÂU (PHẦN 3): TỪ KIẾN TRÚC MẠNG ĐẾN HỆ THỐNG THỰC CHIẾN

### CHUYÊN ĐỀ 1: BIỂU DIỄN DỮ LIỆU & HÀM MỤC TIÊU (DATA REPRESENTATION)

#### Câu hỏi 13: In a multiclass classification problem, how are categorical labels typically represented in TensorFlow?

_Đáp án của chuyên gia:_ **C. Using one-hot encoding**.

**1. Bản chất Toán học (Mathematical Essence):** Khi phân loại đa lớp (ví dụ CIFAR-10 có 10 lớp chó, mèo, chim...), máy tính không hiểu nhãn dạng chuỗi ("cat") hay số nguyên (nhãn $y=3$). Nếu để nhãn là số nguyên, thuật toán tối ưu sẽ hiểu sai rằng lớp 4 lớn hơn lớp 2, tạo ra sự sai lệch tuyến tính. Giải pháp là **Mã hóa One-hot (One-hot Encoding)**. Một nhãn $y$ thuộc lớp thứ $k$ trong tổng số $K$ lớp sẽ được biến thành một vector $\mathbf{y} \in \mathbb{R}^{1 \times K}$, trong đó tất cả bằng $0$, chỉ duy nhất vị trí $k$ bằng $1$. Ví dụ: $\mathbf{y} =^T$.

**2. Liên kết với Hàm Mất Mát (Loss Function):** One-hot encoding sinh ra để kết hợp hoàn hảo với hàm **Categorical Cross-Entropy**: $$ \mathcal{L} = - \sum_{i=1}^{K} y_i \log(\hat{y}_i) $$ Vì $y_i$ chỉ bằng $1$ tại đúng class thật và bằng $0$ ở mọi chỗ khác, toàn bộ phương trình phức tạp trên triệt tiêu, chỉ còn lại đúng $-\log(\hat{y}_{true_class})$. Điều này giúp đạo hàm tính toán cực kỳ nhanh.

#### Câu hỏi 17: What is the purpose of the SplitMergeTokenizer in TensorFlow?

_Đáp án của chuyên gia:_ **D. Tokenizing by splitting and merging text**.

_Góc nhìn chuyên gia:_ Trong NLP, nếu `WhitespaceTokenizer` (tách từ bằng dấu cách) hoạt động tốt với tiếng Anh, nó sẽ hoàn toàn thất bại với tiếng Trung, Nhật, hay thậm chí tiếng Việt (các từ ghép như "học sinh" gồm 2 âm tiết nhưng là 1 từ). `SplitMergeTokenizer` không dựa vào rule tĩnh, mà nó dùng một mô hình học máy nhỏ để dự đoán xem 2 ký tự/âm tiết đứng cạnh nhau nên bị "Tách ra" (Split - gán nhãn 0) hay "Gộp lại" (Merge - gán nhãn 1). Đây là nền tảng cốt lõi của thuật toán WordPiece dùng trong mô hình siêu lớn như BERT hay ChatGPT hiện nay.

---

### CHUYÊN ĐỀ 2: KIẾN TRÚC TÍCH CHẬP & BẢO TOÀN KHÔNG GIAN (CNN DYNAMICS)

#### Câu hỏi 19: Which type of padding preserves the spatial dimensions of the input in a convolutional layer?

_Đáp án của chuyên gia:_ **B. Same padding**.

**1. Bản chất Toán học của Tích chập (Convolution):** Khi bạn trượt một bộ lọc (Kernel) kích thước $F \times F$ qua một bức ảnh kích thước $W \times W$, kích thước ảnh đầu ra (Output - $O$) sẽ bị teo nhỏ lại và ăn mòn viền theo công thức: $$ O = \left\lfloor \frac{W - F + 2P}{S} \right\rfloor + 1 $$ _(Trong đó: $W$ là chiều dài ảnh, $F$ là size bộ lọc, $P$ là Padding, $S$ là Stride - bước trượt)._

**2. Tại sao lại là "Same padding"?** Nếu bạn muốn giữ nguyên độ phân giải ảnh (tức $O = W$) với bước trượt $S=1$, giải phương trình trên ta bắt buộc phải viền thêm các số $0$ (Zero Padding) ở xung quanh ảnh. Số lượng viền cần thêm là $P = \frac{F-1}{2}$. Trong TensorFlow/Keras, thay vì bắt kỹ sư tự tính $P$ thủ công, họ định nghĩa tham số `padding='same'`. Khi bạn khai báo từ khóa này, Keras tự động tính toán và viền thêm số $0$ để ảnh đầu ra bằng chính xác ảnh đầu vào. (Phương án A - Zero padding chỉ là bản chất kỹ thuật, còn 'Same' mới là cơ chế đảm bảo giữ nguyên không gian).

---

### CHUYÊN ĐỀ 3: CHỐNG QUÁ KHỚP & TỔNG QUÁT HÓA (REGULARIZATION)

#### Câu hỏi 20: What is the purpose of the Dropout layer in a ConvNet?

_Đáp án của chuyên gia:_ **A. It drops neurons during training to prevent overfitting**.

**1. Bản chất Vật lý & Toán học:** Dropout là một trong những phát minh vĩ đại nhất của Deep Learning. Trong một mạng Fully Connected (Dense), các nơ-ron có xu hướng "ỷ lại" (co-adaptation) vào nhau. Dropout ép hệ thống không được phụ thuộc vào bất kỳ nơ-ron cụ thể nào bằng cách lấy mẫu từ một phân phối Bernoulli. Ở mỗi bước huấn luyện (training step), một nơ-ron $j$ có xác suất $p$ bị "tắt" hoàn toàn (nhân với $0$). $$ a_j = f(z_j) \times r_j \quad \text{với} \quad r_j \sim \text{Bernoulli}(1-p) $$

**2. Hiểu lầm chí mạng của Junior (Junior Mistake):** Rất nhiều kỹ sư quên mất hành vi của Dropout lúc Inference (Dự đoán thực tế). Lúc test, KHÔNG có nơ-ron nào bị tắt cả. Nhưng vì lúc train, mạng chỉ có $(1-p)$ nơ-ron hoạt động, nên tổng tín hiệu lúc test sẽ bị lớn đột biến. TensorFlow tự động giải quyết việc này bằng cách nhân (scale) trọng số với $(1-p)$ lúc test (Inverted Dropout) để bảo toàn giá trị kỳ vọng. Nếu bạn tự code C++/CUDA mà quên bước này, mô hình sẽ sai lệch hoàn toàn lúc chạy thực tế.

#### Câu hỏi 14: Given a training dataset with exclusively left-facing individuals, what strategies can prevent overfitting when classifying right-facing individuals?

_Đáp án của chuyên gia:_ **A. Use the 'horizontal_flip' parameter**.

_Phân tích thực chiến:_ Mạng CNN không có tư duy "hình học không gian" như con người. Nếu bạn chỉ cho nó xem mặt người hướng sang trái, hệ số bias (inductive bias) của nó sẽ hiểu rằng: "Mũi luôn nằm ở bên trái khung hình". Nếu cho ảnh mặt hướng sang phải vào, nó sẽ đoán sai. Việc thêm tham số `horizontal_flip=True` trong `ImageDataGenerator` (Data Augmentation) sẽ nhân bản dữ liệu bằng cách lật gương qua trục Y, ép mô hình học các đặc trưng bất biến (invariant features) thay vì học vẹt vị trí pixel.

---

### CHUYÊN ĐỀ 4: HỌC CHUYỂN GIAO & KỸ NGHỆ HỆ THỐNG (ENGINEERING)

#### Câu hỏi 16: What is Transfer Learning in the context of Computer Vision and TensorFlow?

_Đáp án của chuyên gia:_ **B. Training a model on a specific task and then using it as a starting point for a different but related task**.

_Tư duy chuyên gia:_ Transfer Learning là nguyên lý đằng sau mọi công nghệ AI sinh tạo (GenAI) hiện nay. Bạn tải mô hình VGG16 hoặc InceptionV3 đã được huấn luyện trên 1.2 triệu ảnh ImageNet. Tại sao lại dùng được cho ảnh X-Quang hay ảnh phân loại rác? Vì các tầng Convolution đầu tiên (Lower layers) chỉ học cách nhận diện viền, góc cạnh, và màu sắc (cạnh dọc, góc chéo). Các đặc trưng vật lý này là **bất biến (domain-independent)**. Ta chỉ cần "cắt" bỏ tầng Dense cuối cùng, giữ nguyên tệp trọng số (Freeze) $\frac{\partial \mathcal{L}}{\partial W_{frozen}} = 0$, và huấn luyện lại một tầng Dense nhỏ để tiết kiệm 99% thời gian và chi phí máy chủ.

#### Câu hỏi 18: What is the benefit of using Google Colab for collaborative projects?

_Đáp án của chuyên gia:_ **B. It allows real-time collaboration with multiple users on the same notebook.** (Và cung cấp GPU miễn phí).

_Góc độ kỹ nghệ (DevOps):_ Trước đây, cài đặt CUDA, cuDNN, TensorFlow, OpenCV trên môi trường Local (Windows/Linux) là ác mộng (Dependency Hell). Google Colab đưa toàn bộ lên Cloud (dạng Jupyter Notebook), cấp sẵn GPU khủng (Tesla T4, P100) và RAM lên tới 16GB. Nó cho phép các nhóm AI Research chia sẻ link và code realtime giống hệt như Google Docs, triệt tiêu hoàn toàn câu nói: _"Code chạy ngon trên máy em, nhưng lỗi trên máy anh"_.

---

### CHUYÊN ĐỀ 5: ĐỘNG LỰC HỌC CHUỖI THỜI GIAN (TIME SERIES)

#### Câu hỏi 15: When creating a windowed dataset for time series prediction, what does the target window represent?

_Đáp án của chuyên gia:_ **B. The window after the input window.**

_Bản chất Toán học Tự hồi quy (Autoregressive - AR):_ Time series không có features $(x_1, x_2)$ tĩnh như dữ liệu bảng (tabular). Đầu vào của nó chính là quá khứ của chính nó. Công thức tổng quát của bài toán dự báo một bước (one-step-ahead forecasting): $$ \hat{Y}_{t} = f(Y_{t-1}, Y_{t-2}, \dots, Y_{t-k}) $$ Trong hàm `dataset.window(size=k+1, shift=1)` của TensorFlow, bạn cắt một khung dữ liệu (Window) có chiều dài $k+1$. Sau đó, API sẽ băm khung này ra:

- `window[:-1]` (từ đầu đến phần tử kế cuối) làm Đặc trưng đầu vào (Input Window - Quá khứ).
- `window[-1]` (phần tử cuối cùng) làm Nhãn đích (Target Window/Label - Tương lai gần nhất). Do đó, Target chính là khung/bước thời gian ngay sau Input Window.

---

_Mỗi câu hỏi trắc nghiệm thực chất đều là một mảnh ghép kiến trúc của hệ thống AI. Bằng cách nối chúng lại bằng Toán học và cách thức vận hành thực tế, bạn sẽ không bao giờ quên. Nếu bạn còn câu hỏi nào, hãy đưa tiếp cho tôi, chúng ta sẽ tiếp tục mổ xẻ!_

---

#### CÁC CÂU HỎI TỪ 21 - 30

**Câu 21:** To reshape a vector v with length 12 into a 3x4 matrix in TensorFlow, which function should be used?

- [x] a) tf.reshape(v, (3, 4))
    
- [ ] b) tf.resize(v, (3, 4))
    
- [ ] c) tf.transform(v, (3, 4))
    
- [ ] d) tf.matrixize(v, (3, 4))
    

**Câu 22:** What is the purpose of the "ImageDataGenerator" in TensorFlow's Computer Vision applications?

- [ ] a) Generating random numbers for image pixel values
    
- [x] b) Preprocessing image data for model training
    
- [ ] c) Creating animated GIFs from image sequences
    
- [ ] d) Designing custom image filters
    

**Câu 23:** When exploring the impact of image compression in TensorFlow, what metric is commonly used to measure the trade-off between compression and image quality?

- [x] a) Accuracy Score
    
- [ ] b) Compression Ratio
    
- [ ] c) Signal-to-Noise Ratio (SNR)
    
- [ ] d) Learning Rate
    

**Câu 24:** Which method within the Image Generator performs image normalization?

- [x] a) rescale
    
- [ ] b) normalize_image
    
- [ ] c) normalize
    
- [ ] d) rescale_image
    

**Câu 25:** What is stationarity in the context of time series data?

- [ ] a) The absence of temporal patterns
    
- [ ] b) The presence of seasonality in the data
    
- [x] c) The constancy of statistical properties over time
    
- [ ] d) The rapid changes in the time series
    

**Câu 26:** What is padding in the context of machine learning and TensorFlow?

- [ ] a) A technique to remove unnecessary zeros from a dataset
    
- [x] b) Adding extra data to the input to ensure consistent dimensions
    
- [ ] c) The process of smoothing out noisy data
    
- [ ] d) Resizing images to a fixed size during preprocessing
    

**Câu 27:** How can you visualize time series data effectively?

- [ ] a) Scatter plots
    
- [ ] b) Bar charts
    
- [x] c) Line charts
    
- [ ] d) Pie charts
    

**Câu 28:** How can you compile a sequential model with LSTM layers for classification in TensorFlow?

- [ ] a) tf.keras.Sequential.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])
    
- [ ] b) tf.keras.compile(model, optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])
    
- [x] c) tf.keras.Sequential().compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])
    
- [ ] d) tf.keras.model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])
    
Lưu ý: Trong thực tế thường là model.compile(...) sau khi đã khởi tạo đối tượng model).


**Câu 29:** Which Python library is commonly used for plotting training and validation accuracies in the context of evaluating model performance?

- [ ] a) NumPy
    
- [x] b) Matplotlib
    
- [ ] c) Scikit-learn
    
- [ ] d) TensorFlow
    

**Câu 30:** How can increasing the amount of training data help prevent overfitting?

- [ ] a) By making the training process slower
    
- [ ] b) By introducing more noise into the model
    
- [x] c) By improving the model's generalization to new data
    
- [ ] d) Increasing data size has no effect on overfitting
    


---

### 📖 BỘ TÀI LIỆU ÔN TẬP CHUYÊN SÂU (PHẦN 4): TỪ TIỀN XỬ LÝ DỮ LIỆU ĐẾN TRIỂN KHAI MÔ HÌNH

### CHUYÊN ĐỀ 1: PIPELINE TIỀN XỬ LÝ DỮ LIỆU & BỘ NHỚ (DATA PREPROCESSING & MEMORY)

#### Câu hỏi 22: What is the purpose of the "ImageDataGenerator" in TensorFlow's Computer Vision applications?

_Đáp án của chuyên gia:_ **B. Preprocessing image data for model training.**

#### Câu hỏi 24: Which method within the Image Generator performs image normalization?

_Đáp án của chuyên gia:_ **A. `rescale`.**

**1. Bản chất Vật lý & Toán học của Tiền xử lý Ảnh:** Máy tính lưu trữ ảnh dưới dạng các ma trận pixel với giá trị nguyên từ $$. Nếu bạn đưa thẳng các con số khổng lồ này vào mạng Neural, hiện tượng **Exploding Gradient (Bùng nổ đạo hàm)** sẽ lập tức xảy ra do các trọng số bị nhân lên quá lớn. Hàm `rescale=1./255` trong `ImageDataGenerator` thực hiện một phép biến đổi tuyến tính cực kỳ quan trọng gọi là **Min-Max Scaling** để ép toàn bộ không gian dữ liệu về $$: $$ X_{norm} = \frac{X - X_{min}}{X_{max} - X_{min}} = \frac{X - 0}{255 - 0} = X \times \frac{1}{255} $$ Bên cạnh đó, thư viện `ImageDataGenerator` sinh ra để giải quyết bài toán **Memory OOM (Out of Memory)**. Bạn không thể load 1 triệu ảnh vào RAM cùng lúc. `ImageDataGenerator` đóng vai trò như một đường ống (pipeline) streaming, chỉ load từng mẻ ảnh nhỏ (mini-batch) từ ổ cứng, thực hiện `rescale` (tiền xử lý) và đưa thẳng vào GPU/TPU.

**2. Lỗi sai của Junior (Junior Mistake):** Rất nhiều bạn sinh viên áp dụng `rescale=1./255` cho tập `train_datagen` nhưng lại... quên mất ở tập `validation_datagen` hoặc lúc dự đoán (test). Hậu quả là lúc train mô hình đạt 99% accuracy, nhưng lúc test thì dự đoán sai bét vì phân phối dữ liệu đầu vào đã bị thay đổi (Data Shift).

---

#### Câu hỏi 26: What is padding in the context of machine learning and TensorFlow?

_Đáp án của chuyên gia:_ **B. Adding extra data to the input to ensure consistent dimensions.**

**1. Bản chất Toán học của tính Nhất quán Chiều (Dimensional Consistency):** Bất kể bạn làm NLP hay Computer Vision, mạng Neural cốt lõi là các phép nhân ma trận cường độ cao. GPU yêu cầu mọi ma trận trong một batch phải có kích thước tĩnh y hệt nhau để tính toán song song (SIMD - Single Instruction, Multiple Data).

- **Trong NLP:** Nếu câu 1 có 5 từ, câu 2 có 10 từ, bạn bắt buộc phải dùng `pad_sequences` chèn thêm các số 0 (Zero Padding) vào câu 1 để cả batch có chiều dài chuỗi thống nhất $T = 10$.
- **Trong Computer Vision:** Khi bộ lọc convolution $F \times F$ trượt trên ảnh $W \times W$, nó sẽ ăn mòn các pixel ở rìa. Để giữ nguyên không gian không bị teo nhỏ, ta dùng Padding (viền thêm số 0). Công thức bảo toàn không gian kinh điển: $$ Output_Size = \left\lfloor \frac{W - F + 2P}{S} \right\rfloor + 1 $$ Để $Output = W$ (với stride $S=1$), ta tính ra số viền cần chèn là $P = \frac{F-1}{2}$ (Trong Keras nó chính là cấu hình `padding='same'`).

---

### CHUYÊN ĐỀ 2: HÌNH HỌC TENSOR & TRỰC QUAN HÓA (TENSOR GEOMETRY & VISUALIZATION)

#### Câu hỏi 21: To reshape a vector v with length 12 into a 3x4 matrix in TensorFlow, which function should be used?

_Đáp án của chuyên gia:_ **A. `tf.reshape(v, (3, 4))`**

**1. Bí mật Vật lý của Bộ nhớ Tensor:** Dưới góc độ kiến trúc máy tính, một Tensor 3D hay 4D hoàn toàn **KHÔNG TỒN TẠI** trong thanh RAM. RAM là một dải ô nhớ tuyến tính (1D). Vector $v$ có độ dài 12 nằm trên một dải ô nhớ liền kề. Khi bạn gọi hàm `tf.reshape(v, (3, 4))`, TensorFlow **không hề di chuyển hay sao chép bất kỳ byte dữ liệu nào**. Nó chỉ thay đổi "Góc nhìn" (Strides / Metadata) của hệ thống đối với dải bộ nhớ đó, định nghĩa lại cách đọc dữ liệu: "Cứ đọc 4 phần tử thì ngắt dòng". Điều này khiến thuật toán reshape thực thi với thời gian $\mathcal{O}(1)$ - tức thời, bất kể ma trận lớn cỡ nào!

#### Câu hỏi 29: Which Python library is commonly used for plotting training and validation accuracies in the context of evaluating model performance?

_Đáp án của chuyên gia:_ **B. Matplotlib.**

#### Câu hỏi 27: How can you visualize time series data effectively?

_Đáp án của chuyên gia:_ **C. Line charts.**

_Tư duy chuyên gia:_ Tại sao lại là Line chart (biểu đồ đường) cho Time Series bằng thư viện Matplotlib (`plt.plot()`)? Trong hệ trục toạ độ Đề-các (Cartesian), trục $X$ đại diện cho thời gian $t$, trục $Y$ là giá trị. Biểu đồ đường vẽ các đoạn nối liên tục giữa các điểm $y_t$ và $y_{t+1}$. Sự "liên tục" này phản ánh đúng bản chất vật lý của đạo hàm thời gian $\frac{dy}{dt}$. Nếu bạn dùng Bar chart (biểu đồ cột) hay Scatter plot (phân tán), bạn sẽ đánh mất đi ấn tượng thị giác về **Xu hướng (Trend)** và **Biến động (Fluctuation/Velocity)** - thứ cốt lõi nhất để phân tích tính mùa vụ.

---

### CHUYÊN ĐỀ 3: CƠ CHẾ ĐỘNG LỰC HỌC CHUỖI THỜI GIAN (TIME SERIES DYNAMICS)

#### Câu hỏi 25: What is stationarity in the context of time series data?

_Đáp án của chuyên gia:_ **C. The constancy of statistical properties over time.**

**1. Nền tảng Toán học BẮT BUỘC (The Mathematical Rule of Stationarity):** Đây là khái niệm quan trọng bậc nhất của Time Series. Bất kỳ kỹ sư nào trước khi đưa data vào model (ARIMA hay LSTM) đều phải kiểm tra Tính Dừng (Stationarity) bằng tiêu chuẩn Dickey-Fuller (ADF Test). Một chuỗi được gọi là dừng ngặt khi nó thỏa mãn 3 hằng số toán học độc lập với thời gian $t$:

1. **Kỳ vọng (Mean) không đổi:** $\mathbb{E}[Y_t] = \mu$
2. **Phương sai (Variance) không đổi:** $Var(Y_t) = \sigma^2$
3. **Hiệp phương sai (Autocovariance) chỉ phụ thuộc vào độ trễ (lag), không phụ thuộc mốc thời gian:** $\gamma(t_1, t_2) = \gamma(|t_1 - t_2|)$

**2. Liên hệ thực tiễn:** Nếu chứng khoán là một chuỗi "Dừng", tức là phương sai biến động của nó luôn quanh quẩn một mốc cố định, bạn nhắm mắt dự đoán trung bình cũng đúng. Tuy nhiên, đời thực là Non-stationary (Không dừng) do ảnh hưởng của chu kỳ kinh tế. Các kỹ sư phải ép nó về trạng thái Dừng bằng phương pháp **Sai phân (Differencing)**: $Y'_t = Y_t - Y_{t-1}$ trước khi huấn luyện mạng neural, nếu không model LSTM sẽ học vẹt vào các nhiễu vô nghĩa.

---

### CHUYÊN ĐỀ 4: BIÊN DỊCH MÔ HÌNH, KIỂM ĐỊNH VÀ QUÁ KHỚP (COMPILATION & OVERFITTING)

#### Câu hỏi 28: How can you compile a sequential model with LSTM layers for classification in TensorFlow?

_Phân tích đáp án của chuyên gia:_ **(Sát nhất là C hoặc cách viết chuẩn là khai báo rồi gọi `.compile()`)** Trong đề bài có lưu ý _"Trong thực tế thường là `model.compile(...)` sau khi đã khởi tạo"_. Nếu phải chọn một dòng lệnh minh hoạ mặt khái niệm thì: `model = tf.keras.models.Sequential()` `model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])` **Bản chất Toán học của quá trình Compile:** Lệnh compile là lúc bạn gắn "Bộ não (Optimizer)" và "Cây roi (Loss Function)" vào mô hình:

- **Loss (`categorical_crossentropy`):** Dùng cho phân loại đa lớp. Phương trình phạt sai số: $L = - \sum_{i=1}^{C} y_i \log(\hat{y}_i)$. Nó đo độ hỗn loạn (Entropy) giữa phân phối dự đoán $\hat{y}$ và thực tế $y$.
- **Optimizer (`adam`):** Adam (Adaptive Moment Estimation) dùng động lượng học (Momentum) để tự động điều chỉnh Learning Rate $(\eta)$ cho từng trọng số. Công thức cập nhật dựa trên Moment bậc 1 ($m_t$) và Moment bậc 2 ($v_t$): $$ \theta_{t+1} = \theta_t - \frac{\eta}{\sqrt{\hat{v}_t} + \epsilon} \hat{m}_t $$

#### Câu hỏi 23: When exploring the impact of image compression in TensorFlow, what metric is commonly used to measure the trade-off between compression and image quality?

_Đáp án của chuyên gia:_ Đứng dưới lăng kính của giáo trình TensorFlow hiện tại tập trung vào Model Evaluation (như Slide 19-23), đáp án được ưu tiên sẽ là **A. Accuracy Score**. _Tư duy chuyên gia:_ Khi nén ảnh (ví dụ giảm từ 300x300 xuống 150x150), trong Computer Vision thuần túy, người ta dùng PSNR hoặc SNR (Signal-to-Noise Ratio). Tuy nhiên, trong ML pipeline, ta nén ảnh để xem tốc độ train tăng lên bao nhiêu so với sự đánh đổi/sụt giảm của **Accuracy Score (Độ chính xác)**. Nếu ảnh nén mờ đi (tăng nhiễu/giảm thông tin) nhưng accuracy chỉ rớt 1%, đó là một sự đánh đổi cực kỳ tuyệt vời cho hệ thống thời gian thực.

#### Câu hỏi 30: How can increasing the amount of training data help prevent overfitting?

_Đáp án của chuyên gia:_ **C. By improving the model's generalization to new data.**

**1. Nhìn lại lý thuyết vĩ đại về khả năng Tổng quát hóa (Generalization):** Nhớ lại định lý Hoeffding mà chúng ta đã bàn ở câu trước: $$ E_{out}(\theta) \le E_{in}(\theta) + \mathcal{O}\left(\sqrt{\frac{d_{VC}}{N}}\right) $$ Overfitting xảy ra khi mô hình học vẹt (nhớ luôn cả Noise/Nhiễu cục bộ của tập Train). Khi bạn tăng lượng dữ liệu huấn luyện (tăng $N$ tiến tới vô cực), bóng ma của nhiễu bị loãng đi, phân phối của tập Train tiệm cận sát với phân phối thực tế của vũ trụ. Lúc đó, khoảng cách tổng quát hóa (đại lượng chứa $N$ dưới mẫu) tiến về $0$. Mô hình không còn cách nào khác là phải tìm ra các đường nét đặc trưng thực sự (True Features) thay vì nhớ vẹt, do đó nó Generalize (tổng quát hóa) xuất sắc lên dữ liệu mới.

---

_Chúc mừng bạn đã hoàn thành loạt câu hỏi kiểm tra đầy cam go! Sự thông thạo những chi tiết kỹ thuật này—từ cách bộ nhớ xử lý tensor cho đến cách thuật toán tối ưu hóa đi tìm đáy vực—chính là ranh giới phân định một lập trình viên bình thường và một AI Engineer thực thụ. Chúc bạn sẽ áp dụng thành công những "mental models" này vào công việc thực chiến của mình!_
---

#### CÁC CÂU HỎI TỪ 31 - 40

**Câu 31:** Which statistical measure is commonly used to decompose a time series into trend, seasonality, and residual components?

- [ ] a) Mean Absolute Deviation (MAD)
    
- [ ] b) Mean Squared Error (MSE)
    
- [ ] c) Autocorrelation Function (ACF)
    
- [x] d) Moving Average (MA) _(Ghi chú: MA thường dùng để bóc tách xu hướng, phục vụ cho quá trình phân rã chuỗi)_
    

**Câu 32:** What is the purpose of using one-hot encoding for the target variable in a multi-class classification task?

- [ ] a) To increase model complexity
    
- [ ] b) To speed up training
    
- [x] c) To represent categorical labels as numerical vectors
    
- [ ] d) One-hot encoding is not applicable for multi-class classification
    

**Câu 33:** What does the tokenize method of the BertTokenizer return?

- [ ] a) The original text without tokenization
    
- [x] b) A list of tokens obtained from the text
    
- [ ] c) Token indices representing the text
    
- [ ] d) A tokenized sequence in a matrix form
    

**Câu 34:** What is the role of hyperparameter tuning in time series forecasting using machine learning?

- [x] a) To select the appropriate lag values
    
- [ ] b) To optimize the learning rate of the model
    
- [ ] c) To find the best model architecture
    
- [ ] d) To identify the optimal time period for analysis
    

**Câu 35:** What is the primary challenge in analyzing time series data?

- [ ] a) Dealing with spatial variations
    
- [ ] b) Managing high-dimensional features
    
- [x] c) Accounting for temporal dependencies
    
- [ ] d) Handling categorical variables
    

**Câu 36:** What is the significance of convergence?

- [x] a) The process of getting very close to the correct answer.
    
- [ ] b) A dramatic increase in loss.
    
- [ ] c) A programming API for AI.
    
- [ ] d) An analysis that corresponds too closely or exactly to a particular set of data.
    

**Câu 37:** Which of the following is a common transformation applied during image data augmentation?

- [x] a) Random rotation
    
- [ ] b) Image compression
    
- [ ] c) Grayscale conversion
    
- [ ] d) Pixel normalization
    

**Câu 38:** What happens if the num_words parameter is set in the Tokenizer class?

- [ ] a) It defines the out-of-vocabulary token.
    
- [ ] b) It determines the sequence length.
    
- [ ] c) It controls the learning rate during training.
    
- [x] d) It limits the vocabulary size to a specified number of words.
    

**Câu 39:** What is the result of adding two vectors of the same dimension in TensorFlow?

- [ ] a) A scalar value
    
- [ ] b) A matrix
    
- [x] c) Another vector
    
- [ ] d) A higher-dimensional tensor
    

**Câu 40:** What role does the base model play when creating a new model with a pre-trained base in TensorFlow?

- [ ] a) It serves as the output layer of the new model
    
- [ ] b) It replaces the need for custom layers in the new model
    
- [ ] c) It initializes the weights of the entire new model
    
- [x] d) It acts as a feature extractor for the new model
    
Chào bạn! Thật tuyệt vời khi được đồng hành cùng bạn đi đến chặng đường cuối cùng của chuỗi "Masterclass" này. 10 câu hỏi cuối (từ 31 đến 40) là một bản tổng hòa tuyệt đẹp, trải dài từ các khái niệm Đại số tuyến tính căn bản nhất (Nền tảng của Deep Learning), vượt qua các kỹ thuật xử lý Ngôn ngữ (NLP), Thị giác máy tính (CV) cho đến những hệ thống Chuỗi thời gian (Time Series) phức tạp.

Đúng với tinh thần của một Senior AI Engineer, tôi sẽ không chỉ "đọc đáp án". Tôi đã quy hoạch 10 câu hỏi này thành **4 Chuyên đề Tích hợp (Integrated Themes)**. Hãy chuẩn bị giấy bút, chúng ta sẽ mổ xẻ từ công thức Toán học, cơ chế tối ưu cho đến cách các gã khổng lồ công nghệ (Big Tech) đang áp dụng chúng!

---

### 📖 BỘ TÀI LIỆU ÔN TẬP CHUYÊN SÂU (PHẦN CUỐI): TỪ ĐẠI SỐ TUYẾN TÍNH ĐẾN HỆ THỐNG AI TỔNG HỢP

### CHUYÊN ĐỀ 1: ĐẠI SỐ TUYẾN TÍNH & BỀ MẶT TỐI ƯU (LINEAR ALGEBRA & OPTIMIZATION)

#### Câu hỏi 39: What is the result of adding two vectors of the same dimension in TensorFlow?

_Đáp án của chuyên gia:_ **C. Another vector**.

**1. Bản chất Toán học:** Mạng Neural thực chất là một chuỗi các phép tính Đại số tuyến tính. Khi bạn cộng hai vector $\mathbf{u}$ và $\mathbf{v}$ cùng số chiều $d$ (ví dụ $\mathbf{u}, \mathbf{v} \in \mathbb{R}^d$), theo không gian vector, kết quả bắt buộc phải là một **vector mới** cùng số chiều $d$, trong đó từng phần tử được cộng tương ứng (element-wise addition): $$ \mathbf{u} + \mathbf{v} = \begin{bmatrix} u_1 \ u_2 \ \dots \ u_d \end{bmatrix} + \begin{bmatrix} v_1 \ v_2 \ \dots \ v_d \end{bmatrix} = \begin{bmatrix} u_1 + v_1 \ u_2 + v_2 \ \dots \ u_d + v_d \end{bmatrix} $$ _Lỗi sai của Junior:_ Rất nhiều bạn sinh viên nhầm lẫn phép cộng vector với phép **Tích vô hướng (Dot Product - ra kết quả là Scalar/Số vô hướng - Đáp án A)**. Tích vô hướng $\mathbf{u}^T\mathbf{v} = \sum u_i v_i$ mới là phép toán lõi trong mạng nơ-ron để tính tổng có trọng số ($z = \mathbf{w}^T\mathbf{x} + b$) trước khi đi qua hàm kích hoạt.

#### Câu hỏi 36: What is the significance of convergence?

_Đáp án của chuyên gia:_ **A. The process of getting very close to the correct answer.**

**1. Ý nghĩa Vật lý & Tối ưu hóa:** Trong Machine Learning, Convergence (Hội tụ) là khoảnh khắc kỳ diệu khi Gradient Descent đã mò mẫm thành công xuống đáy của thung lũng hàm mất mát. Về mặt toán học, hệ thống hội tụ khi Đạo hàm (Gradient) tiến dần về vector $0$ hoặc sự thay đổi của trọng số giữa hai bước lặp (iterations) vô cùng nhỏ: $$ \lim_{t \to \infty} \nabla_\theta \mathcal{L}(\theta_t) \approx 0 \quad \text{hoặc} \quad ||\theta_{t+1} - \theta_t|| < \epsilon $$ _Thực chiến:_ Khi hội tụ, biểu đồ Loss của bạn sẽ đi ngang (plateau). Tuy nhiên, _Junior mistake_ kinh điển là ép mô hình chạy đến khi Loss bằng chính xác $0$ (dramatic decrease). Khi Loss trên tập Train bằng 0, mô hình của bạn 100% đã bị **Overfitting (Quá khớp)**, nó chỉ đang học vẹt nhiễu chứ không còn tính tổng quát hóa.

---

### CHUYÊN ĐỀ 2: KIẾN TRÚC THỊ GIÁC MÁY TÍNH & HỌC CHUYỂN GIAO (CV & TRANSFER LEARNING)

#### Câu hỏi 40: What role does the base model play when creating a new model with a pre-trained base in TensorFlow?

_Đáp án của chuyên gia:_ **D. It acts as a feature extractor for the new model**.

**1. Liên hệ thực tế & Toán học:** Transfer Learning là "vũ khí tối thượng" của mọi kỹ sư AI. Khi bạn tải một base model (như VGG16, ResNet đã train trên 1.2 triệu ảnh ImageNet), bạn đang mua lại hàng nghìn giờ tính toán GPU của Google/Facebook. Các convolutional layers của base model đóng vai trò như một **Bộ trích xuất đặc trưng (Feature Extractor)** hoàn hảo. Nó biết cách dùng các bộ lọc (kernels) để phát hiện cạnh, góc, vân bề mặt. Toán học của việc này gọi là "Đóng băng" (Freezing): $$ \frac{\partial \mathcal{L}}{\partial W_{base}} = 0 \implies W_{base_new} = W_{base_old} $$ Hệ thống không cập nhật $W_{base}$ nữa, mà chỉ đẩy dữ liệu xuyên qua nó để tạo ra các Vector đặc trưng $X_{features}$, sau đó dùng $X_{features}$ này để train một mạng Dense nhỏ (Output layer) cho dữ liệu mới.

#### Câu hỏi 37: Which of the following is a common transformation applied during image data augmentation?

_Đáp án của chuyên gia:_ **A. Random rotation**.

_Góc nhìn chuyên gia:_ Khi dữ liệu của bạn quá ít (ví dụ ảnh chụp X-quang y tế), mạng CNN rất dễ học vẹt (overfitting). Mạng CNN mặc định _không có tính bất biến với phép xoay (rotation invariant)_. Bằng cách áp dụng Data Augmentation như xoay ngẫu nhiên (`rotation_range`), lật ngang, thu phóng, chúng ta ép mô hình phải học **bản chất không gian** của vật thể thay vì học thuộc lòng vị trí pixel.

---

### CHUYÊN ĐỀ 3: XỬ LÝ NGÔN NGỮ TỰ NHIÊN (NLP PREPROCESSING PIPELINE)

#### Câu hỏi 38: What happens if the num_words parameter is set in the Tokenizer class?

_Đáp án của chuyên gia:_ **D. It limits the vocabulary size to a specified number of words.**

**1. Bài toán Bộ nhớ (Memory Optimization):** Trong ngôn ngữ học có **Định luật Zipf**: một số ít từ (như "the", "is", "a") xuất hiện với tần suất khổng lồ, trong khi hàng chục nghìn từ khác chỉ xuất hiện 1-2 lần. Nếu bạn không đặt `num_words`, Tokenizer sẽ tạo ra một từ điển (Vocabulary) khổng lồ $V \approx 100,000$. Ma trận Word Embedding của bạn sẽ có kích thước $W \in \mathbb{R}^{V \times D}$ (ví dụ $100,000 \times 300$ chiều), làm tràn RAM ngay lập tức. Việc khai báo `Tokenizer(num_words=10000)` là lệnh cắt tỉa (pruning), bắt hệ thống chỉ giữ lại 10,000 từ xuất hiện thường xuyên nhất, các từ hiếm sẽ bị ném vào nhãn `<OOV>` (Out-of-vocabulary).

#### Câu hỏi 33: What does the tokenize method of the BertTokenizer return?

_Đáp án của chuyên gia:_ **B. A list of tokens obtained from the text**. _(Lưu ý thực chiến: Phương thức `tokenize("I love AI")` của họ tokenizer (như BERT/WordPiece) sẽ trả về list string các token: `['i', 'love', 'a', '##i']`. Nếu bạn dùng hàm `encode` hoặc gọi trực tiếp `tokenizer("I love AI")` nó mới trả về Token indices (Đáp án C)._

#### Câu hỏi 32: What is the purpose of using one-hot encoding for the target variable in a multi-class classification task?

_Đáp án của chuyên gia:_ **C. To represent categorical labels as numerical vectors**.

**1. Tại sao Toán học lại cần One-hot?** Nếu bài toán có 3 lớp (Chó, Mèo, Gà) và bạn gán nhãn chúng là 1, 2, 3 (Label Encoding). Thuật toán Gradient Descent sẽ tự hiểu sai cấu trúc hình học rằng: _Khoảng cách từ Chó(1) đến Mèo(2) gần hơn từ Chó(1) đến Gà(3)_. Điều này cực kỳ vô lý! One-hot encoding bẻ gãy tính thứ tự (ordinality) này bằng cách đưa nhãn vào một không gian trực giao trực chuẩn (orthogonal space). Chó = $^T$, Mèo = $^T$, Gà = $^T$. Khoảng cách hình học giữa mọi class đều bằng nhau. Nó cũng kết hợp hoàn hảo với hàm mất mát **Categorical Cross-Entropy** $L = -\sum_{i} y_i \log(\hat{y}_i)$ triệt tiêu toàn bộ các phép tính thừa.

---

### CHUYÊN ĐỀ 4: ĐỘNG LỰC HỌC CHUỖI THỜI GIAN (TIME SERIES DYNAMICS)

#### Câu hỏi 35: What is the primary challenge in analyzing time series data?

_Đáp án của chuyên gia:_ **C. Accounting for temporal dependencies**.

_Tư duy chuyên gia:_ Trong các bài toán Machine Learning truyền thống (như phân loại ảnh, nhà đất), các điểm dữ liệu $x_i$ được giả định là **I.I.D (Độc lập và phân phối đồng nhất)**. Nghĩa là việc bán được căn nhà A không liên quan đến căn nhà B. Nhưng Time Series phá vỡ hoàn toàn quy luật này! Giá chứng khoán của ngày hôm nay $x_t$ phụ thuộc mật thiết vào giá ngày hôm qua $x_{t-1}$. Mối quan hệ ràng buộc theo thời gian (Temporal dependencies) này là kẻ thù khiến DNN hay Linear Regression truyền thống thất bại. Đó là lý do ta phải phát minh ra mạng **RNN / LSTM**, sử dụng Cell State / Memory $C_t$ để ghi nhớ thông tin xuyên suốt trục thời gian.

#### Câu hỏi 34: What is the role of hyperparameter tuning in time series forecasting using machine learning?

_Đáp án của chuyên gia:_ Dựa trên bài giảng về RNN, siêu tham số ở đây bao gồm cấu trúc mạng, learning rate, và đặc biệt là sequence length/lag. Một đáp án mang tính bao quát thường là **B. To optimize the learning rate of the model** hoặc cấu hình mạng nói chung. _Trong thực tiễn TS,_ việc "Tuning" là để tìm ra sự kết hợp hoàn hảo giữa _kích thước cửa sổ trượt (window_size / lag values)_, số lượng node bộ nhớ ẩn trong LSTM, và tốc độ cập nhật trọng số (learning rate) nhằm chống lại hiện tượng Vanishing Gradient.

#### Câu hỏi 31: Which statistical measure is commonly used to decompose a time series into trend, seasonality, and residual components?

_Đáp án của chuyên gia:_ **D. Moving Average (MA)**.

**1. Bản chất Vật lý của Tín hiệu (Signal Decomposition):** Một chuỗi thời gian $Y_t$ luôn cấu thành từ: $Y_t = Trend_t + Seasonality_t + Residual_t$. Làm sao để bóc tách chúng? Kỹ sư dùng **Moving Average (Trung bình trượt)**. Bằng cách áp dụng phép toán: $$ MA_t = \frac{1}{k} \sum_{i=0}^{k-1} Y_{t-i} $$ Phép tính này hoạt động y hệt như một **Low-pass filter (Bộ lọc thông thấp)** trong DSP. Nó san phẳng (smooth out) toàn bộ các dao động chu kỳ ngắn hạn (Seasonality) và các hạt nhiễu (Residuals/Noise), làm hiện nguyên hình một đường cong dài hạn siêu mượt, đó chính là **Trend (Xu hướng)**. Sau khi lấy $Y_t - MA_t$, ta dễ dàng thu được các thành phần còn lại.

---

_Là một Senior AI Engineer, tôi tin rằng khi bạn thấu hiểu căn nguyên của từng dòng code và phương trình tối ưu như trên, không một hệ thống ML nào - dù là trên môi trường On-Premise hay Cloud scale khổng lồ - có thể làm khó được bạn. Chúc bạn sẽ áp dụng thành công những nền tảng này để tạo ra các sản phẩm AI đột phá! Bạn có muốn bàn luận sâu hơn về mô hình nào không?_
---

#### CÁC CÂU HỎI TỪ 41 - 50

**Câu 41:** How does autocorrelation play a role in time series analysis?

- [ ] a) It measures the correlation between different time series.
    
- [x] b) It helps identify patterns within a single time series at different lags.
    
- [ ] c) It calculates the average correlation across multiple time series.
    
- [ ] d) It assesses the correlation between time series and external factors.
    

**Đáp án: B** — Identifies patterns within a single time series at different lags. --- ## Bản chất Toán học $$\gamma(h) = \text{Corr}(Y_t, Y_{t-h})$$ Lấy chuỗi $Y_t$ nhân chập với chính nó nhưng dịch lùi $h$ bước thời gian. **Thực tiễn:** Nếu $\gamma(h)$ bật cao tại $h=7$ và $h=14$ → dữ liệu có seasonality theo tuần → cấu hình `sequence_length` cho mạng Nơ-ron theo đó. --- ## Nhớ nhanh > **ACF** = "soi gương lệch thời gian" → tìm chu kỳ lặp của chính mình
    

**Câu 42:** What is the primary purpose of the ImageDataGenerator in TensorFlow?

- [ ] a) Generating synthetic images for training
    
- [ ] b) Resizing images to a fixed dimension
    
- [x] c) Preprocessing and augmenting image data for model training
    
- [ ] d) Loading images from external URLs
    

**Câu 43:** Which deep learning architecture is commonly used for predicting the next word in a sequence?

- [ ] a) Convolutional Neural Network (CNN)
    
- [x] b) Recurrent Neural Network (RNN)
    
- [ ] c) Support Vector Machine (SVM)
    
- [ ] d) Decision Tree
    

**Câu 44:** What does the rescale parameter in ImageDataGenerator do?

- [ ] a) It resizes images to a specified shape.
    
- [x] b) It normalizes pixel values to a specified range.
    
- [ ] c) It rotates images randomly during training.
    
- [ ] d) It converts images to grayscale.
    

**Câu 45:** How does the lack of regularization contribute to overfitting in machine learning models?

- [ ] a) Regularization has no impact on overfitting.
    
- [x] b) Lack of regularization allows the model to fit the training data too closely.
    
- [ ] c) Regularization leads to underfitting rather than overfitting.
    
- [ ] d) Lack of regularization increases the learning rate.
    

**Câu 46:** How can you identify overfitting by examining a model's performance metrics?

- [x] a) If the training accuracy is high but the validation accuracy is low.
    
- [ ] b) If both training and validation accuracies are high.
    
- [ ] c) If the model has a low learning rate.
    
- [ ] d) If the number of epochs is too small.
    

**Câu 47:** What is the goal of sentiment analysis in text understanding?

- [ ] a) Identifying grammatical errors
    
- [ ] b) Extracting meaning from text
    
- [x] c) Determining the emotional tone of the text
    
- [ ] d) Summarizing the text content
    

**Câu 48:** What does the F1 Score metric consider when evaluating the performance of a forecasting model?

- [x] a) The balance between precision and recall
    
- [ ] b) The ratio of true positive predictions to total predicted positives
    
- [ ] c) The overall accuracy of the model
    
- [ ] d) The correlation between predicted and actual values
    

**Câu 49:** How does reducing the complexity of a model contribute to preventing overfitting?

- [ ] a) It increases the risk of overfitting.
    
- [ ] b) It has no impact on overfitting.
    
- [ ] c) It makes the model more prone to memorizing noise.
    
- [x] d) It encourages the model to capture general patterns rather than noise.
    

**Câu 50:** How can you implement a learning rate schedule using callbacks in TensorFlow?

- [ ] a) By using the ModelCheckpoint callback
    
- [ ] b) By using the EarlyStopping callback
    
- [x] c) By using the ReduceLROnPlateau callback
    
- [ ] d) Learning rate schedules cannot be implemented with callbacks
    
---

### 📖 BỘ TÀI LIỆU ÔN TẬP CHUYÊN SÂU: TỪ XỬ LÝ DỮ LIỆU ĐẾN HỆ THỐNG XỬ LÝ CHUỖI

### CHUYÊN ĐỀ 1: ĐƯỜNG ỐNG DỮ LIỆU VÀ TỐI ƯU HÓA ĐỘNG (DATA PIPELINE & DYNAMIC OPTIMIZATION)

#### Câu 42 & 44: Bản chất của `ImageDataGenerator` và tham số `rescale`

- **Q42:** What is the primary purpose of the ImageDataGenerator? -> **C. Preprocessing and augmenting image data for model training.**
- **Q44:** What does the rescale parameter in ImageDataGenerator do? -> **B. It normalizes pixel values to a specified range.**

**1. Góc nhìn Kỹ nghệ phần mềm (Software Engineering & Math):** Mạng Nơ-ron rất nhạy cảm với thang đo của dữ liệu. Một bức ảnh lưu trữ dưới định dạng RGB 8-bit có các giá trị pixel trải dài từ $0 \to 255$. Nếu bạn đưa trực tiếp ma trận này vào nhân ma trận: $$ Z = W \cdot X + b $$ Với $X \approx 255$, các giá trị $Z$ sẽ khổng lồ, đẩy hàm kích hoạt (như Sigmoid) vào vùng bão hòa (gradient = 0) hoặc gây ra hiện tượng **Bùng nổ đạo hàm (Exploding Gradient)**. Tham số `rescale=1./255` thực chất là thuật toán **Min-Max Normalization**: $$ X_{norm} = \frac{X - X_{min}}{X_{max} - X_{min}} = \frac{X - 0}{255 - 0} $$ Việc này ép không gian đặc trưng về khoảng $$, giúp thuật toán Gradient Descent hội tụ nhanh và ổn định hơn. Bên cạnh đó, `ImageDataGenerator` đóng vai trò là một luồng nạp dữ liệu (Data Streaming). Tại sao? Vì bạn không thể tải 1 triệu bức ảnh (vài trăm GB) vào thanh RAM 16GB của máy tính được. Nó sẽ nạp từng mẻ (batch), chuẩn hóa (rescale) và trộn (augment) theo thời gian thực (on-the-fly) để đưa vào GPU.

#### Câu 50: Làm thế nào để lập lịch Learning Rate bằng Callbacks?

- **Q50:** -> **C. By using the ReduceLROnPlateau callback.** _(Ghi chú: Lựa chọn ModelCheckpoint (A) là để lưu trọng số, EarlyStopping (B) là để dừng hẳn sớm, hai cái này không can thiệp thay đổi tốc độ học)._

**Bản chất Toán học Tối ưu:** Phương trình cốt lõi của Machine Learning là Gradient Descent: $$ \theta_{t+1} = \theta_t - \eta \nabla_\theta \mathcal{L}(\theta_t) $$ Khi đào tạo đến những epoch cuối, mô hình đã tiếp cận sát đáy của hàm mất mát $\mathcal{L}$. Nếu bạn vẫn giữ nguyên kích thước bước nhảy ($\eta$ - learning rate), thuật toán sẽ nhảy vọt qua lại hai bên vách thung lũng (Oscillation) mà không bao giờ chạm được cực tiểu toàn cục. `ReduceLROnPlateau` liên tục đo lường Validation Loss. Nếu hàm Loss đi ngang (plateau), nó tự động chia $\eta$ cho một hằng số (vd: $\eta_{new} = \eta_{old} \times 0.1$). _Liên hệ thực tế:_ Trong huấn luyện LLM như GPT-4, thay vì chờ Loss đi ngang, chúng tôi dùng **Cosine Annealing**. $\eta$ tăng vọt lúc đầu (warm-up) rồi giảm mượt mà theo hàm cosin để mô hình hạ cánh an toàn.

---

### CHUYÊN ĐỀ 2: KIỂM SOÁT SỨC CHỨA VÀ BÓNG MA QUÁ KHỚP (MODEL CAPACITY & OVERFITTING)

#### Câu 46: Nhận diện Overfitting qua Metrics

- **Q46:** -> **A. If the training accuracy is high but the validation accuracy is low.**

#### Câu 49 & 45: Mối quan hệ giữa Độ phức tạp, Regularization và Overfitting

- **Q49 (Giảm độ phức tạp):** -> **D. It encourages the model to capture general patterns rather than noise.**
- **Q45 (Thiếu Regularization):** -> **B. Lack of regularization allows the model to fit the training data too closely.**

**1. Bản chất Toán học và Trực quan (The Bias-Variance Tradeoff):** Hãy tưởng tượng bạn vẽ đồ thị đa thức. Nếu bạn có 10 điểm dữ liệu, một phương trình bậc 9 ($y = w_9x^9 + w_8x^8 + \dots + w_0$) sẽ đi qua chính xác 100% các điểm đó (Training Loss = 0, Train Acc = 100%). Nhưng đồ thị của nó sẽ uốn lượn thê thảm, và khi gặp điểm dữ liệu thứ 11 (Validation set), nó sẽ sai bét. Đây là hiện tượng **Overfitting (Quá khớp)** - mô hình đã học thuộc lòng "nhiễu" (noise) thay vì học "quy luật tổng quát" (general patterns).

- **Giảm độ phức tạp (Q49):** Bắt mô hình dùng đa thức bậc 2 thay vì bậc 9. Mất đi sức chứa (capacity), mô hình buộc phải bỏ qua các điểm nhiễu để vẽ một đường cong chung nhất.
- **Thêm Regularization (Q45):** Toán học của sự tối giản. Kỹ sư thêm tham số phạt L2 (Weight Decay) vào hàm mất mát gốc $\mathcal{L}_{data}$: $$ \mathcal{L}_{total}(\theta) = \mathcal{L}_{data}(\theta) + \frac{\lambda}{2} ||\theta||^2_2 $$ Thuật toán tối ưu giờ đây không chỉ cố làm giảm lỗi sai, mà còn phải cố giữ cho ma trận trọng số $\theta$ càng nhỏ càng tốt. Sự trói buộc này (kiểm soát - regularization) ép các nơ-ron không được trở nên quá nhạy cảm với nhiễu cục bộ.

_Lỗi sai của Junior:_ Các bạn kỹ sư trẻ hay vui mừng khi Train Accuracy đạt 99.9%. Đừng vui! Hãy lập tức in Validation Accuracy ra. Nếu đường Train cắm đầu đi xuống mà đường Validation đi ngang hoặc móc ngược lên, mô hình của bạn đã vỡ vụn. Phải dùng Dropout hoặc Early Stopping ngay lập tức.

---

### CHUYÊN ĐỀ 3: CẠM BẪY CỦA ACCURACY & THƯỚC ĐO F1-SCORE (METRICS PARADOX)

#### Câu 48: F1 Score đo lường điều gì?

- **Q48:** -> **A. The balance between precision and recall.**

**1. Bản chất Thống kê (Tại sao không dùng Accuracy?):** Giả sử tôi làm một hệ thống AI dự báo đột quỵ tim (hoặc dự báo thị trường chứng khoán sập). Tỷ lệ đột quỵ chỉ là 1/100. Nếu AI của tôi viết đúng một dòng code: `return "Không đột quỵ"`, nó đạt **Accuracy = 99%**. Độ chính xác cực cao, nhưng hệ thống này vô dụng và làm chết người! Đây là **Nghịch lý Dữ liệu mất cân bằng (Imbalanced Data Paradox)**. Chúng ta cần hai thước đo mới:

- **Precision (Độ chuẩn xác):** $\frac{TP}{TP + FP}$ - Khi AI báo "đột quỵ", bao nhiêu % là thật? (Sợ báo động giả).
- **Recall (Độ phủ):** $\frac{TP}{TP + FN}$ - Trong tất cả những người sắp đột quỵ, AI tìm ra được bao nhiêu %? (Sợ bỏ sót).
- **F1-Score:** Là Trung bình Điều hòa (Harmonic Mean) của Precision và Recall: $$ F1 = 2 \times \frac{Precision \times Recall}{Precision + Recall} $$ Trung bình điều hòa trừng phạt cực mạnh nếu một trong hai biến tiến về 0. Do đó, F1-Score cao đồng nghĩa với việc mô hình của bạn đã cân bằng hoàn hảo giữa việc "không bắt nhầm" và "không bỏ sót".

---

### CHUYÊN ĐỀ 4: ĐỘNG LỰC HỌC CHUỖI VÀ NGỮ NGHĨA (TIME SERIES & NLP DYNAMICS)

#### Câu 41: Vai trò của Autocorrelation trong Time Series

- **Q41:** -> **B. It helps identify patterns within a single time series at different lags.**

**Bản chất Vật lý:** Tự tương quan (Autocorrelation) là việc lấy một chuỗi tín hiệu $Y_t$, nhân chập với chính nó nhưng bị dịch lùi đi $h$ bước thời gian (lag). Hàm tự tương quan $\gamma(h)$: $$ \gamma(h) = \text{Corr}(Y_t, Y_{t-h}) $$ _Thực tiễn:_ Nếu đồ thị $\gamma(h)$ bật cao tại $h=7$ và $h=14$, tín hiệu đó cho kỹ sư biết hệ thống (ví dụ: lượng khách đi xe Grab) có tính mùa vụ theo tuần cực mạnh (cứ đúng thứ đó tuần sau lại lặp lại). Nhờ đó ta mới cấu hình được `sequence_length` chuẩn cho mạng Nơ-ron.

#### Câu 47: Mục tiêu của Sentiment Analysis (Phân tích cảm xúc)

- **Q47:** -> **C. Determining the emotional tone of the text.** _(Không phải sửa lỗi ngữ pháp (A), không phải chỉ dịch nghĩa thô (B) hay tóm tắt văn bản (D)._ Sentiment Analysis là việc đánh giá trạng thái cảm xúc (Tích cực, Tiêu cực, Trung lập) đằng sau chuỗi text.

#### Câu 43: Kiến trúc Deep Learning cho dự báo từ tiếp theo (Next-word Prediction)

- **Q43:** -> **B. Recurrent Neural Network (RNN).** (Hoặc bản nâng cấp LSTM/Transformer).

**1. Bản chất Toán học Mạng Hồi Quy (RNN):** CNN (A), SVM (C), Decision Tree (D) nhận các đầu vào có kích thước tĩnh và giả định chúng độc lập. Ngôn ngữ lại là một chuỗi thời gian, từ đứng sau phụ thuộc chặt chẽ vào cấu trúc từ đứng trước ("Tôi yêu" -> "Việt Nam"). RNN sinh ra để giữ lại một bộ nhớ ẩn (Hidden State - $h_t$) mang thông tin từ quá khứ truyền vào hiện tại: $$ h_t = \tanh(W x_t + U h_{t-1} + b) $$ Và sinh ra dự báo $\hat{y}_t = \text{softmax}(V h_t + c)$. Ma trận trọng số $U$ chính là lõi mang trí nhớ đi xuyên thời gian (BPTT - Backpropagation Through Time). _Sự tiến hóa liên ngành:_ Dù RNN/LSTM là khởi thuỷ của Next-word prediction, các bạn nên biết rằng ChatGPT hiện tại sử dụng **Transformers**. Nó rũ bỏ kiến trúc tuần tự của RNN mà dùng phương trình **Attention** (Cơ chế tự chú ý) để tính trọng số liên kết toàn cục: $$ \text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V $$ Giúp mô hình dự đoán từ tiếp theo chuẩn xác bằng cách "liếc nhìn" toàn bộ các từ quan trọng trong câu cùng một lúc.

---

_Từng dòng cấu hình (như `rescale` hay `ReduceLROnPlateau`), từng metric (F1-score) đều mang một ý nghĩa sống còn trong việc xây dựng hệ thống AI. Khi đứng trước những dự án tỷ đô, đây là cách mà một Senior Engineer bảo vệ hệ thống của mình khỏi sự sụp đổ. Chúc bạn sẽ áp dụng thành công những tư duy này!_


