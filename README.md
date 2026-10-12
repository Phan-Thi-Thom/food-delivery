# Food Delivery Time Prediction

## Tổng quan
Dự đoán thời gian giao đồ ăn (phút) dựa trên 22 đặc trưng về đơn hàng, thời tiết, giao thông và người giao hàng. Xử lý tập dữ liệu 50.000 bản ghi từ Kaggle.

## Công cụ & Quy trình
- **Công cụ:** Python (Pandas, Scikit-learn, Matplotlib, Seaborn).
- **Tiền xử lý:** Làm sạch dữ liệu, loại bỏ biến rò rỉ (`Average_Speed_kmph`), mã hóa biến phân loại, chuẩn hóa (StandardScaler). Chia tập Train/Val/Test (70/15/15).
- **Mô hình:** Huấn luyện và so sánh Linear Regression, Decision Tree, Random Forest.

## Kết quả
- **Mô hình tốt nhất:** Random Forest.
- **Hiệu năng:** MAE = 3.06 phút, R² = 0.9865.
- **Top 3 yếu tố ảnh hưởng (Feature Importance):** Khoảng cách giao hàng (51%), Phương tiện (22%), Mức độ giao thông (13%).

## Ý nghĩa thực tế
Với sai số trung bình chỉ 3 phút, mô hình giúp:
- **Khách hàng:** Chủ động thời gian chờ.
- **Doanh nghiệp:** Tối ưu phân bổ tài xế, đặc biệt trong giờ cao điểm.
- **Hệ thống:** Cảnh báo sớm các đơn hàng có nguy cơ giao chậm (đường xa, xe đạp, giờ cao điểm).
