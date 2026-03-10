- Data description
    
    measure central tendency ( tập trung)
    
    measure variation ( phân tán)
    
    distribution ( symmetric, …)
    
- measure central tendency
    
    mean population
    
    - sample(n)
        
        **Sample Size**
        
        : The number of observations or data points in a sample.
        
        - **Cỡ mẫu**: Số lượng cá thể được đưa vào mẫu nghiên cứu sao cho chúng ta có thể ngoại suy từ các đặc điểm của mẫu ra các đặc điểm tương ứng của quần thể (Statistical inference)
    
    median sorted data ( trung vị)
    
    mode
    
    - **Range**: The difference between the largest and smallest values in a data set.
    - **Khoảng**: Sự chênh lệch giữa giá trị lớn nhất và nhỏ nhất trong một tập dữ liệu

### 6.1 Numerical Summaries of Data

Ta có n observations(quan sát) trong sample là x1, x2, x3, ... xn.

Sample mean:

![](https://sondeptraicbg.github.io/lrn/img/611.png)

Kỳ vọng của sample đơn giản là trung bình của các giá trị.

Sample variance:

![](https://sondeptraicbg.github.io/lrn/img/612.png)

Phương sai là tổng bình phương sai số chia cho n-1. Nhưng ấn được máy tính nên không cần nhớ cái cồng kềnh này nhé.

Sample standard deviation ký hiệu là s.

Sample range :

![](https://sondeptraicbg.github.io/lrn/img/613.png)

### 6.2 Stem-and-Leaf Diagrams

Khi có nhiều dữ liệu, họ sẽ chia thành cài bảng này cho dễ nhìn hơn. VD:

![](https://sondeptraicbg.github.io/lrn/img/621.png)

Giải: Dữ liệu mà ta có sẽ là : 101, 105, 110, 115, 118, .... . Nói chung là cột 'leaf' thì là 1 chữ số, sau đó nối với bên 'stem'.

- sample median (khác với sample mean) là giá trị nằm giữa của các dữ liệu này. Nếu dữ liệu có n số thì sample median sẽ là số thứ (n+1)/2. nếu (n+1)/2 mà ra dạng x,5 thì sample median sẽ = trung bình số thứ x và số thứ x+1.

VD1: cho sample: 1, 3, 5, 6, 8, 9, 10.

Giải: Số số hạng là n=7, vậy thì (n+1)/2 = 4 suy ra sample median = số thứ 4 là 6.

VD2: cho sample: 2, 3, 4, 6, 7, 8.

Giải: Số số hạng là n=6, vậy thì (n+1)/2 = 3.5 suy ra sample median = trung bình số thứ 3 và thứ 4 là (4+6)/2 = 5.

- sample mode là giá trị xuất hiện nhiều nhất, nếu tất cả các số đều có số lượng như nhau thì không có sample mode
- Quartiles:

Ta chia data thành 4 phần bằng nhau thì đó gọi là Quartiles, có 3 điểm là q1, q2 (chính là median), q3. Xấp xỉ 25% số lượng observations ở dưới q1, 50% dưới q2 và 75% dưới q3. Cách tính q1: số thứ (1+n)/4 , nếu ra .5 thì lấy 2 số gần đó nhất chia trung bình

Cách tính q2: là median.

Cách tính q3: số thứ (1+n) x 3/4 , nếu ra .5 thì lấy 2 số gần đó nhất chia trung bình

- interquartile range: IQR = q3-q1.

### 6.3 Frequency Distributions and Histograms (Kiểu theo tần số, số lần xuất hiện hay tỉ lệ ấy)

Relative frequency distribution Ví dụ:

![](https://sondeptraicbg.github.io/lrn/img/631.png)

Cumulative frequency distribution ví dụ:

![](https://sondeptraicbg.github.io/lrn/img/632.png)

Nhớ lại: Cumulative là tích lũy, nó sẽ bằng tổng từ cái nhỏ nhất đến nó.

Histogram ví dụ:

![](https://sondeptraicbg.github.io/lrn/img/633.png)

### 6.4 Box plot

Như phần 6.2, bạn đã biết được p1, p2, p3 là gì rồi. Và giờ ta dùng chúng để kiểu sàng lọc những phần tử quá khác biệt vậy. Box plot có 2 đầu mút. Bây giờ tính q3 + 1.5IQR, rồi lấy số lớn nhất trong data mà nhỏ hơn giá trị đấy làm đầu mút trên, sau đó tính q1-1.5IQR, lấy số nhỏ nhất trong data mà lớn hơn số đấy làm đầu mút dưới, vậy là đã có box plot, nếu trong data có số nào không nằm trong đó thì gọi là outlier.

![](https://sondeptraicbg.github.io/lrn/img/641.png)