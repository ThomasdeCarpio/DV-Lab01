## Role and Problem Definition
*   **Vai trò:** Chuyên viên Phân tích Chiến lược Bán lẻ (Tech-Retail Consultant).
*   **Bài toán chung:** Tối ưu hóa chiến lược giá và danh mục sản phẩm (inventory) giữa 7 chuỗi bán lẻ lớn tại VN nhằm chiếm lĩnh thị phần.

---

### Theme 1: Price and Competitive Landscape (Giá & Năng lực cạnh tranh)

**Objective 1: So sánh mức độ tập trung ngành hàng của các đối thủ**
- **Selected metrics:** Số lượng model (Laptop count) và Loại máy (Category: Gaming/Office/Creator).
- **Metric meaning:** Số lượng mẫu mã laptop được phân bổ theo từng mục đích sử dụng tại mỗi chuỗi bán lẻ.
- **Why this metric fits:** Giúp xác định chính xác ai là đối thủ cạnh tranh chính trong từng mảng thị trường cụ thể.
- **Chart choice:** Clustered column chart, phù hợp để so sánh trực tiếp số lượng của nhiều hạng mục giữa các chuỗi bán lẻ.

**Objective 2: Đánh giá thị phần theo phân khúc giá**
- **Selected metrics:** Số lượng model thuộc các mức giá (Dưới 15tr, 15-25tr, 25-45tr, Trên 45tr).
- **Metric meaning:** Tỷ trọng hàng hóa của một cửa hàng được chia theo các mức giá khác nhau.
- **Why this metric fits:** Nó cho thấy đối thủ đang tập trung phục vụ tệp khách hàng bình dân hay cao cấp.
- **Chart choice:** 100% Stacked column chart, phù hợp để thể hiện cơ cấu phần trăm (%) danh mục sản phẩm của mỗi bên.

**Objective 3: Đánh giá chiến lược định giá tổng thể của các chuỗi bán lẻ**
- **Selected metrics:** Giá bán hiện tại (Current price) và Chuỗi bán lẻ (Source).
- **Metric meaning:** Sự phân bổ các mức giá (giá thấp nhất, cao nhất, và giá trung vị) của toàn bộ sản phẩm trong một cửa hàng.
- **Why this metric fits:** Giúp xác định ngay lập tức chuỗi nào chuyên bán hàng giá rẻ, chuỗi nào định vị cao cấp, và chuỗi nào có khoảng giá rộng nhất (phục vụ mọi đối tượng) mà không cần so khớp từng model.
- **Chart choice:** Boxplot (Biểu đồ hộp), hoàn hảo để so sánh mức giá trung vị (median), độ phân tán (spread) và các mức giá ngoại lệ (outliers) giữa nhiều đối thủ cùng lúc.

---

### Theme 2: Technology Transition (Chuyển đổi "Laptop AI")

**Objective 4: Định giá giá trị của tính năng AI (AI Premium)**
- **Selected metrics:** Giá bán hiện tại và Nhãn AI (is_ai_laptop: True/False).
- **Metric meaning:** Chênh lệch mức giá trung bình giữa máy có NPU (AI) và máy thường có cùng cấu hình.
- **Why this metric fits:** Nó giúp đánh giá xem việc tăng giá bán lẻ cho tính năng AI có đang ở mức hợp lý với người dùng hay không.
- **Chart choice:** Grouped bar chart, phù hợp để so sánh trực tiếp mức giá trung bình giữa hai nhóm máy.

---

### Theme 3: Hardware Trends (Cấu hình & Công nghệ)

**Objective 5: Theo dõi xu hướng chuyển dịch lên RAM 32GB**
- **Selected metrics:** Dung lượng RAM (16GB vs 32GB) và Phân khúc giá.
- **Metric meaning:** Tỷ lệ phần trăm laptop sử dụng RAM 32GB trong từng tầm giá.
- **Why this metric fits:** Nó giúp nhà bán lẻ ra quyết định có nên giảm nhập hàng 16GB để chuyển sang ưu tiên nhập chuẩn RAM 32GB hay không.
- **Chart choice:** 100% Stacked bar chart, phù hợp để quan sát sự thay đổi tỷ trọng cấu hình trên các mức giá.

---

### Theme 4: Product and Brand Strategy (Sản phẩm & Thương hiệu)

**Objective 6: Xác định thế mạnh của từng thương hiệu**
- **Selected metrics:** Số lượng model, Thương hiệu (Brand), và Loại máy (Category).
- **Metric meaning:** Tỷ trọng phân bổ dòng sản phẩm của một hãng (ví dụ: Hãng A làm bao nhiêu % Gaming, bao nhiêu % Office).
- **Why this metric fits:** Cung cấp cơ sở để tư vấn cho chuỗi bán lẻ nên chọn nhập hàng của hãng nào khi muốn mở rộng một ngách thị trường cụ thể.
- **Chart choice:** 100% Stacked column chart, phù hợp để hiển thị cấu trúc định vị bên trong của mỗi thương hiệu.

**Objective 7: Phân loại thương hiệu theo Giá và Cấu hình**
- **Selected metrics:** Giá trung bình (Median price) và RAM trung bình của từng thương hiệu.
- **Metric meaning:** Mức chi phí và hiệu năng đại diện cho từng hãng trên thị trường.
- **Why this metric fits:** Nó giúp phân loại các hãng thành nhóm "Bình dân", "Tầm trung", và "Cao cấp" để setup danh mục hàng hóa phù hợp với định vị của shop.
- **Chart choice:** Scatter plot, phù hợp để phân cụm (clustering) các thương hiệu dựa trên hai biến số định lượng.

---

### Theme 5: Consumer Demand (Nhu cầu Khách hàng - TGDD Deep Dive)

**Objective 8: Nhận diện thương hiệu được ưa chuộng nhất theo nhu cầu**
- **Selected metrics:** Số lượt khách hài lòng (Satisfied info), Thương hiệu, và Loại máy.
- **Metric meaning:** Tổng khối lượng tương tác và sự hài lòng của người tiêu dùng đối với từng hãng.
- **Why this metric fits:** Đóng vai trò như một thước đo thay thế cho doanh số (sales proxy), giúp cửa hàng biết hãng nào đang bán chạy nhất để tự tin nhập hàng.
- **Chart choice:** Bar chart, phù hợp để xếp hạng quy mô mức độ ưa chuộng giữa các hãng.

**Objective 9: Xác thực nhu cầu nâng cấp RAM thực tế của thị trường**
- **Selected metrics:** Số lượt khách hài lòng và Dung lượng RAM (16GB vs 32GB).
- **Metric meaning:** Mức độ quan tâm và sẵn sàng chi trả của khách hàng cho nhóm máy nhiều RAM (ở phân khúc >20tr).
- **Why this metric fits:** Kiểm chứng xem xu hướng nhập hàng RAM 32GB của các đại lý có thực sự khớp với nhu cầu mua thực tế của người dùng hay không.
- **Chart choice:** Donut chart, phù hợp để so sánh tỷ lệ chia sẻ sự quan tâm giữa hai nhóm cấu hình.

**Objective 10: Đánh giá mức độ hài lòng theo phân khúc giá**
- **Selected metrics:** Điểm đánh giá trung bình (Avg rating), Số lượt khách hài lòng, và Phân khúc giá.
- **Metric meaning:** Mức độ đáp ứng kỳ vọng của sản phẩm đối với số tiền khách hàng bỏ ra.
- **Why this metric fits:** Tìm ra phân khúc giá có điểm đánh giá thấp nhất, từ đó phát hiện "khoảng trống thị trường" để cửa hàng nhập các model thay thế chất lượng hơn.
- **Chart choice:** Bubble chart, với trục X là Phân khúc giá, trục Y là Điểm đánh giá, và độ lớn bong bóng là Số lượng khách, phù hợp để thấy bức tranh toàn cảnh về sự hài lòng.