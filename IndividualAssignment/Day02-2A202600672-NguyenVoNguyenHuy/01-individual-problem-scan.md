Case: **Rà soát nhanh trong quản lý chất lượng**

Tình huống: Trong một công ty sản xuất, khi nhân viên thực hiện kiểm tra chất lượng sản phẩm đều phải đưa ra báo cáo chi tiết về quy trình kiểm tra, nếu sản phẩm có vấn đề, phải quay lại rà soát lại quy trình để tìm ra nguyên nhân. Tuy nhiên, việc rà soát này thường mất nhiều thời gian và công sức, đặc biệt khi có nhiều sản phẩm cần kiểm tra.

# 01 — Individual Problem Scan

## Scan rộng

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Tốn thời gian | Lục tìm hồ sơ, file Excel/log cũ để xem quy trình của sản phẩm lỗi đã diễn ra thế nào | QC Specialist | Mất 1-2 tiếng/lần truy vết khi có lỗi nghiêm trọng |
| 2 | Lặp lại | Phải gõ lại các thông tin cơ bản (Mã lô, mã máy, mã nhân viên) vào các form báo cáo rà soát | QC Specialist | Mất 15-20 phút/ca chỉ để nhập liệu data cơ bản |
| 3 | Pain từ người khác | Đội sản xuất phải dừng hoặc chạy chậm máy để chờ kết quả rà soát từ QC xem lỗi do đâu | Production team, QC | Downtime sản xuất tăng, tạo áp lực thời gian lên QC |
| 4 | AI có thể tốt hơn | Đối chiếu nguyên nhân lỗi hiện tại với lịch sử các lỗi tương tự trong quá khứ rất thủ công | QC Specialist, QA Manager | Phụ thuộc hoàn toàn vào trí nhớ/kinh nghiệm cá nhân |
| 5 | Tốn thời gian | Đối chiếu kết quả đo lường với tài liệu SOP dài hàng chục trang để tìm bước làm sai | QC Specialist (đặc biệt người mới) | Mất 20-30 phút/lần mở tài liệu để tra cứu thông số |
| 6 | Lặp lại | Soạn email/tin nhắn cảnh báo chất lượng cho các bộ phận (Sản xuất, Bảo trì) khi phát hiện lỗi | QC Specialist | Lặp lại format thông báo mỗi khi có lỗi phát sinh |
| 7 | Pain từ người khác | Quản lý cần update tình hình xử lý lỗi ngay lập tức nhưng báo cáo rà soát chưa viết xong | QA Manager, QC Specialist | Thường bị giục báo cáo hoặc trễ deadline cuối ca |
| 8 | AI có thể tốt hơn | Gom nhóm và phân loại các ghi chú mô tả lỗi lủng củng từ công nhân để đưa vào báo cáo chuẩn | QC Specialist | Mất thời gian đọc hiểu và chuẩn hóa lại thuật ngữ |
| 9 | Tốn thời gian | Phải xử lý hình ảnh sản phẩm lỗi (chụp, crop, nén) và chèn vào đúng vị trí trong file báo cáo | QC Specialist | Thao tác thủ công lắt nhắt mất 10-15 phút/báo cáo |
| 10 | Lặp lại | Viết báo cáo phân tích nguyên nhân gốc rễ (ví dụ: 5-Why) theo cùng một quy chuẩn | QC Specialist | Tiêu tốn 45-60 phút/báo cáo do phải tư duy lại format |

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Lục tìm hồ sơ truy vết lỗi | Tốn nhiều thời gian (1-2h), workflow rõ ràng, có metric đo lường tốt | Dữ liệu lịch sử (Excel, log máy, bản cứng) có đủ chuẩn hóa để hệ thống/AI đọc hiểu không |
| 2 | Viết báo cáo RCA (5-Why) | Pain lặp lại rõ ràng hằng ngày, AI có khả năng tổng hợp và cấu trúc form tốt | Chất lượng phân tích nguyên nhân gốc rễ của AI có đủ sâu và sát thực tế nhà máy không |
| 3 | Đối chiếu lỗi với lịch sử | Giá trị cao, giảm phụ thuộc vào trí nhớ cá nhân, AI (RAG) xử lý bài toán này rất tốt | Thuật ngữ công nhân ghi chú thường lủng củng, khó để AI map đúng bối cảnh lỗi |

## Problem Card #1 — Lục tìm hồ sơ truy vết lỗi

**Problem 1 câu:** Mỗi khi phát hiện sản phẩm lỗi nghiêm trọng, QC Specialist mất từ 1 đến 2 tiếng lục tìm hồ sơ bản cứng, file Excel và log máy phân tán để truy vết quy trình, làm kéo dài thời gian dừng máy (downtime).

**Actor:** Chuyên viên Quản lý chất lượng (QC Specialist) chịu trách nhiệm điều tra nguyên nhân gốc rễ và báo cáo cho QA Manager, Đội sản xuất.

**Thời điểm / bối cảnh:** Xảy ra bất chợt trong ca làm việc khi có sản phẩm lỗi (NG - No Good) vượt mức cho phép cần phải điều tra ngay lập tức.

**Current workflow:**

```text
1. Nhận thông báo lỗi và xác định mã lô, mã máy.
2. Tìm hồ sơ giấy tờ lưu trữ của ca trước hoặc tải các file Excel/log máy rời rạc.
3. Đọc dò từng dòng ghi chú thủ công của công nhân để tìm điểm bất thường.
4. Đối chiếu thông số thực tế tại thời điểm đó với tài liệu tiêu chuẩn (SOP).
5. Tổng hợp chuỗi sự kiện để phán đoán nguyên nhân lỗi.
6. Viết báo cáo nhanh và thông báo cho Production/Maintenance.
```
**Bottleneck:**  
Bước 2 và 3 — Việc tìm kiếm dữ liệu phân tán ở nhiều định dạng (đặc biệt là giấy tờ cứng hoặc ghi chú lủng củng) mất khoảng 60 phút và rất dễ bỏ sót thông tin.

**Impact:**  
Mất trung bình 90 phút/lần truy vết. Trong thời gian này, dây chuyền sản xuất có thể phải dừng hoặc chạy chậm để chờ kết quả, gây thiệt hại lớn về năng suất. Áp lực thời gian khiến QC dễ đưa ra kết luận vội vàng.

**Success metric:**  
Giảm tổng thời gian truy vết và gom dữ liệu từ 90 phút xuống dưới 15 phút, thông tin trích xuất phải chính xác 100% so với log/hồ sơ gốc.
**Non-AI alternative:**  
Số hóa toàn bộ hồ sơ lên hệ thống phần mềm MES/ERP, sử dụng barcode/QR code để scan và dùng rule-based filter để lọc lịch sử. (Tuy nhiên, vẫn khó giải quyết việc đọc hiểu ghi chú dạng text tự do của công nhân).
**AI hypothesis:**  
AI (hệ thống RAG) hỗ trợ tìm kiếm đa nguồn, trích xuất dữ liệu từ file scan/log và tự động tóm tắt dòng thời gian sản xuất của lô hàng, làm nổi bật các thông số bất thường. QC review lại bằng chuyên môn trước khi kết luận.
**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — 90 phút

[1 Xác định mã lô/lỗi: 5']
→ [2 Tìm hồ sơ/log rời rạc: 40']  <-- bottleneck 1
→ [3 Đọc và dò ghi chú: 20']  <-- bottleneck 2
→ [4 Đối chiếu SOP: 10']
→ [5 Chuỗi sự kiện & phán đoán: 10']
→ [6 Thông báo/Báo cáo: 5']
```

### Draft future workflow

```text
FUTURE STATE — 17 phút

[1 Nhập mã lô vào hệ thống: 1']
→ [2 AI search & gom dữ liệu: 2']
→ [3 AI tóm tắt timeline & highlight bất thường: 2']
→ [4 QC review data + chốt nguyên nhân: 10']  <-- human boundary
→ [5 QC gửi báo cáo: 2']

Fallback: AI không tìm thấy dữ liệu do bản scan mờ/lỗi hệ thống → QC quay lại quy trình tìm file cứng hoặc Ctrl+F thủ công.
```

## Problem Cards #2 và #3 — tóm tắt

| Card | Actor | Bottleneck | Metric | Quick gut | Vì sao chưa chọn làm #1 |
|---|---|---|---|---|---|
| Viết báo cáo RCA (5-Why) | QC Specialist | Tư duy lại format và chuẩn hóa câu chữ từ raw data | 45-60 phút → 15 phút | Workflow | Báo cáo phụ thuộc vào bước truy tìm nguyên nhân. Nếu tìm sai, báo cáo vô nghĩa. AI khó bám sát logic thực tế nhà máy. |
| Đối chiếu lỗi với lịch sử | QC Specialist, QA Manager | Phụ thuộc trí nhớ, khó map keyword với ghi chú lủng củng cũ | Tốn thời gian hỏi han → dưới 2 phút | Agent / Workflow | Thuật ngữ ghi chú của công nhân không chuẩn hóa, cần làm sạch data trước. Scope dự án phức tạp hơn. |