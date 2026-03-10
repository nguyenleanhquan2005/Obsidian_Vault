## (Biến ngẫu nhiên rời rạc và phân bố xác suất)

### 3.1 Discrete Random Variables (biến ngẫu nhiên rời rạc)

Định nghĩa: Biến rời rạc là biến hữu hạn hoặc vô hạn đếm được. vd: số lượng người, lượng trộm chó, ... .

### 3.2 Probability distributions and Probability Mass Functions

### (Phân bố xác suất và hàm khối lượng xác suất)

Định nghĩa: Probability distributions (phân bố xác suất) là bảng, công thức hay biểu đồ, nó biểu diễn xác xuất theo các giá trị của biến cố.

![](https://sondeptraicbg.github.io/lrn/img/probabilitydis.png)

VD: tung 1 đồng xu 4 lần, X biểu diễn cho số mặt chẵn xuất hiện, vậy nên X có thể nhận các giá trị là 0, 1, 2, 3, 4, sẽ được điền vào hàng X, còn hàng P tự tính.

Note:

+, pi= P(X=x), có nghĩa là p1= P(X=1): xác suất để x=1, ...

+, p1 + p2 + p3 + ... pn = 1

Probability Mass Function (hàm khối lượng xác suất)

f(xi) = P(X=xi) với mọi i = 1, 2, ... n

+, f(xi) >= 0 với mọi i = 1, 2, ... n.

+, f(x1) + f(x2) + ... + f(xn) = 1

Đây là f(x), tổng xác suất của tất cả các trường hợp xảy ra phải = 1, và không có chuyện xác suất của 1 biến cố < 0 bởi vì nó không thể xảy ra thì = 0, không thì > 0.

### 3.3 Cumulative Distribution Function

### (Hàm phân bố tích lũy)

Còn cái này là F(x), nhiều người đôi lúc nhầm giữa 2 cái F này. Hàm F(x):

![](https://sondeptraicbg.github.io/lrn/img/cumulativedis.png)

Ta thấy nó gọi là tích lũy, bởi vì nó là tổng của tất cả xác suất từ giá trị nhỏ nhất đến giá trị của x mà ta đang tính. Về mặt toán học, nó giống như tích phân từ hàm nhỏ vậy. Sau này học sang biến liên tục ta sẽ thấy rõ nét hơn về điều này.

### 3.4 Mean and Variance of a Discrete Random Variable

### (Kỳ vọng và phương sai trong biến ngẫu nhiên rời rạc)

Từ đây, ta sẽ được tiếp cận với một số khái niệm mới sẽ đi suốt từ đây đến hết môn.

Ta có : Cho X là biến ngẫu nhiên rời rạc với các giá trị khả dĩ x1, x2, x3, ... xn. Sau đây sẽ là các giá trị của X :

- Đầu tiên, Mean, còn gọi là Expected value, là giá trị kỳ vọng của dữ liệu. Ký hiệu là μ hoặc E(X) :

![](https://sondeptraicbg.github.io/lrn/img/mean.png)

- Tiếp theo, Variance, gọi là phương sai, chúng ta có thể ngầm hiều đó là giá trị trung bình của tổng bình phương sai số của dữ liệu. Ký hiệu là σ² hoặc V(X) :

![](https://sondeptraicbg.github.io/lrn/img/variance.png)

(Tính tay thì dùng công thức cuối)

- Cuối cùng, Standard deviation, gọi là độ lệch chuẩn, lệch tức là sai số, chúng ta hiểu rằng trên kia là tổng của bình phương, vậy cái này sẽ là căn của cái trên kia là xong

![](https://sondeptraicbg.github.io/lrn/img/standarddeviation.png)

- Ngoài ra, nếu áp dụng cho 1 hàm của X, thì mean của hàm đó sẽ là:

![](https://sondeptraicbg.github.io/lrn/img/meanoffunction.png)

### 3.5 Discrete Uniform Distribution

### (Phân bố đồng đều rời rạc)

Phần này khá dễ, nên học hiểu, không hiểu được thì tạch môn.

Một biến ngẫu nhiên X có phân phối đều rời rạc nếu mỗi n giá trị trong khoảng của nó, chẳng hạn, x1, x2, . . . , xn , có xác suất bằng nhau.

![](https://sondeptraicbg.github.io/lrn/img/uniformdiscrete.png)

Nếu biến rời rạc phân bố đồng đều và là các số nguyên liên tiếp : a, a+1, a+2, ... b. Ta có mean và variance :

![](https://sondeptraicbg.github.io/lrn/img/meanuniformdis.png)

### 3.6 Binomial Distribution

### (Phân phối nhị thức)

Bài này bao gồm n phép thử, mỗi phép thử đều độc lập và không liên quan đến nhau. Mỗi phép thử có 2 khả năng là “success” và “failure”. Và xác suất vào “success” trong mỗi phép thử là p.

- **Binomial X ~ B (n,p)**
    
    n trials independent
    
    - each trial:
        
        success p
        
        failure q = 1- p
        

VD: Mỗi ngày bạn đều đánh đề, mỗi lần đánh bạn sẽ có cơ hội là thắng(“success”) hoặc thua(“failure”). Như bạn thấy, mỗi hôm đánh đề chả liên quan gì đến nhau nên người ta gọi đó là độc lập. Bạn nợ môn và về nhà 30 ngày để đánh đề, vậy n = 30, Và mỗi lần đánh, bạn có xác suất thắng là p = 1/100. Như bạn thấy dạng này sẽ có 2 thông số là n và p.

Công thức xác suất cho x lần bạn có được “success” trong n lần thử là :

![](https://sondeptraicbg.github.io/lrn/img/binorminalDis.png)

Hơi dài dòng, nhưng thực ra nó đơn giản và nếu hiểu thì không cần nhớ công thức. Nó có nghĩa là trong n phép thử, ta có thể chọn ra x lần để “success” là nCx (tổ hợp), và vì mỗi lần “success” thì có xác suất là p nên ta có p^x, còn lại n-x lần “failure” thì là (1-p)^(n-x).

Mean và variance của Binomial Distribution:

![](https://sondeptraicbg.github.io/lrn/img/binormialMean.png)

### 3.7 Geometric and Negative Binomial Distribution

### (Đ biết dịch như nào nên ace cố nhớ tên tiếng anh nhé)

Dạng bài này cũng như dạng trên, nhưng chỉ có thông số p và tính chất bài toán nó hơi khác 1 chút.

Geometric Distribution:

Lấy ví dụ đánh đề lúc nãy: mỗi ngày bạn đều đánh đề, mỗi lần đánh bạn sẽ có cơ hội là thắng(“success”) hoặc thua(“failure”). bạn thấy rằng mỗi hôm đánh đề chả liên quan gì đến nhau, người ta gọi đó là độc lập. Mỗi lần đánh, bạn có xác suất thắng là p = 1/100. Bài toán sẽ là bạn đánh đến bao giờ thắng(lần đầu) thì thôi. Như bạn thấy dạng này sẽ chỉ có 1 thông số p. Bài toán mà thử đến khi đạt được “success” lần đầu thì nó sẽ là phân bố geometric.

trial with the first success

Xác suất để thử đến lần thứ x ta sẽ thu được “success” đầu tiên:

![](https://sondeptraicbg.github.io/lrn/img/geometricP.png)

Giải thích công thức như sau: đến lần thứ x bạn sẽ được “success”, vậy thì ta sẽ có x-1 những lần trước đều ra “failure”, mà mỗi lần “failure” sẽ có xác suất 1-p, suy ra ta có (1-p)^(x-1), sau đó nhân thêm p là xác suất ra “success” tại lần thứ x là xong.

Mean và variance của Geometric Distribution:

![](https://sondeptraicbg.github.io/lrn/img/geometricMean.png)

Negative Binomial Distribution:

Khá giống như bài trên, nhưng mà bài toán sẽ là bạn cần x phép thử để thu được r “success” . Tất nhiên là phép thử cuối sẽ là “success” vì khi thu được r “success” thì ta sẽ dừng luôn, và r phải nhỏ hơn hoặc bằng x.

trials until rth success

Xác suất để cần x phép thử ta thu được r “success”:

![](https://sondeptraicbg.github.io/lrn/img/negativeP.png)

Giải thích công thức: Trong x phép thử, sẽ có r lần là “success”, nhưng vì phép thử cuối chắc chắn “success” nên ta chỉ xét x-1 phép thử trước đó và trong x-1 phép thử đó có r-1 lần “success”, vậy ta sẽ có (x-1)C(r-1) (tổ hợp chập r-1 của x-1), rồi nhân với (1-p)^(x-r) vì có tổng cộng x-r lần là “failure”, cuối cùng nhân với p^r vì tổng cộng r lần “success”.

Mean và variance của Negative Binormial Distribution:

![](https://sondeptraicbg.github.io/lrn/img/negativeMean.png)

### 3.8 Hypergeometric Distribution

Cho N cái, trong đó có K là “success”, N-K cái là “failure”. Bài toán là lấy n cái từ trong đó, và trong n chứa x “success”., Xác suất để có điều đó là:

- Hypergeometric distribution: phân phối siêu bội
    
    n trials not independent
    
    - each trial
        
        success p
        
        failure q = 1-p
        

![](https://sondeptraicbg.github.io/lrn/img/hypogeometricP.png)

Giải thích: Tử số sẽ là số cách chọn ra n cái, trong đó có chứa x “success” từ K cái “success” là KCx (tổ hợp chập x của K), và lấy n-x trong N-K cái là “failure” là (N-K)C(n-x) (tổ hợp chập n-x của N-K), nhân 2 thứ đó ta được số cách chọn thỏa mãn. Mẫu số là tổng số cách chọn ra n cái từ N cái ban đầu. Vậy số cách chọn thỏa mãn chia cho tổng tố cách chọn ta có xác suất.

Mean và variance của Hypergeometric Distribution:

![](https://sondeptraicbg.github.io/lrn/img/hypogeometricMean.png)

### 3.9 Poisson Distribution

Đây là loại phân bố trên không gian hay thời gian, có một thông số duy nhất là λ. Thể hiện cho λ cái gì đấy trên một khoảng không gian hay thời gian nào đó. Ví dụ như trung bình bạn có 5 cuộc gọi trên 1 ngày thì tức là λ = 5.

Chú ý một điều là đơn vị của khoảng không gian/ thời gian kia giữa đề với câu hỏi phải bằng nhau, nếu không thì ta phải tự quy đổi. Ví dụ như đề cho 5 cuộc gọi / 1 ngày, mà câu hỏi là tính xác suất để có 8 cuộc gọi/ 2 ngày thì lúc này λ = 10, bởi ta phải đổi sang là có trung bình 10 cuộc gọi / 2 ngày

Xác suất để có x cái / 1 khoảng là:

![](https://sondeptraicbg.github.io/lrn/img/possionP.png)

Mean và variance của Poisson Distribution:

![](https://sondeptraicbg.github.io/lrn/img/possionMean.png)

Riêng Poisson thì 2 cái này bằng nhau nhé!