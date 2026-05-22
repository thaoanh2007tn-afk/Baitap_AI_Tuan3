# 🏥 HealthAI — Hệ Thống Dự Đoán Tiểu Đường

Ứng dụng Streamlit đa trang với giao diện **Luxury Medical Dark** (Navy + Teal).

## Cấu trúc thư mục

```
diabetes_app/
│
├── main.py                  ← Entry point 
│
├── assets/
│   ├── style.css            ← Toàn bộ CSS/thiết kế chung
│   
├── models/
│   ├── diabetes_model.h5    ← Mô hình Keras đã train
│   └── scaler.pkl           ← StandardScaler đã fit
│
└── pages/
    ├── __init__.py
    ├── login.py             ← Trang đăng nhập
    ├── home.py              ← Trang chủ + gallery ảnh
    └── predict.py           ← Form nhập liệu + popup kết quả
```

## Cách chạy

```bash
# Cài dependencies
pip install streamlit keras tensorflow scikit-learn pandas numpy

# Chạy ứng dụng
streamlit run main.py
```

## Tài khoản demo

DEFAULT_ACCOUNTS = {
    "tonngokhong@health.ai":   {"password": "tonngokhong", "name": "Tôn Ngộ Không"},
    "trubacgioi@health.ai":  {"password": "trubatgioi",  "name": "Trư Bát Giới"},
    "duongtang@health.ai": {"password": "duongtang123", "name": "Đường Tăng"},
    "satang@health.ai": {"password": "satang123", "name": "Sa Tăng"},
}

## Luồng điều hướng

```
Login page  ─(đăng nhập thành công)→  Home page
Home page   ─(bấm "Bắt đầu kiểm tra")→  Predict page
Predict page ─(bấm "Phân tích")→  Popup kết quả =
Pop up kết quả ─(bấm "Thực hiện đánh giá nới")→  Predict pages
Home page   ─(bấm "Đăng xuất")→  Login page
```


