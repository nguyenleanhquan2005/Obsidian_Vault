**PageRank** là một thuật toán phân tích liên kết dùng để **đánh giá mức độ quan trọng, uy tín và mức độ phổ biến của một trang web** trên mạng lưới Internet. Thuận toán gán cho mỗi trang web một điểm số bằng số nằm trong khoảng từ 0 đến 1.

Thuật toán này hoạt động dựa trên các nguyên lý cốt lõi sau:

- **Tính chất đệ quy (Recursive):** Một trang web được đánh giá là có điểm PageRank cao nếu nó **được trỏ tới bởi nhiều trang web khác cũng có điểm PageRank cao**. Các liên kết trỏ đến (inbound links) từ các trang khác được hệ thống xem như những "lá phiếu" bầu chọn cho độ uy tín của trang đó.
- **Mô hình người lướt web ngẫu nhiên (Random Surfer):** PageRank mô phỏng hành vi của một người lướt web ngẫu nhiên, cứ liên tục nhấp vào các đường link có trên màn hình. Điểm PageRank của một trang thực chất là **xác suất (hoặc tỷ lệ phần trăm thời gian) mà người lướt web ngẫu nhiên đó sẽ dừng chân tại trang này**.
- **Cơ chế chia sẻ điểm:** Điểm PageRank của một trang web không giữ nguyên mà sẽ được chia đều cho tất cả các liên kết trỏ ra ngoài (outgoing links) của trang đó để truyền giá trị cho các trang khác.

**Vai trò của PageRank trong máy tìm kiếm:** Trong khi TF-IDF chuyên đánh giá mức độ khớp giữa nội dung văn bản và từ khóa, thì PageRank hoạt động như một **tín hiệu xếp hạng tĩnh (static rank)** hoàn toàn độc lập với câu truy vấn. Khi bạn tìm kiếm một từ khóa phổ biến trả về hàng triệu kết quả (ví dụ: "eBay"), điểm PageRank giúp công cụ tìm kiếm lọc ra và xếp hạng trang chủ chính thức uy tín nhất lên đầu tiên thay vì một trang vô danh cũng chứa từ khóa đó