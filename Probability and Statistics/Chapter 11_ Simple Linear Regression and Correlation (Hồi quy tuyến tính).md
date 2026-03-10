Nếu chỉ học qua môn thì gần như không cần học sâu chương này (Với điều kiện những chương trước đã khá vững :D).

The error in simple linear regression model is a random variable with mean 0

### 11.1 Empirical Models (Mô hình thực nghiệm)

Chúng ta sẽ có 2 cái dữ liệu khác nhau, và ta xem chúng ta xem chúng có mối liên hệ chặt chẽ với nhau không. Vậy ta sẽ lập 1 phương trình tuyến tính giữa 2 cái dữ liệu này, xem có thể dự báo trước giá trị của biến này theo biến kia hay không. Biến cần dự đoán là dependent variable và biến mà mình dùng nó để suy ra biến kia là independent variables.

Ví dụ: cho 1 tập các dữ liệu về nhiệt độ ban ngày ở HN, và 1 tập các dữ liệu về các mặt đường bị rạn nứt và tất nhiên 2 tập này phải liên kết từng cặp với nhau, rồi lập ra một phương trình tuyến tính giữa 2 thứ đó. Khi này nếu như ta thấy nó có mối tương quan lớn thì sau đó ta có thể dự đoán về số vết nứt nhờ vào nhiệt độ. Và nhiệt độ ở HN là independent variable và số vết nứt là dependent variable

Linear Regression function (hồi quy tuyến tính) là hàm khi xây dựng mối tương quan giữa 2 dữ liệu kia :

![](https://sondeptraicbg.github.io/lrn/img/1111.png)

Thực ra công thức trên chả khác gì Y = a.X + b, nhưng viết khác bởi nó có các mục đích khác nhau.

### 11.2 Simple Linear Regression

Có n cặp dữ liệu:

![](https://sondeptraicbg.github.io/lrn/img/1121.png)

Từ các cặp dữ liệu trên, ta vẽ ra hàm tuyến tính như ở phần 11.1 sao cho nó là "best fit" với các dữ liệu. Và chúng ta dùng phương pháp đó là method of least squares, tức là tối thiểu hóa tổng bình phương các sai số(ε). Để dễ hiểu hơn, bạn thấy ta có phương trình hồi quy như ở 11.1, nhưng rõ ràng ta không thể tính giá trị của yi bằng cách gán xi như các bài toàn bình thường bởi vì luôn có sai số:

![](https://sondeptraicbg.github.io/lrn/img/1122.png)

Vì vậy, với sai số là ε, thì mỗi yi ta sẽ có :

![](https://sondeptraicbg.github.io/lrn/img/1123.png)

Do đó, tổng bình phương sai số được nhắc ở trên là :

![](https://sondeptraicbg.github.io/lrn/img/1124.png)

Note: Trên thực tế, ta không có hàm hồi quy cho toàn bộ dữ liệu được nên ta chỉ ước tính nó bằng những dữ liệu mà ta có sẵn, Và từ trước đến giờ mình chỉ đang giới thiệu về lí thuyết, các bạn không cần nhớ các công thức ở trên nhưng phải hiểu. Và về sau các công thức cũng giống nhưng kí hiệu khác, bởi vì trên là các công thức cho tổng thể, mà ta chỉ tính trên các dữ liệu có sẵn (sample) thôi.

Các tham số trong phương trình hồi quy tuyến tính đó là:

![](https://sondeptraicbg.github.io/lrn/img/1125.png)

với :

![](https://sondeptraicbg.github.io/lrn/img/1126.png)

Và từ đó, ta có estimated linear regression line:

![](https://sondeptraicbg.github.io/lrn/img/1128.png)

Sai số residual (giống ε của tổng thể):

![](https://sondeptraicbg.github.io/lrn/img/1129.png)

Tổng bình phương các residual ei là error sum of squares:

![](https://sondeptraicbg.github.io/lrn/img/11210.png)

Từ đó, ta có công thức tính ước tính của σ² :

![](https://sondeptraicbg.github.io/lrn/img/11211.png)

Sợ nhiều người lú, thì thực ra phần này chỉ gói gọn rằng:

- Hồi quy tuyến tính (Regression line):

![](https://sondeptraicbg.github.io/lrn/img/1128.png)

- Residual (kiểu sai số, độ lệch):

![](https://sondeptraicbg.github.io/lrn/img/1129.png)

- Phương sai, tổng bình phương các độ lệch:

![](https://sondeptraicbg.github.io/lrn/img/11211.png)

Trên đó là các tham số mấu chốt, còn tính thế nào thì các bạn phải hiểu nó đặc trưng cho cái gì.

### 11.3 Properties of the Least Squares Estimators (Các ước tính)

estimated standard error of the slope (ước tính sai số của slope) và estimated standard error of the intercept(ước tính sai số của intercept):

![](https://sondeptraicbg.github.io/lrn/img/1131.png)

### 11.4 Hypothesis Tests in Simple Linear Regression (Kiểm định H0 trên hồi quy tuyến tính)

### Test trên Slope

Hypotheses:

![](https://sondeptraicbg.github.io/lrn/img/1141.png)

Nếu đã hiểu về phần kiểm định H0 rồi thì phần này cũng sẽ không xa lạ gì, cũng chỉ là kiểm định về một cái phát biểu bằng cách tính test statistic rồi so sánh với biên rồi kết luận.

Test statistic:

![](https://sondeptraicbg.github.io/lrn/img/1142.png)

Reject H0 nếu :

![](https://sondeptraicbg.github.io/lrn/img/1144.png)

(Nhớ là n − 2 degrees of freedom.)

### Trường hợp đặc biệt:

![](https://sondeptraicbg.github.io/lrn/img/1145.png)

Nếu Failure to reject H0, tức β1 = 0 thì sẽ không có mối quan hệ giữa X và Y.

### Test trên Intercept

Hypotheses:

![](https://sondeptraicbg.github.io/lrn/img/1146.png)

Test statistic:

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/d4f30e5b-760a-413c-a21a-a24af71087d9/53225e2d-b713-467a-bb9a-9c2700827f87/image.png)

Reject H0 nếu :

![](https://sondeptraicbg.github.io/lrn/img/1144.png)

(Nhớ là n − 2 degrees of freedom.)

### 11.8 Correlation (Hệ số tương quan)

Hệ số tương quan của X và Y là ρ, nhưng với sample, nó sẽ là:

![](https://sondeptraicbg.github.io/lrn/img/1182.png)

Note:

.) −1 ≤ r ≤ 1.

.) Nó đặc trưng cho mối liên hệ giữa 2 dữ liệu đó

.) r và β1 có cùng dấu

.) r² gọi là coefficient of determination (hệ số xác định)

![](https://sondeptraicbg.github.io/lrn/img/1184.png)

Như vậy, r càng tiến về 0 thì mối liên hệ giữa X và Y càng thấp, và ngược lại.

### Test Hypotheses about the Correlation Coefficient

Hypotheses:

![](https://sondeptraicbg.github.io/lrn/img/1185.png)

Test statistic:

![](https://sondeptraicbg.github.io/lrn/img/1186.png)

Reject H0 nếu :

![](https://sondeptraicbg.github.io/lrn/img/1144.png)