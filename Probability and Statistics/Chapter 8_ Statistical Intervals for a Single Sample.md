### 8.1 Introduction

Confidence interval (khoảng tin cậy) là khoảng mà ta tính ra từ các dữ liệu của sample để dự đoán thông số của Population. Ví dụ 1-α level of confidence của μ tức là:

Xác suất để μ nằm trong khoảng tin cậy đó là 1-α:

$$ P(L \leq \theta \leq U) = 1 - \alpha $$

L: Lower-confidence limit = $\text{Lower bound} = \bar{X} - E$

U: Upper-confidence limit = $\text{Lower bound} = \bar{X} + E$

### where : $E = z_{\alpha/2} \frac{\sigma}{\sqrt{n}}$

E : margin of error

length of Confidence Interval (CI) = 2E

Ví dụ: Ta không biết tuổi thọ của tất cả các con chó là bao nhiêu, ta sẽ thi thu thập dữ liệu của 100 con. Vậy ta sẽ có sample mean, ví dụ sample mean = 10 năm. Sau đó ta tính khoảng tin cậy 95%, tức α = 5%, ra [7.5, 12,5] chẳng hạn, thì tức là mean μ của Population sẽ có 95% khả năng nằm trong khoảng đó.

### 8.2 Confidence Interval for a Population Mean (Khoảng tin cậy cho mean)

### Ta sẽ chia ra 3 trường hợp

- Trường hợp 1: variance σ² đã biết.
- Trường hợp 2: Đây là 1 phân bố bất kỳ, không nhất thiết phải là normal, nhưng phải có size lớn (≥ 40).
- Trường hợp 3: variance σ² chưa biết.

Trường hợp 1: variance σ² đã biết

1–α confidence interval cho mean μ là:

$$ \bar{x} - z_{\alpha/2} \frac{\sigma}{\sqrt{n}} \leq \mu \leq \bar{x} + z_{\alpha/2} \frac{\sigma}{\sqrt{n}} $$

Zα/2 là giá trị của Z để xác suất P(Z > zα/2) = α/2.

Để dễ hình dung, ta có α=5%, Zα/2= Z0.025 = 1.96, hay P(Z>1.96) = α/2 = 0.025

![](https://sondeptraicbg.github.io/lrn/img/822.png)

VD: Tuối thọ của bóng đèn được biết là có phân bố chuẩn và có σ = 25 giờ. Ta có một sample gồm 20 bóng và chúng có tuổi thọ trung bình là 1014 giờ. Tìm 95% confidence interval cho mean μ của loại bóng đèn này .

Phân tích: Population Loại bóng đèn này phân bố chuẩn nên sample cũng có phân bố chuẩn, chúng ta đã biết standard deviation σ = 25 giờ. Giải: Ta có thêm một cái sample gồm 20 bóng có tuổi thọ trung bình là 1014 => $\bar{X}$ = 1014, n=20. Ta phải tính độ tin cậy 95%, tức α = 5%, Zα/2 = 1.96. Thay vào tính đc 1003.04 ≤ μ ≤1024.96 .

Còn 1 dạng trong cái này, đó là bắt tính số lượng (n) để có thể đạt được một khoảng confidence interval nhất định.Ta thấy rằng để dự đoán mean μ của tổng thể, thì càng nhiều dữ liệu càng tốt, điều đố khá dể hiểu và bạn cũng có thể nhìn vào phương trình trên kia để thấy điều đó, khi n càng lớn thì confidence interval càng thu hẹp lại. Vì vậy để tự tin rằng ta có một khoảng confidence interval bằng bao nhiêu đó thì ta cũng phải có số lượng dữ liệu nhất định. Công thức:

![](https://sondeptraicbg.github.io/lrn/img/823.png)

E ở đây là

![](https://sondeptraicbg.github.io/lrn/img/824.png)

VD: Lấy lại VD ở trên, thử tính lượng bóng đèn cần để ta có 95% confident để sai số khi ta ước tính mean μ của tổng thể < 5 giờ.

Giải: Ta có : α = 5%, => α/2 = 0.025. σ = 25 giờ, E = 5 giờ, thay vào công thức n = 96.05, tuy nhiên ta luôn phải làm tròn lên nên n=97.

Trường hợp 2: Đây là 1 phân bố bất kỳ, không nhất thiết phải là normal, nhưng phải có size lớn (≥ 40).

1–α confidence interval cho mean μ:

$$ \bar{x} - z_{\alpha/2} \cdot \frac{s}{\sqrt{n}} \leq \mu \leq \bar{x} + z_{\alpha/2} \cdot \frac{s}{\sqrt{n}} $$

Bời vì đây không phải phân bố chuẩn nên không có σ nhé. Chỉ có S cho cái sample đấy thôi, nhưng cũng chả khác nhau đâu.

Trường hợp 3: variance σ² chưa biết biết.

Vì σ chưa biết nên chỉ có S, hãy nhớ trường hợp σ chưa biết, đồng thời là phân bố chuẩn thì mới dùng t, còn không phải dùng z. Công thức:

$$ \bar{x} - t_{\alpha/2, n-1} \cdot \frac{s}{\sqrt{n}} \leq \mu \leq \bar{x} + t_{\alpha/2, n-1} \cdot \frac{s}{\sqrt{n}} $$

### 8.3 Large-Sample Confidence Interval for a Population Proportion (Confidence Interval cho xác suất)

Nó cũng giống như mean thôi, mỗi tội là tìm Confidence Interval cho xác suất. Công thức:

$$ \hat{p} - z_{\alpha/2} \sqrt{\frac{\hat{p}(1 - \hat{p})}{n}} \leq p \leq \hat{p} + z_{\alpha/2} \sqrt{\frac{\hat{p}(1 - \hat{p})}{n}} $$

Trong đó

![](https://sondeptraicbg.github.io/lrn/img/828.png)

là xác suất của sample, x là cái lượng thỏa mãn, còn n là kích thước sample. Nếu để ý, bạn sẽ thấy pˆ(1-pˆ) trong công thức chính là σ² giống như phần binorminal, nên suy cho cùng, công thức này y hệt phần trên.

VD: 1000 ca ung thư được lấy ngẫu nhiên, và 823 ca chết sớm. Tính 95% confidence interval cho tỉ lệ chết sớm.

Giải: Ta có x = 823, n = 1000 => pˆ = 0.823. α=5% = 0.05 => α/2 = 0.025 => Zα/2 = 1.96. Vậy ta tính được 0.799 ≤ p ≤ 0.847.

Trong chap này ta mới chỉ đọc thấy confidence interval được giới hạn 2 đầu, nhưng trong bất kỳ dạng nào đề có các trường hợp confidence interval 1 phía, Ví dụ như Phần 8.1 trường hợp 1, ta sẽ có các bài toán bắt tính confidence interval cho 1 phía,

A ( 1-a) upper- confidence bound for u is

$$ \mu \leq \bar{x} + z_{\alpha} \cdot \frac{\sigma}{\sqrt{n}} $$

A ( 1-a) lower- confidence bound for u is:

$$ \mu \geq \bar{x} - z_{\alpha} \cdot \frac{\sigma}{\sqrt{n}}

$$

Mọi trường hợp 1 phía thì Zα/2 sẽ được thay bằng Zα.



![[image(2).png]]

![[image(1).png]]