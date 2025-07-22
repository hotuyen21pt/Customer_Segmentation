===========================

CUSTOMER SEGMENTATION PROJECT
===========================

 MỤC TIÊU DỰ ÁN
---------------------------
Phân tích dữ liệu hành vi mua sắm của khách hàng tại các trung tâm thương mại nhằm phân khúc khách hàng dựa trên thói quen mua sắm. Mục tiêu là đề xuất các chiến lược tiếp thị phù hợp cho từng nhóm khách hàng để tăng doanh thu và giữ chân khách hàng.

 DỮ LIỆU SỬ DỤNG
---------------------------
- Tập dữ liệu: customer_shopping_data.csv (~99,000 bản ghi)
- Các cột chính: 
  + customer_id
  + gender
  + age
  + category
  + quantity
  + price
  + payment_method
  + invoice_date
  + shopping_mall

⚙️ QUY TRÌNH THỰC HIỆN
---------------------------
1. Tiền xử lý dữ liệu (Python)
   - Chuyển đổi ngày tháng về định dạng datetime
   - Tạo biến mới: total_amount, invoice_monthyear
   - Loại bỏ outliers bằng IQR
   - Mã hóa biến phân loại
   - Chuẩn hóa dữ liệu với StandardScaler

2. Phân tích khám phá (EDA)
   - Doanh thu theo tháng
   - Tỷ lệ giới tính
   - Sản phẩm phổ biến
   - Sản phẩm phổ biến theo giới tính

3. Phân cụm khách hàng (Clustering)
   - Gom nhóm dữ liệu theo customer_id
   - Đặc trưng: độ tuổi, giới tính, tổng chi tiêu, số lượng sản phẩm, số trung tâm từng ghé,...
   - Áp dụng KMeans Clustering
   - Tìm số cụm tối ưu bằng Elbow Method

4. Trực quan hóa trên Power BI
   - Tổng quan doanh thu theo tháng, năm
   - Tỷ lệ khách hàng theo giới tính
   - Doanh thu theo trung tâm thương mại
   - Biểu đồ thể hiện cụm khách hàng và đặc điểm phân nhóm

 KẾT QUẢ PHÂN CỤM & CHIẾN LƯỢC
---------------------------

Cluster 0:
- Số lượng mua trung bình khá thấp, tổng chi tiêu tầm trung
- Chiến lược: tập trung vào upsell/cross-sell để tăng giá trị đơn hàng

Cluster 1:
- Số lượng mua rất thấp, tổng chi tiêu thấp nhất
- Chiến lược: chạy chương trình khuyến mãi, gói bundle để kích thích mua hàng

Cluster 2:
- Số lượng mua nhiều nhất, chi tiêu tầm trung
- Chiến lược: đẩy combo sản phẩm, chương trình khách hàng thân thiết (loyalty)

Cluster 3:
- Số lượng mua cao, tổng chi tiêu rất cao
- Chiến lược: chăm sóc nhóm VIP/Premium, ưu đãi riêng, tặng quà cá nhân hóa

 MÔ HÌNH & CÔNG CỤ SỬ DỤNG
---------------------------
- Python (Pandas, NumPy, Seaborn, Matplotlib)
- Scikit-learn (KMeans, LabelEncoder, StandardScaler)
- Yellowbrick (Elbow Method)
- Google Colab
- Power BI (Dashboard báo cáo và tương tác)

 KẾT LUẬN
---------------------------
Phân khúc khách hàng giúp doanh nghiệp hiểu rõ nhu cầu và hành vi của từng nhóm, từ đó cá nhân hóa tiếp thị, tăng doanh thu và tối ưu chi phí. Dashboard Power BI hỗ trợ trực quan hóa dữ liệu và ra quyết định nhanh chóng.

 CẤU TRÚC FILE DỰ ÁN
---------------------------
- Customer_Segmentation.ipynb  → Notebook chính
- customer_shopping_data.csv   → Dữ liệu gốc
- Dashboard.pbix               → File dashboard Power BI
- README.txt                   → Mô tả dự án

