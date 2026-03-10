### 2.1 Sample spaces and events (Không gian mẫu và biến cố)

Random experiment: là một thực nghiệm để dẫn tới những kết quả khả thi

Ví dụ:

Ramdom experiment: tung 1 đồng xu

Outcomes (kết quả): xấp hoặc ngửa

Sample space: Không gian mẫu, chứa tất cả những kết quả có khả năng xảy ra, kí hiệu là S.

Ví dụ: tung đồng xu 2 lần

S = {xấp xấp, xấp ngửa, ngửa ngửa, ngửa xấp}

### Tree diagram (biểu đồ cây)

Không gian mẫu có thể được biểu diễn dạng biểu đồ cây

Ví dụ: tung 1 đồng xu sau đó tung tiếp 1 cái xúc xắc, tất cả trường hợp khả dĩ:

![](https://sondeptraicbg.github.io/lrn/img/treediagram.png)

Event (biến cố): tập con của không gian mẫu

Ví dụ: tung 1 đồng xu 3 lần, biến cố là đúng 2 lần ra mặt sấp, tính xác suất

Union (hợp) của A và B: A ∪ B, đúng khi nằm trong A hoặc B hoặc cả hai

Intersection (giao) của A và B: A ∩ B, đúng khi nằm trong cả hai

Complement (đối) của A: A', ngược lại với A

### Counting techniques (Kĩ thuật đếm)

Multiplication Rule (quy tắc nhân):

Nếu quá trình cần k bước, bước 1 có n1 cách, bước 2 có n2 cách, ... thì số cách để đi đến kết thúc: n1 x n2 x ... x nk

Permutations (hoán vị):

Số lượng hoán vị là chính là chỉnh hợp, số cách chọn r phần tử từ n phần tử và có sắp xếp, ví dụ như chọn từ 3 người A, B, C sẽ có các cách là: ABC, ACB, BAC, BCA, CAB, CBA. Công thức số cách: nPr (casio).

Combination (tổ hợp):

Rất quen thuộc, số cách chọn r phần tử từ n phần tử và không theo thứ tự, ví dụ như chọn 2 người từ 3 người A, B, C là: A và B, B và C, C và A. Công thức số cách: nCr (casio).

### 2.2 Probability (xác xuất)

Trong một không gian mẫu có n khả năng xảy xa, xác xuất để xảy ra biến cố trong một phép thử là như nhau thì xác xuất mỗi cái đều là 1/n. Ví dụ như tung xúc xắc 1 lần thì khả năng xảy ra mặt 1, 2, 3, 4, 5, 6 là như nhau xác xuất đều là 1/6.

0 ≤ P(A) ≤ 1

- likely
    
    P(A)= 1 /Certain event
    
    P(A) = 0.5
    

Mutually Exclusive Events (biến cố xung khắc): Là các biến cố không thể đồng thời xảy ra, A ∩ B = ∅. Ví dụ như tung xúc xắc, không thể đồng thời ra mặt 1 hoặc 2.

### 2.3 Addition Rules (quy tắc cộng)

P/S: không nên cố nhớ những công thức này, tự vẽ sơ đồ ven sẽ dễ hiểu hơn rất nhiều, tự vẽ ra đi?

P(A ∪ B) = P(A) + P(B) − P(A ∩ B)

if A ∩ B = **∅ (disjoint, mutually exclusive) then P(A**∪ B)= P(A) + P(B)

P(A ∪ B ∪ C) = P(A) + P(B) + P(C) − P(A ∩ B) − P(A ∩ C) − P(B ∩ C) + P(A ∩ B ∩ C)

Nếu A và B xung khắc: P(A ∪ B) = P(A) + P(B)

note: P(A') = 1 - P(A)

### 2.4 Conditional Probability (xác suất có điều kiện)

Xác suất để xảy ra B với điều kiện A, tức là xác suất xảy ra B khi mà A đã thỏa mãn. Kí hiệu P(B|A) : IF/GIVEN THAT

$$ P(B|A) = \frac{P(A \cap B)}{P(A)} $$

Ví dụ xác suất 1 người béo phì(A) là 30%, 1 người tiểu đường(B) là 3%, 1 người béo phì hoặc tiểu đường(A ∪ B) là 31%. Tính xác xuất người bị tiểu đường khi đã béo phì.

Ta thấy P(A U B) = 31% = 0.31.

=> P(A ∩ B) = 0.02 (công thức bên trên, nhưng vẽ biểu đồ ven là thấy ngay)

=> P(B|A) = P(A ∩ B)/P(A) = 0.02/0.3

### 2.5 Multiplication and Total Probability Rules (xác suất tổng)

Multiplication Rule (quy tắc nhân) :

P(A ∩ B) = P(A)P(B|A) = P(B)P(A|B)

P(A ∩ B) = P(A)P(B|A)

note: cái này cũng vẽ biểu đồ ven ra, không thì nhiều người dễ lú

Total Probability Rule (quy tắc tổng xác suất, hình 1)

P(B) = P(A)P(B|A) + P(A')P(B|A')

![](https://sondeptraicbg.github.io/lrn/img/total.png)

Các biến cố E1, E2, . . . , Ek gọi là exhaustive nếu: **mutually exclusive and complementary events**

E1 ∪ E2 ∪ . . . ∪ Ek = S

Total Probability Rule (quy tắc tổng xác suất)

E1, E2, ... Ek là xung khắc và exhaustive (hình 2) thì:

P(B) = P(E1)P(B|E1) + P(E2)P(B|E2) + . . . + P(Ek )P(B|Ek)

### 2.6 Independence (sự độc lập)

2 biến cố A và B độc lập nếu 1 trong các điều sau đúng:

(1) P(A|B) = P(A)

(2) P(B|A) = P(B)

(3) P(A ∩ B) = P(A)P(B)

note: nếu test 2 biến cố có độc lập hay không thường dùng cách 3.

### 2.7 Bayes’ Theorem (định lý Bayes)

E1, E2, ... Ek là xung khắc và exhaustive, B là một biến cố bất kì:

$$ P(E_i | B) = \frac{P(E_i) P(B | E_i)}{P(E_1) P(B | E_1) + P(E_2) P(B | E_2) + \dots + P(E_k) P(B | E_k)}

$$

$$ \text{ for } P(B) > 0. $$

Note:

$$ P(E_i | B) = \frac{P(E_i) P(B | E_i)}{P(B)} $$

Thực ra trông loằng ngoằng nhưng nó chính chính là chỗ quy tắc tổng xác suất phần 2.5 .

### 2.7 Ramdom variable (biến ngẫu nhiên)

Discrete random variable là biến rời rạc, hữu hạn hoặc vô hạn đếm được, như số lượng, ... .

Continuous random variable là biến liên tục, không đếm được, như số đo, ... .