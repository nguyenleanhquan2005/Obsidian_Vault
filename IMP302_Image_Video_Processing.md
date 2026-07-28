# 📘 IMP302 – Image & Video Processing (Tài liệu ôn thi tổng hợp)

> [!note]
> Tài liệu trắc nghiệm tổng hợp lý thuyết môn Xử lý ảnh & Video (IMP302).

## 📌 Table of Contents
1. [📚 I. Câu Hỏi Trắc Nghiệm](#-i-câu-hỏi-trắc-nghiệm)
2. [🔑 II. Đáp Án & Giải Thích Chi Tiết](#-ii-đáp-án--giải-thích-chi-tiết)

---

## 📚 I. Câu Hỏi Trắc Nghiệm

**Câu 1:** Khi quét một tài liệu văn bản cũ bị ố vàng để chuyển thành văn bản trắng đen sắc nét, hệ thống cần tự động tìm một ngưỡng cắt tối ưu để tách chữ ra khỏi nền. Thuật toán nào sau đây phù hợp nhất cho tác vụ này?

- [ ] a) Biến đổi Logarit (Logarithmic Point Operation)
    
- [ ] b) Cân bằng Lược đồ xám (Histogram Equalization)
    
- [x] c) Phương pháp Otsu (Otsu’s Method)
    
- [ ] d) Nội suy song tuyến tính (Bilinear Interpolation)

- **Giải thích:** Phương pháp Otsu (Otsu’s Method) là thuật toán tự động tìm ngưỡng tối ưu bằng cách cực đại hóa phương sai giữa hai lớp (nền và chữ), rất phù hợp để nhị phân hóa tài liệu văn bản.

**Câu 2:** Một bức ảnh X-quang bị chụp thiếu sáng, khiến toàn bộ các chi tiết tập trung ở vùng màu tối và rất khó nhìn. Kỹ thuật xử lý điểm (Point Operation) nào thường được dùng để tự động trải đều độ sáng, giúp bác sĩ dễ dàng quan sát các chi tiết ẩn?

- [ ] a) Trừ ảnh (Image Subtraction)
    
- [ ] b) Lọc trung vị (Median Smoother)
    
- [ ] c) Khớp mẫu (Template Matching)
    
- [x] d) Cân bằng Lược đồ xám (Histogram Equalization)

-  **Giải thích:** Cân bằng Lược đồ xám (Histogram Equalization) là kỹ thuật tự động kéo giãn phân bố độ sáng, giúp làm rõ các chi tiết trong ảnh có độ tương phản thấp (như ảnh y tế bị tối). 

**Câu 3:** Một bức ảnh bị nhiễu do lỗi đường truyền không dây, xuất hiện các đốm trắng và đen li ti (nhiễu muối tiêu) rải rác. Để loại bỏ hoàn toàn các đốm này mà vẫn giữ được độ sắc nét của các đường viền vật thể, bạn nên dùng bộ lọc nào?

- [ ] a) Bộ lọc Gaussian (Gaussian Lowpass Filter)122qawawa
    
- [x] b) Bộ lọc Trung vị (Median Filter)
    
- [ ] c) Bộ lọc Trung bình (Arithmetic Mean Filter)
    
- [ ] d) Toán tử Laplacian

- **Giải thích:** Bộ lọc Trung vị (Median Smoother/Filter) sắp xếp các pixel lân cận và lấy giá trị ở giữa, giúp triệt tiêu hoàn toàn các đốm nhiễu muối tiêu (giá trị cực đoan) mà không làm mờ đường viền.

**Câu 4:** Trong phần mềm Photoshop, công cụ "Unsharp Masking" giúp làm sắc nét ảnh hoạt động dựa trên nguyên lý toán học nào?

- [ ] a) Cộng thêm nhiễu Gaussian vào ảnh gốc.
    
- [x] b) Lấy ảnh gốc trừ đi phiên bản đã làm mờ của chính nó, rồi cộng phần chênh lệch (mask) trở lại ảnh gốc.
    
- [ ] c) Xóa bỏ các tần số cao trong miền Fourier.
    
- [ ] d) Dùng bộ lọc hình thái học (Morphological Dilation).

- **Giải thích:** Quy trình Unsharp Masking gồm 3 bước: Làm mờ ảnh gốc, lấy ảnh gốc trừ đi ảnh mờ để tạo ra mặt nạ (mask chứa chi tiết biên), và cộng mặt nạ này lại vào ảnh gốc để tăng cường độ sắc nét.
    

**Câu 5:** Khi áp dụng bộ lọc Tích chập (Convolution) thay vì Tương quan (Correlation) trong miền không gian, ma trận lọc (Kernel) cần phải được xử lý như thế nào trước khi nhân và cộng?

- [ ] a) Xoay 90 độ.
    
- [x] b) Xoay 180 độ.
    
- [ ] c) Lấy ma trận nghịch đảo.
    
- [ ] d) Giữ nguyên không thay đổi.

- **Giải thích:** Phép toán Tích chập (Convolution) có cùng cơ chế với phép Tương quan (Correlation) nhưng yêu cầu ma trận lọc phải được xoay 180 độ trước khi tính toán để đảm bảo các tính chất toán học (như tính giao hoán).

**Câu 6:** Khi chụp ảnh một chiếc xe đua đang chạy ở tốc độ cao, bức ảnh bị nhòe do chuyển động (Motion Blur) và đồng thời bị nhiễu cảm biến. Bộ lọc nào sau đây là lựa chọn tối ưu nhất để khôi phục lại biển số xe mà không làm bùng nổ nhiễu?

- [ ] a) Bộ lọc Ngược (Direct Inverse Filter)
    
- [ ] b) Bộ lọc Trung bình Điều hòa (Harmonic Mean Filter)
    
- [x] c) Bộ lọc Lỗi Bình phương Trung bình Tối thiểu (Wiener Filter)
    
- [ ] d) Bộ lọc Thông thấp Lý tưởng (Ideal Lowpass Filter)

- **Giải thích:** Bộ lọc Wiener (Minimum Mean Square Error Filter) kết hợp giữa việc giải chập và hạn chế khuyếch đại nhiễu bằng cách sử dụng tỷ số Tín hiệu/Nhiễu (SNR) trong công thức, là giải pháp tối ưu nhất cho ảnh vừa mờ vừa nhiễu.

**Câu 7:** Tại sao Bộ lọc Ngược (Inverse Filter) thuần túy hiếm khi được sử dụng trong thực tế để khôi phục ảnh mờ?

- [ ] a) Vì nó làm mất màu sắc của bức ảnh.
    
- [x] b) Vì khi hàm suy biến H(u,v) tiến tới 0, thành phần nhiễu sẽ bị khuyếch đại lên vô cực, phá hủy hoàn toàn ảnh.
    
- [ ] c) Vì nó tốn quá nhiều tài nguyên tính toán phần cứng.
    
- [ ] d) Vì nó biến đổi ảnh thành dạng nhị phân.

- **Giải thích:** Bộ lọc Ngược (Direct Inverse Filter) chia phổ ảnh cho hàm suy biến H(u,v). Nếu H(u,v) tiến tới 0, thành phần nhiễu N/H sẽ tiến tới vô cực, làm hỏng hoàn toàn kết quả khôi phục.

**Câu 8:** Nguyên lý "Chiếu ngược có lọc" (Filtered Backprojection) sử dụng các phép chiếu 1D từ nhiều góc độ khác nhau là thuật toán cốt lõi đang được ứng dụng trong thiết bị nào?

- [ ] a) Máy quét mã vạch (Barcode Scanner)
    
- [ ] b) Máy ảnh DSLR
    
- [x] c) Máy chụp cắt lớp vi tính y tế (CT Scanner)
    
- [ ] d) Kính viễn vọng không gian

- **Giải thích:** Nguyên lý X-ray Computed Tomography (CT) là tái cấu trúc ảnh 3D từ các phép chiếu tia X ở nhiều hướng khác nhau, dựa trên thuật toán chiếu ngược có lọc.

**Câu 9:** Biến đổi nào sau đây được sử dụng làm thành phần cốt lõi trong chuẩn nén ảnh JPEG vì khả năng dồn năng lượng tuyệt vời và giả định tính tuần hoàn 2N giúp giảm thiểu lỗi gián đoạn ở biên?

- [ ] a) Biến đổi Fourier rời rạc (DFT)
    
- [x] b) Biến đổi Cosin rời rạc (DCT)
    
- [ ] c) Biến đổi Walsh-Hadamard (WHT)
    
- [ ] d) Biến đổi Hartley rời rạc (DHT)

- **Giải thích:** Biến đổi Cosin rời rạc (DCT) được sử dụng trong JPEG vì nó giả định tính tuần hoàn 2N và đối xứng chẵn, giúp giảm thiểu độ gián đoạn biên và tập trung năng lượng tốt hơn DFT.

**Câu 10:** Biến đổi Walsh-Hadamard (WHT) có lợi thế cực lớn về mặt tốc độ tính toán trên phần cứng kỹ thuật số bởi vì:

- [x] a) Các hàm cơ sở của nó chỉ sử dụng hai giá trị +1 và -1, chỉ yêu cầu phép cộng và trừ.
    
- [ ] b) Nó bỏ qua tất cả các tần số cao.
    
- [ ] c) Nó không cần chuyển ảnh sang miền tần số.
    
- [ ] d) Nó sử dụng hàm lượng giác phức tạp nhưng đã được tối ưu hóa.

- **Giải thích:** Biến đổi WHT phân rã tín hiệu thành các sóng vuông góc (Walsh functions) chỉ mang giá trị +1 và -1. Điều này giúp loại bỏ hoàn toàn phép nhân số thực, làm cho nó cực kỳ nhanh trên phần cứng.

**Câu 11:** Trong lý thuyết thông tin, Entropy H(S) đại diện cho:

- [ ] a) Dung lượng bộ nhớ tối đa cho phép để lưu trữ ảnh.
    
- [x] b) Giới hạn dưới (nhỏ nhất) của tốc độ bit trung bình để mã hóa không mất mát một tập dữ liệu.
    
- [ ] c) Mức độ sắc nét của bức ảnh sau khi giải nén.
    
- [ ] d) Số lượng pixel bị sai lệch do nhiễu.

- **Giải thích:** Định lý Shannon chỉ ra rằng đối với bất kỳ bộ mã hóa không mất mát nào, Entropy H(S) luôn là giới hạn dưới (cận dưới) của tốc độ bit trung bình (Bc >= H(S)).

**Câu 12:** Thuật toán mã hóa nào có khả năng gán một từ mã duy nhất (đại diện bởi một khoảng số thực từ 0 đến 1) cho TOÀN BỘ chuỗi thông điệp, thay vì gán mã cho từng ký hiệu riêng lẻ như Huffman?

- [ ] a) Lượng tử hóa Vector (Vector Quantization)
    
- [ ] b) Mã hóa Cắt cụt Khối (Block Truncation Coding)
    
- [x] c) Mã hóa Số học (Arithmetic Coding)
    
- [ ] d) Mã hóa Wavelet

- **Giải thích:** Mã hóa Số học (Arithmetic coding) tạo ra các mã "nonblock", gán một khoảng số thực (interval giữa 0 và 1) duy nhất cho toàn bộ chuỗi thông điệp, giúp đạt tỷ lệ nén sát giới hạn Entropy nhất.

**Câu 13:** Trong sơ đồ nén mất mát của chuẩn JPEG, bước nào là nguyên nhân chính gây ra sự mất mát thông tin vĩnh viễn (lossy) và tạo ra hiệu ứng vỡ khối (blocking artifacts)?

- [x] a) Lượng tử hóa các hệ số DCT (Quantization)
    
- [ ] b) Mã hóa Huffman (Entropy Coding)
    
- [ ] c) Quét Zig-zag (Coefficient to Symbol Map)
    
- [ ] d) Chuyển đổi không gian màu RGB sang YCbCr

- **Giải thích:** Trong sơ đồ JPEG, Lượng tử hóa (Quantizer) chia các hệ số DCT cho bảng Quantization Table và làm tròn. Việc làm tròn này làm mất phần thập phân vĩnh viễn, sinh ra hiện tượng vỡ khối.

**Câu 14:** Khi xem video trực tuyến bị giật lag, bạn thường thấy hình ảnh bị vỡ thành các ô vuông. Kỹ thuật nào trong chuẩn H.264/AVC được thiết kế đặc biệt (nằm trong vòng lặp giải mã) để làm mượt các ranh giới ô vuông này?

- [ ] a) Lượng tử hóa Vector (Vector Quantization)
    
- [ ] b) Dự đoán 2 chiều (B-pictures)
    
- [x] c) Bộ lọc gỡ khối (Deblocking Filter)
    
- [ ] d) Biến đổi Wavelet

- **Giải thích:** Chuẩn H.264/AVC giới thiệu Bộ lọc gỡ khối (Deblocking Filter) ngay trong vòng lặp giải mã để làm mịn các ranh giới giữa các khối macroblock do lượng tử hóa DCT gây ra.

**Câu 15:** Trong cấu trúc Video MPEG, loại khung hình nào được mã hóa độc lập (không tham chiếu đến khung hình khác) và đóng vai trò là điểm truy cập ngẫu nhiên khi người dùng tua video (Fast Forward/Rewind)?

- [ ] a) B-pictures (Bi-directional)
    
- [x] b) I-pictures (Intra-coded)
    
- [ ] c) P-pictures (Predictive)
    
- [ ] d) D-pictures (DC-coded)

- **Giải thích:** I-pictures (Intra-coded) được mã hóa hoàn toàn độc lập, không tham chiếu bất kỳ khung hình nào, do đó nó cung cấp điểm neo (random access points) để tua video.

**Câu 16:** Ứng dụng "Chuyển mã Video" (Video Transcoding) KHÔNG bao gồm tác vụ nào sau đây?

- [ ] a) Giảm độ phân giải không gian từ 4K xuống 1080p để phát trên điện thoại.
    
- [ ] b) Thay đổi định dạng nén từ MPEG-2 sang MPEG-4.
    
- [x] c) Tăng chất lượng của video gốc vượt quá mức lúc mới thu hình.
    
- [ ] d) Giảm tốc độ bit (bit-rate) để phù hợp với băng thông mạng yếu.

- **Giải thích:** Chuyển mã Video (Transcoding) dùng để giảm tốc độ bit, giảm độ phân giải, hoặc đổi định dạng. Theo lý thuyết thông tin, không một thuật toán nào có thể tạo ra thông tin thật để tăng chất lượng vượt qua bản gốc.

**Câu 17:** Để giảm dung lượng, một bức ảnh được lấy mẫu giảm (downsample) bằng cách giữ 1 pixel và vứt bỏ 3 pixel kề cạnh mà không áp dụng bất kỳ bộ lọc nào trước đó. Hiện tượng sai lệch thị giác nghiêm trọng xuất hiện trên các hoa văn kẻ sọc được gọi là gì?

- [ ] a) Blocking artifacts
    
- [x] b) Aliasing (Răng cưa/Nhiễu bóng ma)
    
- [ ] c) Ringing artifacts (Gợn sóng)
    
- [ ] d) Motion blur (Nhòe chuyển động)

- **Giải thích:** Hậu quả lớn nhất của việc Downsampling mà không qua bộ lọc pre-filter là hiện tượng Aliasing (răng cưa, chồng lấp phổ), tạo ra các đường vằn giả trên các hoa văn có tần số cao.

**Câu 18:** Khi phóng to ảnh (Upsampling), thuật toán Nội suy Bậc không (Zero-order / Nearest Neighbor) tạo ra kết quả hình ảnh như thế nào?

- [x] a) Bị vỡ thành các ô vuông (Blocky/Pixelated) do sao chép trực tiếp giá trị pixel cũ.
    
- [ ] b) Rất mượt mà và tự nhiên, không có răng cưa.
    
- [ ] c) Bị tối đi đáng kể do mất năng lượng.
    
- [ ] d) Chuyển thành ảnh đen trắng.

- **Giải thích:** Nội suy Zero-order (Nearest Neighbor / Pixel replication) có độ phức tạp thấp nhất, thuật toán chỉ đơn giản là sao chép pixel kề cận, dẫn đến kết quả bị vỡ thành các ô vuông rõ rệt.

**Câu 19:** Để tăng tốc độ khung hình của một video từ 24 fps lên 60 fps nhằm tạo hiệu ứng slow motion mượt mà, phương pháp tạo ra các khung hình trung gian tốt nhất là:

- [ ] a) Nội suy thời gian thuần túy (Pure temporal interpolation).
    
- [ ] b) Lọc thông thấp không gian (Spatial lowpass filtering).
    
- [x] c) Nội suy có bù chuyển động (Motion-compensated interpolation).
    
- [ ] d) Chuyển đổi mã hóa Huffman.

- **Giải thích:** Để tránh hiện tượng bóng ma khi vật thể di chuyển, việc tăng tốc độ khung hình (Frame-rate conversion) yêu cầu sử dụng Nội suy có bù chuyển động (Motion compensated interpolation) để ước tính đúng vị trí vật thể.

**Câu 20:** Trong phân tích bề mặt vật liệu (kết cấu/texture), ma trận nào được sử dụng để đếm tần suất hai điểm ảnh có mức xám cụ thể nằm cách nhau một khoảng xác định trong không gian?

- [ ] a) Ma trận Hiệp phương sai (Covariance Matrix)
    
- [x] b) Ma trận Đồng xuất hiện Mức xám (Graylevel Co-occurrence Matrix- GLCM)
    
- [ ] c) Ma trận Hadamard
    
- [ ] d) Ma trận Hessian

- **Giải thích:** Ma trận Đồng xuất hiện Mức xám (GLCM) sử dụng toán tử định vị Q để thống kê xác suất hai pixel có mức xám i, j nằm cách nhau một khoảng cho trước, là công cụ mạnh nhất để phân tích cấu trúc không gian của kết cấu (texture).

**Câu 21:** 7 Bất biến Mô-men (Hu Moments) trích xuất từ một vùng ảnh có đặc tính ứng dụng tuyệt vời nào trong nhận dạng mẫu?

- [ ] a) Luôn tạo ra một ảnh nhị phân chất lượng cao.
    
- [x] b) Giữ nguyên giá trị khi đối tượng trong ảnh bị dịch chuyển, phóng to/thu nhỏ, hoặc xoay.
    
- [ ] c) Tự động chuyển đổi ảnh sang miền tần số Fourier.
    
- [ ] d) Không bị ảnh hưởng bởi bóng râm và điều kiện ánh sáng.

- **Giải thích:** 7 Bất biến Mô-men (Moment invariants) của Hu được toán học chứng minh là bất biến (không đổi) khi đối tượng bị tịnh tiến (translation), thu phóng (scale), phản chiếu (mirror) và quay (rotation).

**Câu 22:** Phân tích Thành phần Chính (PCA) áp dụng trên ảnh đa phổ (Multispectral Image) nhằm mục đích chính là gì?

- [ ] a) Làm sắc nét các cạnh của đối tượng.
    
- [x] b) Nén dữ liệu và khử tương quan bằng cách ánh xạ các dải phổ sang một không gian đặc trưng mới.
    
- [ ] c) Tìm ra đường viền (boundary) của vùng sáng nhất.
    
- [ ] d) Chuyển đổi ảnh sang dạng mã chuỗi Freeman (Chain code).

- **Giải thích:** PCA phân tích ma trận hiệp phương sai của nhiều ảnh (VD: ảnh đa phổ) để tìm ra các Vector riêng. Các thành phần này giúp giải tương quan dữ liệu, loại bỏ dư thừa và nén thông tin hữu ích.

**Câu 23:** Giao thức đánh giá độ chính xác của các mô hình nhận diện đối tượng (Object Detection) thường sử dụng chỉ số IoU (Intersection over Union). Chỉ số này đo lường:

- [ ] a) Tỷ lệ giữa thời gian huấn luyện và thời gian suy luận.
    
- [x] b) Tỷ lệ diện tích phần giao nhau chia cho diện tích phần hợp nhất giữa Bounding box dự đoán và Bounding box chuẩn (Ground truth).
    
- [ ] c) Tốc độ khung hình trên giây (FPS) của thuật toán.
    
- [ ] d) Độ tương phản giữa đối tượng và nền.

- **Giải thích:** Chỉ số IoU = Diện tích phần giao (Intersection) / Diện tích phần hợp (Union). Nó dùng để đo lường mức độ trùng khớp giữa Bounding box do AI dự đoán và Bounding box chuẩn.

**Câu 24:** Đặc điểm kiến trúc cốt lõi làm nên tốc độ "thời gian thực" (real-time) của họ mô hình YOLO (You Only Look Once) so với họ R-CNN là gì?

- [ ] a) Sử dụng Mạng đề xuất vùng (Region Proposal Network- RPN) để tìm từng đối tượng.
    
- [x] b) Ánh xạ toàn bộ hình ảnh thành một lưới S×S và dự đoán trực tiếp cả Bounding box lẫn Phân loại trong một lần chạy duy nhất (Single-stage).
    
- [ ] c) Sử dụng các bộ lọc hình thái học (Morphological filters) để tách nền trước khi đưa vào mạng Nơ-ron.
    
- [ ] d) Hoàn toàn không sử dụng Mạng nơ-ron tích chập (CNN).

- **Giải thích:** Khác với R-CNN chia làm 2 giai đoạn (tìm vùng + phân loại), YOLO (You Only Look Once) chia ảnh thành lưới S x S và dự đoán trực tiếp toàn bộ kết quả trong một lần duy nhất, giúp đạt tốc độ thời gian thực.

**Câu 25:** Sự thay đổi tư duy thiết kế từ Anchor-based (dùng các hộp neo định sẵn) sang Anchor-free (như CornerNet, FCOS) giúp giải quyết vấn đề lớn nào trong Object Detection?

- [x] a) Tránh được sự mất cân bằng nghiêm trọng giữa số lượng mẫu âm (background) và mẫu dương, đồng thời giảm sự phụ thuộc vào các siêu tham số thủ công.
    
- [ ] b) Chuyển đổi ảnh màu sang ảnh xám nhanh hơn.
    
- [ ] c) Triệt tiêu được hiện tượng nhòe do chuyển động.
    
- [ ] d) Cải thiện chất lượng âm thanh đi kèm video.

- **Giải thích:** Các phương pháp Anchor-free (như CornerNet) không cần tạo ra hàng ngàn hộp neo giả định. Việc này giúp triệt tiêu vấn đề mất cân bằng lớp (do quá nhiều hộp neo lọt vào vùng nền- negative samples).

**Câu 26:** Trong Bộ phân loại Khoảng cách Tối thiểu (Minimum-distance classifier), nguyên mẫu (prototype) đại diện cho một lớp dữ liệu thông thường được tính bằng cách nào?

- [ ] a) Lấy vector có độ dài ngắn nhất trong lớp.
    
- [x] b) Lấy Vector trung bình (Mean vector) của tất cả các mẫu huấn luyện thuộc lớp đó.
    
- [ ] c) Lấy mẫu nằm ở vị trí biên của lớp.
    
- [ ] d) Dùng thuật toán PCA để tìm thành phần chính duy nhất.

- **Giải thích:** Trong Minimum-distance classifier, nguyên mẫu (prototype vectors) của một lớp thường được định nghĩa chính là Vector trung bình (mean vectors) của tất cả các mẫu thuộc lớp đó.

**Câu 27:** Rào cản lớn nhất khi triển khai Bộ phân loại Thống kê Tối ưu Bayes (Optimum Statistical Bayes Classifier) trong thực tế là gì?

- [x] a) Phải biết trước Hàm mật độ xác suất (PDF) và Xác suất tiên nghiệm của mọi lớp mẫu.
    
- [ ] b) Thuật toán chạy quá chậm so với Mạng Nơ-ron.
    
- [ ] c) Không thể sử dụng cho dữ liệu dạng vector.
    
- [ ] d) Yêu cầu ảnh đầu vào phải là ảnh nhị phân.

- **Giải thích:** Dù tối ưu về lý thuyết, để sử dụng bộ phân loại Bayes, hệ thống phải biết trước Hàm mật độ xác suất p(x|ck) và xác suất xuất hiện P(ck) của từng lớp- điều rất khó trong thực tế.

**Câu 28:** Thuật toán huấn luyện Perceptron (Mạng Nơ-ron cơ bản nhất) được đảm bảo sẽ hội tụ và tìm ra một siêu phẳng (hyperplane) phân chia dữ liệu NẾU VÀ CHỈ NẾU:

- [ ] a) Dữ liệu đầu vào đã được lọc nhiễu Gaussian.
    
- [ ] b) Số lượng nơ-ron ẩn lớn hơn 100.
    
- [x] c) Hai lớp mẫu dữ liệu có thể phân tách tuyến tính (Linearly separable).
    
- [ ] d) Hệ số học (learning rate) thay đổi liên tục.

- **Giải thích:** Định lý hội tụ Perceptron (Perceptron convergence theorem) phát biểu rằng thuật toán sẽ hội tụ trong một số bước hữu hạn nếu và chỉ nếu hai lớp mẫu có thể phân tách tuyến tính (Linearly separable).

**Câu 29:** Kiến trúc Mạng Nơ-ron VGG16 (2014) mang đến triết lý thiết kế nào đã trở thành tiêu chuẩn cho việc trích xuất đặc trưng hình ảnh?

- [ ] a) Sử dụng các bộ lọc tích chập (Convolutional filters) kích thước rất lớn (như 11 x 11) để bao quát ảnh.
    
- [x] b) Sử dụng lặp đi lặp lại các bộ lọc kích thước cực nhỏ (3 x 3) kết hợp với Max Pooling để tăng độ sâu của mạng.
    
- [ ] c) Hoàn toàn loại bỏ lớp Tích chập, chỉ dùng lớp Kết nối đầy đủ (Fully connected).
    
- [ ] d) Sử dụng thuật toán Random Forest thay cho lớp softmax ở cuối.

- **Giải thích:** Đặc điểm của VGG16 là sử dụng lặp đi lặp lại các bộ lọc tích chập kích thước rất nhỏ (3 x 3, 1x1) kết hợp thành các khối (blocks), giúp tăng chiều sâu mạng lên 16-19 lớp mà vẫn kiểm soát được lượng tham số.

**Câu 30:** Mạng Residual Network (ResNet) giải quyết triệt để bài toán suy giảm Gradient (Vanishing Gradient) khi huấn luyện các mô hình cực sâu (hàng trăm lớp) bằng công nghệ lõi nào?

- [ ] a) Sử dụng Lượng tử hóa Vector (Vector Quantization).
    
- [x] b) Thêm các đường kết nối tắt (Shortcut/Skip connections) bỏ qua một số lớp để cộng trực tiếp tín hiệu vào đầu ra.
    
- [ ] c) Thay đổi hàm kích hoạt từ ReLU sang Sigmoid.
    
- [ ] d) Tăng kích thước Batch size lên vô hạn.

- **Giải thích:** Kiến trúc ResNet-50 đột phá bằng cách thêm các "Shortcut / Skip connections". Cấu trúc này cho phép gradient lan truyền ngược đi tắt qua các lớp, giải quyết hoàn toàn vấn đề Vanishing Gradient ở các mạng cực sâu.

---








