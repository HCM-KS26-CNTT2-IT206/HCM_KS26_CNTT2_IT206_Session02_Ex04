# BÀI 4: CHẨN ĐOÁN VÀ “PHẪU THUẬT” PROMPT SƠ SÀI THÀNH CHUẨN CREATE

## PHẦN 1: PHÂN TÍCH CHẨN ĐOÁN LỖI

Khung CREATE gồm 6 thành phần:

- **C – Context:** Bối cảnh, thông tin và vai trò của AI.
- **R – Request:** Yêu cầu cụ thể cần AI thực hiện.
- **E – Examples:** Ví dụ mẫu để AI hiểu cách trả lời mong muốn.
- **A – Adjustment:** Điều chỉnh giọng văn, phong cách và những điều cần tránh.
- **T – Type of Output:** Định dạng đầu ra mong muốn.
- **E – Extras:** Thông tin bổ sung, giới hạn và tiêu chí cần đáp ứng.

### 1. Bộ phận CSKH

**Prompt ban đầu:** "Viết tin nhắn xin lỗi khách vì hàng giao chậm."

**Các lỗi còn thiếu:**

- **Character (vai trò thuộc Context):** Chưa xác định AI là nhân viên chăm sóc khách hàng chuyên nghiệp của TechShop.
- **Adjustment:** Chưa quy định giọng văn lịch sự, chân thành, đồng cảm và không sử dụng lời xin lỗi sáo rỗng.
- **Type of Output:** Chưa yêu cầu định dạng tin nhắn hoàn chỉnh để gửi trực tiếp cho khách hàng.

**Hậu quả:** Tin nhắn dễ bị chung chung, thiếu sự đồng cảm, không đưa ra thời gian giao hàng dự kiến và phương án hỗ trợ khách hàng.

### 2. Bộ phận Bán hàng

**Prompt ban đầu:** "Tư vấn cho anh khách mua laptop gaming."

**Các lỗi còn thiếu:**

- **Extras:** Thiếu ngân sách, nhu cầu sử dụng, thương hiệu yêu thích và tiêu chí lựa chọn laptop.
- **Request:** Chưa yêu cầu AI phân tích cấu hình, so sánh sản phẩm và đề xuất lựa chọn phù hợp.
- **Examples:** Không có ví dụ về cách trình bày một bài tư vấn laptop rõ ràng, dễ hiểu.

**Hậu quả:** AI đưa ra quá nhiều sản phẩm nhưng không tập trung vào nhu cầu thực tế, khiến khách hàng khó lựa chọn.

### 3. Bộ phận Kỹ thuật bảo hành

**Prompt ban đầu:** "Báo giá thay màn hình laptop vỡ cho khách."

**Các lỗi còn thiếu:**

- **Character (vai trò thuộc Context):** Chưa xác định AI là nhân viên kỹ thuật bảo hành có kinh nghiệm của TechShop.
- **Type of Output:** Chưa yêu cầu bảng báo giá cụ thể, có các hạng mục chi phí rõ ràng.
- **Adjustment:** Chưa quy định cách giải thích dễ hiểu, minh bạch, lịch sự và tránh đưa ra thông tin giá không chính xác.

**Hậu quả:** Khách hàng không biết chi phí dự kiến, thời gian sửa chữa và chính sách bảo hành sau khi thay màn hình.

---

## PHẦN 2: NÂNG CẤP VÀ CHUẨN HÓA CÂU LỆNH

### 1. Master Prompt cho bộ phận CSKH

**C – Context (Bối cảnh):**

Bạn là nhân viên chăm sóc khách hàng chuyên nghiệp của chuỗi bán lẻ công nghệ TechShop. Công việc của bạn là tiếp nhận phản hồi, giải quyết khiếu nại và duy trì sự hài lòng của khách hàng. Hiện tại, một khách hàng đang không hài lòng vì đơn hàng laptop bị giao chậm so với thời gian dự kiến.

**R – Request (Yêu cầu):**

Hãy viết một tin nhắn xin lỗi khách hàng, trong đó:

- Thể hiện sự xin lỗi chân thành và đồng cảm với sự bất tiện của khách.
- Giải thích ngắn gọn về tình trạng giao hàng.
- Đưa ra thời gian giao hàng dự kiến nếu đã có thông tin xác nhận.
- Đề xuất phương án hỗ trợ hoặc đền bù phù hợp theo chính sách TechShop.
- Cung cấp lời cam kết theo dõi đơn hàng đến khi giao thành công.

**E – Examples (Ví dụ):**

Ví dụ cách diễn đạt: "TechShop rất xin lỗi vì đơn hàng của anh/chị chưa được giao đúng thời gian dự kiến. Bên em hiểu việc này đã gây ảnh hưởng đến kế hoạch của anh/chị và sẽ chủ động kiểm tra, cập nhật tình trạng đơn hàng sớm nhất."

**A – Adjustment (Điều chỉnh):**

- Sử dụng giọng văn lịch sự, chân thành, gần gũi.
- Không đổ lỗi cho đơn vị vận chuyển.
- Không sử dụng những câu xin lỗi sáo rỗng.
- Không hứa thời gian giao hàng hoặc mức đền bù khi chưa được xác nhận.
- Ưu tiên giải quyết vấn đề và giữ niềm tin của khách hàng.

**T – Type of Output (Định dạng đầu ra):**

Trình bày thành một tin nhắn hoàn chỉnh có thể gửi qua Zalo hoặc Messenger, độ dài khoảng 100–150 từ.

**E – Extras (Thông tin bổ sung):**

Thông tin đơn hàng:

- Mã đơn hàng: [Mã đơn]
- Tên khách hàng: [Tên khách]
- Sản phẩm: [Tên sản phẩm]
- Thời gian giao dự kiến ban đầu: [Ngày giao]
- Tình trạng hiện tại: [Lý do chậm giao]
- Thời gian giao mới: [Nếu đã xác nhận]
- Chính sách hỗ trợ: [Thông tin ưu đãi hoặc đền bù được duyệt]

Nếu thiếu thông tin, hãy đánh dấu những nội dung cần bổ sung thay vì tự ý tạo dữ liệu.

### 2. Master Prompt cho bộ phận Bán hàng

**C – Context (Bối cảnh):**

Bạn là chuyên viên tư vấn bán hàng công nghệ tại TechShop, có kiến thức về các dòng laptop gaming của ASUS, Acer, MSI, Lenovo và các thương hiệu khác. Bạn cần tư vấn cho một khách hàng đang muốn mua laptop gaming để chơi game, học tập và giải trí.

**R – Request (Yêu cầu):**

Hãy phân tích nhu cầu và đề xuất 3 mẫu laptop gaming phù hợp nhất. Với mỗi sản phẩm, cần:

- Nêu tên và thương hiệu sản phẩm.
- Cung cấp cấu hình CPU, GPU, RAM, SSD và màn hình.
- Giải thích khả năng chơi game và sử dụng thực tế.
- Nêu ưu điểm và hạn chế.
- Đưa ra mức giá tham khảo nếu có dữ liệu.
- So sánh 3 sản phẩm và chọn ra một mẫu đáng mua nhất.

**E – Examples (Ví dụ):**

Ví dụ cách tư vấn:

"Laptop ASUS TUF Gaming phù hợp với người dùng cần một chiếc máy có hiệu năng tốt trong tầm giá. Máy có card đồ họa rời, đáp ứng tốt nhu cầu chơi game phổ biến và học tập công nghệ thông tin."

**A – Adjustment (Điều chỉnh):**

- Sử dụng ngôn ngữ thân thiện, dễ hiểu, chuyên nghiệp.
- Không sử dụng quá nhiều thuật ngữ kỹ thuật khó hiểu.
- Không chỉ tập trung giới thiệu sản phẩm đắt tiền.
- Đưa ra nhận xét khách quan, không quảng cáo quá mức.
- Ưu tiên nhu cầu và ngân sách của khách hàng.

**T – Type of Output (Định dạng đầu ra):**

Trình bày theo bảng so sánh 3 sản phẩm, sau đó đưa ra phần tư vấn ngắn gọn và kết luận lựa chọn phù hợp nhất.

**E – Extras (Thông tin bổ sung):**

Thông tin khách hàng:

- Ngân sách: [15–25 triệu đồng]
- Nhu cầu: Chơi game, học tập và giải trí.
- Game thường chơi: [Valorant, GTA V, CS2...]
- Kích thước màn hình mong muốn: [15–16 inch]
- Thương hiệu yêu thích: [Nếu có]
- Ưu tiên: Hiệu năng tốt, tản nhiệt ổn định, sử dụng lâu dài.

Chỉ sử dụng thông tin sản phẩm và giá bán có căn cứ. Nếu chưa có dữ liệu chính xác, hãy ghi rõ là giá tham khảo và đề xuất nhân viên kiểm tra lại tồn kho, giá bán thực tế tại TechShop.

### 3. Master Prompt cho bộ phận Kỹ thuật bảo hành

**C – Context (Bối cảnh):**

Bạn là nhân viên kỹ thuật bảo hành có kinh nghiệm tại TechShop, chuyên kiểm tra, sửa chữa và thay thế linh kiện laptop. Hiện tại, một khách hàng mang laptop đến cửa hàng vì màn hình bị vỡ và muốn biết chi phí thay thế cũng như thời gian sửa chữa.

**R – Request (Yêu cầu):**

Hãy soạn nội dung báo giá thay màn hình laptop cho khách hàng, bao gồm:

- Xác định các thông tin cần thiết để kiểm tra đúng loại màn hình.
- Liệt kê chi phí linh kiện màn hình.
- Liệt kê chi phí công thay thế.
- Tính tổng chi phí dự kiến.
- Thông báo thời gian sửa chữa dự kiến.
- Nêu rõ thời gian và điều kiện bảo hành sau khi thay màn hình.
- Hướng dẫn khách hàng xác nhận trước khi tiến hành sửa chữa.

**E – Examples (Ví dụ):**

Ví dụ cách trình bày:

| Hạng mục | Chi phí tham khảo |
|---|---:|
| Màn hình thay thế | 2.000.000đ |
| Công thay màn hình | 200.000đ |
| Tổng chi phí | 2.200.000đ |

*Lưu ý: Đây chỉ là ví dụ minh họa, không phải bảng giá chính thức của TechShop.*

**A – Adjustment (Điều chỉnh):**

- Sử dụng ngôn ngữ chuyên nghiệp, lịch sự, dễ hiểu.
- Giải thích rõ từng khoản chi phí.
- Không sử dụng thuật ngữ kỹ thuật phức tạp nếu không cần thiết.
- Không tự ý đưa ra giá chính thức khi chưa kiểm tra model và linh kiện.
- Không cam kết bảo hành nếu chưa xác nhận chính sách của cửa hàng.
- Thể hiện sự minh bạch và tôn trọng khách hàng.

**T – Type of Output (Định dạng đầu ra):**

Trình bày thành một bảng báo giá chuyên nghiệp, có các phần:

1. Thông tin thiết bị.
2. Chi tiết chi phí.
3. Tổng chi phí dự kiến.
4. Thời gian sửa chữa.
5. Chính sách bảo hành.
6. Tin nhắn thông báo gửi khách hàng.

**E – Extras (Thông tin bổ sung):**

Thông tin thiết bị:

- Thương hiệu: [ASUS/HP/Dell/Lenovo...]
- Model laptop: [Tên model]
- Kích thước màn hình: [14/15.6/16 inch]
- Tình trạng: [Vỡ màn hình, sọc màn hình, chảy mực...]
- Loại màn hình cần thay: [Thông số nếu đã xác định]
- Giá linh kiện: [Theo bảng giá thực tế]
- Công thay thế: [Theo quy định cửa hàng]
- Thời gian sửa chữa: [Dự kiến]
- Chính sách bảo hành: [Theo quy định TechShop]

Nếu chưa đủ thông tin, hãy yêu cầu khách hàng cung cấp model hoặc kiểm tra thiết bị trước khi báo giá chính thức. Tuyệt đối không tự tạo giá bán và chính sách bảo hành.

---

## NHẬN XÉT CHUNG

Sau khi nâng cấp, cả 3 câu lệnh đều được bổ sung đầy đủ 6 thành phần CREATE. Việc cung cấp rõ vai trò, bối cảnh, yêu cầu và định dạng đầu ra giúp AI hiểu đúng nhiệm vụ của từng bộ phận.

- **CSKH:** Giúp tin nhắn xin lỗi chuyên nghiệp, chân thành và có hướng giải quyết.
- **Bán hàng:** Giúp tư vấn đúng nhu cầu, ngân sách và dễ so sánh sản phẩm.
- **Kỹ thuật bảo hành:** Giúp báo giá minh bạch, hạn chế thông tin sai lệch và tạo sự tin tưởng cho khách hàng.

**Điểm quan trọng:** Một Prompt tốt không chỉ yêu cầu AI làm gì mà còn phải cung cấp đủ thông tin để AI biết làm như thế nào và kết quả cần trình bày ra sao.
