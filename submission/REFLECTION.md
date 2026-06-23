# Lab 19 Reflection

**Khi nào Hybrid Search chiến thắng?**
Hybrid Search phát huy sức mạnh tối đa trên các truy vấn dạng "mixed" (trộn lẫn). Khi người dùng vừa dùng từ khóa chuyên ngành (cần độ chính xác tuyệt đối của BM25), vừa dùng các cụm từ mô tả tự nhiên (cần khả năng hiểu ngữ nghĩa paraphrase của Vector). Công thức Reciprocal Rank Fusion (RRF) giúp đẩy những kết quả xuất hiện ở top của cả 2 thuật toán lên cao nhất, khắc phục điểm mù của từng phương pháp đơn lẻ.

**Khi nào không nên dùng Hybrid?**
Không nên dùng Hybrid khi hệ thống cần ưu tiên 100% "Exact Match", ví dụ: tra cứu mã số lỗi kỹ thuật (Error Code), mã đơn hàng, hoặc tên cấu hình server cụ thể. Trong trường hợp này, Semantic Search có xu hướng "hiểu nhầm" các mã này sang các mã tương đồng về mặt hình thức, làm loãng kết quả của BM25. Ngoài ra, trên các truy vấn thuần túy Paraphrase không có từ khóa gốc, Vector Search độc lập thường đã hoạt động đủ tốt mà không cần tốn thêm tài nguyên tính toán BM25 và RRF.
