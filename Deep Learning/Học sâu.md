**  

# Đề Cương Ôn Tập Toàn Diện về Học Sâu


## Lời nói đầu

  

Học Sâu (Deep Learning), một nhánh của Học Máy (Machine Learning), đã tạo nên một cuộc cách mạng trong lĩnh vực trí tuệ nhân tạo, mang lại những đột phá ngoạn mục trong các bài toán từ nhận dạng hình ảnh, xử lý ngôn ngữ tự nhiên đến xe tự lái và chẩn đoán y khoa.1 Sức mạnh của học sâu nằm ở khả năng tự động học các biểu diễn phân cấp và trừu tượng từ dữ liệu thô, mô phỏng một cách lỏng lẻo cách bộ não con người xử lý thông tin.3

Đề cương này được biên soạn với mục tiêu cung cấp một lộ trình ôn tập toàn diện, có hệ thống và chuyên sâu về Học Sâu. Nội dung không chỉ dừng lại ở việc liệt kê các công thức và kiến trúc, mà còn tập trung vào việc phân tích "câu chuyện" đằng sau sự phát triển của lĩnh vực này: những vấn đề đã thúc đẩy sự ra đời của các kỹ thuật mới, mối liên hệ nhân quả giữa các ý tưởng, và các chiến lược thực tiễn để xây dựng và tối ưu hóa các hệ thống học máy hiệu quả.2

Đề cương được cấu trúc thành các phần chính, bắt đầu từ những viên gạch nền tảng nhất của mạng nơ-ron, đi sâu vào các kỹ thuật tối ưu hóa và điều chuẩn, khám phá các kiến trúc chuyên biệt cho thị giác máy tính và xử lý chuỗi, và cuối cùng là các chiến lược thực hành để quản lý một dự án học máy thành công. Mỗi chương sẽ làm sáng tỏ các khái niệm cốt lõi, phân tích các bài báo khoa học có ảnh hưởng, và cung cấp những góc nhìn sâu sắc để giúp người học không chỉ "biết cái gì" mà còn "hiểu tại sao".

---

## Phần I: Nền tảng của Mạng Nơ-ron

  

Phần này đặt nền móng cho toàn bộ lĩnh vực, giải thích các khái niệm cơ bản nhất mà mọi mô hình học sâu đều được xây dựng dựa trên. Việc nắm vững các nguyên tắc này là điều kiện tiên quyết để hiểu được các kiến trúc phức tạp hơn sau này.

  

### Chương 1: Từ Hồi quy Logistic đến Mạng Nơ-ron

  

Để hiểu được các mạng nơ-ron phức tạp với hàng trăm lớp, điều quan trọng là phải bắt đầu từ đơn vị cấu thành đơn giản nhất. Đơn vị này, về bản chất, chính là mô hình hồi quy logistic, một thuật toán quen thuộc trong học máy cổ điển.

  

#### Phân loại Nhị phân và Hồi quy Logistic

  

Bài toán cơ bản nhất trong học máy có giám sát là phân loại nhị phân (binary classification), nơi mục tiêu là phân loại đầu vào vào một trong hai lớp. Ví dụ kinh điển là xác định một hình ảnh chứa "mèo" (lớp 1) hay "không phải mèo" (lớp 0).2 Thuật toán tiêu chuẩn để giải quyết bài toán này là hồi quy logistic.2

Cơ chế của hồi quy logistic bao gồm hai bước tính toán chính. Đầu tiên, nó tính toán một tổ hợp tuyến tính của các đặc trưng đầu vào x với các tham số trọng số w và thiên vị b 2:

$$
z=wTx+b
$$

  

Sau đó, kết quả z được đưa qua một hàm kích hoạt phi tuyến, gọi là hàm sigmoid (hoặc hàm logistic), để đưa đầu ra về khoảng (0, 1), đại diện cho xác suất của lớp 1 2:

$$
a=σ(z)=1+e−z1​
$$

Giá trị a này, hay ŷ, chính là dự đoán của mô hình.2
#### Hồi quy Logistic như một Mạng Nơ-ron Đơn lớp

Nếu xem xét kỹ hơn, toàn bộ quá trình tính toán của hồi quy logistic có thể được biểu diễn như một nơ-ron nhân tạo duy nhất. Nơ-ron này nhận các đầu vào x, tính toán giá trị z, và áp dụng hàm kích hoạt σ để tạo ra đầu ra a. Do đó, hồi quy logistic có thể được coi là một mạng nơ-ron "nông" nhất có thể, chỉ với một lớp đầu ra chứa một nơ-ron.2

#### Kiến trúc Mạng Nơ-ron

Sức mạnh thực sự của mạng nơ-ron bộc lộ khi chúng ta không chỉ dùng một nơ-ron, mà kết hợp nhiều nơ-ron lại với nhau. Bằng cách xếp chồng nhiều đơn vị tính toán tương tự hồi quy logistic, chúng ta tạo ra một lớp ẩn (hidden layer). Một mạng nơ-ron nông đơn giản bao gồm ba thành phần 2:

1. Lớp đầu vào (Input Layer): Nhận dữ liệu đầu vào x.
    
2. Lớp ẩn (Hidden Layer): Một hoặc nhiều lớp trung gian, mỗi lớp chứa một số lượng nơ-ron nhất định. Các giá trị tính toán trong lớp này không được quan sát trực tiếp từ dữ liệu, do đó có tên là "ẩn".2
    
3. Lớp đầu ra (Output Layer): Lớp cuối cùng tạo ra dự đoán cuối cùng ŷ.
    

Mỗi kết nối giữa các nơ-ron ở các lớp liền kề đều có một trọng số. Tập hợp tất cả các trọng số của một lớp l được biểu diễn bằng ma trận trọng số $W^{[l]}$, và tập hợp các thiên vị được biểu diễn bằng vector $b^{[l]}$.2

Cốt lõi của học sâu nằm ở khả năng tạo ra các biểu diễn ngày càng trừu tượng của dữ liệu qua mỗi lớp. Một nơ-ron đơn lẻ (hồi quy logistic) chỉ có thể học một đường phân cách tuyến tính. Tuy nhiên, bằng cách "xếp chồng" các đơn vị tính toán đơn giản này thành các lớp, và các lớp này lên nhau, mạng nơ-ron có thể học được các hàm vô cùng phức tạp và các đường phân cách phi tuyến tính. Lớp ẩn đầu tiên có thể học các đặc trưng đơn giản (như các cạnh trong ảnh), và các lớp sau đó sẽ kết hợp các đặc trưng này để nhận diện các cấu trúc phức tạp hơn (như mắt, mũi, rồi đến toàn bộ khuôn mặt).2 Đây là tiền đề cho toàn bộ các kiến trúc sâu sau này như VGG hay ResNet. Việc hiểu rằng "độ sâu" cho phép học các mức độ trừu tượng khác nhau là chìa khóa để hiểu tại sao các mạng sâu lại hiệu quả đến vậy.2

  

### Chương 2: Cơ chế Học tập Cốt lõi

  

Quá trình "học" của một mạng nơ-ron thực chất là quá trình điều chỉnh các tham số $W$ và $b$ sao cho dự đoán của mô hình ngày càng gần với nhãn thực tế. Quá trình này được thực hiện thông qua hai cơ chế tính toán trung tâm: lan truyền xuôi và lan truyền ngược.

  

#### Đồ thị Tính toán

  

Để trực quan hóa và hiểu rõ bản chất của hai quá trình này, công cụ đồ thị tính toán (computation graph) là cực kỳ hữu ích. Một đồ thị tính toán biểu diễn bất kỳ hàm số nào dưới dạng một đồ thị có hướng, trong đó các nút là các phép toán hoặc biến. Ví dụ, hàm $J = 3(a + bc)$ có thể được phân rã thành các bước nhỏ hơn: $u = bc$, $v = a + u$, $J = 3v$.2

Dòng chảy tính toán trong đồ thị này diễn ra từ trái sang phải để tính giá trị cuối cùng của $J$. Đây chính là quá trình lan truyền xuôi. Ngược lại, để tính đạo hàm của $J$ đối với các biến đầu vào (a, b, c), chúng ta sẽ đi ngược từ phải sang trái, áp dụng quy tắc chuỗi tại mỗi nút. Đây chính là quá trình lan truyền ngược.2

  

#### Lan truyền Xuôi (Forward Propagation)

  

Lan truyền xuôi là quá trình tính toán đầu ra dự đoán ŷ của mạng từ một đầu vào x. Quá trình này diễn ra tuần tự qua từng lớp của mạng, từ lớp 1 đến lớp cuối cùng L. Tại mỗi lớp l, hai phép tính chính được thực hiện 2:

1. Tính toán tổ hợp tuyến tính: $Z^{[l]} = W^{[l]}A^{[l-1]} + b^{[l]}$
    
2. Áp dụng hàm kích hoạt: $A^{[l]} = g^{[l]}(Z^{[l]})$
    

Trong đó, $A^{[l-1]}$ là đầu ra (kích hoạt) của lớp trước đó, và $A^{}$ chính là dữ liệu đầu vào X. Quá trình này tiếp tục cho đến khi chúng ta có được $A^{[L]}$, chính là dự đoán cuối cùng ŷ của mô hình.2

  

#### Lan truyền Ngược (Backward Propagation)

  

Sau khi có được dự đoán ŷ, chúng ta so sánh nó với nhãn thực tế y thông qua một hàm chi phí (cost function) để đo lường mức độ lỗi. Mục tiêu của việc học là giảm thiểu hàm chi phí này. Để làm được điều đó, chúng ta cần biết mỗi tham số $W^{[l]}$ và $b^{[l]}$ ảnh hưởng đến lỗi cuối cùng như thế nào. Đây là lúc lan truyền ngược phát huy tác dụng.

Lan truyền ngược (backpropagation) là một thuật toán hiệu quả để tính toán đạo hàm (gradient) của hàm chi phí đối với tất cả các tham số trong mạng. Nó hoạt động bằng cách áp dụng quy tắc chuỗi (chain rule) trong giải tích một cách có hệ thống, đi ngược từ lớp cuối cùng về lớp đầu tiên.2

Tại mỗi lớp l, quá trình này tính toán các đạo hàm sau 2:

- $dZ^{[l]}$: Đạo hàm của hàm chi phí đối với $Z^{[l]}$.
    
- $dW^{[l]}$: Đạo hàm của hàm chi phí đối với $W^{[l]}$.
    
- $db^{[l]}$: Đạo hàm của hàm chi phí đối với $b^{[l]}$.
    
- $dA^{[l-1]}$: Đạo hàm của hàm chi phí đối với $A^{[l-1]}$, giá trị này sẽ được truyền về lớp l-1 để tiếp tục quá trình.
    

Việc tính đạo hàm của một hàm chi phí phức tạp đối với hàng triệu tham số có vẻ là một nhiệm vụ bất khả thi. Tuy nhiên, Backpropagation đã biến nó thành một quy trình có thể quản lý được bằng cách áp dụng nguyên tắc "chia để trị". Nó chia nhỏ bài toán lớn thành các bước tính toán đạo hàm cục bộ (local derivative) tại mỗi nút trong đồ thị tính toán. Sau đó, nó sử dụng quy tắc chuỗi để "lan truyền" các gradient này ngược lại qua mạng. Về bản chất, nó tính toán hiệu quả sự đóng góp của mỗi tham số vào lỗi cuối cùng, cho phép chúng ta biết cách điều chỉnh tham số đó để giảm lỗi. Sự hiệu quả của Backpropagation là yếu tố then chốt cho phép huấn luyện các mạng nơ-ron rất sâu. Nếu không có nó, việc tính toán gradient sẽ quá tốn kém, và cuộc cách mạng học sâu có thể đã không xảy ra.2

  

### Chương 3: Các Hàm Kích hoạt và Vai trò của Tính Phi tuyến

  

Các hàm kích hoạt là một thành phần không thể thiếu trong hầu hết các mạng nơ-ron. Chúng được áp dụng cho đầu ra của mỗi nơ-ron và quyết định xem nơ-ron đó có nên được "kích hoạt" hay không.

  

#### Tại sao cần Tính Phi tuyến?

  

Một câu hỏi cơ bản là tại sao chúng ta không thể chỉ xếp chồng các lớp tuyến tính (không có hàm kích hoạt). Câu trả lời nằm ở chỗ, sự kết hợp của hai hàm tuyến tính vẫn là một hàm tuyến tính. Do đó, một mạng nơ-ron dù có bao nhiêu lớp đi chăng nữa, nếu chỉ sử dụng các phép tính tuyến tính, thì về mặt toán học nó chỉ tương đương với một lớp tuyến tính duy nhất. Điều này làm cho các lớp ẩn trở nên hoàn toàn vô dụng và mạng sẽ không thể học được các mối quan hệ phức tạp, phi tuyến tính trong dữ liệu.2 Chính các hàm kích hoạt phi tuyến đã mang lại cho mạng nơ-ron sức mạnh biểu diễn to lớn của chúng.

  

#### Phân tích các Hàm Kích hoạt Phổ biến

  

Sự lựa chọn hàm kích hoạt có ảnh hưởng lớn đến hiệu suất và sự ổn định của mạng. Dưới đây là các hàm phổ biến và sự tiến hóa của chúng:

- Sigmoid: Có công thức $\sigma(z) = 1 / (1 + e^{-z})$. Nó đưa đầu ra về khoảng (0, 1), rất hữu ích cho lớp đầu ra của bài toán phân loại nhị phân để biểu diễn xác suất. Tuy nhiên, nó có hai nhược điểm lớn: (1) Gây ra vấn đề vanishing gradient (gradient biến mất) vì đạo hàm của nó tiến về 0 khi |z| lớn; (2) Đầu ra của nó không được căn giữa quanh 0, có thể làm chậm quá trình học của lớp tiếp theo.2
    
- Tanh (Hyperbolic Tangent): Có công thức $\tanh(z) = (e^z - e^{-z}) / (e^z + e^{-z})$. Nó đưa đầu ra về khoảng (-1, 1). Tanh thường hoạt động tốt hơn Sigmoid cho các lớp ẩn vì đầu ra của nó được căn giữa quanh 0. Tuy nhiên, nó vẫn gặp phải vấn đề vanishing gradient tương tự Sigmoid.2
    
- ReLU (Rectified Linear Unit): Có công thức $\text{ReLU}(z) = \max(0, z)$. Đây là hàm kích hoạt được sử dụng rộng rãi nhất hiện nay cho các lớp ẩn. Ưu điểm của nó là: (1) Rất hiệu quả về mặt tính toán; (2) Không bị bão hòa ở vùng dương, giúp giảm đáng kể vấn đề vanishing gradient. Nhược điểm chính của nó là vấn đề "nơ-ron chết" (dying ReLU), xảy ra khi một nơ-ron có đầu vào luôn âm, khiến gradient của nó luôn bằng 0 và nơ-ron đó ngừng học.2
    
- Leaky ReLU: Có công thức $\text{LeakyReLU}(z) = \max(0.01z, z)$. Đây là một nỗ lực để giải quyết vấn đề "nơ-ron chết" của ReLU. Bằng cách cho phép một độ dốc nhỏ (ví dụ: 0.01) ở vùng âm, nó đảm bảo rằng nơ-ron không bao giờ hoàn toàn "chết" và vẫn có thể học.2
    

Sự tiến hóa của các hàm kích hoạt phản ánh cuộc chiến không ngừng chống lại vấn đề vanishing gradients. Sự chuyển dịch từ Sigmoid/Tanh sang ReLU không phải là ngẫu nhiên. Sigmoid và Tanh có đạo hàm tiến về 0 ở hai đầu, khiến cho gradient bị "triệt tiêu" khi lan truyền ngược qua nhiều lớp. ReLU, với đạo hàm bằng 1 cho tất cả các đầu vào dương, đã tạo ra một "đường cao tốc" cho gradient, cho phép huấn luyện các mạng sâu hơn nhiều một cách hiệu quả. Leaky ReLU và các biến thể khác là những nỗ lực tiếp theo để hoàn thiện hơn nữa, giải quyết nhược điểm của ReLU. Vấn đề vanishing gradient này sẽ quay trở lại một cách nghiêm trọng hơn trong các mạng RNN và là động lực chính cho sự ra đời của LSTM/GRU và ResNet.2

  

### Chương 4: Tối ưu hóa với Gradient Descent

  

Sau khi tính toán được các gradient thông qua lan truyền ngược, bước tiếp theo là sử dụng chúng để cập nhật các tham số của mô hình. Thuật toán làm điều này được gọi là Gradient Descent.

  

#### Hàm Mất mát và Hàm Chi phí

  

Trước khi tối ưu hóa, chúng ta cần một thước đo để biết mô hình hoạt động tệ đến mức nào.

- Hàm Mất mát (Loss Function): Đo lường lỗi trên một ví dụ huấn luyện duy nhất. Đối với hồi quy logistic, hàm mất mát thường dùng là cross-entropy: $\mathcal{L}(\hat{y}, y) = -(y \log(\hat{y}) + (1-y) \log(1-\hat{y}))$.2
    
- Hàm Chi phí (Cost Function): Là trung bình của hàm mất mát trên toàn bộ tập huấn luyện m mẫu. Nó cho ta một con số duy nhất đại diện cho hiệu suất tổng thể của mô hình trên tập huấn luyện: $J(W, b) = \frac{1}{m} \sum_{i=1}^{m} \mathcal{L}(\hat{y}^{(i)}, y^{(i)})$.2
    

Mục tiêu của quá trình huấn luyện là tìm các giá trị của $W$ và $b$ để tối thiểu hóa hàm chi phí $J(W, b)$.

  

#### Trực giác về Gradient Descent

  

Hãy tưởng tượng hàm chi phí $J$ là một bề mặt địa hình lồi lõm trong không gian nhiều chiều. Nhiệm vụ của chúng ta là tìm điểm thấp nhất trên bề mặt này. Gradient Descent là một thuật toán đơn giản để làm điều đó: tại bất kỳ điểm nào trên bề mặt, chúng ta xác định hướng dốc nhất đi xuống (hướng ngược lại của gradient) và đi một bước nhỏ theo hướng đó. Lặp lại quá trình này nhiều lần, chúng ta sẽ dần dần tiến đến một điểm cực tiểu.2

Công thức cập nhật cho mỗi tham số trong mỗi lần lặp là 2:

$$
W:=W−α⋅dWb:=b−α⋅db
$$

  

Trong đó $dW$ và $db$ là các gradient được tính từ backpropagation, và $\alpha$ là tốc độ học (learning rate), một siêu tham số quyết định kích thước của mỗi bước đi.

Gradient Descent là một thuật toán "tham lam" cục bộ. Nó chỉ nhìn vào độ dốc "ngay tại đây" để quyết định bước đi tiếp theo mà không có cái nhìn toàn cục về bề mặt của hàm chi phí. Điều này làm cho nó dễ bị mắc kẹt ở các điểm cực tiểu cục bộ (mặc dù trong không gian nhiều chiều, đây ít là vấn đề hơn so với các điểm yên ngựa).2 Do đó, việc lựa chọn tốc độ học

$\alpha$ trở nên cực kỳ quan trọng. Nếu $\alpha$ quá nhỏ, quá trình hội tụ sẽ rất chậm. Nếu $\alpha$ quá lớn, nó có thể "vọt qua" điểm tối ưu và thậm chí làm cho hàm chi phí phân kỳ. Đây là lý do tại sao các thuật toán tối ưu hóa nâng cao (Adam, RMSProp) và các kỹ thuật như learning rate decay ra đời - chúng cố gắng tự động điều chỉnh tốc độ học một cách thông minh.2

  

#### Tầm quan trọng của Vectorization

  

Trong các triển khai hiện đại, việc sử dụng các vòng lặp for để lặp qua từng mẫu huấn luyện hoặc từng đặc trưng là cực kỳ không hiệu quả. Thay vào đó, chúng ta sử dụng vectorization, tức là thực hiện các phép toán trên toàn bộ ma trận và vector cùng một lúc. Các thư viện như NumPy được tối ưu hóa cao cho các phép toán này, tận dụng các lệnh song song trên CPU và GPU. Việc chuyển từ vòng lặp for sang các phép toán vector hóa có thể tăng tốc độ huấn luyện lên hàng trăm, thậm chí hàng nghìn lần, điều này là tối quan trọng khi làm việc với các tập dữ liệu lớn.2

  

### Chương 5: Khởi tạo Trọng số và Tầm quan trọng của việc Phá vỡ Đối xứng

  

Cách chúng ta bắt đầu quá trình học – tức là các giá trị ban đầu của các trọng số – có thể quyết định liệu mạng có học được hay không.

  

#### Vấn đề Đối xứng

  

Nếu chúng ta khởi tạo tất cả các trọng số $W$ bằng 0 (hoặc bất kỳ hằng số nào khác), một vấn đề nghiêm trọng sẽ xảy ra. Tất cả các nơ-ron trong cùng một lớp ẩn sẽ có cùng đầu vào và cùng trọng số. Do đó, trong quá trình lan truyền ngược, chúng sẽ nhận được cùng một gradient và được cập nhật theo cùng một cách. Điều này có nghĩa là tất cả các nơ-ron trong lớp sẽ mãi mãi giống hệt nhau và học cùng một đặc trưng. Mạng sẽ không có khả năng học các biểu diễn phức tạp, vì về cơ bản, có $n$ nơ-ron cũng chỉ như có một nơ-ron. Đây được gọi là vấn đề phá vỡ đối xứng (symmetry breaking problem).2

  

#### Phá vỡ Đối xứng bằng Khởi tạo Ngẫu nhiên

  

Giải pháp cho vấn đề này rất đơn giản: chúng ta phải phá vỡ sự đối xứng. Điều này được thực hiện bằng cách khởi tạo các trọng số $W$ bằng các giá trị ngẫu nhiên nhỏ. Bằng cách này, mỗi nơ-ron bắt đầu với một bộ tham số hơi khác nhau, nhận được các gradient khác nhau và sẽ học các đặc trưng khác nhau trong quá trình huấn luyện. Các thiên vị $b$ có thể được khởi tạo bằng 0 vì sự ngẫu nhiên trong $W$ đã đủ để phá vỡ đối xứng.2

Việc khởi tạo trọng số với các giá trị ngẫu nhiên quá lớn cũng là một vấn đề. Nó có thể đẩy đầu vào $z$ của các hàm kích hoạt như sigmoid hoặc tanh vào vùng bão hòa, nơi gradient gần bằng 0. Điều này sẽ làm quá trình học bị đình trệ ngay từ đầu. Do đó, người ta thường nhân các giá trị ngẫu nhiên với một hằng số nhỏ (ví dụ: 0.01).2

Việc khởi tạo tốt đặt nền móng cho một cuộc đua công bằng. Hãy tưởng tượng một cuộc đua ngựa mà tất cả các con ngựa đều bị trói vào nhau. Chúng sẽ không thể chạy hiệu quả. Khởi tạo tất cả trọng số bằng nhau cũng tương tự như vậy. Khởi tạo ngẫu nhiên là việc "cởi trói" cho các nơ-ron, cho phép chúng cạnh tranh và chuyên môn hóa. Hơn nữa, việc khởi tạo đúng cách có liên quan chặt chẽ đến vấn đề vanishing/exploding gradients. Các phương pháp khởi tạo nâng cao hơn như Xavier/Glorot và He initialization được thiết kế một cách toán học để điều chỉnh phương sai của các giá trị khởi tạo dựa trên số lượng nơ-ron đầu vào và đầu ra, nhằm đảm bảo rằng phương sai của các kích hoạt và gradient vẫn ổn định khi chúng lan truyền qua các lớp, ngăn chúng không bị triệt tiêu hoặc bùng nổ.2

---

## Phần II: Tối ưu hóa và Điều chuẩn cho Mạng Sâu

  

Khi các mạng nơ-ron trở nên sâu hơn với hàng chục hoặc hàng trăm lớp, các thách thức trong việc huấn luyện chúng cũng tăng lên. Quá trình tối ưu hóa có thể trở nên rất chậm, không ổn định, và mô hình có nguy cơ cao bị overfitting. Phần này sẽ đi sâu vào các kỹ thuật thực tiễn và các thuật toán nâng cao đã được phát triển để giải quyết những vấn đề này, giúp các mạng sâu học nhanh hơn, ổn định hơn và tổng quát hóa tốt hơn trên dữ liệu mới.

  

### Chương 6: Các Thuật toán Tối ưu hóa Nâng cao

  

Gradient Descent cơ bản, mặc dù là nền tảng, nhưng lại có những hạn chế đáng kể khi áp dụng cho các hàm chi phí phức tạp và các tập dữ liệu khổng lồ của học sâu. Các thuật toán tối ưu hóa nâng cao ra đời để khắc phục những nhược điểm này.

  

#### Mini-batch Gradient Descent

  

Việc tính toán gradient trên toàn bộ tập huấn luyện (Batch Gradient Descent) có thể cực kỳ tốn kém và chậm chạp với hàng triệu mẫu dữ liệu. Ngược lại, việc cập nhật sau mỗi mẫu (Stochastic Gradient Descent) lại rất nhiễu và không tận dụng được lợi thế của vectorization. Mini-batch Gradient Descent là một giải pháp trung hòa, trở thành tiêu chuẩn trong thực tế. Nó chia tập huấn luyện thành các "lô nhỏ" (mini-batches) và thực hiện một bước cập nhật gradient sau khi xử lý mỗi lô.2

Cách tiếp cận này mang lại hai lợi ích chính:

1. Hiệu quả tính toán: Nó cho phép sử dụng vectorization trên một lô nhỏ, tận dụng sức mạnh xử lý song song của GPU/CPU.2
    
2. Hội tụ nhanh hơn: Việc cập nhật tham số diễn ra thường xuyên hơn so với Batch GD, giúp quá trình hội tụ nhanh hơn. Mặc dù đường đi của hàm chi phí sẽ nhiễu hơn so với Batch GD, nhưng nó ít nhiễu hơn đáng kể so với SGD và thường tiến về vùng cực tiểu một cách hiệu quả.2
    

Kích thước của mini-batch là một siêu tham số cần được lựa chọn. Các kích thước phổ biến thường là lũy thừa của 2, chẳng hạn như 64, 128, 256, 512, để phù hợp với kiến trúc bộ nhớ của phần cứng.2 Một

epoch được định nghĩa là một lượt đi qua toàn bộ tập huấn luyện.2

  

#### Gradient Descent with Momentum

  

Một vấn đề phổ biến của Gradient Descent là nó có thể dao động mạnh theo các hướng có độ cong lớn và tiến rất chậm theo các hướng có độ cong nhỏ, giống như một quả bóng lăn xuống một khe núi hẹp. Gradient Descent with Momentum được thiết kế để giải quyết vấn đề này. Ý tưởng cốt lõi là tính toán trung bình có trọng số theo cấp số nhân (Exponentially Weighted Averages - EWA) của các gradient trong quá khứ và sử dụng "đà" này để định hướng cho bước cập nhật hiện tại.2

Công thức cập nhật có thể được viết như sau:

  

$$
VdW​=βVdW​+(1−β)dWW:=W−αVdW​
$$

  

Trong đó $V_{dW}$ là "vận tốc" của gradient, và $\beta$ (thường khoảng 0.9) là siêu tham số kiểm soát mức độ ảnh hưởng của các gradient trong quá khứ. Bằng cách này, các dao động theo các hướng không mong muốn sẽ bị triệt tiêu lẫn nhau, trong khi các bước đi theo hướng hội tụ sẽ được tích lũy và tăng tốc.2

  

#### RMSprop (Root Mean Square Propagation)

  

RMSprop là một thuật toán khác cũng giải quyết vấn đề dao động nhưng theo một cách khác. Nó điều chỉnh tốc độ học cho mỗi tham số một cách độc lập. Ý tưởng là giảm tốc độ học cho các tham số có gradient lớn (thường là các hướng dao động) và tăng tốc độ học cho các tham số có gradient nhỏ (thường là các hướng hội tụ chậm).2

Công thức cập nhật của RMSprop:

  

$$
SdW​=βSdW​+(1−β)(dW)2W:=W−αSdW​​+εdW​
$$

  

Ở đây, $S_{dW}$ là trung bình có trọng số theo cấp số nhân của bình phương các gradient. Bằng cách chia gradient $dW$ cho căn bậc hai của $S_{dW}$, thuật toán đã "làm dịu" các bước cập nhật ở những chiều có gradient lớn và tăng tốc ở những chiều có gradient nhỏ. $\varepsilon$ là một hằng số rất nhỏ để đảm bảo không chia cho 0.2

  

#### Adam (Adaptive Moment Estimation)

  

Adam là thuật toán tối ưu hóa có thể được coi là sự kết hợp những ý tưởng tốt nhất từ cả Momentum và RMSProp. Nó đã trở thành thuật toán mặc định cho hầu hết các bài toán học sâu vì hiệu quả và sự mạnh mẽ của nó.4

Adam lưu giữ cả hai loại trung bình có trọng số theo cấp số nhân:

1. Moment bậc nhất (The first moment): Trung bình của các gradient (giống như Momentum).
    
2. Moment bậc hai (The second moment): Trung bình của bình phương các gradient (giống như RMSprop).
    

Sau đó, nó sử dụng cả hai moment này để điều chỉnh tốc độ học cho từng tham số. Adam cũng bao gồm một bước hiệu chỉnh thiên vị (bias correction) để cải thiện ước tính của các moment ở những bước lặp đầu tiên. Mặc dù có nhiều siêu tham số ($\alpha, \beta_1, \beta_2, \varepsilon$), các giá trị mặc định được đề xuất (ví dụ: $\beta_1 = 0.9, \beta_2 = 0.999, \varepsilon = 10^{-8}$) hoạt động tốt một cách đáng kinh ngạc trên nhiều loại bài toán, giúp người thực hành chỉ cần tập trung vào việc tinh chỉnh tốc độ học $\alpha$.2

Sự tiến hóa từ Gradient Descent cơ bản đến Adam có thể được xem như một hành trình hướng tới việc tự động hóa quá trình tối ưu hóa. Các thuật toán này ngày càng thông minh hơn trong việc tự điều chỉnh các bước đi của mình, giảm bớt gánh nặng tinh chỉnh thủ công và cho phép các mạng sâu phức tạp được huấn luyện một cách hiệu quả và đáng tin cậy.

  

#### Learning Rate Decay

  

Một chiến lược phổ biến khác để cải thiện sự hội tụ là giảm dần tốc độ học (learning rate decay) theo thời gian. Trực giác đằng sau kỹ thuật này là: ở giai đoạn đầu của quá trình huấn luyện, khi chúng ta còn ở xa điểm tối ưu, chúng ta có thể đi những bước lớn (tốc độ học cao) để tiến nhanh. Tuy nhiên, khi đã đến gần vùng cực tiểu, chúng ta cần đi những bước nhỏ hơn để không "vọt qua" điểm tối ưu và có thể hội tụ một cách chính xác hơn.2

Có nhiều "lịch trình" (schedules) để giảm tốc độ học, chẳng hạn như giảm theo từng bậc, giảm theo hàm mũ, hoặc một công thức phổ biến là 2:

$$
α=1+decay_rate⋅epoch_num1​⋅α0​
$$

  

Trong đó $\alpha_0$ là tốc độ học ban đầu và decay_rate là một siêu tham số mới cần tinh chỉnh.2

  

### Chương 7: Các Kỹ thuật Điều chuẩn (Regularization) để Chống Overfitting

  

Một trong những thách thức lớn nhất khi huấn luyện các mạng nơ-ron sâu là overfitting (quá khớp). Hiện tượng này xảy ra khi mô hình trở nên quá phức tạp và "học thuộc lòng" các đặc điểm, thậm chí cả nhiễu, của tập dữ liệu huấn luyện, thay vì học các quy luật tổng quát. Kết quả là mô hình hoạt động rất tốt trên tập huấn luyện nhưng lại có hiệu suất kém trên dữ liệu mới (tập phát triển hoặc kiểm tra). Các kỹ thuật điều chuẩn được thiết kế để chống lại overfitting.2

  

#### L2 Regularization (Weight Decay)

  

Đây là một trong những kỹ thuật điều chuẩn phổ biến nhất. Ý tưởng là thêm một thành phần phạt vào hàm chi phí, tỷ lệ với tổng bình phương của tất cả các trọng số trong mạng 2:

$$
Jreg​=J(W,b)+2mλ​l=1∑L​∣∣W[l]∣∣F2​
$$

  

Trong đó $\lambda$ là siêu tham số điều chuẩn. Việc thêm thành phần này khuyến khích mạng giữ cho các trọng số có giá trị nhỏ. Một mạng với các trọng số nhỏ hơn sẽ tạo ra một hàm đầu ra "mượt mà" hơn, ít nhạy cảm với những thay đổi nhỏ ở đầu vào, và do đó ít có khả năng bị quá khớp với nhiễu trong dữ liệu huấn luyện.2

  

#### Dropout

  

Dropout là một kỹ thuật điều chuẩn đơn giản nhưng cực kỳ mạnh mẽ và hiệu quả, được giới thiệu bởi Srivastava và cộng sự.6 Ý tưởng cốt lõi là trong mỗi lần lặp của quá trình huấn luyện, một số nơ-ron trong các lớp ẩn sẽ bị "tắt" (dropped out) một cách ngẫu nhiên với một xác suất nhất định (gọi là

dropout rate).2

Điều này có hai tác động chính:

1. Nó buộc mạng không được phụ thuộc quá nhiều vào bất kỳ một nơ-ron hay một đặc trưng nào.6
    
2. Nó khuyến khích mạng học các biểu diễn dư thừa và mạnh mẽ hơn, vì mỗi nơ-ron phải học cách hoạt động tốt với các tập hợp nơ-ron đầu vào khác nhau một cách ngẫu nhiên.6
    

Tại thời điểm kiểm thử, không có nơ-ron nào bị tắt. Thay vào đó, các kích hoạt của các lớp đã áp dụng dropout sẽ được nhân với keep_prob (1 - dropout rate) để đảm bảo rằng giá trị kỳ vọng của đầu ra vẫn giữ nguyên như trong quá trình huấn luyện.2

  

#### Tăng cường Dữ liệu (Data Augmentation)

  

Về lý thuyết, cách tốt nhất để chống overfitting là có nhiều dữ liệu hơn. Tuy nhiên, việc thu thập và gán nhãn dữ liệu mới thường tốn kém và mất thời gian. Tăng cường dữ liệu là một kỹ thuật để tạo ra dữ liệu huấn luyện "mới" một cách nhân tạo từ tập dữ liệu hiện có.2

Đối với dữ liệu hình ảnh, các phép biến đổi phổ biến bao gồm 2:

- Lật ảnh theo chiều ngang.
    
- Cắt xén ngẫu nhiên (random cropping).
    
- Xoay ảnh.
    
- Thay đổi màu sắc, độ sáng, độ tương phản.
    

Bằng cách huấn luyện trên các phiên bản biến đổi này, mô hình học được tính bất biến đối với các thay đổi đó (ví dụ, một con mèo vẫn là một con mèo dù ảnh bị lật), giúp nó tổng quát hóa tốt hơn.2

Các kỹ thuật điều chuẩn này hoạt động bằng cách áp đặt một "niềm tin" hoặc một sự ràng buộc lên mô hình. L2 regularization áp đặt niềm tin rằng "các mô hình đơn giản hơn (trọng số nhỏ) thì tốt hơn". Dropout áp đặt niềm tin rằng "các đặc trưng nên được học một cách phân tán và dư thừa". Data augmentation áp đặt niềm tin rằng "mô hình nên bất biến với một số loại biến đổi nhất định". Việc áp dụng các kỹ thuật này là chìa khóa để kiểm soát sự cân bằng giữa độ chệch và phương sai (bias-variance tradeoff).2

  

### Chương 8: Chuẩn hóa theo Lô (Batch Normalization)

  

Batch Normalization (Batch Norm) là một trong những phát kiến quan trọng nhất trong thập kỷ qua, giúp việc huấn luyện các mạng nơ-ron rất sâu trở nên khả thi và hiệu quả hơn đáng kể. Nó được giới thiệu bởi Ioffe và Szegedy vào năm 2015.8

  

#### Vấn đề "Internal Covariate Shift"

  

Trong quá trình huấn luyện, khi các tham số của các lớp trước đó ($W^{[l-1]}, b^{[l-1]}$) được cập nhật, phân phối của các đầu vào cho lớp hiện tại ($Z^{[l]}$) cũng thay đổi liên tục. Hiện tượng này được gọi là Internal Covariate Shift.8 Nó giống như việc yêu cầu một người học một nhiệm vụ trong khi các quy tắc của trò chơi liên tục thay đổi. Điều này buộc mỗi lớp phải liên tục thích ứng với một "mục tiêu di động", làm chậm đáng kể quá trình học và đòi hỏi phải sử dụng tốc độ học nhỏ một cách cẩn thận.9

  

#### Cách hoạt động của Batch Norm

  

Batch Norm giải quyết vấn đề này bằng cách chuẩn hóa các đầu vào của mỗi lớp. Cụ thể, tại mỗi lớp, ngay trước hàm kích hoạt, Batch Norm thực hiện các bước sau trên mỗi mini-batch 12:

1. Tính toán trung bình và phương sai của mini-batch: $\mu_B, \sigma_B^2$.
    
2. Chuẩn hóa các giá trị đầu vào ($z^{(i)}$) để có trung bình 0 và phương sai 1:  
$znorm(i)​=σB2​+ε​z(i)−μB$​​
    
3. Co giãn và dịch chuyển (Scale and Shift): Chuẩn hóa cứng nhắc có thể làm giới hạn sức mạnh biểu diễn của lớp. Do đó, Batch Norm giới thiệu hai tham số có thể học được, $\gamma$ (gamma) và $\beta$ (beta), để co giãn và dịch chuyển các giá trị đã chuẩn hóa:  
$z~(i)=γznorm(i)​+β$
    

Bằng cách này, mạng có thể tự học phân phối tối ưu cho đầu vào của mỗi lớp, thay vì bị ép buộc phải có trung bình 0 và phương sai 1.12

Trong quá trình kiểm thử (inference), vì chúng ta thường xử lý từng mẫu một và không có mini-batch, việc tính $\mu_B$ và $\sigma_B^2$ là không khả thi. Thay vào đó, Batch Norm sử dụng các giá trị trung bình và phương sai được ước tính từ toàn bộ tập huấn luyện, thường được tính bằng trung bình động có trọng số mũ trong suốt quá trình huấn luyện.15

  

#### Lợi ích của Batch Normalization

  

- Tăng tốc độ học: Bằng cách ổn định phân phối đầu vào cho mỗi lớp, Batch Norm cho phép sử dụng tốc độ học cao hơn nhiều, giúp quá trình huấn luyện hội tụ nhanh hơn đáng kể.9
    
- Giảm sự nhạy cảm với khởi tạo: Nó làm cho mạng ít phụ thuộc hơn vào việc lựa chọn các giá trị khởi tạo ban đầu.9
    
- Tác dụng điều chuẩn: Do nhiễu được thêm vào từ việc tính toán trung bình và phương sai trên từng mini-batch riêng lẻ, Batch Norm có một tác dụng điều chuẩn nhẹ, đôi khi giúp giảm hoặc loại bỏ nhu cầu sử dụng Dropout.9
    

Batch Norm không chỉ đơn thuần là chuẩn hóa; nó tạo ra một "sân chơi" ổn định cho mỗi lớp, giúp chúng học một cách độc lập và hiệu quả hơn. Sự thành công của Batch Norm là một trong những lý do chính khiến các kiến trúc rất sâu như ResNet có thể được huấn luyện hiệu quả và nó đã trở thành một thành phần gần như tiêu chuẩn trong hầu hết các kiến trúc CNN hiện đại.17

  

### Chương 9: Tinh chỉnh Siêu tham số

  

Hiệu suất của một mô hình học sâu phụ thuộc rất nhiều vào việc lựa chọn các siêu tham số (hyperparameters) – những tham số không được học trong quá trình huấn luyện mà phải được thiết lập bởi người xây dựng mô hình. Quá trình tìm kiếm bộ siêu tham số tối ưu là một phần quan trọng và thường tốn nhiều thời gian trong các dự án học máy.2

  

#### Các Siêu tham số Quan trọng

  

Mặc dù có nhiều siêu tham số, nhưng mức độ ảnh hưởng của chúng đến kết quả cuối cùng là khác nhau. Một thứ tự ưu tiên phổ biến là 2:

1. Tốc độ học (Learning rate $\alpha$): Thường là siêu tham số quan trọng nhất.
    
2. Momentum $\beta$, số đơn vị ẩn, kích thước mini-batch.
    
3. Số lớp ẩn, learning rate decay.
    
4. Các tham số của Adam ($\beta_1, \beta_2, \varepsilon$): Thường được giữ ở giá trị mặc định.
    

  

#### Chiến lược Tìm kiếm

  

- Tìm kiếm theo lưới (Grid Search) vs. Tìm kiếm ngẫu nhiên (Random Search): Grid search thử nghiệm một cách có hệ thống tất cả các kết hợp của các giá trị được xác định trước. Tuy nhiên, nếu một siêu tham số ít quan trọng, chúng ta sẽ lãng phí tài nguyên tính toán để thử nhiều lần cùng một giá trị của siêu tham số quan trọng hơn. Random search thường hiệu quả hơn vì nó cho phép khám phá một phạm vi giá trị rộng hơn và đa dạng hơn cho mỗi siêu tham số, tăng cơ hội tìm thấy một bộ kết hợp tốt.2
    
- Sử dụng Thang đo Phù hợp: Việc lấy mẫu giá trị cho các siêu tham số cần được thực hiện trên một thang đo hợp lý. Ví dụ, tác động của tốc độ học $\alpha$ là theo cấp số nhân. Do đó, việc tìm kiếm trên thang tuyến tính (ví dụ: từ 0.0001 đến 1) sẽ phân bổ quá nhiều tài nguyên cho các giá trị lớn. Thay vào đó, nên lấy mẫu trên thang logarit. Một cách thực hiện là lấy mẫu ngẫu nhiên r trong một khoảng (ví dụ: [-4, 0]) và đặt $\alpha = 10^r$. Tương tự, đối với $\beta$ của EWA (ví dụ: từ 0.9 đến 0.999), nên lấy mẫu 1-β trên thang logarit.2
    

  

#### Các Phương pháp Tiếp cận: Panda vs. Caviar

  

Tùy thuộc vào tài nguyên tính toán sẵn có, có hai chiến lược chính để tinh chỉnh siêu tham số 2:

- Phương pháp Panda: Phù hợp khi có ít tài nguyên. Người thực hành sẽ "chăm sóc" (babysitting) một hoặc một vài mô hình, theo dõi quá trình học của chúng và điều chỉnh các siêu tham số một cách thủ công theo thời gian.
    
- Phương pháp Caviar: Phù hợp khi có nhiều tài nguyên tính toán. Người thực hành sẽ huấn luyện nhiều mô hình song song, mỗi mô hình có một bộ siêu tham số khác nhau, và sau đó chọn ra mô hình hoạt động tốt nhất.
    

Tinh chỉnh siêu tham số là một quá trình thực nghiệm, một sự kết hợp giữa khoa học (các nguyên tắc và chiến lược) và nghệ thuật (kinh nghiệm và trực giác). Không có một bộ quy tắc nào đúng cho mọi bài toán. Việc hiểu rõ bản chất của từng siêu tham số và ảnh hưởng của chúng đến quá trình học là chìa khóa để thực hiện quá trình này một cách hiệu quả.

---

Bảng 2: So sánh các Thuật toán Tối ưu hóa

  

|   |   |   |   |   |
|---|---|---|---|---|
|Thuật toán|Ý tưởng Cốt lõi|Công thức Cập nhật (Dạng đơn giản)|Ưu điểm|Nhược điểm|
|SGD|Cập nhật tham số sau mỗi mẫu (hoặc lô nhỏ).|$W := W - \alpha \cdot dW$|Đơn giản, dễ hiểu. Có thể thoát khỏi cực tiểu cục bộ nông.|Hội tụ chậm, đường đi của hàm chi phí rất nhiễu và dao động.2|
|Momentum|Thêm "đà" từ các gradient quá khứ để làm mịn và tăng tốc hội tụ.|$V_{dW} = \beta V_{dW} + (1-\beta)dW;$<br><br>$W := W - \alpha V_{dW}$|Hội tụ nhanh hơn SGD, giảm dao động đáng kể.2|Thêm một siêu tham số $\beta$ cần tinh chỉnh.|
|RMSprop|Điều chỉnh tốc độ học cho từng tham số một cách độc lập.|$S_{dW} = \beta S_{dW} + (1-\beta)(dW)^2;$<br><br>$W := W - \alpha \frac{dW}{\sqrt{S_{dW}} + \varepsilon}$|Thích ứng tốt với các hàm chi phí không đồng đều (non-stationary). Không cần tinh chỉnh nhiều $\alpha$.2|Vẫn có thể dao động.|
|Adam|Kết hợp những ưu điểm của Momentum (moment bậc nhất) và RMSprop (moment bậc hai).|Kết hợp các công thức của Momentum và RMSprop, có thêm bước hiệu chỉnh thiên vị.|Nhanh, mạnh mẽ, hiệu quả. Thường là lựa chọn mặc định tốt nhất cho hầu hết các bài toán.2|Phức tạp hơn về mặt lý thuyết. Trong một số trường hợp hiếm, có thể không hội tụ tốt bằng các thuật toán đơn giản hơn.|

Bảng so sánh này cho thấy rõ ràng con đường phát triển của các thuật toán tối ưu hóa. Nó bắt đầu từ SGD đơn giản, sau đó Momentum giải quyết vấn đề dao động, RMSProp giải quyết vấn đề tốc độ học đồng nhất, và cuối cùng Adam là sự tổng hợp thông minh của hai giải pháp trước đó. Việc hiểu rõ câu chuyện này giúp người học nắm bắt được "cái tại sao" đằng sau mỗi thuật toán, thay vì chỉ biết "cái gì", từ đó củng cố kiến thức nền tảng và trực giác về tối ưu hóa.

---

## Phần III: Mạng Nơ-ron Tích chập (Convolutional Neural Networks - CNNs)

  

Mạng nơ-ron tích chập (CNNs) là một lớp mạng nơ-ron sâu chuyên biệt, được thiết kế để xử lý dữ liệu có cấu trúc dạng lưới, chẳng hạn như hình ảnh. Chúng đã trở thành công cụ thống trị trong lĩnh vực thị giác máy tính, đạt được hiệu suất vượt trội trong các tác vụ như phân loại ảnh, phát hiện vật thể và phân đoạn ảnh.1 Sức mạnh của CNNs đến từ khả năng tự động và thích ứng học một hệ thống phân cấp các đặc trưng không gian, từ các cạnh và kết cấu đơn giản đến các bộ phận và vật thể phức tạp.

  

### Chương 10: Các Thành phần Cơ bản của CNN

  
  

#### Phép Tích chập (Convolution Operation)

  

Phép tích chập là khối xây dựng cốt lõi của CNN. Thay vì kết nối đầy đủ mọi nơ-ron, lớp tích chập sử dụng các bộ lọc (filters) hoặc kernels nhỏ để trượt qua hình ảnh đầu vào và thực hiện các phép nhân theo từng phần tử.2

- Chia sẻ Tham số (Parameter Sharing): Cùng một bộ lọc được sử dụng trên các phần khác nhau của ảnh, cho phép mạng phát hiện một đặc trưng (ví dụ: một cạnh dọc) bất kể vị trí của nó trong ảnh. Điều này làm giảm đáng kể số lượng tham số so với mạng kết nối đầy đủ.2
    
- Kết nối Thưa thớt (Sparsity of Connections): Mỗi nơ-ron trong lớp đầu ra chỉ kết nối với một vùng nhỏ (receptive field) của lớp đầu vào, giúp mô hình tập trung vào các đặc trưng cục bộ.2
    
- Tích chập trên Khối (Convolutions over Volumes): Đối với ảnh màu (ví dụ: RGB), đầu vào là một khối 3D (chiều cao x chiều rộng x số kênh). Bộ lọc cũng phải có cùng số kênh với đầu vào. Phép tích chập được thực hiện trên toàn bộ khối, tạo ra một bản đồ đặc trưng 2D duy nhất cho mỗi bộ lọc.2
    

  

#### Đệm (Padding) và Sải (Stride)

  

- Padding: Để giải quyết vấn đề hình ảnh bị thu nhỏ sau mỗi lớp tích chập và thông tin ở các cạnh bị mất, người ta thường thêm một đường viền gồm các pixel (thường là số 0) xung quanh ảnh đầu vào. Kỹ thuật này được gọi là đệm. "Same" padding được thiết kế để giữ nguyên kích thước không gian của đầu ra so với đầu vào.2
    
- Stride: Sải là số pixel mà bộ lọc dịch chuyển qua ảnh trong mỗi bước. Sải lớn hơn 1 sẽ làm giảm kích thước của đầu ra, có tác dụng tương tự như một lớp gộp.2
    

  

#### Lớp Gộp (Pooling Layer)

  

Lớp gộp thường được chèn vào giữa các lớp tích chập liên tiếp. Mục đích chính của nó là giảm dần kích thước không gian của biểu diễn để giảm số lượng tham số và tính toán trong mạng, đồng thời giúp kiểm soát overfitting.2

- Max Pooling: Lấy giá trị lớn nhất từ mỗi vùng của bản đồ đặc trưng. Đây là loại gộp phổ biến nhất.2
    
- Average Pooling: Lấy giá trị trung bình từ mỗi vùng.
    

  

### Chương 11: Các Kiến trúc CNN Kinh điển

  

Lịch sử của CNN được đánh dấu bằng một loạt các kiến trúc có ảnh hưởng, mỗi kiến trúc lại cải tiến dựa trên những kiến trúc trước đó.

- LeNet-5 (1998): Được coi là một trong những CNN thực sự đầu tiên, được phát triển bởi Yann LeCun để nhận dạng chữ số viết tay. Nó thiết lập mẫu kiến trúc cơ bản: xếp chồng các lớp tích chập và lớp gộp, theo sau là các lớp kết nối đầy đủ.17
    
- AlexNet (2012): Đã tạo ra một bước đột phá lớn khi chiến thắng cuộc thi ImageNet ILSVRC 2012 với một biên độ đáng kể. Nó sâu và rộng hơn LeNet-5, và là mạng đầu tiên sử dụng thành công ReLU và Dropout trong một kiến trúc CNN lớn. Thành công của AlexNet đã khơi dậy sự quan tâm trở lại đối với mạng nơ-ron và bắt đầu cuộc cách mạng học sâu hiện đại.19
    
- VGGNet (2014): Đóng góp chính của VGGNet là chứng minh rằng một kiến trúc rất sâu, được xây dựng từ các khối tích chập 3x3 rất nhỏ và đồng nhất, có thể đạt được hiệu suất vượt trội. Sự đơn giản và đồng nhất của nó đã làm cho nó trở thành một kiến trúc nền tảng rất phổ biến.17
    

  

### Chương 12: Các Kiến trúc CNN Nâng cao

  

- ResNet (2015): Để giải quyết vấn đề suy giảm hiệu suất (degradation problem) khi các mạng trở nên quá sâu, ResNet đã giới thiệu một khái niệm mang tính cách mạng: kết nối tắt (skip connection) hoặc khối dư (residual block). Các kết nối này cho phép gradient chảy trực tiếp qua các lớp, giúp huấn luyện các mạng sâu hơn nhiều (hàng trăm, thậm chí hàng nghìn lớp) một cách hiệu quả. ResNet đã trở thành một trong những kiến trúc có ảnh hưởng nhất và là nền tảng cho nhiều mô hình hiện đại.22
    
- Inception (GoogLeNet, 2014): Thay vì chỉ xếp chồng các lớp một cách tuần tự, mô-đun Inception thực hiện nhiều phép tích chập với các kích thước bộ lọc khác nhau (1x1, 3x3, 5x5) và một lớp gộp song song, sau đó nối các kết quả lại với nhau. Điều này cho phép mạng nắm bắt các đặc trưng ở nhiều tỷ lệ khác nhau. Việc sử dụng rộng rãi các tích chập 1x1 cũng giúp giảm đáng kể chi phí tính toán bằng cách giảm số kênh trước khi thực hiện các tích chập lớn hơn.17
    
- MobileNet & EfficientNet: Đây là những kiến trúc được thiết kế đặc biệt cho các ứng dụng có tài nguyên hạn chế như thiết bị di động.
    

- MobileNet sử dụng tích chập phân tách theo chiều sâu (depthwise separable convolutions) để giảm đáng kể số lượng tham số và tính toán.2
    
- EfficientNet giới thiệu một phương pháp mở rộng mô hình có nguyên tắc gọi là compound scaling, cân bằng một cách thông minh giữa độ sâu, độ rộng và độ phân giải của mạng để đạt được hiệu quả tối ưu.26
    

---

## Phần IV: Mô hình Chuỗi (Sequence Models)

  

Nhiều bài toán trong thế giới thực liên quan đến dữ liệu tuần tự, nơi thứ tự của các phần tử là quan trọng, chẳng hạn như văn bản, giọng nói, hoặc chuỗi thời gian. Mạng nơ-ron hồi quy (RNNs) được thiết kế đặc biệt để xử lý loại dữ liệu này.

  

### Chương 13: Mạng Nơ-ron Hồi quy (RNNs)

  

- Kiến trúc Cơ bản: Không giống như mạng feedforward, RNN có các kết nối lặp lại, cho phép thông tin tồn tại. Tại mỗi bước thời gian t, RNN nhận một đầu vào $x^{}$ và trạng thái ẩn từ bước trước đó $a^{}$, sau đó tạo ra một đầu ra $ŷ^{}$ và một trạng thái ẩn mới $a^{}$. Trạng thái ẩn này hoạt động như một "bộ nhớ" của mạng, lưu giữ thông tin về các bước trước đó.2
    
- Chia sẻ Tham số: Cùng một bộ tham số ($W_{ax}, W_{aa}, W_{ya}$) được sử dụng ở mọi bước thời gian, làm cho RNN có khả năng xử lý các chuỗi có độ dài thay đổi.2
    

  

### Chương 14: Các Thách thức trong Huấn luyện RNN

  

- Vanishing & Exploding Gradients: Do tính chất hồi quy, quá trình lan truyền ngược qua thời gian (Backpropagation Through Time - BPTT) liên quan đến việc nhân lặp đi lặp lại cùng một ma trận trọng số. Điều này có thể khiến gradient trở nên cực kỳ nhỏ (biến mất) hoặc cực kỳ lớn (bùng nổ) khi chuỗi dài ra. Vấn đề vanishing gradient đặc biệt nghiêm trọng, vì nó ngăn cản mạng học các phụ thuộc dài hạn.2
    
- Gradient Clipping: Một giải pháp thực tế cho vấn đề exploding gradient là cắt gradient (gradient clipping), tức là đặt một ngưỡng cho độ lớn của gradient để ngăn nó trở nên quá lớn.2
    

  

### Chương 15: Các Kiến trúc RNN Nâng cao: LSTM và GRU

  

Để giải quyết vấn đề vanishing gradient, các kiến trúc RNN phức tạp hơn đã được phát triển, sử dụng các cơ chế cổng (gating mechanisms) để kiểm soát luồng thông tin.

- Long Short-Term Memory (LSTM): LSTM giới thiệu một trạng thái ô (cell state) riêng biệt, hoạt động như một "băng chuyền" thông tin. Luồng thông tin vào và ra khỏi trạng thái ô được điều chỉnh bởi ba cổng 2:
    

- Cổng Quên (Forget Gate): Quyết định thông tin nào từ trạng thái ô trước đó nên được loại bỏ.
    
- Cổng Đầu vào (Input Gate): Quyết định thông tin mới nào nên được lưu trữ trong trạng thái ô.
    
- Cổng Đầu ra (Output Gate): Quyết định phần nào của trạng thái ô sẽ được xuất ra dưới dạng trạng thái ẩn.
    

- Gated Recurrent Unit (GRU): GRU là một phiên bản đơn giản hơn của LSTM, kết hợp cổng quên và cổng đầu vào thành một cổng cập nhật (update gate) duy nhất. Nó cũng có một cổng đặt lại (reset gate) để kiểm soát mức độ ảnh hưởng của bộ nhớ quá khứ đến trạng thái hiện tại. GRU thường có hiệu suất tương đương với LSTM nhưng lại hiệu quả hơn về mặt tính toán.2
    

  

### Chương 16: Các Biến thể Kiến trúc Chuỗi

  

- Mạng RNN Hai chiều (Bidirectional RNNs): Để đưa ra dự đoán tại một thời điểm nhất định, việc biết cả ngữ cảnh quá khứ và tương lai đều hữu ích. Bi-RNN xử lý chuỗi theo cả hai hướng (tiến và lùi) bằng hai RNN riêng biệt và sau đó kết hợp các trạng thái ẩn của chúng để đưa ra dự đoán cuối cùng.2
    
- Mạng RNN Sâu (Deep RNNs): Tương tự như CNN, việc xếp chồng nhiều lớp RNN lên nhau có thể cho phép mạng học các biểu diễn phân cấp phức tạp hơn của dữ liệu chuỗi.2
    
- Mô hình Sequence-to-Sequence (Seq2Seq): Đối với các tác vụ như dịch máy, nơi độ dài của chuỗi đầu vào và đầu ra có thể khác nhau, kiến trúc Encoder-Decoder được sử dụng.
    

- Encoder: Một RNN đọc chuỗi đầu vào và nén thông tin của nó thành một vector ngữ cảnh có kích thước cố định (trạng thái ẩn cuối cùng).
    
- Decoder: Một RNN khác nhận vector ngữ cảnh này và tạo ra chuỗi đầu ra, một phần tử tại một thời điểm.2
    

---

## Phần V: Cơ chế Chú ý và Kiến trúc Transformer

  

Một hạn chế lớn của kiến trúc Encoder-Decoder cơ bản là nó phải nén toàn bộ thông tin của chuỗi đầu vào vào một vector có kích thước cố định, tạo ra một "nút cổ chai". Cơ chế chú ý đã được giới thiệu để giải quyết vấn đề này.

  

### Chương 17: Cơ chế Chú ý (Attention Mechanism)

  

- Trực giác: Thay vì chỉ dựa vào vector ngữ cảnh cuối cùng, cơ chế chú ý cho phép decoder, tại mỗi bước tạo ra đầu ra, "nhìn lại" tất cả các trạng thái ẩn của encoder. Nó học một tập hợp các trọng số chú ý (attention weights) để quyết định phần nào của chuỗi đầu vào là quan trọng nhất tại thời điểm đó.2
    
- Cách hoạt động: Tại mỗi bước của decoder, một "điểm số" được tính toán giữa trạng thái ẩn hiện tại của decoder và mỗi trạng thái ẩn của encoder. Các điểm số này sau đó được đưa qua một hàm softmax để tạo ra các trọng số chú ý. Cuối cùng, một vector ngữ cảnh có trọng số được tính bằng cách lấy tổng có trọng số của các trạng thái ẩn của encoder, và vector này được sử dụng để tạo ra đầu ra.2
    

  

### Chương 18: Kiến trúc Transformer

  

Bài báo "Attention Is All You Need" đã giới thiệu kiến trúc Transformer, một mô hình hoàn toàn dựa trên cơ chế chú ý và loại bỏ hoàn toàn các kết nối hồi quy. Điều này cho phép song song hóa tính toán một cách đáng kể và đã trở thành nền tảng cho hầu hết các mô hình xử lý ngôn ngữ tự nhiên hiện đại.29

- Tự chú ý (Self-Attention): Thay vì chú ý đến một chuỗi khác (như trong Seq2Seq), self-attention cho phép các phần tử trong cùng một chuỗi tương tác với nhau và tính toán trọng số chú ý cho chính nó. Điều này giúp mô hình nắm bắt các phụ thuộc bên trong chuỗi.2
    
- Chú ý Đa đầu (Multi-Head Attention): Thay vì chỉ thực hiện chú ý một lần, Transformer thực hiện nó nhiều lần song song với các phép chiếu tuyến tính khác nhau (các "đầu"). Điều này cho phép mô hình cùng lúc chú ý đến thông tin từ các không gian con biểu diễn khác nhau.2
    
- Mã hóa Vị trí (Positional Encoding): Vì Transformer không có tính hồi quy, nó không có nhận thức vốn có về thứ tự từ. Để giải quyết vấn đề này, các vector mã hóa vị trí được thêm vào các embedding đầu vào để cung cấp cho mô hình thông tin về vị trí của các từ trong chuỗi.2
    
- Kiến trúc Encoder-Decoder: Transformer vẫn giữ cấu trúc encoder-decoder, nhưng mỗi khối encoder và decoder đều được xây dựng từ các lớp self-attention và các lớp feed-forward, với các kết nối dư và chuẩn hóa lớp.2
    

---

## Phần VI: Các Ứng dụng và Chiến lược Thực tiễn

  

Phần này khám phá các ứng dụng cụ thể của học sâu và các chiến lược thực tiễn để xây dựng và cải tiến các hệ thống học máy.

  

### Chương 19: Phát hiện Vật thể

  

- Sự tiến hóa từ R-CNN đến Faster R-CNN:
    

- R-CNN: Đề xuất các vùng (region proposals) bằng thuật toán bên ngoài (ví dụ: Selective Search), sau đó đưa từng vùng vào một CNN để phân loại. Rất chậm.33
    
- Fast R-CNN: Chỉ đưa toàn bộ ảnh qua CNN một lần để tạo bản đồ đặc trưng, sau đó sử dụng các vùng đề xuất để lấy các đặc trưng tương ứng (RoI Pooling) và phân loại. Nhanh hơn đáng kể nhưng vẫn phụ thuộc vào đề xuất vùng bên ngoài.33
    
- Faster R-CNN: Giới thiệu Mạng Đề xuất Vùng (Region Proposal Network - RPN), một mạng con được huấn luyện để tự đề xuất các vùng, tạo ra một hệ thống phát hiện vật thể end-to-end thực sự.33
    

- YOLO (You Only Look Once): Một cách tiếp cận khác, coi phát hiện vật thể như một bài toán hồi quy. Nó chia ảnh thành một lưới, và mỗi ô lưới trực tiếp dự đoán các hộp giới hạn và xác suất lớp cho các vật thể có tâm nằm trong ô đó. Cực kỳ nhanh và phù hợp cho các ứng dụng thời gian thực.2
    
- Các Khái niệm Cốt lõi:
    

- Intersection over Union (IoU): Một độ đo để đánh giá độ chính xác của một hộp giới hạn được dự đoán bằng cách tính tỷ lệ diện tích giao trên diện tích hợp của nó với hộp giới hạn thực tế.2
    
- Non-Max Suppression (NMS): Một thuật toán hậu xử lý để loại bỏ các hộp giới hạn trùng lặp và giữ lại những hộp có độ tin cậy cao nhất.2
    
- Anchor Boxes: Các hộp tham chiếu có kích thước và tỷ lệ khung hình được xác định trước, giúp mô hình phát hiện các vật thể có hình dạng khác nhau một cách hiệu quả hơn.2
    

  

### Chương 20: Nhận dạng Khuôn mặt và Chuyển đổi Phong cách Nơ-ron

  

- Nhận dạng Khuôn mặt:
    

- One-Shot Learning: Thách thức của việc nhận dạng một người chỉ từ một hình ảnh duy nhất.2
    
- Mạng Siamese: Huấn luyện hai mạng CNN giống hệt nhau song song để học một hàm đo độ tương đồng giữa hai hình ảnh.2
    
- Triplet Loss: Một hàm mất mát được thiết kế để huấn luyện mạng tạo ra các embedding. Nó cố gắng đẩy embedding của một ảnh "neo" (anchor) lại gần embedding của một ảnh "dương tính" (positive - cùng người) và ra xa embedding của một ảnh "âm tính" (negative - khác người).2
    

- Chuyển đổi Phong cách Nơ-ron (Neural Style Transfer): Một kỹ thuật ấn tượng sử dụng một mạng CNN đã được huấn luyện trước (ví dụ: VGG) để tách biệt biểu diễn nội dung (từ các lớp sâu hơn) và biểu diễn phong cách (từ các ma trận tương quan đặc trưng ở nhiều lớp) của các hình ảnh. Sau đó, nó tạo ra một hình ảnh mới bằng cách tối ưu hóa để khớp với nội dung của một ảnh và phong cách của một ảnh khác.2
    

  

### Chương 21: Biểu diễn Từ (Word Embeddings)

  

- Ý tưởng: Thay vì biểu diễn các từ dưới dạng các vector one-hot thưa thớt, word embeddings biểu diễn chúng dưới dạng các vector dày đặc, chiều thấp trong một không gian liên tục. Các từ có ý nghĩa tương tự sẽ có các vector gần nhau trong không gian này.2
    
- Word2Vec: Một tập hợp các mô hình (Skip-gram và CBOW) học các embedding bằng cách huấn luyện một mạng nơ-ron nông để dự đoán một từ từ các từ ngữ cảnh xung quanh nó (hoặc ngược lại).2
    
- GloVe (Global Vectors): Một cách tiếp cận khác, học các embedding bằng cách thực hiện phân rã ma trận trên ma trận đồng xuất hiện (co-occurrence matrix) của các từ trong toàn bộ kho dữ liệu, nắm bắt cả thống kê cục bộ và toàn cục.2
    

  

### Chương 22: Chiến lược Xây dựng Hệ thống Học máy

  

Xây dựng một hệ thống học máy thành công không chỉ đòi hỏi kiến thức về thuật toán mà còn cần một chiến lược thực tiễn và có hệ thống.

- Thiết lập Dự án:
    

- Lặp lại Nhanh chóng: Thay vì cố gắng xây dựng một hệ thống hoàn hảo ngay từ đầu, hãy nhanh chóng xây dựng một hệ thống cơ bản, sau đó sử dụng các phân tích để lặp lại và cải tiến nó.2
    
- Độ đo Đánh giá Duy nhất: Thiết lập một độ đo đánh giá duy nhất (single-number evaluation metric) giúp tăng tốc quá trình ra quyết định khi so sánh các mô hình khác nhau.2
    
- Optimizing và Satisficing Metrics: Khi có nhiều tiêu chí, hãy chọn một tiêu chí để tối ưu hóa (optimizing metric, ví dụ: độ chính xác) và đặt các ngưỡng chấp nhận được cho các tiêu chí khác (satisficing metrics, ví dụ: thời gian chạy, bộ nhớ).2
    

- Phân tích Lỗi và Dữ liệu:
    

- Phân tích Lỗi: Kiểm tra thủ công các ví dụ mà mô hình dự đoán sai để hiểu các loại lỗi chính và ưu tiên các hướng cải tiến.2
    
- Xử lý Dữ liệu Gán nhãn Sai: Các thuật toán học sâu khá mạnh mẽ với các lỗi ngẫu nhiên trong tập huấn luyện, nhưng lỗi hệ thống cần được sửa chữa. Việc sửa nhãn trong tập dev/test cần được thực hiện cẩn thận để đảm bảo tính nhất quán.2
    
- Xử lý Dữ liệu Không khớp Phân phối: Khi tập huấn luyện và tập dev/test có phân phối khác nhau, hãy tạo một tập "training-dev" từ phân phối của tập huấn luyện để phân biệt giữa vấn đề phương sai và vấn đề không khớp dữ liệu.2
    

- Học Chuyển giao và Học Đa nhiệm:
    

- Học Chuyển giao (Transfer Learning): Tận dụng kiến thức từ một mô hình đã được huấn luyện trước trên một tập dữ liệu lớn (ví dụ: ImageNet) và tinh chỉnh (fine-tune) nó cho một tác vụ mới có ít dữ liệu hơn. Đây là một kỹ thuật cực kỳ hiệu quả trong thực tế.2
    
- Học Đa nhiệm (Multi-task Learning): Huấn luyện một mạng duy nhất để thực hiện nhiều tác vụ cùng một lúc. Điều này có thể cải thiện hiệu suất nếu các tác vụ có thể chia sẻ các biểu diễn cấp thấp.2
    

#### Works cited

1. Stanford University CS231n: Deep Learning for Computer Vision, accessed July 4, 2025, [https://cs231n.stanford.edu/](https://cs231n.stanford.edu/)
    
2. Error Analysis
    
3. Neural networks and deep learning, accessed July 4, 2025, [http://neuralnetworksanddeeplearning.com/](http://neuralnetworksanddeeplearning.com/)
    
4. Adam: A Method for Stochastic Optimization - ResearchGate, accessed July 4, 2025, [https://www.researchgate.net/publication/269935079_Adam_A_Method_for_Stochastic_Optimization](https://www.researchgate.net/publication/269935079_Adam_A_Method_for_Stochastic_Optimization)
    
5. Kingma, D. and Ba, J.L. (2014) Adam A Method for Stochastic Optimization. Computer Science, 1-15. - References - Scientific Research Publishing, accessed July 4, 2025, [https://www.scirp.org/reference/referencespapers?referenceid=2574380](https://www.scirp.org/reference/referencespapers?referenceid=2574380)
    
6. Dropout: A Simple Way to Prevent Neural Networks from Overfitting - ResearchGate, accessed July 4, 2025, [https://www.researchgate.net/publication/286794765_Dropout_A_Simple_Way_to_Prevent_Neural_Networks_from_Overfitting](https://www.researchgate.net/publication/286794765_Dropout_A_Simple_Way_to_Prevent_Neural_Networks_from_Overfitting)
    
7. Dropout: A Simple Way to Prevent Neural Networks from Overfitting, accessed July 4, 2025, [https://jmlr.org/papers/v15/srivastava14a.html](https://jmlr.org/papers/v15/srivastava14a.html)
    
8. Batch normalization - Wikipedia, accessed July 4, 2025, [https://en.wikipedia.org/wiki/Batch_normalization](https://en.wikipedia.org/wiki/Batch_normalization)
    
9. [1502.03167] Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift - arXiv, accessed July 4, 2025, [https://arxiv.org/abs/1502.03167](https://arxiv.org/abs/1502.03167)
    
10. Batch normalization in 3 levels of understanding | Towards Data ..., accessed July 4, 2025, [https://towardsdatascience.com/batch-normalization-in-3-levels-of-understanding-14c2da90a338/](https://towardsdatascience.com/batch-normalization-in-3-levels-of-understanding-14c2da90a338/)
    
11. accessed January 1, 1970, [https://arxiv.org/pdf/1502.03167.pdf](https://arxiv.org/pdf/1502.03167.pdf)
    
12. The Math Behind Batch Normalization - Towards Data Science, accessed July 4, 2025, [https://towardsdatascience.com/the-math-behind-batch-normalization-90ebbc0b1b0b/](https://towardsdatascience.com/the-math-behind-batch-normalization-90ebbc0b1b0b/)
    
13. What is batch normalization? - Towards Data Science, accessed July 4, 2025, [https://towardsdatascience.com/what-is-batch-normalization-46058b4f583/](https://towardsdatascience.com/what-is-batch-normalization-46058b4f583/)
    
14. Why Batch Normalization Matters for Deep Learning | Towards Data Science, accessed July 4, 2025, [https://towardsdatascience.com/why-batch-normalization-matters-for-deep-learning-3e5f4d71f567/](https://towardsdatascience.com/why-batch-normalization-matters-for-deep-learning-3e5f4d71f567/)
    
15. Batch Norm Explained Visually - How it works, and why neural networks need it, accessed July 4, 2025, [https://towardsdatascience.com/batch-norm-explained-visually-how-it-works-and-why-neural-networks-need-it-b18919692739/](https://towardsdatascience.com/batch-norm-explained-visually-how-it-works-and-why-neural-networks-need-it-b18919692739/)
    
16. Visualizing What Batch Normalization Is and Its Advantages : r/datascience - Reddit, accessed July 4, 2025, [https://www.reddit.com/r/datascience/comments/1aihddg/visualizing_what_batch_normalization_is_and_its/](https://www.reddit.com/r/datascience/comments/1aihddg/visualizing_what_batch_normalization_is_and_its/)
    
17. Convolutional Neural Networks (CNNs / ConvNets) - CS231n Deep ..., accessed July 4, 2025, [https://cs231n.github.io/convolutional-networks/](https://cs231n.github.io/convolutional-networks/)
    
18. Deep Learning - LeNet, accessed July 4, 2025, [https://www.doc.ic.ac.uk/~bkainz/teaching/DL/notes/LeNet.pdf](https://www.doc.ic.ac.uk/~bkainz/teaching/DL/notes/LeNet.pdf)
    
19. Paper Summary: ImageNet Classification with Deep Convolutional Neural Networks, accessed July 4, 2025, [https://karan3-zoh.medium.com/paper-summary-imagenet-classification-with-deep-convolutional-neural-networks-41ce6c65960](https://karan3-zoh.medium.com/paper-summary-imagenet-classification-with-deep-convolutional-neural-networks-41ce6c65960)
    
20. AlexNet - Wikipedia, accessed July 4, 2025, [https://en.wikipedia.org/wiki/AlexNet](https://en.wikipedia.org/wiki/AlexNet)
    
21. Very Deep Convolutional Networks for Large-Scale Image Recognition - ResearchGate, accessed July 4, 2025, [https://www.researchgate.net/publication/319770291_Very_Deep_Convolutional_Networks_for_Large-Scale_Image_Recognition](https://www.researchgate.net/publication/319770291_Very_Deep_Convolutional_Networks_for_Large-Scale_Image_Recognition)
    
22. KaimingHe/deep-residual-networks: Deep Residual Learning for Image Recognition - GitHub, accessed July 4, 2025, [https://github.com/KaimingHe/deep-residual-networks](https://github.com/KaimingHe/deep-residual-networks)
    
23. Deep Residual Learning for Image Recognition - ResearchGate, accessed July 4, 2025, [https://www.researchgate.net/publication/286512696_Deep_Residual_Learning_for_Image_Recognition](https://www.researchgate.net/publication/286512696_Deep_Residual_Learning_for_Image_Recognition)
    
24. (PDF) Going deeper with convolutions - ResearchGate, accessed July 4, 2025, [https://www.researchgate.net/publication/305196650_Going_deeper_with_convolutions](https://www.researchgate.net/publication/305196650_Going_deeper_with_convolutions)
    
25. MobileNetV1 Explained | Papers With Code, accessed July 4, 2025, [https://paperswithcode.com/method/mobilenetv1](https://paperswithcode.com/method/mobilenetv1)
    
26. EfficientNet: Rethinking Model Scaling for Convolutional ... - arXiv, accessed July 4, 2025, [https://arxiv.org/abs/1905.11946](https://arxiv.org/abs/1905.11946)
    
27. EfficientNet: Rethinking Model Scaling for Convolutional Neural Networks - ResearchGate, accessed July 4, 2025, [https://www.researchgate.net/publication/333444574_EfficientNet_Rethinking_Model_Scaling_for_Convolutional_Neural_Networks](https://www.researchgate.net/publication/333444574_EfficientNet_Rethinking_Model_Scaling_for_Convolutional_Neural_Networks)
    
28. Sequence to Sequence Learning with Neural Networks - NIPS, accessed July 4, 2025, [http://papers.neurips.cc/paper/5346-sequence-to-sequence-learning-with-neural-networks.pdf](http://papers.neurips.cc/paper/5346-sequence-to-sequence-learning-with-neural-networks.pdf)
    
29. Stanford CS 224N | Natural Language Processing with Deep Learning, accessed July 4, 2025, [https://web.stanford.edu/class/cs224n/](https://web.stanford.edu/class/cs224n/)
    
30. 'Attention Is All You Need' - The foundation research paper for all LLMs and it's India link, accessed July 4, 2025, [https://www.reddit.com/r/Science_India/comments/1ifrq2m/attention_is_all_you_need_the_foundation_research/](https://www.reddit.com/r/Science_India/comments/1ifrq2m/attention_is_all_you_need_the_foundation_research/)
    
31. Attention Is All You Need - Wikipedia, accessed July 4, 2025, [https://en.wikipedia.org/wiki/Attention_Is_All_You_Need](https://en.wikipedia.org/wiki/Attention_Is_All_You_Need)
    
32. Jay Alammar – Visualizing machine learning one concept at a time., accessed July 4, 2025, [https://jalammar.github.io/](https://jalammar.github.io/)
    
33. #027 R-CNN, Fast R-CNN, and Faster R-CNN explained with a demonstration in PyTorch - Master Data Science 16.01.2023, accessed July 4, 2025, [https://datahacker.rs/027-r-cnn-fast-r-cnn-and-faster-r-cnn-explained-with-a-demonstration-in-pytorch/](https://datahacker.rs/027-r-cnn-fast-r-cnn-and-faster-r-cnn-explained-with-a-demonstration-in-pytorch/)
    
34. From R-CNN to Faster R-CNN – The Evolution of Object Detection Technology - Alibaba Cloud Community, accessed July 4, 2025, [https://www.alibabacloud.com/blog/from-r-cnn-to-faster-r-cnn-the-evolution-of-object-detection-technology_593829](https://www.alibabacloud.com/blog/from-r-cnn-to-faster-r-cnn-the-evolution-of-object-detection-technology_593829)
    
35. Faster R-CNN Explained for Object Detection Tasks - DigitalOcean, accessed July 4, 2025, [https://www.digitalocean.com/community/tutorials/faster-r-cnn-explained-object-detection](https://www.digitalocean.com/community/tutorials/faster-r-cnn-explained-object-detection)
    
36. The Fundamental Guide to Faster R-CNN - viso.ai, accessed July 4, 2025, [https://viso.ai/deep-learning/faster-r-cnn-2/](https://viso.ai/deep-learning/faster-r-cnn-2/)
    
37. Faster RCNN in 2025: How it works and why it's still the benchmark for Object Detection, accessed July 4, 2025, [https://www.thinkautonomous.ai/blog/faster-rcnn/](https://www.thinkautonomous.ai/blog/faster-rcnn/)
    
38. Getting Started with R-CNN, Fast R-CNN, and Faster R-CNN - MATLAB & - MathWorks, accessed July 4, 2025, [https://www.mathworks.com/help/vision/ug/getting-started-with-r-cnn-fast-r-cnn-and-faster-r-cnn.html](https://www.mathworks.com/help/vision/ug/getting-started-with-r-cnn-fast-r-cnn-and-faster-r-cnn.html)
    
39. The Story of YOLO. I have recently worked with the team in… | by ..., accessed July 4, 2025, [https://medium.com/@yasser.maree/the-story-of-yolo-72cf7dd7d9bc](https://medium.com/@yasser.maree/the-story-of-yolo-72cf7dd7d9bc)
    
40. Redmon, J. and Farhadi, A. (2018) YOLOv3 An Incremental Improvement. - References, accessed July 4, 2025, [https://www.scirp.org/reference/referencespapers?referenceid=2633270](https://www.scirp.org/reference/referencespapers?referenceid=2633270)
    
41. YOLOv3 Explained | Papers With Code, accessed July 4, 2025, [https://paperswithcode.com/method/yolov3](https://paperswithcode.com/method/yolov3)
    
42. [1804.02767] YOLOv3: An Incremental Improvement - arXiv, accessed July 4, 2025, [https://arxiv.org/abs/1804.02767](https://arxiv.org/abs/1804.02767)
    
43. YOLOv3 - Home - Papers - Read the Docs, accessed July 4, 2025, [https://papers.readthedocs.io/en/latest/imagedetection/yolov3/](https://papers.readthedocs.io/en/latest/imagedetection/yolov3/)
    
44. YOLOv3 - Tethys, accessed July 4, 2025, [https://tethys.pnnl.gov/sites/default/files/publications/Redmonetal.pdf](https://tethys.pnnl.gov/sites/default/files/publications/Redmonetal.pdf)
    
45. [1804.02767] YOLOv3: An Incremental Improvement - arXiv, accessed July 4, 2025, [https://arxiv.org/abs/1804.02767?utm_campaign=The%20Batch&utm_source=hs_email&utm_medium=email&_hsenc=p2ANqtz-868D-YXjT5eAIoIzXlkWEVl2Na3PsgKSM6ZNj6Bg_p9pNIu664bfyXWBjdkk6pNLkc2zH_](https://arxiv.org/abs/1804.02767?utm_campaign=The+Batch&utm_source=hs_email&utm_medium=email&_hsenc=p2ANqtz-868D-YXjT5eAIoIzXlkWEVl2Na3PsgKSM6ZNj6Bg_p9pNIu664bfyXWBjdkk6pNLkc2zH_)
    
46. FaceNet: A Unified Embedding for Face Recognition and Clustering, accessed July 4, 2025, [https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Schroff_FaceNet_A_Unified_2015_CVPR_paper.pdf](https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Schroff_FaceNet_A_Unified_2015_CVPR_paper.pdf)
    
47. FaceNet: A Unified Embedding for Face Recognition and Clustering - GitHub, accessed July 4, 2025, [https://raw.githubusercontent.com/ankurharitosh/Study-Reports-and-Implementation-on-VIPLFaceNet-FaceNet/master/FaceNet_Ankur.pdf](https://raw.githubusercontent.com/ankurharitosh/Study-Reports-and-Implementation-on-VIPLFaceNet-FaceNet/master/FaceNet_Ankur.pdf)
    
48. A Neural Algorithm of Artistic Style arXiv:1508.06576v2 [cs.CV] 2 ..., accessed July 4, 2025, [https://arxiv.org/abs/1508.06576](https://arxiv.org/abs/1508.06576)
    
49. tjwhitaker/a-neural-algorithm-of-artistic-style - GitHub, accessed July 4, 2025, [https://github.com/tjwhitaker/a-neural-algorithm-of-artistic-style](https://github.com/tjwhitaker/a-neural-algorithm-of-artistic-style)
    
50. 10 Years of word2vec: Motivations and Success » David Strohmaier, accessed July 4, 2025, [https://dstrohmaier.com/10-years-of-word2vec/](https://dstrohmaier.com/10-years-of-word2vec/)
    
51. GloVe: Global Vectors for Word Representation - Stanford NLP Group, accessed July 4, 2025, [https://nlp.stanford.edu/pubs/glove.pdf](https://nlp.stanford.edu/pubs/glove.pdf)
    
52. GloVe: Global Vectors for Word Representation - Kaggle, accessed July 4, 2025, [https://www.kaggle.com/datasets/rtatman/glove-global-vectors-for-word-representation](https://www.kaggle.com/datasets/rtatman/glove-global-vectors-for-word-representation)
    

**