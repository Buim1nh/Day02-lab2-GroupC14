# 🔍 Phase 1 & 2 — Individual Problem Scan

Phần này ghi lại quá trình quét vấn đề thực tế từ trải nghiệm cá nhân của **Nguyễn Duy Thắng (2A202600622)** và chi tiết hóa Top 3 Problem Cards.

---

## 📊 Phase 1 — Bảng Quét Vấn Đề (Scan Problems)



| # | Lăng kính | Vấn đề quan sát được | Ai đang đau? (Actor) | Dấu hiệu thật / Tác động |
|---|---|---|---|---|
| 1 | **AI tốt hơn** | Kiểm tra lỗi lập luận (logical flow) và sửa văn phong tiếng Anh học thuật cho các bài luận. | Sinh viên | Đọc đi đọc lại bài viết thủ công mất hơn 60 phút nhưng vẫn sót lỗi diễn đạt mập mờ, lặp từ, hoặc lập luận chưa chặt chẽ. |
| 2 | **Lặp lại** | Lên lịch học và đăng ký tín chỉ hằng kỳ. Phải xếp nhiều phương án (Plan A, B, C) thủ công trên Excel để tránh trùng lịch hoặc hết slot. | Sinh viên | Mất 2-3 tiếng tự xếp lịch trên Excel hằng kỳ; khi môn học chính bị hết slot thì cuống cuồng xếp lại từ đầu mất thêm 30-45 phút sát giờ. |
| 3 | **Tốn thời gian**  | Tìm kiếm quyết định, deadline, tài liệu học tập cũ trong group chat Discord/Teams của lớp học hoặc kênh CLB. | Sinh viên / Thành viên CLB | Mất 15-20 phút gõ từ khóa trên Slack/Discord để tìm lại link Drive hoặc slide cũ, nhiều khi không tìm được do tin nhắn trôi quá nhanh. |
| 4 | **Tốn thời gian** | Viết tóm tắt tài liệu nghiên cứu (Research papers) để phục vụ cho Literature Review của bài tập lớn hoặc NCKH. | Sinh viên nghiên cứu | Phải đọc từng bài báo học thuật tiếng Anh dài 10-15 trang mất 45-60 phút chỉ để trích xuất phương pháp, kết quả và hạn chế; cực kỳ nản. |
| 5 | **Lặp lại** | Tổng hợp báo cáo tiến độ đồ án nhóm hàng tuần để nộp cho Giảng viên/Mentor. | Trưởng nhóm đồ án | Mất 45-60 phút mỗi tối Chủ Nhật để lục tìm tin nhắn Slack, git commits, Drive để tổng hợp; dễ bỏ sót công sức thực tế của thành viên. |
| 6 | **AI tốt hơn** | Phân loại và tóm tắt thông báo quan trọng từ LMS Canvas, Email trường và Kênh tin tức CLB hằng ngày. | Sinh viên năng động | Nhận 15-20 email/thông báo mỗi ngày; mất 15 phút kiểm tra thủ công và đôi khi bỏ lỡ các deadline đăng ký hội thảo hay học bổng. |


---

## 🎯 Phase 2 — Top 3 Problem Cards


### 🏆 Đánh giá & Xếp hạng Top 3

| Rank | Tên vấn đề | Vì sao chọn? | Điều còn chưa chắc / Cần làm rõ |
|---|---|---|---|
| **1** | **Tổng hợp báo cáo tiến độ đồ án nhóm hàng tuần** | Quy trình cực kỳ rõ ràng, diễn ra đều đặn hằng tuần, có baseline thời gian cụ thể và ảnh hưởng trực tiếp tới điểm chuyên cần/quá trình của nhóm. | Cách AI trích xuất ngữ cảnh từ tin nhắn chat tự do của thành viên trên Discord mà không bị hiểu sai nghĩa. |
| **2** | **Viết tóm tắt tài liệu nghiên cứu phục vụ Literature Review** | Pain rất sâu của sinh viên VinUni vì khối lượng đọc tài liệu rất lớn, có tính học thuật cao. AI có thế mạnh vượt trội trong việc tóm tắt văn bản. | Làm sao đảm bảo AI không bịa đặt (hallucinate) các số liệu hoặc kết quả nghiên cứu trong paper. |
| **3** | **Kiểm tra lỗi lập luận và văn phong tiếng Anh học thuật cho bài Essay** | Ảnh hưởng trực tiếp đến chất lượng đầu ra của bài essay. AI giúp tiết kiệm thời gian self-edit đáng kể. | Định nghĩa thế nào là một "logical flow" tốt để hướng dẫn AI kiểm tra một cách khách quan nhất. |

---

### 📋 PROBLEM CARD #1: Tổng hợp báo cáo tiến độ đồ án nhóm hàng tuần

```text
Problem 1 câu:
Hằng tuần trưởng nhóm mất khoảng 45-60 phút lục tìm, đối chiếu tiến độ từ GitHub commits, tin nhắn Discord và file quản lý task để tổng hợp viết báo cáo narrative nộp cho giảng viên, dễ bỏ sót đóng góp của thành viên.

Actor (Ai đang đau?):
Trưởng nhóm đồ án .

Thời điểm / Bối cảnh:
Tối Chủ Nhật hằng tuần trước buổi họp nhóm và nộp bài trước thứ Hai.

Current Workflow (Quy trình hiện tại từ 6 bước):
1. Mở GitHub xem danh sách commits trong tuần của từng thành viên.
2. Lướt lại toàn bộ chatbox trên Discord/Slack để xem các cập nhật/khó khăn của thành viên.
3. Mở file Excel/Trello kiểm tra trạng thái Task (Done/In Progress).
4. Tổng hợp thủ công số liệu vào bản nháp Google Docs.
5. Tự viết phần Narrative: Đánh giá tiến độ chung, Highlights, Bottlenecks/Risks và Kế hoạch tuần tới.
6. Soát lỗi chính tả, format lại và gửi link báo cáo cho Giảng viên/Mentor qua email/LMS.

Bottleneck (Bước nghẽn nhất & thời gian mất):
Bước 5 - Viết phần Narrative giải thích số liệu (mất 25-30 phút/lần do mất nhiều thời gian kết nối thông tin rời rạc và dễ bị blank page).

Impact (Tác hại nếu không giải quyết):
Trưởng nhóm mất nhiều thời gian làm việc lặp đi lặp lại; báo cáo nộp trễ hoặc hời hợt khiến giảng viên đánh giá sai tiến độ thực tế, thành viên bị thiệt thòi về điểm đóng góp.

Success Metric (Đo lường thành công):
Giảm tổng thời gian từ 45 phút xuống dưới 10 phút/tuần; báo cáo chi tiết hơn, đầy đủ 100% đầu mục công việc và không có phản hồi phàn nàn từ thành viên.

Non-AI Alternative (Giải pháp thay thế không dùng AI):
Yêu cầu mỗi thành viên tự điền biểu mẫu báo cáo cá nhân hằng tuần. Tuy nhiên, việc này chuyển nỗi đau sang thành viên, dễ dẫn đến tình trạng quên điền hoặc điền đối phó, trưởng nhóm vẫn phải gom và sửa format thủ công.

AI Hypothesis (Giả thuyết AI có thể giúp như thế nào?):
AI đọc dữ liệu raw (Danh sách Git commits + Tóm tắt chat Discord + Trạng thái Task Trello) rồi tự động phân loại, gom nhóm và draft sẵn báo cáo Narrative có cấu trúc. Trưởng nhóm chỉ cần review, edit nhẹ và bấm gửi.

Quick Gut (Nhận định nhanh):
[ ] No AI / Process Fix  [ ] Rule  [x] Workflow  [ ] Agent  [ ] Chưa biết
```

#### 🔄 Quy trình Trước & Sau tối ưu (Draft Workflows)

**Quy trình hiện tại (Current State) — 45 phút:**
```text
[1. Gom Git commits & Discord chat: 15']
➔ [2. Kiểm tra Trello task: 5']
➔ [3. Nhập dữ liệu thô vào Docs: 5']
➔ [4. Tự viết Narrative (Bottleneck): 25']
➔ [5. Kiểm tra format & Gửi: 5']
```

**Quy trình tương lai kì vọng (Future State) — 9 phút:**
```text
[1. Chạy Script tự gom dữ liệu Git/Trello/Chat: 2'] (Rule)
➔ [2. AI cấu trúc dữ liệu và phân loại task: 1'] (Workflow)
➔ [3. AI draft phần Narrative (Highlights/Risks): 1'] (Workflow)
➔ [4. Trưởng nhóm Review & Chỉnh sửa thủ công: 4'] (Human Boundary)
➔ [5. Trưởng nhóm bấm gửi: 1']
```
* **Phương án dự phòng (Fallback):** Nếu AI nháp báo cáo không sát thực tế hoặc bịa tiến độ, Trưởng nhóm sẽ hủy bản nháp, copy dữ liệu thô vào template có sẵn và tự viết lại phần Narrative (quay về quy trình truyền thống).

---

### 📋 PROBLEM CARD #2: Viết tóm tắt tài liệu nghiên cứu phục vụ Literature Review

```text
Problem 1 câu:
Sinh viên nghiên cứu mất 45-60 phút để đọc và tóm tắt thủ công một bài báo khoa học tiếng Anh dài 10-15 trang nhằm trích xuất phương pháp, kết quả và hạn chế phục vụ cho việc viết Literature Review.

Actor:
Sinh viên thực hiện nghiên cứu khoa học / Làm bài tập lớn .

Thời điểm / Bối cảnh:
Giai đoạn chuẩn bị đề cương nghiên cứu hoặc viết báo cáo học thuật cuối kỳ.

Current Workflow:
1. Tìm kiếm và tải file PDF bài báo khoa học về máy.
2. Đọc lướt Abstract, Introduction để nắm ý chính.
3. Đọc chi tiết phần Methodology và Results, ghi chú các công thức, thuật toán hoặc số liệu cốt lõi.
4. Đọc phần Discussion và Conclusion để ghi nhận hạn chế (limitations) và hướng phát triển.
5. Viết lại tóm tắt (khoảng 300-500 từ) bằng ngôn ngữ của mình vào Notion/Word.
6. Đối chiếu lại với bài báo gốc để tránh hiểu sai số liệu.

Bottleneck:
Bước 3 & Bước 4 - Đọc sâu phần học thuật chuyên ngành và trích xuất hạn chế bằng tiếng Anh (mất 30-40 phút, cực kỳ tốn năng lượng não bộ).

Success Metric:
Giảm thời gian đọc và trích xuất thông tin mỗi bài báo từ 60 phút xuống còn 15 phút; tóm tắt đầy đủ chính xác 4 trường thông tin: Câu hỏi nghiên cứu, Phương pháp, Kết quả chính, Hạn chế/Khoảng trống.

Non-AI Alternative:
Đọc các bài blog tóm tắt sẵn trên mạng hoặc chỉ đọc Abstract. Rủi ro cao là bài báo cụ thể không có tóm tắt sẵn, hoặc đọc Abstract thì quá sơ sài, thiếu số liệu cụ thể để đưa vào Literature Review.

AI Hypothesis:
AI (sử dụng RAG hoặc đọc trực tiếp file PDF) tiến hành phân tích văn bản bài báo, trích xuất cấu trúc và điền thông tin vào template tóm tắt nghiên cứu chuẩn hóa. Sinh viên chỉ cần đọc bản tóm tắt và kiểm chứng lại các số liệu quan trọng.

Quick Gut:
[ ] No AI / Process Fix  [ ] Rule  [x] Workflow  [ ] Agent  [ ] Chưa biết
```

#### 🔄 Quy trình Trước & Sau tối ưu (Draft Workflows)

**Quy trình hiện tại (Current State) — 60 phút:**
```text
[1. Tải PDF: 2'] 
➔ [2. Đọc Abstract/Intro: 8'] 
➔ [3. Đọc Methodology & Results (Nghẽn): 25'] 
➔ [4. Đọc Discussion & Limitations: 15'] 
➔ [5. Viết tóm tắt bằng tiếng Anh: 10']
```

**Quy trình tương lai kì vọng (Future State) — 15 phút:**
```text
[1. Tải PDF & Tải lên công cụ AI: 2'] 
➔ [2. AI trích xuất và tóm tắt theo template: 1'] (Workflow step)
➔ [3. Sinh viên đọc bản tóm tắt của AI: 5']
➔ [4. Sinh viên đối chiếu số liệu quan trọng với PDF gốc: 5'] (Human Boundary)
➔ [5. Copy bản tóm tắt chuẩn xác vào cơ sở dữ liệu Notion: 2']
```

---

### 📋 PROBLEM CARD #3: Kiểm tra lỗi lập luận và văn phong tiếng Anh học thuật cho bài Essay

```text
Problem 1 câu:
Sinh viên mất 60-80 phút tự rà soát, viết lại các đoạn văn lủng củng, lặp ý hoặc sai ngữ pháp tiếng Anh học thuật cho bài essay 2000+ từ trước khi nộp, dễ bỏ sót lỗi tư duy lập luận.

Actor:
Sinh viên viết bài essay cuối kỳ / tốt nghiệp .

Thời điểm / Bối cảnh:
2-3 ngày trước deadline nộp bài essay cuối kỳ.

Current Workflow:
1. Hoàn thành bản nháp thô (draft) của bài essay.
2. Đọc đi đọc lại từng đoạn văn để tự phát hiện lỗi chính tả, ngữ pháp bằng Grammarly bản miễn phí.
3. Đọc lại để kiểm tra xem lập luận giữa các câu trong đoạn có mạch lạc (coherent) và kết nối với luận điểm chính (thesis statement) không.
4. Tự viết lại (paraphrase) các câu/đoạn văn bị lặp từ hoặc diễn đạt quá suồng sã sang văn phong học thuật.
5. Gửi cho bạn bè/peer-review nhờ nhận xét hộ.
6. Chỉnh sửa lần cuối và nộp bài.

Bottleneck:
Bước 3 & Bước 4 - Kiểm tra tính mạch lạc của lập luận và nâng cấp văn phong học thuật (mất 45-60 phút vì sinh viên dễ bị "mù chữ" sau khi viết quá nhiều, khó tự phát hiện lỗi tư duy lập luận của chính mình).

Success Metric:
Giảm thời gian biên tập, sửa bài từ 70 phút xuống dưới 20 phút; nâng cao chất lượng lập luận (không còn các lỗi ngụy biện hoặc thiếu dẫn chứng kết nối); bài viết đạt chuẩn Academic English cao hơn.

Non-AI Alternative:
Thuê người sửa bài (proofreading) hoặc nhờ Peer-review. Nhược điểm: tốn chi phí, phụ thuộc vào thời gian của người khác, không thể làm ngay lập tức lúc nửa đêm sát deadline.

AI Hypothesis:
AI đóng vai trò một Peer-reviewer khó tính, phân tích cấu trúc bài viết, phát hiện các đoạn lập luận bị hổng hoặc thiếu dẫn chứng, đồng thời gợi ý các phương án paraphrase chuẩn học thuật. Sinh viên chủ động chọn giữ hay thay đổi dựa trên gợi ý.

Quick Gut:
[ ] No AI / Process Fix  [ ] Rule  [x] Workflow  [ ] Agent  [ ] Chưa biết
```

#### 🔄 Quy trình Trước & Sau tối ưu (Draft Workflows)

**Quy trình hiện tại (Current State) — 70 phút:**
```text
[1. Viết xong bản nháp: 0'] 
➔ [2. Chạy Grammarly check lỗi cơ bản: 15'] 
➔ [3. Tự đọc rà soát logic lập luận (Nghẽn): 35'] 
➔ [4. Tự paraphrase nâng cấp văn phong: 15'] 
➔ [5. Đóng gói & Nộp: 5']
```

**Quy trình tương lai kì vọng (Future State) — 20 phút:**
```text
[1. Upload bản nháp lên AI kèm Prompt chi tiết: 2'] 
➔ [2. AI chỉ ra các điểm yếu lập luận & gợi ý paraphrase học thuật: 2'] (Workflow step)
➔ [3. Sinh viên duyệt từng gợi ý, tự chỉnh sửa trực tiếp: 12'] (Human Boundary)
➔ [4. Chạy Grammarly quét lại lần cuối: 2']
➔ [5. Đóng gói & Nộp: 2']
```

---

## 📢 Pitching Preparation (Chuẩn bị trình bày với nhóm)

- **Vấn đề tôi muốn pitch nhất:** 
  > **Vấn đề 1: Tổng hợp báo cáo tiến độ đồ án nhóm hàng tuần (Weekly Group Project Progress Report)**
- **Vì sao vấn đề này đáng để nhóm làm chung:**
  > Đây là vấn đề mà mọi sinh viên làm việc nhóm đều gặp phải. Nó có quy trình trước/sau cực kỳ rõ nét, dễ đo lường tác động (thời gian gom báo cáo của trưởng nhóm), và có sự phân chia ranh giới người-máy (Human-in-the-loop) hoàn hảo: AI chỉ gom và nháp thông tin, con người vẫn là người duyệt cuối cùng để đảm bảo tính công bằng của điểm số. Bài toán này cũng có thể dễ dàng so sánh giữa các giải pháp Rule-based (nhập form) và AI-based (viết narrative).
- **Câu hỏi tôi muốn nhóm thách thức (challenge) tôi:**
  > *"Làm sao chúng ta thu thập được dữ liệu thô từ các thành viên một cách tự nhiên mà không ép họ phải làm thêm việc? Dữ liệu chat tự do trên Discord liệu có quá hỗn loạn để AI hiểu đúng tiến độ thực tế không?"*
