
**4. Phân tích STFT và Phương pháp OLA (Câu 43, 59)**

- **Công thức STFT:** $$X_{\hat{n}}(e^{j\hat{\omega}}) = \sum_{m=-\infty}^{\infty} x[m]w[\hat{n}-m]e^{-j\hat{\omega}m}$$
- **Sự đánh đổi khốc liệt (Câu 43):** Hàm cửa sổ $w[m]$ sinh ra một nghịch lý vật lý (nguyên lý bất định Heisenberg). Cửa sổ quá dài $\rightarrow$ độ phân giải tần số tốt nhưng nhòe thời gian. Cửa sổ quá ngắn $\rightarrow$ bắt dính thời gian nhưng phổ tần số bị nhòe. Do đó, thách thức vĩnh cửu của STFT là **Cân bằng độ phân giải thời gian và tần số**.
- **Overlap-Add (OLA) (Câu 59):** Khi bạn chỉnh sửa âm thanh (ví dụ như Auto-Tune) trên miền STFT, bạn chia tín hiệu thành các khung. Để ráp chúng lại thành Audio ban đầu mà không bị giật cụ cục (discontinuities), bạn phải xếp chúng gối lên nhau (overlap) và cộng lại (add): $$y[n] = \sum_{r} y_r[n]$$ _Ưu điểm lớn nhất của OLA_ chính là nếu không có chỉnh sửa gì, nó đảm bảo **khôi phục lại tín hiệu hoàn hảo (perfect reconstruction)** 100% so với ban đầu.