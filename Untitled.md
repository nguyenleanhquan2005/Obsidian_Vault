1. **What is a primary learning objective related to optimization methods according to the sources?**
    - [ ] To only apply Stochastic Gradient Descent
    - [ ] To avoid using random minibatches to prevent convergence
    - [x] To apply optimization methods such as Stochastic Gradient Descent, Momentum, RMSProp, and Adam
    - [ ] To ignore the benefits of learning rate decay in optimization

---

2. **What does "mini-batch gradient descent" primarily accelerate in deep learning?**
    - [ ] Data preprocessing only
    - [ ] Deep learning training on large datasets
    - [ ] Model deployment
    - [x] Hyperparameter tuning

---

3. **What is a key difference between Batch Gradient Descent and Mini-Batch Gradient Descent regarding updates?**
    - [ ] Batch Gradient Descent makes quick updates, while Mini-Batch Gradient Descent makes smooth updates
    - [ ] Batch Gradient Descent considers the entire training data for a single update, while Mini-Batch Gradient Descent uses a subset
    - [ ] Mini-Batch Gradient Descent always results in noisier updates than Batch Gradient Descent
    - [ ] Batch Gradient Descent is faster than Mini-Batch Gradient Descent for large datasets

---

4. **In the context of mini-batch gradient descent, what does "an epoch" mean?**
    - [ ] A single iteration through a mini-batch
    - [ ] The total number of training samples
    - [ ] Passing each sample of the training set one time through the network to update the parameters
    - [ ] The size of a mini-batch

---

5. **Given a dataset with n=2000 samples and mini-batch size b=4, how many iterations correspond to one epoch in mini-batch gradient descent?**
    - [ ] 2000 iterations
    - [ ] 1 iteration
    - [ ] 500 iterations
    - [ ] 4 iterations

---

6. **What is one of the main advantages of using random minibatches?**
    - [ ] It simplifies data collection
    - [ ] It accelerates convergence and improves optimization
    - [ ] It reduces the need for bias correction
    - [ ] It guarantees finding the global optima

---

7. **How does the cost function typically behave during mini-batch gradient descent, compared to batch gradient descent?**
    - [ ] It decreases smoothly on every iteration, just like batch gradient descent
    - [ ] It is noisier with mini-batch iterations but still decreases over time
    - [ ] It always increases due to the small sample size
    - [ ] It remains constant due to the iterative updates

---

8. **What is a general guideline for choosing a mini-batch size when the training set is small (m < 2000)?**
    - [ ] Always use the entire training set (mini-batch size = m)
    - [ ] Select a mini-batch size of 64, 128, 256, or 512
    - [ ] Use a mini-batch size of 1 for stochastic gradient descent
    - [ ] The mini-batch size does not affect training for small datasets

---

9. **Mini-batch gradient descent accelerates training on large datasets by employing a loop to iterate through each mini-batch. What technique is crucial for efficient computation on m examples?**
    - [ ] Normalization
    - [ ] Regularization
    - [ ] Vectorization
    - [ ] Initialization

---

10. **What is the primary purpose of Exponentially Weighted Averages (EWAs)?**
    - [ ] To compute a simple average of data points
    - [ ] To compute a moving average of a sequence of data points that assigns exponentially decreasing weights to previous values
    - [ ] To apply bias correction to raw data
    - [ ] To randomly select data points for averaging

---

11. **In the EWA formula (Vt​=βVt−1​+(1−β)θt​), what does the parameter β control?**
    - [ ] The number of data points
    - [ ] The weight given to the current data point
    - [ ] The weight given to the previous average, often referred to as the smoothing factor
    - [ ] The overall magnitude of the average

---

12. **What is the effect of choosing a higher β value (closer to 1) in Exponentially Weighted Averages?**
    - [ ] It leads to a more responsive but volatile sequence
    - [ ] It leads to a smoother sequence with slower adaptation to changes
    - [ ] It completely disregards older data points
    - [ ] It causes overfitting of the data

---

13. **Exponentially Weighted Averages are widely used in which fields?**
    - [ ] Only in financial market analysis
    - [ ] Time series analysis, finance, and machine learning
    - [ ] Image processing and natural language understanding only
    - [ ] Database management and network security

---

14. **Why is bias correction sometimes applied in Exponentially Weighted Averages, especially during the initial phase of learning?**
    - [ ] The initial Vt​ values are too high
    - [ ] The moving average can underestimate the true value of the parameter due to a small number of initial values
    - [ ] It overestimates the parameter values during the initial phase
    - [ ] It causes the algorithm to diverge

---

15. **What is the main goal of applying bias correction in exponentially weighted averages?**
    - [ ] To increase computational costs
    - [ ] To normalize the estimate and account for fewer initial values, providing a more accurate parameter estimate
    - [ ] To make initial bias acceptable
    - [ ] To simplify the overall algorithm

---

16. **What is the primary benefit of using "gradient descent with momentum" compared to the standard gradient descent algorithm?**
    - [ ] It always uses a smaller learning rate
    - [ ] It works faster and reduces oscillations, especially in vertical directions
    - [ ] It focuses only on horizontal movement in the cost function
    - [ ] It prevents reaching the global minima

---

17. **In gradient descent with momentum, which terms resemble acceleration and friction?**
    - [ ] Only the learning rate, α
    - [ ] (1−β) resembles acceleration, and β acts as friction
    - [ ] dw and db
    - [ ] Vdw​ and Vdb​

---

18. **What is the main function of the RMSprop optimization algorithm?**
    - [ ] To maintain a constant learning rate throughout training
    - [ ] To solely reduce horizontal oscillations
    - [ ] To adjust the learning rate for each parameter during the update step by keeping an exponentially weighted average of the squares of the derivatives
    - [ ] To ensure the function is sloped more steeply

---

19. **How does RMSprop effectively reduce oscillations in the vertical direction?**
    - [ ] By increasing the update for each parameter
    - [ ] By dividing the update for each parameter by a larger number in the vertical direction
    - [ ] By adding epsilon to the numerator
    - [ ] By using a simple average of the derivatives

---

20. **What is the purpose of adding a very small epsilon value to the denominator in the RMSprop algorithm's weight update rule?**
    - [ ] To increase the learning rate
    - [ ] To ensure numerical stability and prevent division by zero or very small numbers
    - [ ] To make the oscillations larger
    - [ ] To simplify the calculation of derivatives

---

21. **What is the Adam optimization algorithm (Adaptive Moment Estimation) known for?**
    - [ ] It's a standard gradient descent algorithm with no additional features
    - [ ] It combines the effects of gradient descent with momentum and gradient descent with RMSProp
    - [ ] It is exclusively used for very small datasets
    - [ ] It only adjusts the learning rate for the bias terms

---

22. **What are the recommended default values for the hyperparameters β1​ and β2​ in the Adam optimization algorithm?**
    - [ ] β1​=0.5,β2​=0.9
    - [ ] β1​=0.9,β2​=0.999
    - [ ] β1​=0.1,β2​=0.9
    - [ ] β1​=0.999,β2​=0.9

---

23. **What is the primary intuition behind using learning rate decay?**
    - [ ] To make learning approaches converge slower
    - [ ] To allow for smaller and more precise steps towards the minimum instead of oscillating around it
    - [ ] To increase training speed and allow for larger steps
    - [ ] To prevent the algorithm from reaching the global minima

---

24. **A benefit of using learning rate decay is that initially, when the learning rate is not very small, training will be faster. What happens when the learning rate is slowly reduced?**
    - [ ] It increases the chance of getting stuck in local optima
    - [ ] It leads to larger, less precise steps
    - [ ] There is a higher chance of coming close to the global minima
    - [ ] It causes the model to overfit more quickly

---

25. **In the context of modern deep learning, what is the current understanding of the "problem of local optima"?**
    - [ ] It is the primary obstacle to training deep neural networks
    - [ ] Most points of zero gradient in a cost function are not local optima but saddle points
    - [ ] Deep learning algorithms are highly likely to get stuck in bad local optima
    - [ ] The problem has become more severe with advanced deep learning

---

26. **In high-dimensional spaces, what are common challenges in optimization for neural networks, where the derivative remains near zero?**
    - [ ] Only global optima
    - [ ] Saddle points and plateaus
    - [ ] Convex light functions
    - [ ] Perfect convergence

---

27. **Why is tuning hyperparameters effectively important in deep neural networks?**
    - [ ] It simplifies the network architecture
    - [ ] It can lead to a massive improvement in performance
    - [ ] It eliminates the need for large datasets
    - [ ] It reduces computational costs to zero

---

28. **Among the listed hyperparameters (learning rate, momentum, Adam's parameters, number of hidden layers/units, learning rate decay, mini-batch size), which one is typically considered the most important to tune?**
    - [ ] Mini-batch size
    - [ ] Number of hidden units
    - [ ] Learning rate (α)
    - [ ] Momentum (β)

---

29. **When tuning hyperparameters, why might randomly selecting values from a uniform distribution be preferable for certain hyperparameters like learning rate (alpha) or beta in exponentially weighted averages?**
    - [ ] It guarantees finding the optimal values
    - [ ] Small changes in these parameters can significantly impact results, and random search is often more effective than grid search
    - [ ] It reduces the need for careful tuning
    - [ ] It only works for a small number of hyperparameters

---

30. **For hyperparameters like the learning rate (alpha) or beta in exponentially weighted averages, what kind of scale is often recommended for sampling values?**
    - [ ] Linear scale
    - [ ] Exponential scale
    - [ ] Logarithmic scale
    - [ ] Discrete scale

---

31. **What is the "Panda" approach to hyperparameter tuning in practice?**
    - [ ] Training multiple models in parallel with diverse hyperparameters
    - [ ] Carefully adjusting a single model's learning rate by babysitting it
    - [ ] Using grid search for all hyperparameters
    - [ ] Focusing on a fixed set of hyperparameters

---

32. **What is the primary purpose of Batch Normalization in deep neural networks?**
    - [ ] To increase the complexity of the network
    - [ ] To normalize mean and variance of hidden unit values to speed up learning
    - [ ] To solely adjust the output layer activations
    - [ ] To prevent the network from converging

---

33. **In which part of the neural network is batch normalization typically applied?**
    - [ ] After the activation function
    - [ ] Before the input layer
    - [ ] After calculating the Z-value and before the activation function
    - [ ] Only on the output layer

---

34. **How does Batch Normalization contribute to enhancing the efficiency of training in networks with multiple hidden layers?**
    - [ ] It makes the input features less similar
    - [ ] It enhances the efficiency by normalizing mean and variance of hidden unit values
    - [ ] It removes the need for any regularization
    - [ ] It forces the network to learn slower

---

35. **Besides speeding up learning, how else can Batch Normalization act as a form of regularization?**
    - [ ] By explicitly adding L2 penalties
    - [ ] By adding some noise to the scaled hidden unit values, similar to dropout
    - [ ] By increasing the batch size significantly
    - [ ] By completely eliminating the need for other regularization techniques

---

36. **For what type of classification problem is Softmax regression primarily employed?**
    - [ ] Binary classification (two classes)
    - [ ] Multi-class classification (more than two classes)
    - [ ] Regression problems with continuous outputs
    - [ ] Anomaly detection

---

37. **What do the units in the output layer of a Softmax regression network represent?**
    - [ ] The raw linear outputs only
    - [ ] The total number of hidden layers
    - [ ] Probabilities of the input belonging to each specific class
    - [ ] The activation function values directly

---

38. **How does the Softmax layer transform its linear output into probabilities?**
    - [ ] By applying a sigmoid function
    - [ ] By directly converting values to percentages
    - [ ] By exponentiating and normalizing the values
    - [ ] By summing the values and taking the average

---

39. **What is a key reason for using a Machine Learning Strategy?**
    - [ ] To minimize data collection efforts
    - [ ] To choose the wrong idea and waste time and effort
    - [ ] To determine the most promising ideas and effectively build and ship deep learning products
    - [ ] To avoid experimenting with different algorithms

---

40. **What does "orthogonalization" refer to in machine learning?**
    - [ ] Combining all components into a single, complex module
    - [ ] Separating the concerns of a machine learning system into distinct and independent modules or components
    - [ ] Ensuring that modules heavily depend on each other
    - [ ] Applying the same function across all layers of a network




project-root/
├── game-client/                # C# (Unity/Godot)
│   ├── Assets/                 # UI (phong cách Japandi), Models, Scenes
│   ├── Scripts/                # C# Scripts (áp dụng async/await, Task Parallel Library)
│   │   ├── Core/               # Logic nền tảng, Object Pooling
│   │   └── Network/            # Gọi API an toàn với try-catch toàn diện
│   └── Packages/               # NuGet và các thư viện quản lý qua Package Manager
├── backend-services/           # Go (gRPC/HTTP API Gateway & Logic)
│   ├── cmd/                    # Entry points (hàm main)
│   ├── internal/               # Logic nghiệp vụ bảo mật (không export ra ngoài)
│   ├── pkg/                    # Các thư viện dùng chung (O(N log N) algorithms, Utils)
│   ├── Dockerfile              # Multi-stage build cho Go
│   └── go.mod
├── ai-inference/               # Python (FastAPI xử lý Deep Learning)
│   ├── app/                    # Các async endpoints xử lý yêu cầu
│   ├── models/                 # Chứa trọng số và logic suy luận (YOLO, CDCN, Audio)
│   ├── core/                   # Cấu hình, logging tập trung, và error handling
│   ├── tests/                  # Pytest cho validation
│   ├── requirements.txt        # Quản lý dependencies (ưu tiên thư viện có sẵn)
│   └── Dockerfile              # Môi trường chạy suy luận được tối ưu hóa
├── infrastructure/             # DevOps & Quản lý Đám mây
│   ├── terraform/              # Infrastructure as Code (AWS VPC, EKS, RDS)
│   ├── helm-charts/            # Cấu hình Kubernetes cho toàn bộ dịch vụ
│   └── scripts/                # Các shell script hỗ trợ tự động hóa
├── .github/                    # CI/CD Workflows (GitHub Actions)
│   └── workflows/
│       ├── go-ci.yml
│       ├── python-mlops.yml
│       └── unity-build.yml
└── README.md                   # Tài liệu kiến trúc học thuật và hướng dẫn setup

### Lộ trình 18 Tháng Tiếp Theo (Tháng 7 - 24)

**Quý 3 & 4 (Tháng 7 - 12): Kiến trúc Dữ liệu & Tối ưu hóa Khối lượng công việc** Giai đoạn này dịch chuyển từ phát triển tính năng sang đảm bảo khả năng chịu tải và xử lý bất đồng bộ.

- **Kỹ thuật (Go & Python):** Tích hợp Message Queue (như RabbitMQ hoặc Kafka). Thay vì Game Client gọi thẳng AI, client sẽ gửi dữ liệu (hình ảnh/âm thanh) tới Go Backend. Go sẽ đẩy vào hàng đợi để các Python AI Workers xử lý bất đồng bộ. Đảm bảo kiến trúc Go thread-safe và cảnh báo các race conditions tiềm ẩn.
    
- **Kỹ thuật (C#):** Tối ưu hóa bộ nhớ Game Client. Áp dụng nghiêm ngặt Object Pooling để giảm thiểu Garbage Collection (GC) spikes, đảm bảo tốc độ khung hình (FPS) ổn định. Tích hợp hệ thống logging chuẩn của .NET.
    
- **Tài chính (FinOps):** Phân tích hiệu quả chi phí. Chạy suy luận (inference) Deep Learning tiêu tốn tài nguyên lớn. Triển khai kiến trúc dùng AWS Spot Instances cho các tác vụ AI không yêu cầu thời gian thực nhằm tiết kiệm đến 70% chi phí máy chủ.
    
- **Lãnh đạo & PM:** Áp dụng quy trình Code Review học thuật. Mọi thay đổi về thuật toán đều phải đi kèm với benchmarks độ phức tạp thời gian/không gian.
    

**Quý 5 & 6 (Tháng 13 - 18): Trí tuệ Nhân tạo Động & MLOps Nâng cao** Sử dụng dữ liệu để trực tiếp thay đổi trải nghiệm tương tác.

- **Tâm lý học & Thiết kế (Game):** Sử dụng dữ liệu từ mô hình Speech Emotion Recognition để điều chỉnh độ khó động (Dynamic Difficulty Adjustment). Nếu AI phân tích giọng nói người chơi có dấu hiệu bực tức, hệ thống tự động tinh chỉnh hành vi của NPC hoặc giảm rào cản tài nguyên, giữ người chơi ở trạng thái "Flow".
    
- **Kỹ thuật (MLOps):** Triển khai Model Registry (ví dụ: MLflow) trên Kubernetes. Thiết lập 파이프라인 (pipeline) tự động đánh giá: nếu mô hình YOLO mới có chỉ số mAP cao hơn mô hình hiện tại trên tập dữ liệu kiểm thử, tự động thực hiện Blue/Green Deployment.
    
- **Bảo mật:** Áp dụng Secret Manager (như AWS Secrets Manager hoặc HashiCorp Vault) để lưu trữ mọi API keys, database credentials và certificates. Tuyệt đối không hardcode trong bất kỳ môi trường nào.
    
- **Nghiên cứu (AI):** Cập nhật hệ thống Face Anti-Spoofing với các phương pháp trích xuất đặc trưng mới ở miền tần số, giảm thiểu các trường hợp False Positives từ luồng camera trực tiếp.
    

**Quý 7 & 8 (Tháng 19 - 24): Vận hành Toàn cầu (SRE) & Ra mắt Phân tích** Chuẩn bị hệ thống ở cấp độ sẵn sàng phát hành và bảo vệ tính học thuật của dự án.

- **Kỹ thuật (SRE):** Xây dựng hệ thống giám sát khả năng quan sát (Observability) toàn diện. Triển khai Distributed Tracing để theo dõi một request từ lúc người chơi click chuột ở C# Client, đi qua Go Backend, đến lúc Python AI trả kết quả. Mục tiêu là duy trì SLA 99.9% và phát hiện các nút thắt cổ chai (bottlenecks) dưới 100ms.
    
- **Kinh tế học & Marketing:** Phân tích sự cân bằng của nền kinh tế vi mô trong game dựa trên lượng dữ liệu lớn thu thập được. Thực hiện App Store Optimization (ASO) dựa trên các từ khóa chuyển đổi cao nhất.
    
- **Nghiên cứu Học thuật:** Viết tài liệu/luận văn tổng kết. So sánh định lượng giữa kiến trúc Microservices hiện tại với các kiến trúc Monolithic truyền thống trong việc xử lý tín hiệu âm thanh và hình ảnh theo thời gian thực.
    

Bạn có muốn mình tạo cấu hình `go.mod` và `Dockerfile` đa bước (multi-stage) tối ưu nhất cho Go backend để đảm bảo an toàn và dung lượng siêu nhẹ không?