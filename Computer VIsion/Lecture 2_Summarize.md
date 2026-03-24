
Dưới đây là phần tóm tắt và giải thích chi tiết nội dung của cả hai file bài giảng để bạn có cái nhìn hệ thống nhất về môn học Thị giác máy tính (Computer Vision - CV).

---



---

### File 2: 2 Geometric primitives and transformations.pptx (Toán học và Hình học)

Nếu file 1 là "lý thuyết suông", thì file 2 là "công cụ toán học" để thực hiện những điều đó.

**1. Các đối tượng hình học cơ bản (Primitives):**

- **2D:** Điểm $(x, y)$ và Đường thẳng ($ax + by + c = 0$).
    
- **3D:** Điểm $(x, y, z)$ và Mặt phẳng ($ax + by + cz + d = 0$).
    

**2. Tọa độ đồng nhất (Homogeneous Coordinates):**

- Đây là kỹ thuật quan trọng nhất. Thay vì dùng $(x, y)$, ta dùng $(x, y, w)$.
    
- **Mục đích:** Để biến phép Dịch chuyển (cộng) thành phép Nhân ma trận, giúp tính toán đồng bộ và xử lý được các điểm ở vô cực.
    

**3. Các phép biến đổi (Transformations):**

Slide phân cấp các loại biến đổi từ đơn giản đến phức tạp:

- **Translation (Dịch):** Giữ nguyên hình dạng, chỉ thay đổi vị trí.
    
- **Rigid/Euclidean (Cứng):** Dịch + Xoay. Bảo toàn độ dài.
    
- **Similarity (Đồng dạng):** Có thêm Co giãn (Scale). Bảo toàn góc.
    
- **Affine:** Bảo toàn các đường thẳng song song.
    
- **Projective (Phóng chiếu):** Biến đổi mạnh nhất, các đường song song có thể hội tụ (như khi ta nhìn đường ray tàu hỏa).
    

**4. Phóng chiếu 3D sang 2D (Projections):**

Cách máy tính chuyển thế giới thực (3D) vào tấm ảnh (2D):

- **Orthography (Trực giao):** Bỏ qua chiều sâu (trục Z). Thường dùng trong bản vẽ kỹ thuật.
    
- **Perspective (Phối cảnh):** Mô phỏng mắt người/camera thật. Vật ở xa thì nhỏ, ở gần thì lớn.
    

**5. Độ biến dạng ống kính (Lens Distortion):**

- Thực tế camera không hoàn hảo. Ống kính góc rộng thường gây ra hiện tượng méo hình: **Barrel** (méo phồng - giống thùng gỗ) hoặc **Pincushion** (méo lõm - giống gối cắm kim).
    

---

### Mối liên hệ giữa 2 file:

- **File 1** nói rằng: "Máy tính thấy ảnh là một ma trận số".
    
- **File 2** cung cấp các công thức ma trận để: Di chuyển vật thể trong ảnh, xoay ảnh, sửa lỗi méo của camera, và hiểu được khoảng cách xa gần (phối cảnh).
    

Bạn có đang gặp khó khăn ở công thức ma trận cụ thể nào trong file 2 không? Tôi có thể giải thích chi tiết cách nhân ma trận cho từng phép biến đổi.