---
tags:
  - machine-learning
  - deep-learning
status: "⬜ chưa học"
created: 2025-01-01
---

# Activation Functions

> **Quay về:** [[🗺️ MOC - Machine Learning]] | [[Deep Learning Overview]]

---

## 📝 Định nghĩa của tôi

> *(Viết lại bằng lời của bạn sau khi học xong)*

---

## Nội dung
| Phương diện                         | **Softmax**                                                                                                                                   | **ReLU (Rectified Linear Unit)**                                                                    | **Sigmoid**                                                                                             | **Tanh (Hyperbolic Tangent)**                                                                                                 |
| ----------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **Công thức**                       | $$ \sigma(\mathbf{z})_i = \frac{e^{z_i}}{\sum_{j=1}^{K} e^{z_j}} $$                                                                           | $$f(x)=max⁡(0,x)$$                                                                                  | $$ \sigma(x) = \frac{1}{1 + e^{-x}} $$                                                                  | $$ \tanh(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}} $$                                                                            |
| **Miền giá trị đầu ra**             | (0, 1) và tổng các đầu ra = 1 (xác suất)                                                                                                      | [0,+∞)                                                                                              | (0, 1)                                                                                                  | (-1, 1)                                                                                                                       |
| **Dạng đồ thị**                     | ![[canvas.png]]                                                                                                                               | ![[canvas1.png]]                                                                                    | ![[canvas2.png]]<br>Chữ S, bão hòa ở 0 và 1                                                             | ![[canvas3.png]]<br>Chữ S, bão hòa ở -1 và 1, đối xứng qua 0                                                                  |
| **Ứng dụng chính**                  | **Lớp đầu ra** của bài toán phân loại nhiều lớp (multiclass, classification)<br><br>attention mechanism                                       | **Lớp ẩn** của mạng nơ-ron sâu (CNN, MLP, ResNet, Transformer...)                                   | **Lớp đầu ra** cho phân loại nhị phân; ít dùng trong lớp ẩn hiện nay<br><br>LSTM, GRU                   | **Lớp ẩn** trong các mạng cũ (RNN cổ điển); hoặc lớp đầu ra cho bài toán regression với giá trị trong (-1,1)(Gioi han)        |
| **Tính chất đạo hàm**               | ![[daoham.png]]<br>Đạo hàm phụ thuộc vào toàn bộ các giá trị Softmax, tính toán hơi phức tạp nhưng ổn định                                    | ![[daoham1.png]]<br><br>Đạo hàm: 0 với x<0, 1 với x>0; không xác định tại x=0 (thường lấy 0 hoặc 1) | ![[daoham2.png]]<br>$$f'(x) = f(x)(1 - f(x))$$<br>> **Ghi chú:** Giá trị lớn nhất là $0.25$ tại $x = 0$ | ![[daoham3.png]]<br>$$f'(x) = 1 - f(x)^2$$<br>> **Ghi chú:** Giá trị lớn nhất là $1$ tại $x = 0$                              |
| **Vấn đề bão hòa (saturation)**     | Không bão hòa theo nghĩa gradient biến mất, nhưng khi giá trị quá lớn, Softmax gần như one-hot (gradient rất nhỏ với các lớp không được chọn) | **Không bão hòa** ở vùng dương, giúp tránh vanishing gradient                                       | Bão hòa mạnh ở hai đầu (x rất âm hoặc rất dương), **gây vanishing gradient**                            | Bão hòa ở hai đầu (x rất âm → -1, x rất dương → 1), **gây vanishing gradient** mạnh hơn Sigmoid một chút (do đạo hàm lớn hơn) |
| **Trung tâm (zero-centered)**       | Không (đầu ra >0)                                                                                                                             | Không (đầu ra ≥0)                                                                                   | Không (đầu ra >0)                                                                                       | **Có** (đầu ra đối xứng qua 0) – giúp hội tụ nhanh hơn                                                                        |
| **Tính toán chi phí**               | Trung bình (cần tính exp và tổng)                                                                                                             | **Rất thấp** (chỉ so sánh với 0)                                                                    | Trung bình (cần exp)                                                                                    | Trung bình (cần exp)                                                                                                          |
| **Vấn đề chết neuron (dying ReLU)** | Không xảy ra                                                                                                                                  | **Có**: Nếu nhiều đầu vào âm, neuron có thể không bao giờ kích hoạt (gradient = 0)                  | Không                                                                                                   | Không                                                                                                                         |
| **Biến thể cải tiến**               | Không có biến thể phổ biến                                                                                                                    | Leaky ReLU, ELU, PReLU, Swish...                                                                    | Không có                                                                                                | Không có                                                                                                                      |
| **Khả năng gây exploding gradient** | Không                                                                                                                                         | Ít (vì gradient = 1 khi x>0, có thể khuếch đại, nhưng không phổ biến)                               | Không                                                                                                   | Không                                                                                                                         |

Câu hỏi 1: How is the softmax activation function typically used in next-word prediction models?

_Đáp án đúng của chuyên gia:_ **A. To normalize the output probabilities over multiple words.**

**1. Bản chất Toán học (Mathematical Essence):** Trong các mô hình sinh văn bản (như RNN, LSTM, hay siêu mô hình Transformer của GPT-4), lớp ẩn cuối cùng sẽ xuất ra một vector điểm số thô gọi là **Logits** (z). Các giá trị này có thể âm, dương và không cộng lại bằng 1. Softmax là một hàm ánh xạ (mapping function) biến toàn bộ vector Logits này thành một **phân phối xác suất** hợp lệ. Công thức Toán học Bắt buộc: ai​=Softmax(zi​)=∑j=1V​ezj​ezi​​ _Trong đó:_

- zi​: Điểm số thô (logit) của từ thứ i trong từ điển.
- V: Kích thước từ điển (Vocabulary size - ví dụ 10,000 từ).
- Mẫu số ∑ezj​: Là hằng số chuẩn hóa, đảm bảo tổng xác suất của tất cả các từ cộng lại chính xác bằng 1. Hàm mũ (ex) ép mọi giá trị phải lớn hơn 0 và đẩy sự chênh lệch lên cao (từ nào điểm cao sẽ chiếm gần hết xác suất).

---

## Related
- [[Deep Learning Overview]]
- [[Neural Network Fundamentals]]
