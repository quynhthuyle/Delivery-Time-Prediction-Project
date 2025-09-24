Mô tả dự án
Dự án này tập trung vào việc dự đoán thời gian giao hàng (Delivery Time Prediction) trong lĩnh vực giao đồ ăn bằng cách áp dụng các kỹ thuật Machine Learning. Mục tiêu chính là xây dựng một hệ thống có khả năng ước lượng chính xác ETA – Estimated Time of Arrival, giúp tối ưu hóa quy trình vận hành logistics và mang lại trải nghiệm tốt hơn cho khách hàng.

Quy trình thực hiện dự án bao gồm nhiều giai đoạn:
- Tiền xử lý dữ liệu (Data Preprocessing): Làm sạch và chuẩn hóa dữ liệu từ tập Food Delivery Dataset, loại bỏ giá trị nhiễu, chuẩn hóa định dạng thời gian, đồng thời xây dựng các đặc trưng (features) quan trọng cho mô hình.
- Phân cụm dữ liệu (Clustering): Sử dụng các thuật toán như K-Means để nhóm các đơn hàng hoặc khách hàng theo đặc điểm giống nhau, từ đó hỗ trợ việc huấn luyện mô hình dự đoán.
- Xây dựng mô hình dự đoán (Prediction Models): Triển khai các thuật toán hồi quy (Regression Models) để ước lượng thời gian giao hàng dựa trên nhiều yếu tố: khoảng cách, điều kiện giao thông, đặc điểm khách hàng và tài xế giao hàng.
- Lưu trữ và tái sử dụng mô hình: Các mô hình và bộ biến đổi (scaler) đã được huấn luyện được lưu dưới dạng file .pkl, giúp dễ dàng triển khai và sử dụng lại trong các lần dự đoán sau.
- Trực quan hóa kết quả (Dashboard): Một dashboard được thiết kế nhằm trực quan hóa hiệu suất của mô hình, so sánh thời gian dự đoán với thực tế, và cung cấp các chỉ số đánh giá để dễ dàng theo dõi.

Thông qua dự án, nhóm mong muốn mang lại giải pháp hỗ trợ cho doanh nghiệp trong việc giảm tỷ lệ giao hàng trễ, tối ưu chi phí vận hành, nâng cao hiệu quả quản lý đội ngũ shipper, đồng thời tăng mức độ hài lòng của khách hàng trong bối cảnh thương mại điện tử và dịch vụ giao nhận ngày càng phát triển.
