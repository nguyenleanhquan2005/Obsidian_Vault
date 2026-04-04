# 📋 Hướng dẫn setup Obsidian

## 1. Cấu trúc thư mục

```
Machine Learning/
├── 🗺️ MOC - Machine Learning.md     ← Điểm bắt đầu
├── Supervised/
│   ├── Supervised Learning Overview.md
│   ├── Linear Regression.md
│   ├── Logistic Regression.md
│   ├── Decision Tree.md
│   ├── Naive Bayes Classifier.md
│   ├── Perceptron Algorithm.md
│   ├── Support Vector Machine.md
│   ├── K-Nearest Neighbors.md
│   ├── Regularization Algorithms.md
│   ├── Random Forest.md
│   ├── XGBoost.md
│   └── LightGBM.md
├── Unsupervised/
├── Deep Learning/
├── MLOps/
├── Applications/
├── Math Foundation/
└── (các file còn lại nằm thẳng trong Machine Learning/)
```

---

## 2. Plugin cần cài

### Bắt buộc
- **Dataview** — để các bảng query hoạt động

### Khuyên dùng
- **Obsidian Git** — backup vault lên GitHub tự động
- **Kanban** — theo dõi tiến độ học bằng board
- **Calendar** — review hàng tuần
- **Templater** — tạo note mới nhanh từ template

---

## 3. Cách dùng Dataview

Các file có frontmatter `status`. Bạn có thể đổi status theo tiến độ:

```
⬜ chưa học
📖 đang học  
✅ đã hiểu
🔁 cần ôn lại
```

Query tất cả note chưa học:
```dataview
TABLE file.folder AS "Folder"
FROM "Machine Learning"
WHERE status = "⬜ chưa học"
SORT file.folder ASC
```

Query note đã học xong:
```dataview
TABLE file.mtime AS "Lần cuối sửa"
FROM "Machine Learning"
WHERE status = "✅ đã hiểu"
SORT file.mtime DESC
```

---

## 4. Template cho note thuật toán mới

Khi tạo note mới cho thuật toán bạn tự nghiên cứu, copy format này:

```markdown
---
tags:
  - machine-learning
  - algorithm
  - [thêm tag phù hợp]
status: "⬜ chưa học"
type: [classification / regression / clustering]
created: YYYY-MM-DD
---

# Tên Thuật Toán

> **Quay về:** [[🗺️ MOC - Machine Learning]] | [[Tên Overview liên quan]]

---

## 📝 Định nghĩa của tôi

> (Viết lại bằng lời của bạn)

---

## 🧠 Ý tưởng cốt lõi

---

## 📐 Công thức

---

## ✅ Ưu / ❌ Nhược điểm

---

## 🎯 Use case thực tế

---

## 💻 Code mẫu

---

## 🔗 Related

---

## 📚 Nguồn tham khảo
```

---

## 5. Workflow học hàng ngày

1. Mở **MOC** → chọn note tiếp theo cần học
2. Đổi `status` thành `📖 đang học`
3. Học xong → điền **"📝 Định nghĩa của tôi"** trước tiên
4. Thêm code mẫu, công thức, use case
5. Đổi `status` thành `✅ đã hiểu`
6. Mở Graph View — thấy wikilink tạo thành web kiến thức
