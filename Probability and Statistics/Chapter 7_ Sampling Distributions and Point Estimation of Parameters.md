### 7.1 Introduction

Ta chọn ra X1, X2, X3, ... , Xn và gọi tập này là random sample với kích thước n.

VD: chọn 100 cái điện thoại từ nhà máy để test.

Sample mean và sample variance gọi là Statistic(bởi nó là của sample):

$$ \bar{X} = \frac{X_1 + X_2 + \dots + X_n}{n} $$

$$  S^2 = \frac{(X_1 - \bar{X})^2 + (X_2 - \bar{X})^2 + \dots + (X_n - \bar{X})^2}{n - 1} $$

Nên nhớ đây là của Sample nhé, và chúng gọi là Statistic được kí hiệu như trên. Chứ của Population thì gọi là Parameter được ký hiệu là μ và σ².

### Point Estimation

- Các Sample mean và sample variance là Statistic, ta gọi chúng lần lượt là

point estimator

của mean μ và variance σ² của Population.

- Còn khi tính ra số cụ thể, ta gọi nó là

point estimate

### 7.2 Sampling Distributions and the Central Limit Theorem

### Central Limit Theorem

Một Population có các tham số là μ và σ², và ta có sample mean ̅ x. Bạn nhớ lại phần 4.6 khi ta học standard normal distribution, thì cách tính Z sẽ là

.

$$ \text{If } X \sim N(\mu, \sigma^2), \text{ then } Z = \frac{X - \mu}{\sigma} \sim N(0, 1) $$

Còn bây giờ ta chỉ tính cho sample, với n là số số hạng trong sample ta có:

$$ Z = \frac{\bar{X} - \mu}{\sigma / \sqrt{n}} $$

- Nếu như Population có mean μ và variance σ² thì khi ta lấy ra 1 sample, nó sẽ có các thông số :

$$ \mu_{\bar{X}} = \mu, \quad \sigma_{\bar{X}} = \frac{\sigma}{\sqrt{n}} $$

- Nếu Population là phân bố chuẩn, thì sample cũng là phân bố chuẩn.
- Nếu Population không phải phân bố chuẩn, thì sample sẽ là phân bố xấp xỉ chuẩn nếu như kích thước(lượng dữ liệu) ≥ 30.

### Sampling Distribution of a Difference in Sample Means

Ta có

$X, Y: \text{Independent} \\E(aX + bY) = aE(X) + bE(Y) \\V(aX + bY) = a^2V(X) + b^2V(Y)$

$V(\bar{X_1} - \bar{X_2}) = \frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}$

$X_1, X_2 \sim \text{normal} \\\bar{X_1} \sim N\left(\mu_1, \frac{\sigma_1^2}{n_1}\right) \\\bar{X_2} \sim N\left(\mu_2, \frac{\sigma_2^2}{n_2}\right)$

$\bar{X_1} - \bar{X_2} \sim N\left(\mu_1 - \mu_2, \frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}\right)$

Cái này là khi ta so sánh 2 cái sample với nhau. Ví dụ so sánh độ chênh lệch tuổi thọ chó với mèo chẳng hạn, thì ta sẽ có:

$$ \mu_{\bar{X}_1 - \bar{X}_2} = \mu_1 - \mu_2 $$

$$ \sigma_{\bar{X}_1 - \bar{X}_2}^2 = \frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2} $$