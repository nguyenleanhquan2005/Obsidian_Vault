### (Biến ngẫu nhiên liên tục và phân bố xác suất)

### 4.1 Continuous Random Variables (biến ngẫu nhiên liên tục)

Just a definition:

Biến ngẫu nhiên liên tục (Continuous Random Variables) là biến ngẫu nhiên có một khoảng các số thực cho các khả năng của nó.

VD: tốc độ, xe bạn có thể đi trong khoảng 0-50km/h, vậy bạn có thể đạt bất kì giá trị nào, 40.00001, 25, 36.9999, ... .

### 4.2 Probability Distributions and Probability Density Functions (phân bố xác suất và hàm mật độ xác suất)

f(x) là hàm phân bố xác suất của biến ngẫu nhiên X nếu :

![](https://sondeptraicbg.github.io/lrn/img/continuousDis.png)

Đây là hàm phân bố, nó liên tục chứ không giống với biến rời rạc. Đối với biến rời rạc, mỗi giá trị của X nó sẽ có giá trị cụ thể của X kèm theo nó. Nhưng với biến liên tục, nó sẽ có vô hạn giá trị nên xác suất để xảy ra giá trị cụ thể sẽ = 0. Vậy nên ta thường tính xác suất theo 1 khoảng, nó sẽ bằng tích phân (hay diện tích) trong khoảng đó.

![](https://sondeptraicbg.github.io/lrn/img/continuousDia.png)

Như hình trên ta thấy xác suất của X để nó nằm trong khoảng a và b là tích phân từ a đến b, hay diện tích trong khoảng đó.

![](https://sondeptraicbg.github.io/lrn/img/aAndB.png)

Chú ý 1 điều rằng dấu "<" và "≤" tương đương nhau trong biến liên tục, bởi xác suất để xảy ra giá trị cụ thể luôn = 0. Bạn thử tưởng tượng khi đi xe, bạn không thể nào đi đúng 40Km/h được, bởi có thể bạn đang đi 39.99999 km/h hay 40.0001km/h. Chẳng có gì là tuyệt đối cả.

### 4.3 Cumulative Distribution Functions (Hàm phân bố tích lũy)

Hàm phân bố tích lũy:

![](https://sondeptraicbg.github.io/lrn/img/cumulativeContinue.png)

Cũng giống như bên phần rời rạc thì phần liên tục cũng có concept tương tự, là tại giá trị x thì F(x) sẽ có giá trị là xác suất để ≤ x. ta thấy nó sẽ là tích phân từ −∞, nhưng nếu đề cho khoảng giá trị ban đầu là a≤X≤b thì ta có thể thay −∞ bằng a để tính F(x).

![](https://sondeptraicbg.github.io/lrn/img/hieuHaiKhong.png)

Công thức trên khá dễ để hiểu và cũng hay dùng, giá trị của F(b) bằng xác suất để X≤b, F(a) là xác suất để X≤a, vậy thì xác suất để a≤X≤b sẽ là F(b)-F(a).

### 4.4 Mean and Variance of a Continuous Random Variable (Kỳ vọng và phương sai của biến liên tục)

f(x) là density function (hàm phân bố), ta có:

mean (kỳ vọng) :

![](https://sondeptraicbg.github.io/lrn/img/meanOfContinuous.png)

variance (phương sai) :

![](https://sondeptraicbg.github.io/lrn/img/varianceOfConti.png)

standard deviation (độ lệch chuẩn) :

![](https://sondeptraicbg.github.io/lrn/img/standardOfConti.png)

### 4.5 Continuous Uniform Distribution (phân bố đồng đều liên tục)

Cũng tương tự như biến rời rạc, biến liên tục cũng có phần đồng đều, khá dễ và chúng có dạng:

![](https://sondeptraicbg.github.io/lrn/img/uniformOfConti.png)

Đồ thị:

![](https://sondeptraicbg.github.io/lrn/img/uniformDiaOfCon.png)

mean (kỳ vọng) : và variance (phương sai) :

![](https://sondeptraicbg.github.io/lrn/img/meanOfUniformCon.png)

Cumulative function (Hàm tích lũy) của biến liên tục phân bố đồng đều:

![](https://sondeptraicbg.github.io/lrn/img/cumulativeOfUniOfCon.png)

### 4.6 Normal Distribution (Phân bố chuẩn)

Phần này quan trọng, nó sẽ liên quan đến nhiều thứ về sau. Nó sẽ sử dụng cho các bài toán mang tính chất có lượng dữ liệu rất lớn. Sau này ta sẽ thấy họ sử dụng cái này để ước lượng các thông số của tổng thể (Population) thông qua một phần dữ liệu (Sample).

VD: nghiên cứu lương 1000 người dân để đánh giá lương trung bình của toàn dân số.

Biến ngẫu nhiên X sẽ được coi là có phân bố chuẩn (normal distribution) với tham số μ và σ², ký hiệu X ∼ N(μ, σ²), nếu như hàm phân bố xác suất của nó là:

![](https://sondeptraicbg.github.io/lrn/img/normalDisFunc.png)

Tin vui là cái hàm trên bạn không phải nhớ, chỉ là giới thiệu qua thôi. Để dễ hình dung hơn về mean μ và variance σ² , ta quan sát biểu đồ sau:

![](https://sondeptraicbg.github.io/lrn/img/exampleNormalDis.png)

Ta thấy rằng μ chính là kỳ vọng, giá trị trung bình của Population(tổng thể), các giá trị sẽ tập trung nhiều về đó, còn σ² biểu diễn cho sai số nên dễ dàng thấy rằng phương sai càng lớn thì đồ thị sẽ thoải hơn, không tập trung nhiều gần μ bằng khi σ² nhỏ. Và cái này sẽ giúp bạn hiểu bản chất hơn thôi, chứ thi thì không có phần đồ thị này.

mean (kỳ vọng) : và variance (phương sai) :

![](https://sondeptraicbg.github.io/lrn/img/meanOfNormal.png)

Standard Normal Distribution :

Từ đây, chúng ta sẽ không dùng biểu đồ như bên trên nữa, mà mọi bài toán liên quan đến phân bố chuẩn sẽ được quy về Z. với các tham số μ = 0, σ = 1, nó kiểu như đồ thị phân bố của các độ lệch chia cho standard deviation (độ lệch chuẩn). Đồ thị nó sẽ như này:

![](https://sondeptraicbg.github.io/lrn/img/diagramOfZ.png)

Còn hàm Cumulative (tích lũy) của nó sẽ như sau:

$$ \Phi(z) = P(Z \leq z) $$

Cái này dùng nhiều, nó là diện tích từ z trở về trước, là xác suất để Z ≤ z, VD:

![](https://sondeptraicbg.github.io/lrn/img/exampleOfPZ.png)

Khi ta có giá trị μ , σ của X, thì ta sẽ chuyển sang Z bằng cách:

$$ \text{If } X \sim N(\mu, \sigma^2) \text{ then } Z = \frac{X - \mu}{\sigma} \sim N(0,1) $$

Ta sẽ tính xác suất khi X nhỏ hơn a bằng cách quy đổi sang giá trị của z, và đồ thị của Z luôn cố định cho mọi bài toán:

$$ P(X < a) = P\left(Z < \frac{a - \mu}{\sigma}\right) $$

$$ P(a < X < b) = P\left(Z < \frac{b - \mu}{\sigma}\right) - P\left(Z < \frac{a - \mu}{\sigma}\right) $$

### 4.7 Normal Approximation to the Binomial and Poisson Distributions

### (Phân bố xấp xỉ chuẩn cho Binomial and Poisson)

Binomial and Poisson là 2 loại phân bố ta đã học ở chapter 3. Nhưng mà khi đó ta chỉ làm với những thông số nhỏ, bạn thử tưởng tượng với binomial, khi ta có rất nhiều phép thử thì ta không thể tính bằng các con số có số mũ vài chục vài trăm được, vì vậy họ sẽ sử dụng phân bố xấp xỉ chuẩn cho những trường hợp này.

### Binomial Distribution:

Như đã học, Binomial Distribution sẽ có 2 thông số là n và p, lần lượt biểu thị cho số phép thử và xác suất ra "success" ở mỗi lần thử. Ở dạng đó ta có:

### mean $\mu = np$

và variance $\sigma^2 = np(1 - p)$ .

### Poisson Distribution:

Poisson cũng vậy, đôi khi ra sẽ gặp phải trường hợp có thông số rất lớn ta cũng sẽ phải sử dụng phân bố xấp xỉ chuẩn. Các thông số của Poisson sẽ là

### mean μ = λ và variance σ² = λ và μ = σ².

Các công thức xác suất cho 2 trường hợp này:

$$ P(X \leq x) = P(X \leq x + 0.5) \approx P \left( Z \leq \frac{x + 0.5 - \mu}{\sigma} \right) $$

$$ P(X \geq x) = P(X \geq x - 0.5) \approx P \left( Z \geq \frac{x - 0.5 - \mu}{\sigma} \right) $$

Nó sẽ được áp dụng hiệu quả nếu μ lớn hơn 5.

### 4.8 Exponential Distribution (Phân bố mũ)

Với Poisson, ta có λ là số lượng trung bình/ 1 khoảng thời gian hoặc không gian. Thì với phân bố mũ, nó sẽ tính về khoảng thời gian hay không gian giữa 2 lần xuất hiện liên tiếp.

VD: Với Poisson, ta có λ = 5 cuộc gọi/ ngày, thì với phân bố mũ, ta sẽ quan tâm tới khoảng cách trung bình giữa 2 lần suất hiện liên tiếp, tức trung bình mean = 1/λ = 4.8 giờ.

Hàm phân bố xác suất (Probability density function) :

$$ f(x; \lambda) = \begin{cases} \lambda e^{-\lambda x}, & x \geq 0, \\0, & x < 0\end{cases} $$

Cái hàm này là f nhỏ, phân bố chứ không phải là hàm tính xác suất nhé. Nên nhớ là phần biến liên tục thì ta sẽ tính xác suất bằng cách tích phân trong 1 khoảng nếu muốn tính xác suất để X nó rơi vào khoảng đó.

$$ F(x) = \int_0^\infty \left[ \frac{1}{\mu} e^{-\frac{x}{\mu}} \right] = 1 - e^{-\frac{x}{\mu}} $$

$$ F(x; \lambda) = \begin{cases} 1 - e^{-\lambda x}, & x \geq 0, \\0, & x < 0\end{cases} $$

mean (kỳ vọng) : và variance (phương sai) cho exponential distribution:

$$ \mu = E(X) = \frac{1}{\lambda}, \quad \sigma^2 = V(X) = \frac{1}{\lambda^2} $$

Z table:

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/d4f30e5b-760a-413c-a21a-a24af71087d9/ebd30742-6de0-4979-889b-ba07c5def986/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/d4f30e5b-760a-413c-a21a-a24af71087d9/f229932d-a374-41bc-a58f-cb0a0be01723/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/d4f30e5b-760a-413c-a21a-a24af71087d9/c6d88bb3-dcb7-4be6-800b-461b0f948a5f/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/d4f30e5b-760a-413c-a21a-a24af71087d9/4c5423bd-3676-4547-94ba-796ac3bdda23/image.png)