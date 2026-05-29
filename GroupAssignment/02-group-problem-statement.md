# 02 — Group Problem Statement

## 1. Group Convergence

**Cluster các vấn đề từ cá nhân:**
Nhóm gom các ý tưởng ban đầu thành 5 nhóm chính:

| Cluster | Candidate examples | Pattern chung |
| --- | --- | --- |
| Phân tích dữ liệu luồng video/gameplay | **Phân tích VOD TFT** | Nhu cầu phân tích luồng hình ảnh/video để rút ra chiến thuật, tình huống thực tế có bối cảnh phức tạp. |
| Hỗ trợ học tập sinh viên | Kiểm tra lỗi lập luận, tìm tài liệu cũ trong Discord/Teams, xếp lịch học tín chỉ bằng Excel. | Nhu cầu rà soát lỗi logic văn bản, tra cứu thông tin cũ bị trôi, và tự động hóa quá trình lập kế hoạch cá nhân.
| Tự động hóa xử lý dữ liệu nghiên cứu | TTrích xuất cột nhiệt độ/năng lượng từ hàng trăm file thô, lọc rác, định dạng xuất 500 file ảnh Gnuplot. | Giải quyết các thao tác cơ học lặp đi lặp lại trên khối lượng lớn dữ liệu, đòi hỏi độ chính xác tuyệt đối ở các số thập phân. |
| Nhận diện và giải thích giao thông | Tra lại ý nghĩa biển báo, giải thích biển phụ và biển cấm theo giờ trong ngữ cảnh thực tế. |Chuyển đổi từ việc chỉ nhận diện hình ảnh (detect object) sang khả năng hiểu ngữ cảnh (contextual understanding) để hỗ trợ người đi đường.
| Quản lý tài chính cá nhân | Trợ lý nhập liệu chi tiêu từ hóa đơn và chi phí cố định | Giải quyết bài toán nhập liệu thủ công lặp đi lặp lại, dữ liệu bị phân mảnh từ hóa đơn giấy/ảnh chụp màn hình, và lãng phí thời gian nhập các khoản chi định kỳ. |

**Shortlist và Score:**

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **Phân tích VOD TFT** | 5 | 5 | 5 | 5 | 4 | 5 | 5 | 34 |
| Tự động làm sạch & vẽ đồ thị (Gnuplot) | 5 | 5 | 5 | 5 | 4 | 5 | 5 | 34 |
| Bot tìm kiếm tài liệu group chat học tập | 5 | 4 | 4 | 4 | 4 | 4 | 5 | 30 |
| Trợ lý AI giải thích biển báo giao thông | 5 | 4 | 4 | 3 | 3 | 4 | 4 | 27 |
| Trợ lý tự động hóa nhập liệu chi tiêu | 5 | 5 | 5 | 5 | 5 | 4 | 5 | 34 |

**Nhóm chọn:** Phân tích VOD TFT.
**Vì sao chọn:** Workflow cực kỳ rõ ràng, nỗi đau đủ lớn (tiêu tốn tới 45 phút cho mỗi video) và quan trọng nhất là tính khả thi khi so sánh phương án dùng AI (tạo bước đột phá lớn) với phương án Non-AI (gần như không thể giải quyết triệt để).

**Vì sao không chọn các bài khác:** 

Tự động làm sạch & vẽ đồ thị (Gnuplot): Đã được xác định rõ là "No-Go cho Agent". Rủi ro ảo giác (AI đọc sai số thập phân, làm lệch dòng dữ liệu) sẽ phá hỏng hoàn toàn tính minh bạch khoa học. Bài toán này nên được giải quyết bằng Rule/Python Script cứng để đảm bảo chính xác 100% thay vì dùng AI.

Bot tìm kiếm tài liệu group chat học tập: Rào cản lớn về phân quyền truy cập dữ liệu (data access) vào các kênh chat riêng tư. Phạm vi dễ bị trượt sang việc xây dựng một hệ thống RAG (Retrieval-Augmented Generation) khổng lồ vượt quá thời lượng của một buổi lab.

Trợ lý AI giải thích biển báo giao thông: Thiếu tính khả thi để kiểm chứng (validate). Việc thử nghiệm một hệ thống AI nhận diện và suy luận luật giao thông trong điều kiện người dùng đang trực tiếp lái xe tiềm ẩn rủi ro an toàn quá lớn.

Trợ lý tự động hóa nhập liệu chi tiêu: Bài toán có pain point rất thực tế nhưng gặp rào cản cực lớn về bảo mật dữ liệu (Privacy) và lòng tin của người dùng khi phải chia sẻ ảnh chụp hóa đơn, màn hình banking nhạy cảm. Đồng thời, hệ thống đối mặt với bài toán "Cold start" nghiêm trọng ở những tháng đầu tiên khi chưa có đủ lịch sử dữ liệu để AI nhận diện chính xác các pattern chi phí định kỳ. Việc giải quyết triệt để rào cản data access và xử lý các hóa đơn mờ, nhòe, viết tắt vượt quá phạm vi và thời gian cho phép của một buổi lab.

---

## 2. Quick Validation & Research

**Quick Validation (Khảo sát nhanh):**

| Nguồn | Số người | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
| --- | --- | --- | --- | --- |
| Hỏi game thủ trong Discord TFT | 5 | 4/5 người thừa nhận họ rất lười xem VOD giải đấu vì "tua đi tua lại mỏi tay mà chả hiểu sao nó lại bán máu roll cạn tiền lúc đó". | 1 người cho rằng chỉ cần xem các video highlight cắt sẵn trên Youtube là đủ. | Bổ sung vào "Non-AI alternative" rằng highlight cắt sẵn thường thiếu tính thời sự và phụ thuộc vào người chỉnh sửa. Nhấn mạnh bài toán là học **tư duy logic (reasoning)** chứ không chỉ xem bề nổi. |

**Research giải pháp hiện có:**

| Nguồn / tool / case | Họ giải quyết phần nào? | Khoảng trống / rủi ro (Gap) | Bài học cho nhóm |
| --- | --- | --- | --- |
| **Insights.gg** (Video bookmarking) | Tự động gắn thẻ sự kiện (timestamp) dựa trên nhận diện màn hình. | Chưa có khả năng suy luận ngược bối cảnh. Chỉ cắt video, không giải thích "Tại sao". | Không chỉ làm auto-clipper, cần tập trung vào lớp Reasoning. |
| **Mobalytics / iTero** (API Analytics) | Quét dữ liệu toàn trận qua API để thống kê sức mạnh. | Phụ thuộc hoàn toàn vào API. Không áp dụng được cho video VOD tĩnh của người khác. | Bắt buộc phải dùng Computer Vision/OCR làm đầu vào. |
| **Trophi.ai** (AI Coach) | Dùng Computer Vision cảnh báo lỗi sai cơ bản. | Thiếu suy luận ngược bối cảnh sâu; chi phí xử lý tài nguyên tính toán cao. | AI cần liên kết biến số bối cảnh thay vì chỉ soi lỗi thao tác. |

---

## 3. Workflow Before / After

**CURRENT STATE — 45 phút**

```text
[1 Mở video VOD: 2'] 
→ [2 Tua tìm mốc thời gian xảy ra biến động lớn: 10'] 
→ [3 Ghi nhận thao tác bề nổi của tuyển thủ: 10'] 
→ [4 Dừng video, tự quan sát bối cảnh và suy đoán lý do: 15'] <-- Bottleneck
→ [5 Rút ra kết luận và ghi chép chiến thuật: 8']

```

**FUTURE STATE — 9 phút**

```text
[1 Cung cấp liên kết VOD cho AI Agent: 1'] 
→ [2 Agent quét dữ liệu toàn trận và lập bản đồ biến số: 3'] 
→ [3 Agent phân tích logic hành vi và tạo báo cáo lý giải: 2'] 
→ [4 Đọc báo cáo giải thích chiến thuật tại mốc trọng tâm: 3'] <-- Human Boundary

Fallback: AI Agent không giải thích được quyết định do lối chơi dị biệt hoặc dữ liệu che khuất → Đánh dấu đoạn video kèm thông số để người dùng tự phân tích lại.

```

**Before/After Impact:**

| Metric | Trước | Sau kỳ vọng | Ghi chú |
| --- | --- | --- | --- |
| Tổng thời gian | 45 phút | 9 phút | Giảm ~80% thời gian nghiên cứu 1 VOD |
| Số bước | 5 | 4 | Giảm bớt các thao tác cơ học vô nghĩa |
| Số bước thủ công | 5/5 | 2/4 | Con người chỉ nhập input và đọc kết quả |
| Bottleneck chính | Suy đoán lý do xoay bài (15') | Đọc & đối chiếu báo cáo (3') | Human boundary kiểm soát chất lượng |
| Risk mới | Suy đoán sai do thiếu tập trung | AI Hallucination (bịa lý luận) | Bắt buộc kèm video snippet 10s để user đối chiếu |

---

## 4. Problem Statement v0

| Field | Nội dung |
| --- | --- |
| **Actor** | Game thủ TFT có nhu cầu nghiên cứu chiến thuật và nâng cao kỹ năng. |
| **Workflow** | Mở VOD → Tua tìm mốc → Ghi nhận thao tác → Tự quan sát suy đoán lý do xoay bài → Rút ra kết luận. |
| **Bottleneck** | Việc dò tìm mốc thời gian thủ công và quá trình tự phân tích bối cảnh rất dễ sai lệch, bỏ sót biến số, tiêu tốn 15-25 phút cho mỗi pha xử lý. |
| **Impact** | Lãng phí công sức, gây chán nản, làm giảm đáng kể số lượng trận đấu có thể nghiên cứu, chậm cập nhật meta. |
| **Success Metric** | Giảm thời gian trích xuất & phân tích 1 video 40p xuống dưới 10p. Tỷ lệ trích xuất đúng các mốc lên cấp/xoay bài đạt >90%. |
| **Boundary** | AI chỉ xuất ra báo cáo phân tích và đoạn cắt video (timestamp). AI không tự động chơi game, không khẳng định 100% logic của tuyển thủ. Con người vẫn phải tự đọc, tự kiểm chứng và áp dụng. |

---

## 5. Rule / Workflow / Agent

| Mức | Phương án cho bài toán nhóm | Khi nào đủ | Rủi ro | Chọn? |
| --- | --- | --- | --- | --- |
| **Rule** | Tự động bắt màu pixels để timestamp thời điểm roll tiền/lên cấp. | Chỉ cần biết KHI NÀO tuyển thủ thao tác. | Không giải thích được TẠI SAO (thiếu Reasoning). | Không |
| **Workflow** | Dùng rule/script cắt video thành clip nhỏ → AI OCR đọc ảnh lấy text → Nhét vào ChatGPT tóm tắt. | Nếu các bước tĩnh và bối cảnh màn hình không phức tạp. | Text OCR quá rời rạc, AI không tự xâu chuỗi được bối cảnh lobby (như máu của nhà khác). | Không |
| **Agent** | Agent liên tục theo dõi luồng hình ảnh, tự map các biến số bối cảnh (máu, vàng, lõi, lobby) và suy luận ngược (Reverse Engineering) tại sao có hành động T dựa trên bối cảnh T-1. | Cần tư duy đa biến, logic mờ và tự đánh giá bối cảnh. | Quá trình suy luận có thể tốn kém GPU hoặc sinh ra ảo giác. | **Chọn** |

**Mức chọn:** **Agent**
**Vì sao chọn:** Bài toán này có độ phức tạp và độ mơ hồ cao. Input là một luồng video không cấu trúc. Việc lấy dữ liệu bề mặt (máu, vàng, tướng) chỉ là bước đệm. Cốt lõi giải quyết bottleneck là việc AI phải tự liên kết các biến số tại thời điểm T để giải thích hành động đột ngột tại thời điểm T+1 (VD: Tại sao đang tích tiền lại xả sạch?). Rule hoặc Workflow tĩnh không thể xử lý được logic mờ và khả năng quan sát liên tục này.

---

## 6. Problem Statement v1

| Field | Nội dung |
| --- | --- |
| **Actor** | Game thủ TFT có nhu cầu nghiên cứu chiến thuật và nâng cao kỹ năng. |
| **Workflow** | Cung cấp URL VOD → Agent lập bản đồ biến số → Agent xuất báo cáo lý giải → Human đọc & kiểm chứng. |
| **Bottleneck** | (Như cũ) Dò tìm mốc thời gian thủ công và tự phân tích bối cảnh rất dễ sai lệch, tiêu tốn 15-25 phút cho mỗi pha xử lý. |
| **Impact** | Lãng phí công sức, gây chán nản, làm giảm số lượng trận có thể nghiên cứu, chậm cập nhật meta. |
| **Success Metric** | Giảm thời gian trích xuất & phân tích 1 video 40p xuống dưới 10p. Tỷ lệ trích xuất đúng các mốc lên cấp/xoay bài đạt >90%. |
| **Boundary** | AI chỉ xuất ra báo cáo phân tích và timestamp video, không tự động chơi game thay người, không khẳng định 100% logic của tuyển thủ. Con người vẫn phải đọc và tự ứng dụng. |
| **AI intervention point** | Can thiệp thay thế hoàn toàn bước "Tua tay dò tìm mốc" và "Tự quan sát bối cảnh để suy đoán lý do". |
| **Mức chọn** | **Agent** (Phối hợp Computer Vision và Reasoning Engine). |
| **Rủi ro & Kiểm tra** | *Rủi ro:* Hallucination trong suy luận logic (VD: báo roll vì thiếu damage nhưng thực ra roll vì giữ máu). *Người thật kiểm tra:* Báo cáo bắt buộc đính kèm clip ngắn 10 giây gốc trước khi thao tác diễn ra để Human tự đối chiếu lại logic của AI. |

---

## 7. Final Decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú |
| --- | --- | --- |
| Actor và workflow đã rõ chưa? | Yes | Workflow rõ ràng từ người dùng đến AI. |
| Baseline và success metric đã đo được chưa? | Yes | Baseline là 45p, Target là 9p. |
| Có data/input đủ dùng chưa? | Yes | Video VOD giải đấu có sẵn trên Youtube/Twitch. |
| Nếu AI sai, hậu quả có chấp nhận được không? | Yes | User chỉ tốn thêm 1-2 phút tự xem lại đoạn video 10s được cắt. Không gây chết người/mất tiền. |
| Có người review/owner vận hành không? | Yes | Game thủ đọc báo cáo là người review cuối cùng. |
| Có cách non-AI đơn giản hơn không? | No | Xem highlight mất bối cảnh, đọc guide text thiếu tính thời sự của trận đấu cụ thể. |

**Decision:**
`GO (với scope là Pilot nhỏ)`

**Lý do:**
Bài toán có pain point rất thật và đau, workflow được mapping chi tiết. Mặc dù hướng tiếp cận bằng Agent đa biến khá phức tạp, nhưng rủi ro (hallucination) có thể được kiểm soát hoàn toàn bằng việc kẹp video gốc cho user tự check (Fallback).

**Pilot nhỏ nhất:**
Chỉ dùng Agent phân tích đúng 1 mốc cố định: **Vòng đấu 3-2** (Vòng chọn lõi số 2 và xả tiền đầu tiên). Đưa luồng video 30 giây của vòng 3-2 vào mô hình Multimodal (như Gemini 1.5 Pro) để test khả năng đọc hiểu bối cảnh và lý giải hành động trước khi build toàn bộ hệ thống auto-scan nguyên video 40 phút.

**Exit / rollback:**
Nếu mô hình AI liên tục ảo giác, bịa ra các nguyên nhân xoay bài không liên quan, hoặc OCR không thể đọc được tiền/máu do UI video quá mờ → Rollback: Hạ cấp dự án xuống thành một Workflow đơn giản (chỉ dùng AI nhận diện đổi round để auto-cắt clip, con người tự phân tích clip đó).