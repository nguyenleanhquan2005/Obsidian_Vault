## Mathematics

### 1. Numbers and Arrays (Số và Mảng)

| **Ký hiệu**               | Meaning                                   | **Ý nghĩa**                                                                   |
| ------------------------- | ----------------------------------------- | ----------------------------------------------------------------------------- |
| $a$                       | A scalar (integer or real)                | Một scalar (số nguyên hoặc số thực)                                           |
| $\mathbf{a}$              | A vector                                  | Một vector                                                                    |
| $\mathbf{A}$              | A matrix                                  | Một ma trận                                                                   |
| $\mathsf{A}$              | A tensor                                  | Một tensor                                                                    |
| $\mathbf{I}_n$            | Identity matrix with n rows and n columns | Ma trận đơn vị với $n$ hàng và $n$ cột                                        |
| $\mathbf{I}$              |                                           | Ma trận đơn vị với kích thước được ngầm định bởi ngữ cảnh                     |
| $\mathbf{e}^{(i)}$        |                                           | Vector cơ sở chuẩn $[0, \dots, 0, 1, 0, \dots, 0]$ với giá trị 1 ở vị trí $i$ |
| $\text{diag}(\mathbf{a})$ |                                           | Ma trận đường chéo vuông với các phần tử trên đường chéo là $\mathbf{a}$      |
| $\text{a}$                |                                           | Một biến ngẫu nhiên vô hướng (scalar random variable)                         |
| $\mathbf{a}$              |                                           | Một biến ngẫu nhiên vector (vector-valued random variable)                    |
| $\mathbf{A}$              |                                           | Một biến ngẫu nhiên ma trận (matrix-valued random variable)                   |

---

### 2. Sets and Graphs (Tập hợp và Đồ thị)

| **Ký hiệu**                       | **Ý nghĩa**                                                                      |
| --------------------------------- | -------------------------------------------------------------------------------- |
| $\mathbb{A}$                      | Một tập hợp                                                                      |
| $\mathbb{R}$                      | Tập hợp các số thực                                                              |
| $\{0, 1\}$                        | Tập hợp chứa 0 và 1                                                              |
| $\{0, 1, \dots, n\}$              | Tập hợp tất cả các số nguyên từ 0 đến $n$                                        |
| $[a, b]$                          | Khoảng số thực bao gồm cả $a$ và $b$                                             |
| $(a, b]$                          | Khoảng số thực không bao gồm $a$ nhưng bao gồm $b$                               |
| $\mathbb{A} \setminus \mathbb{B}$ | Phép trừ tập hợp (các phần tử thuộc $\mathbb{A}$ nhưng không thuộc $\mathbb{B}$) |
| $\mathcal{G}$                     | Một đồ thị                                                                       |
| $Pa_{\mathcal{G}}(x_i)$           | Các nút cha của $x_i$ trong đồ thị $\mathcal{G}$                                 |

---

### 3. Indexing (Chỉ mục)

| **Ký hiệu**          | **Ý nghĩa**                                                      |
| -------------------- | ---------------------------------------------------------------- |
| $a_i$                | Phần tử thứ $i$ của vector $\mathbf{a}$ (bắt đầu từ 1)           |
| $\mathbf{a}_{-i}$    | Tất cả các phần tử của vector $\mathbf{a}$ ngoại trừ phần tử $i$ |
| $A_{i,j}$            | Phần tử ở hàng $i$, cột $j$ của ma trận $\mathbf{A}$             |
| $\mathbf{A}_{i,:}$   | Hàng thứ $i$ của ma trận $\mathbf{A}$                            |
| $\mathbf{A}_{:,i}$   | Cột thứ $i$ của ma trận $\mathbf{A}$                             |
| $\mathsf{A}_{i,j,k}$ | Phần tử $(i, j, k)$ của một tensor 3 chiều $\mathsf{A}$          |
| $\mathsf{A}_{:,:,i}$ | Một lát cắt 2 chiều của tensor 3 chiều                           |
| $\text{a}_i$         | Phần tử thứ $i$ của biến ngẫu nhiên vector $\mathbf{a}$          |

---

### 4. Linear Algebra Operations (Đại số tuyến tính)

| **Ký hiệu**                   | **Ý nghĩa**                                                                  |
| ----------------------------- | ---------------------------------------------------------------------------- |
| $\mathbf{A}^\top$             | Chuyển vị của ma trận $\mathbf{A}$                                           |
| $\mathbf{A}^+$                | Nghịch đảo giả Moore-Penrose của $\mathbf{A}$                                |
| $\mathbf{A} \odot \mathbf{B}$ | Tích Hadamard (nhân từng phần tử tương ứng) của $\mathbf{A}$ và $\mathbf{B}$ |
| $\text{det}(\mathbf{A})$      | Định thức của ma trận $\mathbf{A}$                                           |

---

### 5. Calculus (Giải tích)

|**Ký hiệu**|**Ý nghĩa**|
|---|---|
|$\frac{dy}{dx}$|Đạo hàm của $y$ theo biến $x$|
|$\frac{\partial y}{\partial x}$|Đạo hàm riêng của $y$ theo biến $x$|
|$\nabla_{\mathbf{x}}y$|Gradient của $y$ theo vector $\mathbf{x}$|
|$\nabla_{\mathbf{X}}y$|Đạo hàm ma trận của $y$ theo ma trận $\mathbf{X}$|
|$\frac{\partial \mathbf{f}}{\partial \mathbf{x}}$|Ma trận Jacobian $\mathbf{J} \in \mathbb{R}^{m \times n}$ của hàm $\mathbf{f} : \mathbb{R}^n \rightarrow \mathbb{R}^m$|
|$\nabla^2_{\mathbf{x}}f(\mathbf{x})$ hoặc $\mathbf{H}(f)(\mathbf{x})$|Ma trận Hessian của hàm $f$ tại điểm $\mathbf{x}$|
|$\int f(\mathbf{x}) d\mathbf{x}$|Tích phân xác định trên toàn bộ miền xác định của $\mathbf{x}$|

---
### 6. Probability and Information Theory (Xác suất & Lý thuyết thông tin)

| **Ký hiệu**                                                      | **Ý nghĩa**                                                                                                    |                                                    |
| ---------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- |
| $\text{a} \perp \text{b}$                                        | Hai biến ngẫu nhiên $\text{a}$ và $\text{b}$ độc lập với nhau                                                  |                                                    |
| $\text{a} \perp \text{b} \mid \text{c}$                          | Độc lập có điều kiện khi biết $\text{c}$                                                                       |                                                    |
| $P(\text{a})$                                                    | Phân phối xác định trên một biến rời rạc                                                                       |                                                    |
| $p(\text{a})$                                                    | Phân phối xác định trên một biến liên tục                                                                      |                                                    |
| $\text{a} \sim P$                                                | Biến ngẫu nhiên $\text{a}$ có phân phối $P$                                                                    |                                                    |
| $\mathbb{E}_{\text{x} \sim P}[f(x)]$                             | Kỳ vọng của $f(x)$ đối với phân phối $P(x)$                                                                    |                                                    |
| $\text{Var}(f(x))$                                               | Phương sai của $f(x)$                                                                                          |                                                    |
| $H(\text{x})$                                                    | Entropy Shannon của biến ngẫu nhiên $\text{x}$                                                                 |                                                    |
| $D_{KL}(P \\                                                     | Q$                                                                                                             | Độ đo khoảng cách Kullback-Leibler giữa $P$ và $Q$ |
| $\mathcal{N}(\mathbf{x}; \boldsymbol{\mu}, \boldsymbol{\Sigma})$ | Phân phối Gaussian của $\mathbf{x}$ với trung bình $\boldsymbol{\mu}$ và hiệp phương sai $\boldsymbol{\Sigma}$ |                                                    |

---
### 7. Functions (Hàm số)

| **Ký hiệu**                            | **Ý nghĩa**                                                            |     |                              |
| -------------------------------------- | ---------------------------------------------------------------------- | --- | ---------------------------- |
| $f: \mathbb{A} \rightarrow \mathbb{B}$ | Hàm số $f$ với miền xác định $\mathbb{A}$ và miền giá trị $\mathbb{B}$ |     |                              |
| $f \circ g$                            | Hàm hợp của $f$ và $g$                                                 |     |                              |
| $\sigma(x)$                            | Hàm Logistic sigmoid: $\frac{1}{1 + \exp(-x)}$                         |     |                              |
| $\zeta(x)$                             | Hàm Softplus: $\log(1 + \exp(x))$                                      |     |                              |
| $\\                                    | \mathbf{x}\\                                                           | $   | Chuẩn $L^p$ của $\mathbf{x}$ |
| $x^+$                                  | Phần dương của $x$: $\max(0, x)$                                       |     |                              |
| $\mathbf{1}_{\text{condition}}$        | Hàm chỉ thị (trả về 1 nếu điều kiện đúng, ngược lại trả về 0)          | -   |                              |

---
### 8. Datasets and Distributions (Tập dữ liệu và Phân phối)

| **Ký hiệu**             | **Ý nghĩa**                                                                                          |
| ----------------------- | ---------------------------------------------------------------------------------------------------- |
| $p_{\text{data}}$       | Phân phối tạo dữ liệu thực tế                                                                        |
| $\hat{p}_{\text{data}}$ | Phân phối thực nghiệm được xác định bởi tập huấn luyện                                               |
| $\mathbb{X}$            | Tập hợp các ví dụ huấn luyện                                                                         |
| $\mathbf{x}^{(i)}$      | Ví dụ thứ $i$ (đầu vào) từ một tập dữ liệu                                                           |
| $y^{(i)}$               | Mục tiêu (target/label) tương ứng với đầu vào $\mathbf{x}^{(i)}$                                     |
| $\mathbf{X}$            | Ma trận kích thước $m \times n$ chứa các ví dụ đầu vào, với mỗi hàng $\mathbf{X}_{i,:}$ là một ví dụ |

## Machine Learning

| Words              | Meaning | **Ý nghĩa**                                                                                          |
| ------------------ | ------- | ---------------------------------------------------------------------------------------------------- |
| Autoencoder        |         | Phân phối tạo dữ liệu thực tế                                                                        |
| Encoder            |         | Phân phối thực nghiệm được xác định bởi tập huấn luyện                                               |
| $\mathbb{X}$       |         | Tập hợp các ví dụ huấn luyện                                                                         |
| $\mathbf{x}^{(i)}$ |         | Ví dụ thứ $i$ (đầu vào) từ một tập dữ liệu                                                           |
| $y^{(i)}$          |         | Mục tiêu (target/label) tương ứng với đầu vào $\mathbf{x}^{(i)}$                                     |
| $\mathbf{X}$       |         | Ma trận kích thước $m \times n$ chứa các ví dụ đầu vào, với mỗi hàng $\mathbf{X}_{i,:}$ là một ví dụ |
