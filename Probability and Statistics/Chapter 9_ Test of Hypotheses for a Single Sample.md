Chapter 8 ta đã biết cách tính confidence interval, thì chapter này ta sẽ dùng nó để xem 1 cái kết luận nào đó có sai hay không. Ví dụ có 1 người nói số giờ làm trung bình trong 1 ngày của người Việt là 4.5 tiếng , thì để kiểm chứng câu nói này, ta sẽ đi thu thập dữ liệu 1000 người, sau đó ta sẽ tính confidence interval như trên chapter 8, rồi sau đó so sánh 2 dữ liệu để đưa ra kết luận.

### 9.1 Hypothesis Testing (kiểm chứng giả thuyết)

Statistical hypothesis (giả thuyết) là 1 cái phát biểu về Parameter của Population. Nhớ lại rằng Parameter là các thông số của Population, còn Statistic là của Sample, rõ ràng là các Parameter thì chúng ta chưa thể biết, ta chỉ có thể ước chừng chúng bằng cách lấy 1 sample để tính confidence interval như ở chapter 8.

Vì vậy ta sẽ lấy 1 cái sample để tính confidence interval, sau đó so sánh với cái giả thuyết để đưa ra kết luận (VD như cái đóng khung ở trên). Và với ví dự đó, ta có :

![](https://sondeptraicbg.github.io/lrn/img/911.png)

Trong 1 vài trường hợp, có thể giả thuyết sẽ là 1 phía:

![](https://sondeptraicbg.github.io/lrn/img/912.png)

VD: 1 phát biểu rằng chiều cao trung bình người Việt lớn hơn 1m65. khi đó H1 : μ>1m65.

Như đã thấy ở trên, H0 là null hypothesis, H1 là alternative hypothesis.

- Nếu reject H0 thì có nghĩa là ta có bằng chứng đủ mạnh để kết luận rằng H1 đã đúng.
- Còn nếu không reject H0, thì ta không có đủ bằng chứng là H0 đã đúng.

![](https://sondeptraicbg.github.io/lrn/img/913.png)

Note: Nhìn biết đồ trên, nó có ý nghĩa rằng ta có 1 cái sample và ta tính được rằng khoảng tin cậy confidence interval là [4.1, 4.9], tức là H0 cho μ bằng bất kỳ số nào từ 4.1 đến 4.9, ta đều phải fail to reject, còn H0 mà nằm ngoài khoảng đấy, thì ta reject . Và nên nhớ 1 điều, H0 thì luôn luôn là dấu "=", và H1 thì ghi là khác một giá trị cố định, nhưng thực chất ta chỉ reject H0 và chấp nhận H1 khi giá trị của H0 nằm ngoài khoảng tin cậy (confidence interval).

VD: Có 1 người nghĩ rằng chiều cao trung bình của người Việt là 1m65, để ông đấy xem suy đoán của mình có đúng hay không, ông ta đi khảo sát 1000 người ở Hà Nội. Ông ta tính được khoảng tin cậy là [1m55, 1m66], Vì vậy ông ta phải fail to reject H0, bởi vì H0: μ = 1m65, nằm trong khoảng tin cậy.

Tuy nhiên, các bạn phải hiểu rằng ta chỉ tính trên sample để kết luận, nên đôi khi kết luận của ta có thể sai do dữ liệu ta thu thập là toàn những trường hợp đặc biệt. Như khi ta tính khoảng tin cậy 95% thì ta có 95% khả năng là đúng, rõ ràng ta vẫn có 5% khả năng kết luận sai. Và sự sai sót ấy chia thành 2 trường hợp:

- Type 1 error : Reject H0 khi mà nó đúng. Để dễ hình dung hãy nhìn lại hình bên trên, nó có nghĩa rằng tiên đoán trước đó của mình về mean là đúng, nhưng do thu thập được toàn dữ liệu cùi mà ta tính được khoảng tin cậy bị lệch đi, dẫn đến mean μ của ta nằm ngoài khoảng tin cậy.
- Type 2 error : Fail to reject H0, tức là mình không bác bỏ H0 trong khi nó sai, ngược lại với Type 1.

### 9.2 Tests on the Mean of a Normal Distribution N(μ, σ²)

Trong phần 9.1 mình đã giải thích khá rõ về reject và fail to reject, các bạn cũng đã hiểu về confidence interval. Và trong các bài toán cụ thể, các bạn sẽ gặp 2 trường hợp để tính toán rồi đưa ra kết luận về H0:

- Case 1: Variance σ² của Population đã biết.

Test Statistic:

![](https://sondeptraicbg.github.io/lrn/img/921.png)

Trong bài toán cụ thể, ta sẽ tính Test Statistic, sau đó so sánh nó với các Z của giới hạn của khoảng tin cậy(confidence interval). Nếu nằm ngoài thì reject H0 thôi.

![](https://sondeptraicbg.github.io/lrn/img/922.png)

Như hình trên,

(a) là khoảng tin cậy có 2 phía với H1: μ ≠ μ0

(b) là khoảng tin cậy 1 phía với H1: μ > μ0

(c) là khoảng tin cậy 1 phía với H1: μ < μ0.

- Case 2: Variance σ² của Population chưa biết.

Test Statistic:

![](https://sondeptraicbg.github.io/lrn/img/924.png)

Khi không biết σ thì dùng t, khi biết σ thì dùng z, rất dễ, không khác gì nhau.

![](https://sondeptraicbg.github.io/lrn/img/925.png)

### 9.3 Tests on a population proportion (Kiểm định xác suất)

Phần trên thì kiểm định trên mean, bây giờ thì kiểm định xác suất, cách tính thì không khác gì nhau.

![](https://sondeptraicbg.github.io/lrn/img/926.png)

Thay vì tiên đoán trước giá trị trung bình của cái gì đấy, thì H0 của phần này sẽ là tiên đoán trước xác suất. Và ta cũng loại chúng nếu chúng nằm ngoài khoảng tin cậy thôi.

Ta sẽ có xác suất trong sample là p mũ, sau đó ta sẽ tính Test Statistic:

![](https://sondeptraicbg.github.io/lrn/img/927.png)

Rồi so sánh với Z của các giới hạn của khoảng tin cậy confidence interval:

Ví dụ: Một tạp chí nói rằng 1 nửa số tiến sĩ sẽ học tiếp sau khi tốt nghiệp. Dữ liệu từ một khảo sát cho thấy 117 người trong số 484 người ở trường X học tiếp sau khi tốt nghiệp. Câu hỏi: với α = 0.05, đưa ra kết luận về phát biểu trước đó.

Giải:

H0: P0 = 0.5 (1 nửa)

Ta có P mũ = 117/484 = 0.24. Test Statistic Z0 = -11.44 .

α = 0.05 => Zα/2 = Z0.025 = 1.96. Mà |Z0| = 11.44 > 1.96, nằm ngoài khoảng tin cậy nên ta reject H0.