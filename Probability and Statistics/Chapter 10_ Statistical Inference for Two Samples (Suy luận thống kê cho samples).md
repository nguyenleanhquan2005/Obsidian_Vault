Chapter 9 chúng ta đã làm quen với suy luận thống kê của 1 sample, về mean μ và xác suất p. Còn chapter 10 thì cũng sẽ làm về mean μ và xác suất p, chỉ khác là sẽ thực hiện trên 2 sample, 2 cái trừ cho nhau. Sẽ có 2 cái chính là tính confidence interval cho hiệu của 2 mean μ của 2 tổng thể khác nhau, và kiểm định H0 của nó.

### 10.1 Inference on the Difference in Means of Two Normal Distributions (Hiệu 2 mean)

Cũng như khi tính confidence interval cho 1 sample, thì phần này cũng chia thành 2 trường hợp: σ đã biết và chưa biết.

- Case 1: σ đã biết

Khi đó, hiệu 2 mean sẽ có :

![](https://sondeptraicbg.github.io/lrn/img/1011.png)

Khi này bạn sẽ dễ dàng đoán được công thức của 1-α confidence interval của hiệu 2 mean:

![](https://sondeptraicbg.github.io/lrn/img/1012.png)

- Case 2: σ chưa biết

Khi mà σ chưa biết thì ta chỉ tính được các variance s của sample thôi. Và khi này, sẽ có 1 cái variance chung được gọi là pooled estimator của σ²

![](https://sondeptraicbg.github.io/lrn/img/1016.png)

Công thức 1-α confidence interval của hiệu 2 mean, ghi nhớ là t sẽ có n1+n2-2 bậc tự do:

![](https://sondeptraicbg.github.io/lrn/img/1013.png)

Note: Các trường hợp đều có những bài toán tính confidence interval 1 phía. Và ta chỉ cần thay α/2 bằng α với những bài toán ấy.

### Hypothesis Tests on the Difference in Means

Cho hypothesis:

![](https://sondeptraicbg.github.io/lrn/img/1018.png)

Khi này H0 sẽ là một phát biểu về độ chênh lệch giữa mean của 2 tổng thể: ∆0.

VD: Một người cho rằng độ chênh lệch tuổi thọ trung bình giữa nam hơn nữ là 2 tuổi. Khi đó ta có H0: μ1 − μ2 = 2 tuổi.

Trong các bài toán cụ thể, ta lại gặp 2 trường hợp : σ đã biết và chưa biết. Và chúng ta làm y hệt các bài toán về H0 trước đó: tính test Statistic và so sánh với các giới hạn của confidence interval, nếu nằm ngoài thì reject H0

- Case 1: σ đã biết

Test Statistic:

![](https://sondeptraicbg.github.io/lrn/img/1019.png)

- Case 2: σ chưa biết

Test Statistic:

![](https://sondeptraicbg.github.io/lrn/img/10110.png)

(Sp là pooled estimator)

### 10.6 Inference on the Two Proportions (Hiệu xác suất của 2 tổng thể)

1-α confidence interval của hiệu 2 xác suất:

![](https://sondeptraicbg.github.io/lrn/img/1061.png)

p mũ là xác suất trong sample.

### Tests on the Difference in Population Proportions

![](https://sondeptraicbg.github.io/lrn/img/1062.png)

Tương tự như các bài toán trước đó, ta có test statistic:

![](https://sondeptraicbg.github.io/lrn/img/1063.png)

|**Difference in Mean**|**Point Estimate**|**Case**|**Formula (Confidence Interval)**|**Formula (Test Hypothesis)**|
|---|---|---|---|---|

| **For mean difference** | $\bar{X}_1 - \bar{X}_2$ $\bar{X_1} - \bar{X_2} \sim N(\mu_1 - \mu_2, \frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2})$  | σ12,σ22\sigma_1^2, \sigma_2^2σ12​,σ22​ known | Xˉ1−Xˉ2±E\bar{X}_1 - \bar{X}_2 \pm EXˉ1​−Xˉ2​±E, where E=zα/2σ12n1+σ22n2E = z_{\alpha/2} \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}E=zα/2​n1​σ12​​+n2​σ22​​​ | Z0=(Xˉ1−Xˉ2)−Δ0σ12n1+σ22n2Z_0 = \frac{(\bar{X}_1 - \bar{X}_2) - \Delta_0}{\sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}}Z0​=n1​σ12​​+n2​σ22​​​(Xˉ1​−Xˉ2​)−Δ0​​ | | --- | --- | --- | --- | --- |

| **For mean difference** | $\bar{X}_1 - \bar{X}_2$ | σ12,σ22\sigma_1^2, \sigma_2^2σ12​,σ22​ known | Xˉ1−Xˉ2±E\bar{X}_1 - \bar{X}_2 \pm EXˉ1​−Xˉ2​±E, where E=zα/2σ12n1+σ22n2E = z_{\alpha/2} \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}E=zα/2​n1​σ12​​+n2​σ22​​​ | Z0=(Xˉ1−Xˉ2)−Δ0σ12n1+σ22n2Z_0 = \frac{(\bar{X}_1 - \bar{X}_2) - \Delta_0}{\sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}}Z0​=n1​σ12​​+n2​σ22​​​(Xˉ1​−Xˉ2​)−Δ0​​ | | --- | --- | --- | --- | --- |

|||σ12=σ22=σ2\sigma_1^2 = \sigma_2^2 = \sigma^2σ12​=σ22​=σ2 unknown|Xˉ1−Xˉ2±E\bar{X}_1 - \bar{X}_2 \pm EXˉ1​−Xˉ2​±E, where E=tn1+n2−2⋅Sp1n1+1n2E = t_{n_1 + n_2 - 2} \cdot S_p \sqrt{\frac{1}{n_1} + \frac{1}{n_2}}E=tn1​+n2​−2​⋅Sp​n1​1​+n2​1​​, and Sp2=(n1−1)S12+(n2−1)S22n1+n2−2S_p^2 = \frac{(n_1-1)S_1^2 + (n_2-1)S_2^2}{n_1+n_2-2}Sp2​=n1​+n2​−2(n1​−1)S12​+(n2​−1)S22​​|t0=(Xˉ1−Xˉ2)−Δ0Sp1n1+1n2t_0 = \frac{(\bar{X}_1 - \bar{X}_2) - \Delta_0}{S_p \sqrt{\frac{1}{n_1} + \frac{1}{n_2}}}t0​=Sp​n1​1​+n2​1​​(Xˉ1​−Xˉ2​)−Δ0​​|
|---|---|---|---|---|

|||σ12,σ22\sigma_1^2, \sigma_2^2σ12​,σ22​ unknown, unequal|Xˉ1−Xˉ2±E\bar{X}_1 - \bar{X}_2 \pm EXˉ1​−Xˉ2​±E, where E=tν⋅S12n1+S22n2E = t_{\nu} \cdot \sqrt{\frac{S_1^2}{n_1} + \frac{S_2^2}{n_2}}E=tν​⋅n1​S12​​+n2​S22​​​, and ν\nuν degrees of freedom|t0=(Xˉ1−Xˉ2)−Δ0S12n1+S22n2t_0 = \frac{(\bar{X}_1 - \bar{X}_2) - \Delta_0}{\sqrt{\frac{S_1^2}{n_1} + \frac{S_2^2}{n_2}}}t0​=n1​S12​​+n2​S22​​​(Xˉ1​−Xˉ2​)−Δ|
|---|---|---|---|---|