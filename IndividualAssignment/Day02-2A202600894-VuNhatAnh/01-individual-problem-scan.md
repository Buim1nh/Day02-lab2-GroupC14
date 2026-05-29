# 01 — Individual Problem Scan

## Scan rộng
Scan 7 problems

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Phải nhớ và gõ tay từng chi tiêu nhỏ lẻ (giá, số lượng, tên) vào cuối ngày. | Chi (User) | Tốn 5-10 phút mỗi tối. Nhiều ô nhập liệu trên điện thoại là thấy nản và lười. |
| 2 | Tốn thời gian | Giữ lại đống hóa đơn giấy trong ví hoặc chụp ảnh màn hình giao dịch online để làm bằng chứng nhập liệu | Chi (User) | Bộ sưu tập ảnh điện thoại bừa bộn vì chứa đầy ảnh banking |
| 3 | Tốn thời gian | Tiền nằm rải rác ở nhiều nơi | Chi (User) | Mất 30-45 phút mỗi cuối tuần để lục lại từng app |
| 4 | Tốn thời gian | Gõ nhầm số tiền (thừa/thiếu số 0) hoặc chọn sai danh mục chi phí do bấm nhầm trên màn hình điện thoại nhỏ. | Chi (User) | Số dư trên file tính toán lệch hoàn toàn so với số dư thực tế trong tài khoản.|
| 5 | Tốn thời gian | Cuối tháng/năm phải tự ngồi tính toán, cộng trừ, làm hàm Excel | Chi (User) | Tfile ngày càng nặng, rối mắt và rất khó nhìn |
| 6 | AI có thể tốt hơn | Không cảnh báo hay ngăn chặn hành vi vỡ quỹ ngay lúc chuẩn bị xuống tiền | Chi (User) | "Biết thế đầu tháng không mua món này". |
| 7 | Lặp lại | Các khoản chi cố định (tiền mạng, Netflix, tiền nhà, tiền gửi xe...) xuất hiện đều đặn mỗi ngày/tuần/tháng nhưng ngày nào cũng phải nhập tay lại. | Chi (User) | Phải lặp lại thao tác nhập y chang một nội dung |


Vì sao phần scan này mạnh:

- Có scan rộng trước khi hội tụ.
- Có nhiều lăng kính khác nhau.
- Mỗi problem có actor và dấu hiệu thật.
- Không bắt đầu bằng "làm chatbot" hoặc "xây agent".

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | High Friction & Cognitive Load | Tần suất lặp lại siêu cao, AI có thể giúp lấy thông tin từ hình ảnh  | Tỷ lệ quét ảnh chính xác của AI (OCR) với các hóa đơn giấy bị mờ, nhòe hoặc chữ viết tắt |
| 2 | Data Fragmentation | Người dùng hiện đại có nguồn tiền nằm rải rác ở nhiều ngân hàng, ví Momo, ShopeePay, tiền mặt | Data access khó |
| 3 | The Ghost Expenses Problem | Xảy ra âm thầm hàng tháng | Làm sao để hệ thống tự động phát hiện ra một khoản chi là "định kỳ" ở những tháng đầu tiên khi chưa có đủ lịch sử dữ liệu |

## Problem Card #1 — High Friction & Cognitive Load

**Problem 1 câu:**  
Phải nhớ và gõ tay từng chi tiêu nhỏ lẻ (giá, số lượng, tên) vào cuối ngày hoặc ngay tại luc thanh toán xong

**Actor:**  
Người dùng có tần suất tiêu dùng cao với các khoản nhỏ lẻ. 

**Thời điểm / bối cảnh:**  
Ngay tại khoảnh khắc vừa xuống tiền thanh toán xong hoặc khoảng 10-11 giờ tối trước khi đi ngủ

**Current workflow:**

```text
1. Phát sinh giao dịch -> Nhận bill giấy hoặc tự chụp màn hình banking để lưu lại bằng chứng.
2. Mở app quản lý chi tiêu
3. Tạo một dòng mới -> Gõ bàn phím tên sản phẩm -> Gõ số tiền -> Gõ số lượng
4. Chọn đúng Danh mục đúng
5. Chọn nguồn tiền
6. Tự rà soát & Lưu
```

**Bottleneck:**  
Bước 3: Tạo một dòng mới -> Gõ bàn phím tên sản phẩm -> Gõ số tiền -> Gõ số lượng

**Impact:**  
Khi có quá nhiều chi tiêu nhỏ lẻ sẽ dẫn đến việc nhập liệu tốn nhiều thời gian và việc nhớ những chi tiêu không có bằng chứng sẽ khiến sinh ra cảm giác stress

**Success metric:**  
Giảm từ 5-7 lượt gõ/chọn xuống còn 1-2 lần chạm của bước 3. 

**Non-AI alternative:**  
Xây dựng các nút bấm nhanh chọn các mức tiền cố định gợi ý sẵn

**AI hypothesis:**  
Tích hợp AI Vision / OCR kết hợp LLM vào ngay đầu luồng nhận diện (Input), người dùng chỉ cần tốn đúng 1 hành động duy nhất: Chụp/Gửi một bức ảnh (ảnh bill giấy, ảnh màn hình banking, ảnh đơn hàng Shopee). Không có hình ảnh sẽ dùng NLP xử lý. AI trích xuất json.

Cách vận hành: AI sẽ tự động đọc ảnh, hiểu ngữ cảnh tiếng Việt (dù chữ mờ hay viết tắt), trích xuất ra cấu trúc dữ liệu hoàn chỉnh (Tên, Giá, Danh mục) và tự điền vào DB. Sẽ cho người dùng review lại nội dung.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — 5 đến 10 phút

[1 Gom bằng chứng: 1 - 2']
→ [2 Mở app & Định vị: 30s]
→ [3 Gõ thông tin thô: 2 - 3']  <-- bottleneck
→ [4 Cuộn tìm Danh mục: 1 - 2']  
→ [5 Chọn nguồn tiền: 30s]
→ [6 Tự rà soát & Lưu: 1']
```

### Draft future workflow

```text
FUTURE STATE — 21 phút

[1 Chụp & Share ảnh: 1.5s]
→ [2 AI xử lý ngầm: 2 - 3s]
→ [3 AI Auto-fill: ]
→ [4 Duyệt kết quả & Chạm lưu: 1.5s] <-- human

Fallback: AI trích xuất tệ → User tự viết lại.
```

## Problem Cards #2 và #3 — tóm tắt

| Card | Actor | Bottleneck | Metric | Quick gut | Vì sao chưa chọn làm #1 |
|---|---|---|---|---|---|
| Data Fragmentation | User | Nguồn tiền nằm rải rác ở quá nhiều nơi khác nhau | 5 phút → 1 phút | Workflow / Integration | Data access khó, nhiều rào cản kỹ thuật, bảo mật và thủ tục pháp lý|
| The Ghost Expenses Problem | User | Dăng ký nhiều dịch vụ subscription | Phát hiện trễ → Tự động phát hiện | Agent | Cold start |

---