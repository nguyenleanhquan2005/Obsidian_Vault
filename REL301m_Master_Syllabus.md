`# 📘 REL301m – Fundamentals of Reinforcement Learning (Tài liệu ôn thi tổng hợp)

> [!IMPORTANT]
> **Tài liệu hệ thống hóa toàn bộ kiến thức trọng tâm môn Học Tăng Cường (Reinforcement Learning - REL301m).**
> Được biên soạn dựa trên chương trình đào tạo của Đại học Alberta (Coursera) bao gồm:
> 1. *Fundamentals of Reinforcement Learning* (Cơ sở RL & MDPs)
> 2. *Sample-based Learning Methods* (MC, TD, Dyna-Q)
> 3. *Prediction and Control with Function Approximation* (Xấp xỉ hàm, Policy Gradient, Actor-Critic)
> 4. *Guided Project* (Tic-Tac-Toe & Capstone System)
>
> Tài liệu tích hợp công thức toán học LaTeX chuẩn xác, các bảng so sánh trực quan, bộ từ khóa phản xạ nhanh (Cheat-sheet) và 20 câu hỏi trắc nghiệm ôn tập kèm lời giải chi tiết.

---

## 📌 MỤC LỤC
1. [Phần 1: Cơ sở của Học tăng cường (Chương 1)](#phần-1-cơ-sở-của-học-tăng-cường-chương-1)
2. [Phần 2: Phương pháp dạng bảng dựa trên mẫu (Chương 2)](#phần-2-phương-pháp-dạng-bảng-dựa-trên-mẫu-chương-2)
3. [Phần 3: Xấp xỉ hàm & Học tăng cường sâu (Chương 3)](#phần-3-xấp-xỉ-hàm--học-tăng-cường-sâu-chương-3)
4. [Phần 4: Xây dựng hệ thống hoàn chỉnh & Dự án Tic-Tac-Toe](#phần-4-xây-dựng-hệ-thống-hoàn-chỉnh--dự-án-tic-tac-toe)
5. [🔑 Bí kíp phản xạ từ khóa nhanh (Exam Cheat-sheet)](#-bí-kíp-phản-xạ-từ-khóa-nhanh-exam-cheat-sheet)
6. [💡 Mẹo làm trắc nghiệm & Cách nhớ sâu kiến thức](#-mẹo-làm-trắc-nghiệm--cách-nhớ-sâu-kiến-thức)
7. [📚 Bộ 30 câu hỏi trắc nghiệm ôn tập (AI1910 - Lưu Giang Nam)](#-bộ-30-câu-hỏi-trắc-nghiệm-ôn-tập-ai1910---lưu-giang-nam)

---

## PHẦN 1: CƠ SỞ CỦA HỌC TĂNG CƯỜNG (CHƯƠNG 1)

Reward scaler feedback signal provided by the environment to the learning agent
### 1. K-Armed Bandit & Sự đánh đổi Exploration vs. Exploitation
Bài toán K-Armed Bandit là mô hình cơ bản nhất của RL, nơi Agent đối mặt với các hành động độc lập không thay đổi trạng thái môi trường nhằm tối đa hóa phần thưởng nhận được.

* **Công thức cập nhật giá trị hành động (Incremental Update):**
  $$Q_{n+1}(A) = Q_n(A) + \alpha_n \left[ R_n - Q_n(A) \right]$$
  Trong đó:
  * $\alpha_n = \frac{1}{N_n(A)}$: Trung bình số học (Sample-average) cho bài toán tĩnh (stationary).
  * $\alpha_n = \alpha \in (0, 1]$: Hằng số tốc độ học (Constant step-size) cho bài toán biến động theo thời gian (non-stationary).
* **Upper Confidence Bound (UCB):** Cân bằng Exploration bằng cách thêm hệ số bất định vào ước lượng:
  $$A_t \doteq \arg\max_{a} \left[ Q_t(a) + c \sqrt{\frac{\ln t}{N_t(a)}} \right]$$
  *Nếu $N_t(a) = 0$, hành động $a$ sẽ được chọn tối đa.*
* **Giá trị khởi tạo lạc quan (Optimistic Initial Values):** Thiết lập $Q_1(a)$ rất cao để khuyến khích Exploration mạnh mẽ ở các bước đầu tiên.

#### ❖ Ứng dụng thực tiễn của K-Armed Bandit:
* **Tối ưu hóa tỷ lệ click quảng cáo (Ad CTR Optimization):** Hiển thị quảng cáo có tỷ lệ click cao đã biết (Exploit) hay thử nghiệm quảng cáo mới (Explore) để tìm quảng cáo hấp dẫn hơn.
* **Thử nghiệm lâm sàng y khoa (Clinical Trials):** Phân bổ bệnh nhân vào phác đồ điều trị hiệu quả tốt nhất hiện tại (Exploit) hoặc thử phác đồ mới để kiểm chứng hiệu quả thực tế (Explore).
	* **Hệ thống gợi ý (Recommender Systems):** Gợi ý bài hát/video đúng gu người dùng (Exploit) hay thử đề xuất thể loại mới để khám phá sở thích ẩn (Explore).

---

### 2. Markov Decision Process (MDP)
MDP là khung toán học chuẩn hóa để mô tả tương tác giữa **Agent** và **Environment** thông qua Trạng thái (State), Hành động (Action) và Phần thưởng (Reward).

* **Hàm phân bố xác suất chuyển đổi trạng thái (Transition Dynamics):**
  $$p(s', r | s, a) \doteq \mathbb{P}(S_t = s', R_t = r \mid S_{t-1} = s, A_{t-1} = a)$$
  Thỏa mãn thuộc tính Markov: trạng thái tiếp theo $S_t$ chỉ phụ thuộc vào trạng thái hiện tại $S_{t-1}$ và hành động $A_{t-1}$.
* **Phân loại Tác vụ (Tasks):**
  * **Episodic Tasks:** Có điểm kết thúc rõ ràng (Terminal State $S_T$). Tổng phần thưởng (Return): $G_t = R_{t+1} + R_{t+2} + \dots + R_T$.
  * **Continuing Tasks:** Chạy vô hạn. Sử dụng hệ số chiết khấu $\gamma \in [0, 1)$ để tính tổng phần thưởng hữu hạn:
    $$G_t = \sum_{k=0}^{\infty} \gamma^k R_{t+k+1}$$

#### ❖ Ứng dụng thực tiễn của MDP:
* **Quản lý kho hàng (Inventory Management):** Trạng thái là lượng hàng hiện tại, hành động là số lượng nhập thêm, phần thưởng là doanh thu trừ đi chi phí lưu trữ/phạt thiếu hàng.
* **Tối ưu hóa danh mục đầu tư (Financial Portfolio Optimization):** Trạng thái là số dư tài khoản và xu hướng thị trường, hành động là tỷ lệ phân bổ tài sản, phần thưởng là tăng trưởng lợi nhuận dài hạn.

---

### 3. Phương trình Bellman (Bellman Equations)
Các phương trình Bellman thiết lập mối liên hệ đệ quy giữa hàm giá trị hiện tại và các trạng thái kế tiếp.

* **Bellman Expectation Equation cho $v_\pi(s)$:**
  $$v_\pi(s) = \sum_{a} \pi(a|s) \sum_{s', r} p(s', r | s, a) \left[ r + \gamma v_\pi(s') \right]$$
* **Bellman Expectation Equation cho $q_\pi(s, a)$:**
  $$q_\pi(s, a) = \sum_{s', r} p(s', r | s, a) \left[ r + \gamma \sum_{a'} \pi(a'|s') q_\pi(s', a') \right]$$
* **Bellman Optimality Equation cho $v_*(s)$:**
  $$v_*(s) = \max_{a} \sum_{s', r} p(s', r | s, a) \left[ r + \gamma v_*(s') \right]$$
* **Bellman Optimality Equation cho $q_*(s, a)$:**
  $$q_*(s, a) = \sum_{s', r} p(s', r | s, a) \left[ r + \gamma \max_{a'} q_*(s', a') \right]$$

---

### 4. Quy hoạch động (Dynamic Programming - DP)
DP yêu cầu **mô hình hoàn hảo** của môi trường (biết trước $p(s',r|s,a)$).

* **Policy Evaluation (Prediction):** Sử dụng Bellman Expectation Equation làm quy tắc cập nhật lặp để tìm $v_\pi$.
* **Policy Improvement (Control):** Cải thiện chính sách bằng cách chọn hành động tham lam theo hàm giá trị hiện tại:
  $$\pi'(s) \doteq \arg\max_{a} \sum_{s', r} p(s', r | s, a) \left[ r + \gamma v_\pi(s') \right]$$
* **Policy Iteration:** Thực hiện lặp lại chu kỳ Đánh giá chính sách và Cải thiện chính sách cho đến khi hội tụ:
  $$\pi_0 \xrightarrow{E} v_{\pi_0} \xrightarrow{I} \pi_1 \xrightarrow{E} v_{\pi_1} \dots \xrightarrow{I} \pi_* \xrightarrow{E} v_*$$
* **Value Iteration:** Tích hợp trực tiếp bước tối ưu hóa vào mỗi vòng lặp bằng cách chuyển đổi phương trình tối ưu Bellman thành quy tắc cập nhật (không cần đợi chính sách hội tụ):
  $$v_{k+1}(s) \doteq \max_{a} \sum_{s', r} p(s', r | s, a) \left[ r + \gamma v_k(s') \right]$$
* **Generalized Policy Iteration (GPI):** Khái niệm tổng quát mô tả sự tương tác giữa tiến trình đánh giá (Evaluation) và cải thiện (Improvement) nhằm hướng tới giá trị tối ưu.

#### ❖ Ứng dụng thực tiễn của DP:
* **Định tuyến gói tin trong mạng (Network Routing):** Tìm đường đi ngắn nhất thông qua bảng định tuyến được tính toán trước bằng các thuật toán đệ quy (như Bellman-Ford).
* **Lập lịch tài nguyên (Resource Allocation):** Phân bổ công suất phát của các trạm viễn thông hoặc năng lượng của lưới điện thông minh dựa trên mô hình phụ tải biết trước.

---

## PHẦN 2: PHƯƠNG PHÁP DẠNG BẢNG DỰ TRÊN MẪU (CHƯƠNG 2)

Không giống như Quy hoạch động, các phương pháp dựa trên mẫu **không cần biết trước mô hình môi trường** ($p(s',r|s,a)$) mà học trực tiếp từ các chuỗi trải nghiệm thực tế.

### 1. Phương pháp Monte Carlo (MC)
* **Đặc điểm:** Chỉ cập nhật giá trị sau khi một tập (Episode) hoàn thành hoàn toàn (Offline learning).
* **Phân loại:**
  * *First-visit MC:* Chỉ tính toán phần thưởng nhận được từ lần đầu tiên ghé thăm trạng thái $s$ trong một Episode.
  * *Every-visit MC:* Tính toán trung bình phần thưởng cho tất cả các lần ghé thăm trạng thái $s$ trong Episode.
* **Exploring Starts:** Giả định mọi cặp trạng thái - hành động đều có xác suất được chọn làm điểm khởi đầu để đảm bảo tính khám phá.
* **On-policy vs. Off-policy:**
  * **On-policy:** Học về chính sách $\pi$ bằng dữ liệu được sinh ra bởi chính $\pi$. Để duy trì khám phá, $\pi$ thường được cấu hình là $\epsilon$-soft.
  * **Off-policy:** Học về chính sách mục tiêu $\pi$ (Target policy) từ dữ liệu sinh ra bởi một chính sách hành vi $b$ (Behavior policy) khác.
* **Tỷ số tầm quan trọng (Importance Sampling Ratio):**
  $$\rho_{t:T-1} \doteq \prod_{k=t}^{T-1} \frac{\pi(A_k|S_k)}{b(A_k|S_k)}$$
  * **Ordinary Importance Sampling (Phương sai vô hạn, không chệch):**
    $$V(s) \doteq \frac{\sum_{t \in \mathcal{T}(s)} \rho_{t:T(t)-1} G_t}{|\mathcal{T}(s)|}$$
  * **Weighted Importance Sampling (Phương sai hữu hạn, bị chệch nhưng thực tế dùng nhiều hơn):**
    $$V(s) \doteq \frac{\sum_{t \in \mathcal{T}(s)} \rho_{t:T(t)-1} G_t}{\sum_{t \in \mathcal{T}(s)} \rho_{t:T(t)-1}}$$

#### ❖ Ứng dụng thực tiễn của Monte Carlo:
* **Trò chơi có kết thúc (Blackjack, Poker, Tic-Tac-Toe):** Đánh giá sức mạnh của các nước đi hoặc chiến thuật bằng cách tự đấu thử nghiệm hàng triệu ván đấu hoàn chỉnh để tính trung bình phần thưởng.
* **Mô phỏng rủi ro và định giá phái sinh tài chính:** Đánh giá các kịch bản biến động thị trường qua nhiều quỹ đạo đóng để tính toán giá trị rủi ro tối đa (VaR).

---

### 2. Temporal Difference (TD) Learning
TD kết hợp ưu điểm của MC (học từ thực tế) và DP (tự khởi động - bootstrapping, cập nhật dựa trên ước lượng khác mà không cần đợi kết thúc tập).

* **Cập nhật TD(0) (One-step TD):**
  $$V(S_t) \leftarrow V(S_t) + \alpha \left[ R_{t+1} + \gamma V(S_{t+1}) - V(S_t) \right]$$
  * **TD Target:** $R_{t+1} + \gamma V(S_{t+1})$
  * **TD Error ($\delta_t$):** $R_{t+1} + \gamma V(S_{t+1}) - V(S_t)$
* **TD Control Algorithms:**

| Thuật toán         | Loại chính sách        | Quy tắc cập nhật hành động tiếp theo                                                                                                                                                         | Ưu điểm / Nhược điểm                                                                                |
| :----------------- | :--------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------- |
| **Sarsa**          | On-policy              | Dùng hành động thực tế tiếp theo $A_{t+1}$ được chọn bởi $\pi$:<br>$Q(S_t, A_t) \leftarrow Q(S_t, A_t) + \alpha [R_{t+1} + \gamma Q(S_{t+1}, A_{t+1}) - Q(S_t, A_t)]$                        | An toàn, tránh các khu vực nguy hiểm có phần thưởng phạt cao (ví dụ: Cliff Walking).                |
| **Q-Learning**     | Off-policy             | Dùng hành động tối ưu (greedy) bất kể hành động thực tế tiếp theo:<br>$Q(S_t, A_t) \leftarrow Q(S_t, A_t) + \alpha [R_{t+1} + \gamma \max_{a} Q(S_{t+1}, a) - Q(S_t, A_t)]$                  | Học trực tiếp chính sách tối ưu, nhưng dễ bị **Overestimation Bias** (thiên kiến đánh giá quá cao). |
| **Expected Sarsa** | On-policy / Off-policy | Sử dụng giá trị kỳ vọng của tất cả hành động khả thi tại $S_{t+1}$:<br>$Q(S_t, A_t) \leftarrow Q(S_t, A_t) + \alpha [R_{t+1} + \gamma \sum_{a} \pi(a\|S_{t+1}) Q(S_{t+1}, a) - Q(S_t, A_t)]$ | Giảm phương sai so với Sarsa thông thường; tốn thêm chi phí tính toán kỳ vọng.                      |

* **Double Q-Learning:** Giải quyết vấn đề thiên kiến đánh giá quá cao bằng cách sử dụng hai bảng độc lập ($Q_1, Q_2$), bảng này ước lượng giá trị cho hành động được chọn greedy bởi bảng kia.

#### ❖ Ứng dụng thực tiễn của TD Learning:
* **Hệ thống điều hướng xe tự hành (Autonomous Driving):** Xe học cách giữ khoảng cách an toàn, bám làn và rẽ hướng theo thời gian thực dựa trên các phản hồi phạt (khi lệch làn) cập nhật tức thì qua từng giây.
* **Game AI (TD-Gammon):** Tác nhân tự học cách chơi cờ Backgammon ở cấp độ thế giới bằng cách tự đấu và tự cập nhật điểm số ước lượng sau mỗi nước đi đơn lẻ.

---

### 3. Model & Planning (Kiến trúc Dyna)
* **Model:** Định nghĩa cách môi trường phản hồi.
  * *Sample Model:* Chỉ sinh ra một mẫu trạng thái kế tiếp và phần thưởng ngẫu nhiên theo phân bố xác suất.
  * *Distribution Model:* Cung cấp toàn bộ phân bố xác suất của tất cả các trạng thái kế tiếp khả thi.
* **Planning (Lập kế hoạch):** Quá trình sử dụng mô hình giả lập để tạo ra trải nghiệm ảo (Simulated Experience) nhằm cập nhật hàm giá trị hoặc chính sách.
* **Kiến trúc Dyna-Q:** Tích hợp trực tiếp việc học từ môi trường thật (Direct RL) và lập kế hoạch từ mô hình giả lập (Planning):
```mermaid
graph TD
    A[Real Experience] -->|Direct RL| B(Value/Policy)
    A -->|Model Learning| C[Model]
    C -->|Search Control| D[Simulated Experience]
    D -->|Planning| B
    B -->|Acting| E[Environment]
    E --> A
```
* **Dyna-Q+:** Giải quyết các mô hình thiếu chính xác (Inaccurate Models) khi môi trường thay đổi. Thuật toán cộng thêm một lượng phần thưởng khám phá (exploration bonus) cho các trạng thái đã lâu không được ghé thăm:
  $$R^{planning} = R + \kappa \sqrt{\tau}$$
  Với $\tau$ là số bước trôi qua kể từ lần cuối cùng cặp trạng thái-hành động đó được trải nghiệm ngoài thực tế, và $\kappa$ là một hằng số nhỏ.

#### ❖ Ứng dụng thực tiễn của Dyna-Q:
* **Huấn luyện cánh tay robot (Robotic Manipulation):** Giảm thiểu va chạm vật lý gây hỏng hóc thiết bị bằng cách học một mô hình mô phỏng môi trường (Model), sau đó chạy giả lập hàng ngàn lượt trong đầu (Planning) để tinh chỉnh chính sách trước khi thực thi thực tế.

---

## PHẦN 3: XẤP XỈ HÀM & HỌC TĂNG CƯỜNG SÂU (CHƯƠNG 3)

Khi không gian trạng thái quá lớn hoặc liên tục (như cờ vây hay robot tự hành), phương pháp dạng bảng (Tabular) không còn khả thi. Chúng ta bắt buộc phải sử dụng hàm xấp xỉ tham số hóa (Mạng nơ-ron, hàm tuyến tính).

### 1. Hàm mục tiêu xấp xỉ trị số (Value Function Approximation)
* **Hàm mục tiêu On-policy Prediction ($\overline{\text{VE}}$):**
  $$\overline{\text{VE}}(\mathbf{w}) \doteq \sum_{s \in \mathcal{S}} d(s) \left[ v_\pi(s) - \hat{v}(s, \mathbf{w}) \right]^2$$
  Trong đó:
  * $\mathbf{w}$: Vector trọng số của mô hình xấp xỉ.
  * $d(s)$: Phân bố trạng thái ổn định (State distribution) dưới chính sách $\pi$.
* **Cập nhật Semi-gradient TD(0):**
  $$\mathbf{w}_{t+1} \doteq \mathbf{w}_t + \alpha \left[ R_{t+1} + \gamma \hat{v}(S_{t+1}, \mathbf{w}_t) - \hat{v}(S_t, \mathbf{w}_t) \right] \nabla \hat{v}(S_t, \mathbf{w}_t)$$
  *Giải thích: Gọi là "Semi-gradient" vì mục tiêu (TD Target) phụ thuộc vào trọng số hiện tại $\mathbf{w}_t$, bỏ qua đạo hàm của thành phần này trong quá trình tối ưu.*

#### ❖ Ứng dụng thực tiễn của Xấp xỉ hàm & Học tăng cường sâu (Deep RL):
* **Học máy cho các trò chơi phức tạp (AlphaGo, AlphaZero, Atari):** Sử dụng mạng nơ-ron tích chập (CNN) hoặc mạng nơ-ron truyền thẳng để biểu diễn bàn cờ hoặc khung hình game làm đặc trưng trạng thái, giúp xử lý không gian trạng thái vô hạn mà bảng tra cứu thông thường không thể lưu trữ.

---

### 2. Feature Construction trong phương pháp tuyến tính
Với phương pháp tuyến tính: $\hat{v}(s, \mathbf{w}) = \mathbf{w}^T \mathbf{x}(s)$. Hiệu quả phụ thuộc rất lớn vào cách thiết lập vector đặc trưng $\mathbf{x}(s)$:
* **State Aggregation:** Chia không gian trạng thái thành các nhóm/miền rời rạc. Các trạng thái trong cùng một nhóm chia sẻ cùng một giá trị ước lượng.
* **Coarse Coding:** Biểu diễn các đặc trưng bằng các vùng chồng lấn nhau.
* **Tile Coding:** Một dạng Coarse Coding đa chiều hiệu quả. Không gian trạng thái được chia nhỏ bởi nhiều lưới phân vùng (tilings) dịch chuyển lệch nhau. Mỗi trạng thái sẽ kích hoạt chính xác một ô (tile) trong mỗi tiling.
* **Radial Basis Functions (RBF):** Xấp xỉ liên tục bằng cách sử dụng các hàm phân bố Gaussian để biểu diễn mức độ gần của trạng thái với các tâm điểm xác định.

---

### 3. Tác vụ tiếp diễn với Phần thưởng trung bình (Average Reward Settings)
Trong các continuing tasks không phân rã, việc sử dụng hệ số chiết khấu $\gamma$ với hàm xấp xỉ có thể dẫn đến các vấn đề về hội tụ. Do đó, người ta chuyển sang tối ưu **Tốc độ phần thưởng trung bình (Average Reward Rate)**:

* **Tốc độ phần thưởng trung bình:**
  $$r(\pi) \doteq \lim_{h \to \infty} \frac{1}{h} \sum_{t=1}^{h} \mathbb{E}[R_t \mid A_{0:t-1} \sim \pi]$$
* **Hàm lợi nhuận sai lệch (Differential Return):**
  $$G_t \doteq \sum_{k=1}^{\infty} \left( R_{t+k} - r(\pi) \right)$$
* **Lỗi TD sai lệch (Differential TD Error):**
  $$\delta_t \doteq R_{t+1} - \bar{R}_t + \hat{v}(S_{t+1}, \mathbf{w}_t) - \hat{v}(S_t, \mathbf{w}_t)$$
  Trong đó $\bar{R}_t$ là giá trị ước lượng của phần thưởng trung bình $r(\pi)$, được cập nhật liên tục qua mỗi bước:
  $$\bar{R}_{t+1} \leftarrow \bar{R}_t + \beta \delta_t$$

---

### 4. Thuật toán Policy Gradient & Actor-Critic
Thay vì tối ưu hóa hàm giá trị rồi suy ra chính sách, các phương pháp Policy Gradient tối ưu hóa trực tiếp các tham số $\boldsymbol{\theta}$ của chính sách $\pi(a|s, \boldsymbol{\theta})$.

* **Các dạng tham số hóa chính sách (Policy Parameterizations):**
  * **Softmax Policy (Cho hành động rời rạc):**
    $$\pi(a|s, \boldsymbol{\theta}) \doteq \frac{e^{h(s, a, \boldsymbol{\theta})}}{\sum_{b} e^{h(s, b, \boldsymbol{\theta})}}$$
  * **Gaussian Policy (Cho hành động liên tục):**
    $$\pi(a|s, \boldsymbol{\theta}) \doteq \frac{1}{\sigma(s, \boldsymbol{\theta})\sqrt{2\pi}} \exp\left( -\frac{(a - \mu(s, \boldsymbol{\theta}))^2}{2\sigma(s, \boldsymbol{\theta})^2} \right)$$
* **Định lý Policy Gradient (Policy Gradient Theorem):**
  $$\nabla J(\boldsymbol{\theta}) \propto \sum_{s} d^\pi(s) \sum_{a} q_\pi(s, a) \nabla \pi(a|s, \boldsymbol{\theta})$$
* **Thuật toán REINFORCE (Monte Carlo Policy Gradient):**
  $$\boldsymbol{\theta}_{t+1} \doteq \boldsymbol{\theta}_t + \alpha G_t \nabla \ln \pi(A_t | S_t, \boldsymbol{\theta}_t)$$
* **Kiến trúc Actor-Critic:**
  * **Actor (Tham số $\boldsymbol{\theta}$):** Đóng vai trò thực thi hành động, cập nhật tham số chính sách theo chiều tăng của gradient:
    $$\boldsymbol{\theta}_{t+1} \leftarrow \boldsymbol{\theta}_t + \alpha^{\boldsymbol{\theta}} \delta_t \nabla \ln \pi(A_t | S_t, \boldsymbol{\theta}_t)$$
  * **Critic (Tham số $\mathbf{w}$):** Đóng vai trò đánh giá, cập nhật hàm giá trị trạng thái $v(s, \mathbf{w})$ bằng cách sử dụng lỗi TD để dẫn dắt Actor:
    $$\mathbf{w}_{t+1} \leftarrow \mathbf{w}_t + \alpha^{\mathbf{w}} \delta_t \nabla \hat{v}(S_t, \mathbf{w}_t)$$
  * **Lỗi TD ($\delta_t$):**
    $$\delta_t = R_{t+1} + \gamma \hat{v}(S_{t+1}, \mathbf{w}_t) - \hat{v}(S_t, \mathbf{w}_t)$$

#### ❖ Ứng dụng thực tiễn của Policy Gradient & Actor-Critic:
* **Điều khiển chuyển động liên tục của Robot (Robotic Locomotion):** Robot đi bộ, chạy nhảy hoặc giữ thăng bằng (như robot Spot của Boston Dynamics) đòi hỏi điều khiển lực mô-tơ ở các khớp dưới dạng biến liên tục (Gaussian Policy).
* **Tối ưu hóa phản hồi từ con người (RLHF trong LLMs):** Actor sinh câu trả lời (Softmax Policy trên tập từ vựng), Critic (hoặc Reward Model) đánh giá chất lượng câu trả lời để hướng dẫn Actor phản hồi tự nhiên, chính xác và an toàn hơn.

---

## PHẦN 4: XÂY DỰNG HỆ THỐNG HOÀN CHỈNH & DỰ ÁN TIC-TAC-TOE

### 1. Phân tích thiết kế hệ thống RL Capstone
Quy trình xây dựng một hệ thống RL hoàn chỉnh ứng dụng vào các bài toán công nghiệp thực tế gồm 4 bước:
1. **Định hình bài toán (Problem Formulation):**
   * Định nghĩa chính xác State Space (không gian trạng thái), Action Space (không gian hành động) và Reward Signal (tín hiệu phần thưởng).
   * Đảm bảo phần thưởng phản ánh đúng mục tiêu cuối cùng (Ví dụ: Thắng ván cờ được +1, thua -1; không nên thưởng cho các bước trung gian để tránh Agent "học lách" hệ thống).
2. **Lựa chọn thuật toán phù hợp (Algorithm Selection):**
   * Sử dụng thuật toán Tabular (Q-learning, Sarsa) cho bài toán không gian nhỏ.
   * Sử dụng Function Approximation hoặc Policy Gradient khi không gian trạng thái liên tục hoặc quá lớn.
3. **Triển khai lập trình (Implementation):**
   * Thiết kế môi trường tuân thủ giao thức tiêu chuẩn (như cấu trúc gym/gymnasium: `reset()`, `step()`).
4. **Đánh giá thực nghiệm (Empirical Study):**
   * So sánh hiệu quả của các siêu tham số (Hyperparameters) như $\alpha$, $\epsilon$, $\gamma$. Đánh giá mức độ hội tụ qua đồ thị tổng phần thưởng tích lũy theo số tập học.

### 2. Thiết kế trò chơi Tic-Tac-Toe trong Python
* **State Representation:** Bàn cờ $3 \times 3$ có thể được biểu diễn bằng một mảng 1D hoặc 2D gồm 9 phần tử. Giá trị: `0` (trống), `1` (X), `-1` (O).
* **Action Space:** Tập hợp các vị trí ô trống còn lại trên bàn cờ (từ 0 đến 8).
* **Reward Structure:**
  * Thắng ván đấu: $+10$ (hoặc $+1$).
  * Thua ván đấu: $-10$ (hoặc $-1$).
  * Hòa hoặc các bước đi bình thường không kết thúc game: $0$.
* **Thuật toán áp dụng tối ưu:** Q-learning hoặc Monte Carlo Control là lựa chọn lý tưởng cho Tic-Tac-Toe vì số lượng trạng thái tối đa của bàn cờ tương đối nhỏ ($\approx 3^9 = 19683$ trạng thái).

---

## 🔑 BÍ KÍP PHẢN XẠ TỪ KHÓA NHANH (EXAM CHEAT-SHEET)

> [!TIP]
> Ghi nhớ các cặp từ khóa cốt lõi dưới đây giúp quét nhanh đề bài tiếng Anh và chọn đáp án chính xác nhất trong phòng thi.

* Thấy **"Finite number of pulls / Optimize winning"** hoặc **"Arm"** $\rightarrow$ Chọn **K-Armed Bandit**.
* Thấy **"Try something new vs Order the same meal"** $\rightarrow$ Chọn **Exploration vs Exploitation Tradeoff**.
* Thấy **"Discount the rewards / Future"** $\rightarrow$ Chọn **Hệ số chiết khấu $\gamma$ (với $0 \le \gamma < 1$)**.
* Thấy **"Relate current and future values"** $\rightarrow$ Chọn **Bellman Equation**.
* Thấy **"Average of the return / Blackjack"** hoặc **"End of episode"** $\rightarrow$ Chọn **Monte Carlo (MC)**.
* Thấy **"Off-policy Temporal Difference Control"** $\rightarrow$ Chọn **Q-Learning**.
* Thấy **"On-policy Temporal Difference Control"** $\rightarrow$ Chọn **Sarsa**.
* Thấy **"Allows for planning / Simulate environment"** $\rightarrow$ Chọn **Model / Planning**.
* Thấy **"Formalism for planning"** $\rightarrow$ Chọn **Dyna (hoặc Dyna-Q)**.
* Thấy **"Minimize mean-squared error / Gradient Descent"** $\rightarrow$ Chọn **Value Function Approximation**.
* Thấy **"Overlapping receptive fields / Multidimensional grids"** $\rightarrow$ Chọn **Tile Coding**.
* Thấy **"Objective for Continuing Tasks with function approximation"** $\rightarrow$ Chọn **Average Reward (Differential Return)**.
* Thấy **"Actor-Critic"** $\rightarrow$ Chọn **Actor cập nhật Policy, Critic cập nhật Value / TD Error**.
* Thấy **"Discrete Actions"** (Hành động rời rạc) $\rightarrow$ Chọn **Softmax Policy**.
* Thấy **"Continuous Actions"** (Hành động liên tục như lái xe) $\rightarrow$ Chọn **Gaussian Policy**.
* Thấy **"Double Q-Learning"** $\rightarrow$ Chọn **Giải quyết Overestimation Bias**.
* Thấy **"Bootstrapping"** $\rightarrow$ Chọn **Cập nhật dựa trên ước lượng khác (TD, DP)** (MC không bootstrap).

---

## 💡 MẸO LÀM TRẮC NGHIỆM & CÁCH NHỚ SÂU KIẾN THỨC

### 1. Mẹo làm bài trắc nghiệm phản xạ nhanh (Exam Tips)
> [!TIP]
> Áp dụng các nguyên lý loại trừ nhanh dưới đây khi làm bài thi trắc nghiệm:

* **Mẹo 1: Nhận diện On-Policy vs. Off-Policy qua công thức:**
  * Nhìn vào phần cập nhật giá trị tương lai:
    * Nếu có hành động thực tế tiếp theo ($A_{t+1}$ hoặc dạng xác suất $\sum_a \pi(a|s)$) $\rightarrow$ Chắc chắn là **On-Policy** (Sarsa, Expected Sarsa).
    * Nếu xuất hiện toán tử tìm cực trị ($\max_{a} Q(s_{t+1}, a)$) hoặc hoàn toàn không phụ thuộc hành động thực tế tiếp theo $\rightarrow$ Chắc chắn là **Off-Policy** (Q-Learning).
* **Mẹo 2: Tam giác quan hệ DP - MC - TD:**
  * **DP (Quy hoạch động):** Có Bootstrap ($V(S_{t+1})$) + Không Sample (phải biết trước mô hình $p$).
  * **MC (Monte Carlo):** Không Bootstrap (phải đợi hết episode lấy $G_t$) + Có Sample (học từ tương tác thực tế).
  * **TD (Temporal Difference):** Có Bootstrap ($V(S_{t+1})$) + Có Sample (học step-by-step ngoài thực tế).
* **Mẹo 3: Phân biệt Reward vs. Value:**
  * **Reward (Phần thưởng):** Do môi trường trả về tức thời tại thời điểm $t$, không phụ thuộc vào chính sách.
  * **Value (Giá trị):** Kỳ vọng tổng phần thưởng trong tương lai, hoàn toàn phụ thuộc vào chính sách đi đứng của Agent.
* **Mẹo 4: Softmax vs. Gaussian trong Policy Gradient:**
  * Không gian hành động **Rời rạc (Discrete)** $\rightarrow$ Dùng **Softmax parameterization**.
  * Không gian hành động **Liên tục (Continuous)** $\rightarrow$ Dùng **Gaussian parameterization**.

---

### 2. Phương pháp nhớ sâu kiến thức Học Tăng Cường
Để biến lý thuyết REL khô khan thành trực quan sinh động, hãy sử dụng các phương pháp liên tưởng sau:

* **Sự khác biệt thực tế giữa Q-learning và Sarsa (Ví dụ Cliff Walking):**
  * Tưởng tượng mép vực nguy hiểm:
    * **Q-learning** là một kẻ liều lĩnh, nó lập kế hoạch dựa trên hành động tối ưu nhất (max) nên nó chọn đi sát mép vực (đường ngắn nhất). Nó quên mất rằng khi chạy thực tế nó vẫn đi ngẫu nhiên để khám phá ($\epsilon$-greedy), dẫn tới việc thỉnh thoảng trượt chân ngã vực.
    * **Sarsa / Expected Sarsa** là người cẩn thận, khi lập kế hoạch nó tính toán cả những bước đi loạng choạng ngẫu nhiên của chính nó (on-policy). Vì thế nó thấy mép vực quá nguy hiểm và chủ động chọn đường vòng xa hơn nhưng an toàn.
* **Tại sao cần Double Q-learning? (Overestimation Bias):**
  * Q-learning thông thường giống như một người nghe tin đồn: luôn chọn giá trị lớn nhất ($\max$). Nếu các ước lượng có nhiễu, toán tử $\max$ sẽ liên tục thiên vị các ước lượng bị phóng đại quá mức.
  * **Double Q-learning** giải quyết bằng cách dùng 2 người độc lập kiểm chứng lẫn nhau: Người A chọn hành động tốt nhất theo ý mình, nhưng Người B sẽ là người định giá hành động đó. Điều này triệt tiêu hoàn toàn thiên kiến đánh giá quá cao.
* **Mối liên kết Dyna (Planning & Learning):**
  * Hãy hình dung **Dyna-Q** giống như một vận động viên: Ban ngày chạy thực tế để lấy kinh nghiệm (Direct RL) và ghi nhớ quy luật (Model Learning). Ban đêm ngủ nằm mơ, tự diễn tập các tình huống giả định trong đầu để cải thiện kỹ năng (Planning).
  * **Dyna-Q+** là vận động viên có thêm tính tò mò ($R_{bonus} = \kappa \sqrt{\tau}$): Nếu có một lối đi nào đó đã quá lâu anh ta chưa đi qua, anh ta sẽ chủ động quay lại kiểm tra xem môi trường có thay đổi gì mới không (phát hiện đường tắt).

---

## 📚 BỘ 30 CÂU HỎI TRẮC NGHIỆM ÔN TẬP (AI1910 - LƯU GIANG NAM)
*(30 PRACTICE MULTIPLE-CHOICE QUESTIONS)*

**Câu 1 (Question 1):** Tín hiệu "Phần thưởng" (Reward) trong cấu trúc Học tăng cường (Reinforcement Learning) có định dạng toán học là gì?
*(What is the mathematical format of the "Reward" signal in the Reinforcement Learning framework?)*

- [ ] A. Một chuỗi (sequence) các trạng thái. *(A sequence of states.)*
- [ ] B. Một vector đa chiều chứa các đặc trưng của môi trường. *(A multidimensional vector containing environmental features.)*
- [x] C. Một giá trị vô hướng (scalar feedback signal). *(A scalar feedback signal.)*
- [ ] D. Một ma trận xác suất chuyển đổi. *(A transition probability matrix.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Theo định nghĩa chuẩn của RL, tín hiệu phần thưởng $R_t$ luôn là một giá trị số vô hướng thực ($R_t \in \mathbb{R}$), đại diện cho phản hồi trực tiếp từ môi trường tại mỗi bước thời gian.
  * **English:** In standard RL, the reward signal $R_t$ is always a scalar real value ($R_t \in \mathbb{R}$), representing direct feedback from the environment at each time step.

**Câu 2 (Question 2):** Trong ứng dụng thử nghiệm lâm sàng y khoa bằng mô hình K-Armed Bandit, "Action" (hành động) và "Reward" (phần thưởng) tương ứng với đại lượng nào trong thực tế?
*(In a clinical trial application using the K-Armed Bandit model, what do "Action" and "Reward" correspond to in practice?)*

- [ ] A. Action: Chọn bác sĩ; Reward: Giá tiền thuốc. *(Action: Choosing a doctor; Reward: Price of medicine.)*
- [x] B. Action: Chọn phác đồ điều trị; Reward: Sự phục hồi/phúc lợi của bệnh nhân. *(Action: Choosing a treatment protocol; Reward: Patient recovery/well-being.)*
- [ ] C. Action: Khám bệnh; Reward: Mức độ chính xác của chẩn đoán. *(Action: Examination; Reward: Accuracy of diagnosis.)*
- [ ] D. Action: Bệnh nhân uống thuốc; Reward: Tác dụng phụ của thuốc. *(Action: Patient taking medicine; Reward: Side effects of medicine.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Mỗi cánh tay (arm) của Bandit tương ứng với một phác đồ điều trị (Action). Mục tiêu là tối đa hóa sự phục hồi hoặc chỉ số phúc lợi y khoa của bệnh nhân (Reward) dựa trên việc thử nghiệm và khai thác các phác đồ điều trị khác nhau.
  * **English:** Each arm of the Bandit corresponds to a treatment protocol (Action). The goal is to maximize the patient's recovery or medical well-being index (Reward) based on exploring and exploiting different treatment protocols.

**Câu 3 (Question 3):** Trong chiến lược $\epsilon$-greedy, nếu đặt $\epsilon = 0.0$, Agent sẽ có hành vi như thế nào?
*(In an $\epsilon$-greedy strategy, if $\epsilon = 0.0$, how will the agent behave?)*

- [ ] A. Khám phá (Explore) ngẫu nhiên 100% thời gian. *(Explore randomly 100% of the time.)*
- [x] B. Khai thác (Exploit) liên tục, chỉ chọn hành động có giá trị kỳ vọng cao nhất hiện tại. *(Exploit continuously, only choosing the action with the highest estimated expected value.)*
- [ ] C. Luôn chọn các hành động chưa từng được thử nghiệm. *(Always choose actions that have never been tried.)*
- [ ] D. Dừng học hỏi và tắt chương trình. *(Stop learning and terminate the program.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Tham số $\epsilon$ quyết định xác suất chọn hành động ngẫu nhiên (exploration). Khi $\epsilon = 0.0$, xác suất khai thác (exploitation) là $1 - \epsilon = 1.0$, nghĩa là Agent luôn hành động tham lam (greedy) chọn hành động có giá trị $Q(s,a)$ lớn nhất.
  * **English:** The parameter $\epsilon$ determines the probability of choosing a random action (exploration). When $\epsilon = 0.0$, the exploitation probability $1 - \epsilon = 1.0$, meaning the agent always acts greedily to choose the action with the largest value $Q(s,a)$.

**Câu 4 (Question 4):** Nếu hành động A có 50% xác suất nhận phần thưởng -11 và 50% xác suất nhận phần thưởng +9. Giá trị hành động (Action-value) $q_*(A)$ là bao nhiêu?
*(If action A has a 50% probability of receiving a reward of -11 and a 50% probability of receiving a reward of +9, what is the action-value $q_*(A)$?)*

- [ ] A. 1
- [x] B. -1
- [ ] C. -2
- [ ] D. 0
- **Giải thích (Explanation):**
  * **Vietnamese:** Giá trị hành động $q_*(a)$ được định nghĩa là kỳ vọng toán học của phần thưởng nhận được:
    $$q_*(A) = \mathbb{E}[R \mid A] = 0.5 \times (-11) + 0.5 \times (+9) = -5.5 + 4.5 = -1$$
  * **English:** The action-value $q_*(a)$ is defined as the mathematical expectation of the received reward:
    $$q_*(A) = \mathbb{E}[R \mid A] = 0.5 \times (-11) + 0.5 \times (+9) = -5.5 + 4.5 = -1$$

**Câu 5 (Question 5):** Mục đích chính của việc sử dụng công thức cập nhật tăng dần (incremental update rule): $Q_{new} = Q_{old} + \frac{1}{n}[R - Q_{old}]$ là gì?
*(What is the main purpose of using the incremental update rule: $Q_{new} = Q_{old} + \frac{1}{n}[R - Q_{old}]$?)*

- [x] A. Tiết kiệm bộ nhớ vì không cần lưu trữ toàn bộ lịch sử phần thưởng. *(Saving memory because there is no need to store the entire reward history.)*
- [ ] B. Tăng cường khả năng khám phá (exploration). *(Enhancing exploration.)*
- [ ] C. Ngăn Agent rơi xuống vách đá trong môi trường Cliff Walking. *(Preventing the agent from falling off the cliff in the Cliff Walking environment.)*
- [ ] D. Ép môi trường phải thay đổi xác suất trả thưởng. *(Forcing the environment to change reward probabilities.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Bằng cách biến đổi toán học về dạng cập nhật tăng dần, thuật toán chỉ cần lưu trữ giá trị ước lượng hiện tại $Q_{old}$ và số lượng mẫu $n$ mà không cần lưu lại toàn bộ chuỗi phần thưởng lịch sử trong bộ nhớ RAM.
  * **English:** By mathematically transforming the update into an incremental form, the algorithm only needs to store the current estimate $Q_{old}$ and the sample count $n$ without keeping the entire history of rewards in RAM.

**Câu 6 (Question 6):** Phương trình Bellman đóng vai trò nền tảng trong Học tăng cường vì nó biểu diễn điều gì?
*(Why do Bellman equations serve as a foundation in Reinforcement Learning? What do they represent?)*

- [x] A. Mối quan hệ đệ quy (recursive) giữa giá trị của một trạng thái hiện tại và giá trị của các trạng thái kế tiếp. *(The recursive relationship between the value of the current state and the values of successor states.)*
- [ ] B. Quỹ đạo (trajectory) tối ưu duy nhất để Agent đi đến đích. *(The unique optimal trajectory for the agent to reach the goal.)*
- [ ] C. Công thức tính gradient cho mạng nơ-ron sâu. *(The gradient computation formula for deep neural networks.)*
- [ ] D. Mức độ nhiễu (variance) của các phần thưởng ngẫu nhiên. *(The variance of random rewards.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Phương trình Bellman phân rã hàm giá trị thành phần thưởng tức thời và giá trị chiết khấu của trạng thái kế tiếp, tạo cơ sở đệ quy cho các thuật toán học (bootstrapping).
  * **English:** The Bellman equation decomposes the value function into the immediate reward and the discounted value of the next state, establishing a recursive basis for learning algorithms (bootstrapping).

**Câu 7 (Question 7):** Sự khác biệt toán học cốt lõi giữa Phương trình Kỳ vọng Bellman (Expectation) và Phương trình Tối ưu Bellman (Optimality) là gì?
*(What is the core mathematical difference between the Bellman Expectation Equation and the Bellman Optimality Equation?)*

- [ ] A. Phương trình Tối ưu không có hệ số chiết khấu $\gamma$. *(The Optimality Equation does not have a discount factor $\gamma$.)*
- [x] B. Phương trình Tối ưu loại bỏ tổng xác suất chính sách $\pi$ và thay bằng toán tử max. *(The Optimality Equation removes the policy probability sum $\sum \pi(a|s)$ and replaces it with a max operator.)*
- [ ] C. Phương trình Kỳ vọng chỉ áp dụng cho bài toán Bandit. *(The Expectation Equation only applies to the Bandit problem.)*
- [ ] D. Phương trình Kỳ vọng sử dụng trung bình nhân thay vì trung bình cộng. *(The Expectation Equation uses geometric mean instead of arithmetic mean.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Phương trình tối ưu Bellman mô tả trạng thái lý tưởng khi Agent đi theo chính sách tối ưu nhất. Do đó, thay vì lấy trung bình có trọng số theo phân bố chính sách $\sum_a \pi(a|s)$, ta sử dụng toán tử $\max_a$ để chọn hành động mang lại giá trị lớn nhất.
  * **English:** The Bellman Optimality Equation describes the ideal state when the agent follows the optimal policy. Thus, instead of taking a weighted average over the policy distribution $\sum_a \pi(a|s)$, the $\max_a$ operator is used to select the action that yields the highest value.

**Câu 8 (Question 8):** Tại sao việc giải trực tiếp phương trình Bellman bằng phương pháp giải tích (lập hệ phương trình tuyến tính) không khả thi cho bài toán cờ vua (Chess)?
*(Why is solving the Bellman equation analytically (solving a system of linear equations) infeasible for Chess?)*

- [ ] A. Vì cờ vua không có điểm kết thúc rõ ràng. *(Chess does not have a clear terminal state.)*
- [ ] B. Vì phần thưởng trong cờ vua luôn bằng 0. *(The reward in chess is always 0.)*
- [x] C. Vì số lượng trạng thái quá khổng lồ (khoảng $10^{45}$), không máy tính nào giải nổi hệ phương trình này. *(The state space is astronomically large (about $10^{45}$ states), making it physically impossible for any computer to solve.)*
- [ ] D. Vì cờ vua yêu cầu phải có hai Agent cạnh tranh nhau. *(Chess requires two competing agents.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Dù cờ vua có thể biểu diễn dưới dạng MDP tuyến tính, kích thước không gian trạng thái $\mathcal{S}$ của nó quá lớn ($\approx 10^{45}$). Giải tích trực tiếp bằng cách nghịch đảo ma trận có độ phức tạp $O(|\mathcal{S}|^3)$ là điều bất khả thi về mặt vật lý.
  * **English:** Although chess can be represented as a linear MDP, its state space size $|\mathcal{S}|$ is too large ($\approx 10^{45}$). Directly solving it analytically via matrix inversion requires $O(|\mathcal{S}|^3)$ complexity, which is physically impossible.

**Câu 9 (Question 9):** Trong Quy hoạch động (Dynamic Programming), sự phân biệt giữa "Policy Evaluation" và "Control" là:
*(In Dynamic Programming (DP), the distinction between "Policy Evaluation" and "Policy Control" is:)*

- [x] A. Evaluation là ước lượng giá trị của một chính sách cụ thể; Control là tìm ra chính sách tốt nhất. *(Evaluation estimates the value of a specific policy; Control finds the optimal policy.)*
- [ ] B. Evaluation là tìm chính sách tối ưu; Control là tính toán phương sai. *(Evaluation finds the optimal policy; Control computes variance.)*
- [ ] C. Evaluation chỉ dùng cho Monte Carlo; Control chỉ dùng cho Temporal Difference. *(Evaluation is only for Monte Carlo; Control is only for Temporal Difference.)*
- [ ] D. Cả hai thuật ngữ đều mang cùng một ý nghĩa. *(Both terms have the same meaning.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Policy Evaluation (đánh giá chính sách) trả lời câu hỏi "Chính sách $\pi$ hiện tại tốt đến mức nào?" bằng cách ước lượng $v_\pi(s)$. Policy Control (điều khiển/tối ưu chính sách) giải quyết bài toán tìm kiếm chính sách tối ưu nhất $\pi_*$.
  * **English:** Policy Evaluation answers "How good is the current policy $\pi$?" by estimating $v_\pi(s)$. Policy Control solves the problem of finding the optimal policy $\pi_*$.

**Câu 10 (Question 10):** Tại sao thuật toán Đánh giá Chính sách lặp (Iterative Policy Evaluation) thường được cài đặt bằng kỹ thuật 2 mảng (V và V’)?
*(Why is the Iterative Policy Evaluation algorithm often implemented using a two-array technique (V and V’)?)*

- [ ] A. Để tính toán phần thưởng của 2 Agent cùng lúc. *(To calculate rewards for two agents simultaneously.)*
- [x] B. Để đảm bảo các giá trị mới được tính toán bằng cách dùng toàn bộ dữ liệu của vòng lặp cũ, tránh việc ghi đè dữ liệu gây sai lệch toán học trong quá trình quét (sweep). *(To ensure that new values are calculated using the entire data from the old iteration, avoiding data overwrites that cause mathematical inconsistencies during sweeps.)*
- [ ] C. Để lưu trữ đồng thời cả chính sách $\pi$ và mô hình p. *(To simultaneously store both policy $\pi$ and model $p$.)*
- [ ] D. Để giảm một nửa thời gian biên dịch mã Python. *(To cut the Python compilation time in half.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Khi cập nhật đồng thời (synchronous update), thuật toán cần giữ lại mảng $V$ cũ để tính toán mảng $V'$ mới cho mọi trạng thái mà không bị ảnh hưởng bởi thứ tự duyệt trạng thái (sweep) gây ghi đè giá trị trong bộ nhớ.
  * **English:** During synchronous updates, the algorithm needs to keep the old array $V$ to compute the new array $V'$ for all states, without being affected by the sweep order overwriting values in memory.

**Câu 11 (Question 11):** Điều kiện dừng ($\Delta < \theta$) trong thuật toán Iterative Policy Evaluation có ý nghĩa gì?
*(What does the stopping condition ($\Delta < \theta$) in the Iterative Policy Evaluation algorithm mean?)*

- [ ] A. Dừng khi Agent đã tìm được đường đến đích. *(Stop when the agent has found a path to the goal.)*
- [x] B. Dừng khi sự thay đổi giá trị lớn nhất giữa mảng cũ và mới nhỏ hơn một ngưỡng cực nhỏ (thuật toán đã hội tụ). *(Stop when the maximum change between old and new value arrays is smaller than a tiny threshold (convergence).)*
- [ ] C. Dừng khi phần thưởng nhận được đạt mức tối đa. *(Stop when the received reward reaches a maximum.)*
- [ ] D. Dừng khi hết bộ nhớ RAM. *(Stop when out of RAM.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** $\Delta = \max_{s \in \mathcal{S}} |v_{k+1}(s) - v_k(s)|$. Khi sai lệch lớn nhất giữa hai vòng lặp nhỏ hơn ngưỡng $\theta$, ta coi hàm giá trị đã hội tụ tiệm cận về giá trị thực tế và kết thúc vòng lặp.
  * **English:** $\Delta = \max_{s \in \mathcal{S}} |v_{k+1}(s) - v_k(s)|$. When the maximum discrepancy between iterations is less than the threshold $\theta$, the value function is considered to have converged close to the true values, ending the loop.

**Câu 12 (Question 12):** Phương pháp Monte Carlo (MC) khác biệt cơ bản với Quy hoạch động (DP) ở điểm nào?
*(How does the Monte Carlo (MC) method fundamentally differ from Dynamic Programming (DP)?)*

- [ ] A. MC cần biết trước hoàn toàn mô hình động lực học của môi trường, DP thì không. *(MC needs to know the complete transition dynamics of the environment, whereas DP does not.)*
- [x] B. MC là phương pháp không cần mô hình (model-free) và học trực tiếp từ kinh nghiệm tương tác thực tế. *(MC is a model-free method that learns directly from actual interaction experience.)*
- [ ] C. MC hội tụ nhanh hơn DP trong mọi trường hợp. *(MC converges faster than DP in all cases.)*
- [ ] D. MC chỉ có thể giải quyết các bài toán có phần thưởng liên tục. *(MC can only solve problems with continuous rewards.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Quy hoạch động (DP) bắt buộc phải biết rõ phân bố xác suất chuyển trạng thái $p$, còn Monte Carlo (MC) thu thập mẫu qua các ván đấu thực tế (sample experience) nên hoạt động mà không cần biết quy luật vật lý của môi trường (model-free).
  * **English:** Dynamic Programming (DP) requires knowing the transition probability distribution $p$, while Monte Carlo (MC) collects samples through actual episodes (sample experience), thus functioning without knowing the rules of the environment (model-free).

**Câu 13 (Question 13):** Tại sao phương pháp Monte Carlo cổ điển chỉ áp dụng được cho các bài toán Episodic (có trạng thái kết thúc)?
*(Why can classical Monte Carlo methods only be applied to Episodic tasks (tasks that terminate)?)*

- [ ] A. Vì nó cần Agent bị trừ điểm liên tục để học. *(Because the agent needs to lose points continuously to learn.)*
- [ ] B. Vì bộ nhớ máy tính không đủ để lưu trữ. *(Because computer memory is insufficient to store it.)*
- [x] C. Vì nó bắt buộc phải đợi đến khi episode kết thúc hoàn toàn thì mới quan sát được phần thưởng tích lũy (Return $G_t$) để cập nhật hàm giá trị. *(Because it must wait until the episode completely ends to observe the actual accumulated return $G_t$ for updating the value function.)*
- [ ] D. Vì nó không hỗ trợ hệ số chiết khấu $\gamma$. *(Because it does not support the discount factor $\gamma$.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Monte Carlo cập nhật giá trị trạng thái dựa vào toàn bộ lượng lợi nhuận thực tế thu được từ bước thời gian đó cho đến hết episode: $V(S_t) \leftarrow V(S_t) + \alpha [G_t - V(S_t)]$. Nếu episode không bao giờ kết thúc, ta không thể có giá trị cụ thể của $G_t$ để thực hiện phép trừ.
  * **English:** Monte Carlo updates state values based on the actual total return from that step onwards until the end of the episode: $V(S_t) \leftarrow V(S_t) + \alpha [G_t - V(S_t)]$. If the episode never ends, a concrete value of $G_t$ cannot be computed.

**Câu 14 (Question 14):** Khi mô hình hóa trò chơi Blackjack thành MDP để giải bằng Monte Carlo, yếu tố nào KHÔNG nằm trong Không gian trạng thái (State Space) của Agent?
*(When modeling Blackjack as an MDP to solve using Monte Carlo, which of the following is NOT part of the agent's State Space?)*

- [ ] A. Tổng điểm số hiện tại của Agent. *(The agent's current total score.)*
- [ ] B. Việc Agent có quân Át linh hoạt (usable ace) hay không. *(Whether the agent has a usable ace.)*
- [x] C. Quân bài đang úp (chưa lật) của nhà cái. *(The dealer's face-down card.)*
- [ ] D. Quân bài đang lật ngửa của nhà cái. *(The dealer's face-up card.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Trong Blackjack, quân bài úp của nhà cái là thông tin ẩn (hidden information). Để MDP hợp lệ, trạng thái quan sát của Agent chỉ chứa các thông tin công khai: tổng điểm của mình, sự xuất hiện của quân Át hữu dụng và quân bài ngửa của đối thủ.
  * **English:** In Blackjack, the dealer's face-down card is hidden information. For a valid MDP, the agent's observation state must only contain public information: its own card total, whether it has a usable ace, and the dealer's showing face-up card.

**Câu 15 (Question 15):** Trong lập trình thuật toán Monte Carlo Prediction, tại sao việc tính Return ($G_t$) lại được thiết lập bằng vòng lặp chạy ngược từ cuối episode về đầu?
*(In implementing Monte Carlo Prediction, why is the return ($G_t$) calculation structured as a backward loop from the end of the episode to the beginning?)*

- [x] A. Nhằm tận dụng công thức đệ quy $G_t = R_{t+1} + \gamma G_{t+1}$, giúp tính toán toàn bộ chuỗi phần thưởng hiệu quả với độ phức tạp $O(T)$. *(To utilize the recursive formula $G_t = R_{t+1} + \gamma G_{t+1}$, allowing efficient computation of the entire sequence with $O(T)$ complexity.)*
- [ ] B. Vì Agent chỉ có thể lùi lại phía sau. *(Because the agent can only move backward.)*
- [ ] C. Để loại bỏ hoàn toàn các phần thưởng âm. *(To eliminate negative rewards entirely.)*
- [ ] D. Vì Python không hỗ trợ vòng lặp chạy tiến với ma trận. *(Because Python does not support forward iteration with matrices.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Bằng cách duyệt ngược từ bước cuối cùng $T-1$ về $0$, ta có thể tính $G_t$ ở thời điểm hiện tại trực tiếp từ $G_{t+1}$ đã tính ở bước trước đó chỉ bằng một phép tính nhân cộng đơn giản, giảm độ phức tạp tính toán từ $O(T^2)$ xuống $O(T)$.
  * **English:** By iterating backwards from the last step $T-1$ to $0$, we compute $G_t$ at the current step directly from $G_{t+1}$ using a simple multiplication and addition, reducing the complexity from $O(T^2)$ to $O(T)$.

**Câu 16 (Question 16):** Công thức đúng để tính Sai số Khác biệt Thời gian (TD Error - $\delta_t$) trong thuật toán TD(0) là:
*(What is the correct formula to compute the Temporal Difference (TD) Error ($\delta_t$) in TD(0)?)*

- [ ] A. $\delta_t = R_{t+1} - V(S_t)$
- [x] B. $\delta_t = R_{t+1} + \gamma V(S_{t+1}) - V(S_t)$
- [ ] C. $\delta_t = R_{t+1} + \gamma \max_a Q(S_{t+1}, a)$
- [ ] D. $\delta_t = V(S_t) - V(S_{t+1})$
- **Giải thích (Explanation):**
  * **Vietnamese:** Công thức định nghĩa lỗi TD một bước: lấy mục tiêu ước lượng (Target) $R_{t+1} + \gamma V(S_{t+1})$ trừ đi giá trị ước lượng hiện tại $V(S_t)$.
  * **English:** The formula defines the one-step TD error: subtracting the current estimate $V(S_t)$ from the estimated target $R_{t+1} + \gamma V(S_{t+1})$.

**Câu 17 (Question 17):** Đại lượng $R_{t+1} + \gamma V(S_{t+1})$ trong phương trình TD được gọi là gì?
*(What is the quantity $R_{t+1} + \gamma V(S_{t+1})$ in the TD equation called?)*

- [ ] A. Kích thước bước (Learning rate). *(Learning rate / Step size.)*
- [x] B. Mục tiêu TD (TD Target). *(TD Target.)*
- [ ] C. Xác suất chuyển đổi (Transition probability). *(Transition probability.)*
- [ ] D. Lợi nhuận thực tế (Actual return). *(Actual return.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Đây là giá trị mục tiêu mà hàm ước lượng $V(S_t)$ hướng tới trong quá trình cập nhật từng bước một của TD.
  * **English:** This is the target value that the estimated function $V(S_t)$ updates towards in each step of TD learning.

**Câu 18 (Question 18):** Đặc tính "Bootstrapping" trong Học tăng cường mang ý nghĩa gì?
*(What does the term "Bootstrapping" mean in Reinforcement Learning?)*

- [ ] A. Reset lại toàn bộ hệ thống khi Agent rơi xuống vách đá. *(Resetting the entire system when the agent falls off a cliff.)*
- [x] B. Cập nhật ước lượng hiện tại dựa vào một ước lượng của trạng thái tương lai (dự đoán dựa trên dự đoán). *(Updating a current estimate based on an estimate of a future state (guessing based on another guess).)*
- [ ] C. Tính trung bình cộng của toàn bộ phần thưởng trong quá khứ. *(Computing the average of all past rewards.)*
- [ ] D. Chọn hành động ngẫu nhiên để tăng tính khám phá. *(Choosing random actions to increase exploration.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Bootstrapping là hành vi cập nhật một giá trị dự báo dựa trên một giá trị dự báo khác ở bước tiếp theo (như TD dùng $V(S_{t+1})$ để cập nhật cho $V(S_t)$), thay vì chờ đợi kết quả thực tế cuối cùng như MC.
  * **English:** Bootstrapping refers to updating an estimated value based on subsequent estimated values (e.g., TD using $V(S_{t+1})$ to update $V(S_t)$), rather than waiting for the final actual outcome as in MC.

**Câu 19 (Question 19):** Đâu là lợi thế tuyệt đối của phương pháp TD(0) so với Monte Carlo (MC) đối với các hệ thống thời gian thực (real-time)?
*(What is the absolute advantage of TD(0) over Monte Carlo (MC) for real-time systems?)*

- [x] A. TD có thể cập nhật kiến thức ngay lập tức sau mỗi một bước đi (Online Learning) mà không cần chờ kết thúc Episode. *(TD can update its knowledge immediately after each single step (Online Learning) without waiting for the episode to end.)*
- [ ] B. TD có thể giải được cờ vua bằng phương pháp phân tích. *(TD can solve chess analytically.)*
- [ ] C. TD sử dụng ít bộ nhớ RAM hơn. *(TD uses less RAM.)*
- [ ] D. TD không cần sử dụng hệ số $\gamma$. *(TD does not require the discount factor $\gamma$.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** MC bắt buộc phải đợi hết Episode mới có thể học, không phù hợp cho các bài toán chạy liên tục hoặc quá dài. TD(0) cập nhật ước lượng ngay lập tức tại mỗi bước chuyển đổi đơn lẻ (step-by-step).
  * **English:** MC must wait until the end of the episode to learn, making it unsuitable for continuous or extremely long tasks. TD(0) updates the estimate immediately at each individual state transition (step-by-step).

**Câu 20 (Question 20):** Tại sao Temporal Difference (TD) lại xử lý cực tốt các "chuỗi dữ liệu không hoàn chỉnh" (incomplete sequences)?
*(Why does Temporal Difference (TD) handle "incomplete sequences" extremely well?)*

- [ ] A. Vì TD tự động điền phần thưởng lớn nhất vào dữ liệu bị thiếu. *(Because TD automatically fills in the maximum reward for missing data.)*
- [x] B. Vì TD cập nhật dựa trên từng bước chuyển đổi (step-by-step), không phụ thuộc vào việc Episode có kết thúc hay không. *(Because TD updates step-by-step based on individual transitions, independent of whether the episode has completed.)*
- [ ] C. Vì TD yêu cầu người dùng nạp dữ liệu thủ công. *(Because TD requires the user to feed data manually.)*
- [ ] D. Vì TD chỉ quan tâm đến trạng thái khởi đầu. *(Because TD only cares about the starting state.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Do đặc tính cập nhật từng bước đơn lẻ và không cần đợi hết ván đấu để lấy Return $G_t$, TD có thể học từ bất kỳ đoạn quỹ đạo (trajectory) ngắn nào bị cắt nửa chừng.
  * **English:** Due to step-by-step updates without waiting for the episode to end to get return $G_t$, TD can learn from any short segment of a trajectory cut mid-way.

**Câu 21 (Question 21):** Trong môi trường Cliff Walking, thực nghiệm cho thấy Q-Learning thường rơi xuống vách đá nhiều hơn Expected Sarsa. Giải thích nào sau đây là chính xác?
*(In the Cliff Walking environment, experiments show that Q-learning falls off the cliff more often than Expected Sarsa. Which explanation is correct?)*

- [ ] A. Vì Q-Learning không hỗ trợ môi trường dạng lưới. *(Because Q-learning does not support gridworld environments.)*
- [x] B. Vì Q-Learning là thuật toán Off-policy, nó cập nhật hàm Q giả định rằng nó luôn chọn hành động tối ưu (sát vách đá), nhưng khi thực thi nó lại dùng $\epsilon$-greedy nên thỉnh thoảng trượt chân. *(Because Q-learning is an Off-policy algorithm, it updates the Q-function assuming it always chooses the optimal action (along the cliff edge), but in practice it executes using $\epsilon$-greedy, occasionally stepping off the cliff randomly.)*
- [ ] C. Vì Expected Sarsa tính toán nhanh hơn Q-Learning. *(Because Expected Sarsa computes faster than Q-learning.)*
- [ ] D. Vì $\epsilon$ của Q-learning luôn lớn hơn 1. *(Because $\epsilon$ of Q-learning is always greater than 1.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Q-learning cập nhật dựa trên giả thuyết Agent luôn chọn hành động Greedy ($\max$). Tuy nhiên trong quá trình tương tác thực tế, Agent vẫn dùng $\epsilon$-greedy để khám phá. Khi Agent di chuyển sát mép vực, các bước đi ngẫu nhiên do $\epsilon$ sẽ khiến Agent ngã xuống vực thường xuyên.
  * **English:** Q-learning updates assuming the agent always chooses the greedy action ($\max$). However, in practice, the agent still uses $\epsilon$-greedy for exploration. Moving right next to the cliff edge, the random steps caused by $\epsilon$ result in frequent falls.

**Câu 22 (Question 22):** Tại sao Expected Sarsa lại chọn con đường vòng xa hơn và an toàn hơn trong môi trường Cliff Walking?
*(Why does Expected Sarsa choose a longer, safer path in Cliff Walking?)*

- [x] A. Vì nó là thuật toán On-policy, nó tính kỳ vọng bao gồm cả xác suất xảy ra các hành động khám phá (đi sai bước), do đó nó đánh giá việc đi sát vách đá là quá rủi ro. *(Because it is an On-policy algorithm that computes expectations over all actions (including exploratory ones), thereby evaluating pathing close to the cliff edge as too risky.)*
- [ ] B. Vì nó không biết đường ngắn nhất. *(Because it does not know the shortest path.)*
- [ ] C. Vì nó nhận được phần thưởng dương khi đi đường vòng. *(Because it receives a positive reward when detouring.)*
- [ ] D. Vì nó không sử dụng tham số $\alpha$. *(Because it does not use the parameter $\alpha$.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Expected Sarsa tính toán mục tiêu cập nhật bằng cách nhân giá trị $Q(S_{t+1}, a)$ với xác suất chọn hành động tương ứng $\pi(a|S_{t+1})$. Điều này bao gồm cả xác suất Agent sẽ chọn bước đi ngẫu nhiên (rơi xuống vực), dẫn đến giá trị ước lượng ở gần vách vực bị kéo giảm rất mạnh, khiến Agent chủ động chọn đường vòng xa hơn nhưng an toàn hơn.
  * **English:** Expected Sarsa computes the update target by weighting $Q(S_{t+1}, a)$ by the probability of choosing each action under the policy $\pi(a|S_{t+1})$. This incorporates the probability of choosing random steps (falling off), which dramatically drops the value estimate near the cliff and drives the agent to take the safer detour.

**Câu 23 (Question 23):** Kiến trúc Dyna trong Học tăng cường là sự kết hợp (cầu nối) giữa hai cơ chế nào?
*(The Dyna architecture in Reinforcement Learning bridges which two mechanisms?)*

- [ ] A. Tối ưu hàm mất mát và Backpropagation. *(Loss optimization and backpropagation.)*
- [x] B. Học trực tiếp từ thực tế (Model-Free RL) và Lập kế hoạch dựa trên mô phỏng (Model-Based Planning). *(Direct learning from real experience (Model-Free RL) and planning based on simulation (Model-Based Planning).)*
- [ ] C. Khai thác (Exploitation) và Hệ số chiết khấu ($\gamma$). *(Exploitation and discount factor $\gamma$.)*
- [ ] D. Monte Carlo and Q-learning. *(Monte Carlo and Q-learning.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Dyna là kiến trúc tích hợp, sử dụng kinh nghiệm thực tế để vừa cập nhật hàm giá trị (Direct RL), vừa xây dựng Mô hình môi trường (Model). Sau đó, nó dùng Mô hình này để giả lập trải nghiệm ảo phục vụ bước Lập kế hoạch (Planning).
  * **English:** Dyna is an integrated architecture that uses real experience to update value/policy directly (Direct RL) and to learn a model of the environment (Model). It then uses this model to generate simulated experiences for Planning.

**Câu 24 (Question 24):** Trong thuật toán Dyna-Q, kho dữ liệu để Agent thực hiện pha "Lập kế hoạch" (Planning) được lấy từ đâu?
*(In Dyna-Q, where does the agent source data from to perform the Planning phase?)*

- [ ] A. Tải từ bộ dữ liệu có sẵn trên Internet. *(Downloading from pre-existing datasets on the internet.)*
- [x] B. Từ một Mô hình (Model) do chính Agent tự xây dựng thông qua việc ghi nhớ các cặp Trạng thái- Hành động đã trải qua trong thực tế. *(From a Model built by the agent itself by recording past state-action-reward pairs experienced in reality.)*
- [ ] C. Từ một thuật toán Monte Carlo chạy ngầm. *(From a background Monte Carlo algorithm.)*
- [ ] D. Từ mã nguồn cứng (hardcode) của kỹ sư. *(From hardcoded rules by engineers.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Trong Dyna-Q, Mô hình (Model) đóng vai trò ghi nhớ các cặp $(S, A) \rightarrow (S', R)$ đã xảy ra. Khi lập kế hoạch, Agent truy vấn ngẫu nhiên các cặp đã lưu từ Model này để thực hiện cập nhật Q-value ảo.
  * **English:** In Dyna-Q, the Model functions to remember the experienced transitions $(S, A) \rightarrow (S', R)$. During planning, the agent queries randomly from the recorded transitions to perform virtual Q-value updates.

**Câu 25 (Question 25):** Trong biến thể Dyna-Q+, mục đích của việc cộng thêm phần thưởng $R_{bonus} = R + \kappa\sqrt{\tau}$ (với $\tau$ là thời gian trôi qua) là để giải quyết vấn đề gì?
*(In the Dyna-Q+ variant, what problem does adding the exploration bonus $R_{bonus} = R + \kappa\sqrt{\tau}$ (where $\tau$ is time elapsed) solve?)*

- [ ] A. Bù đắp phần thưởng cho những trận thua. *(Compensating rewards for losses.)*
- [x] B. Khuyến khích Agent quay lại khám phá những khu vực đã lâu không ghé thăm, đặc biệt hữu ích khi môi trường bất ngờ mở ra một đường tắt mới. *(Encouraging the agent to return and explore states/actions not visited for a long time, particularly useful when the environment opens up a new shortcut.)*
- [ ] C. Giảm thiểu hiện tượng Overfitting. *(Reducing overfitting.)*
- [ ] D. Tính toán thời gian thực thi của thuật toán. *(Measuring algorithmic execution time.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Khi môi trường thay đổi theo hướng có lợi hơn (ví dụ xuất hiện đường đi tắt mới), một Agent Dyna-Q thuần túy sẽ bỏ lỡ vì nó chỉ đi theo con đường đã tìm thấy trước đó. Dyna-Q+ thêm phần thưởng khám phá $\kappa\sqrt{\tau}$ để thôi thúc Agent kiểm tra lại các khu vực đã lâu không ghé thăm ($\tau$ lớn).
  * **English:** When the environment changes to be more favorable (e.g., a new shortcut appears), a basic Dyna-Q agent misses it because it follows the previously discovered optimal path. Dyna-Q+ adds an exploration bonus $\kappa\sqrt{\tau}$ to prompt the agent to re-check areas unvisited for a long time (large $\tau$).

**Câu 26 (Question 26):** Sự khác biệt cơ bản giữa Q-Learning và SARSA trong cách cập nhật hàm giá trị là:
*(The fundamental difference between Q-learning and SARSA in value function updating is:)*

- [x] A. Q-learning cập nhật dựa trên hành động có giá trị Max ở trạng thái kế tiếp, trong khi SARSA cập nhật dựa trên hành động thực tế tiếp theo được chọn. *(Q-learning updates based on the action with the maximum estimated value in the next state, whereas SARSA updates based on the actual next action chosen by the policy.)*
- [ ] B. SARSA không cần tính TD Error. *(SARSA does not need to compute the TD Error.)*
- [ ] C. Q-Learning dùng phương pháp DP, SARSA dùng Monte Carlo. *(Q-learning uses DP, SARSA uses Monte Carlo.)*
- [ ] D. Q-Learning chỉ dùng cho không gian liên tục. *(Q-learning is only for continuous state spaces.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Q-learning là Off-policy, dùng $\max_a Q(S_{t+1}, a)$ làm target. SARSA là On-policy, dùng $Q(S_{t+1}, A_{t+1})$ thực tế được chọn bởi chính sách làm target.
  * **English:** Q-learning is Off-policy, using $\max_a Q(S_{t+1}, a)$ as the target. SARSA is On-policy, using the actual action $Q(S_{t+1}, A_{t+1})$ chosen by the policy as the target.

**Câu 27 (Question 27):** Hai phương pháp Monte Carlo (MC) và Temporal Difference (TD) chia sẻ điểm chung cốt lõi nào?
*(What core commonality do Monte Carlo (MC) and Temporal Difference (TD) methods share?)*

- [ ] A. Đều sử dụng cơ chế Bootstrapping. *(Both use bootstrapping.)*
- [ ] B. Đều bắt buộc phải chờ đến khi Episode kết thúc. *(Both must wait until the episode ends.)*
- [x] C. Đều là các phương pháp Học không cần mô hình (Model-Free), học trực tiếp từ kinh nghiệm. *(Both are Model-Free methods that learn directly from experience.)*
- [ ] D. Cả hai thuật toán không dùng cho bài toán Episodic. *(Neither algorithm can be used for Episodic tasks.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Cả hai phương pháp đều là Model-free, nghĩa là chúng không đòi hỏi thông tin phân bố xác suất chuyển trạng thái của môi trường để cập nhật hàm giá trị.
  * **English:** Both are Model-free, meaning they do not require environmental transition dynamics distributions to update the value function.

**Câu 28 (Question 28):** Trong hệ thống phân phối quảng cáo (Ad CTR), sự đánh đổi "Khám phá - Khai thác" được thể hiện cụ thể bằng hành động nào?
*(In ad serving systems (Ad CTR), how is the "Exploration - Exploitation" tradeoff specifically manifested?)*

- [ ] A. Khai thác: Chi tiền chạy quảng cáo giờ vàng; Khám phá: Chạy quảng cáo lúc nửa đêm. *(Exploitation: Spending money on prime-time ads; Exploration: Running ads at midnight.)*
- [x] B. Khai thác: Hiển thị các quảng cáo đã biết là có tỷ lệ click cao; Khám phá: Hiển thị thử các quảng cáo mới/lạ để đo lường tỷ lệ click thực tế. *(Exploitation: Displaying ads known to have high click-through rates; Exploration: Displaying new/unfamiliar ads to measure their click-through rate.)*
- [ ] C. Khai thác: Tắt máy chủ; Khám phá: Bật máy chủ mới. *(Exploitation: Turning off servers; Exploration: Booting new servers.)*
- [ ] D. Khai thác: Dùng AI; Khám phá: Dùng nhân viên thủ công. *(Exploitation: Using AI; Exploration: Using manual labor.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Khai thác (Exploitation) là hiển thị các mẫu quảng cáo đã biết chắc chắn thu hút lượng click lớn để giữ doanh thu. Khám phá (Exploration) là đưa ra quảng cáo mới để tìm kiếm xem liệu chúng có tiềm năng tốt hơn các quảng cáo hiện tại hay không.
  * **English:** Exploitation is showing ads that are known to yield high click-through rates to maintain revenue. Exploration is introducing new ads to see if they might perform better than current ones.

**Câu 29 (Question 29):** Khi triển khai Monte Carlo, sự khác biệt giữa thuật toán "First-Visit" và "Every Visit" là gì?
*(When implementing Monte Carlo, what is the difference between "First-visit" and "Every-visit" algorithms?)*

- [x] A. First-Visit chỉ cập nhật phần thưởng cho lần gặp mặt đầu tiên của trạng thái S trong 1 episode; Every-Visit cập nhật cho tất cả các lần gặp mặt của S trong episode đó. *(First-visit only updates return estimates for the first occurrence of state S in an episode; Every-visit updates for all occurrences of state S in that episode.)*
- [ ] B. First-Visit chỉ học ở episode đầu tiên. *(First-visit only learns on the first episode.)*
- [ ] C. Every-Visit tốn ít RAM hơn First-Visit. *(Every-visit uses less RAM than First-visit.)*
- [ ] D. First-Visit luôn hội tụ về 0. *(First-visit always converges to 0.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** Đây là định nghĩa phân loại của 2 biến thể MC. First-visit chỉ tính trung bình return cho lượt xuất hiện đầu tiên của trạng thái trong mỗi tập; Every-visit tính trung bình cho mọi lượt xuất hiện của trạng thái đó.
  * **English:** This defines the classification of the two MC variants. First-visit averages the returns only from the first visit to a state in each episode; Every-visit averages the returns of all visits to that state across the episode.

**Câu 30 (Question 30):** Tại sao trong các môi trường có không gian trạng thái cực lớn, Temporal Difference (TD) lại có hiệu năng tính toán tốt hơn Monte Carlo (MC)?
*(Why does Temporal Difference (TD) have better computational efficiency than Monte Carlo (MC) in environments with extremely large state spaces?)*

- [ ] A. Vì TD bỏ qua các trạng thái không quan trọng. *(Because TD ignores unimportant states.)*
- [x] B. Vì TD hội tụ nhanh chóng dựa trên các bước chuyển đổi đơn lẻ (single transitions), trong khi MC tốn rất nhiều tài nguyên để tính toán và lưu trữ trung bình cộng cho các chuỗi dữ liệu cực dài. *(Because TD converges quickly based on individual transitions, whereas MC consumes massive resources computing and storing returns for extremely long sequences.)*
- [ ] C. Vì MC không tương thích với ngôn ngữ Python. *(Because MC is incompatible with Python.)*
- [ ] D. Vì TD chạy thuật toán song song trên GPU. *(Because TD runs in parallel on GPU.)*
- **Giải thích (Explanation):**
  * **Vietnamese:** TD(0) chỉ cần lưu trữ và tính toán trên một bước chuyển trạng thái duy nhất tại mỗi lần cập nhật. Ngược lại, MC yêu cầu lưu trữ toàn bộ chuỗi lịch sử vô cùng dài trong một episode trước khi có thể bắt đầu tính toán trung bình cộng ngược, dẫn đến chi phí bộ nhớ khổng lồ.
  * **English:** TD(0) only needs to store and compute on a single transition step per update. Conversely, MC requires storing the entire long episode trajectory before commencing backward return calculations, leading to massive memory overhead.
