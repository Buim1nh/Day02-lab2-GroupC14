# 01 — Individual Problem Scan

## 1. Scan Rộng (6 Problems)

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Mỗi khi gặp Item mới/không biết dùng trong game, luôn phải vào discord/wiki để tìm thông tin/câu trả lời cũ. | Người chơi D&D | Thời gian tiêu tốn không cố định, từ 10-15p đến 1-2 tiếng/lần. |
| 2 | Lặp lại | Mỗi lần Game update phải liên tục cập nhật meta đội hình từ các nguồn Tiktok, Youtube, Facebook, Threads,... | Game thủ TFT | Khó để tìm ra đội hình phù hợp ngay lập tức mỗi khi chơi game. |
| 3 | Tốn thời gian | Quá trình xem toàn bộ video dài 30-40 phút chỉ để học cách tuyển thủ đưa ra quyết định ở các vòng đấu bản lề. | Game thủ TFT | Mất tới 45p-1 tiếng để vừa xem, vừa tua, vừa phân tích 1 trận. |
| 4 | Tốn thời gian | Tìm kiếm và đối chiếu các rule cụ thể (shove action, indomitable) giữa các sách D&D 5e Player Handbook khi đang chơi dở chiến dịch. | Người chơi D&D | Làm gián đoạn nhịp độ trận đấu khoảng 5-10 phút mỗi lần tra cứu. |
| 5 | Lặp lại | Phải theo dõi thủ công lịch ra chương mới của các bộ truyện (Cổ Chân Nhân, Xích Tâm Tuần Thiên) trên nhiều nền tảng (Tangthuvien, WebNovel). | Độc giả Web novel | Ngày nào cũng phải mở 2-3 tab để f5 kiểm tra chương mới. |
| 6 | Tốn thời gian | Đọc log lỗi dài dòng để tìm nguyên nhân crash mỗi khi build Docker hoặc deploy dự án Next.js/ReactJS lên Vercel. | Frontend/Fullstack Dev | Mất 15-30 phút dò từng dòng log để tìm ra dòng báo lỗi thực sự. |

---

## 2. Top 3 Problem Cards & Draft Workflow

### Problem Card #1 
```text
┌──────────────────────────────────────────────┐
│ PROBLEM CARD #1: Phân tích VOD TFT           │
│                                              │
│ Problem 1 câu: Xem VOD dài 40p để học cách   │ 
│ xoay bài của tuyển thủ mất nhiều thời gian,  │
│ hiệu suất kém do thiếu dữ liệu bối cảnh để   │
│ hiểu tư duy logic đằng sau thao tác.         │
│                                              │
│ Ai đang đau? Game thủ TFT trau dồi kỹ năng.  │
│                                              │
│ Workflow hiện tại:                           │
│ 1. Mở VOD → 2. Tua tìm mốc → 3. Ghi nhận     │
│ thao tác → 4. Suy đoán lý do → 5. Chốt note  │
│                                              │
│ Bước nghẽn nhất: Dò tìm mốc quan trọng và    │
│ suy đoán lý do xoay bài (15-25 phút/lần).    │
│                                              │
│ Đo thành công bằng gì? Giảm thời gian trích  │
│ xuất từ 45p xuống dưới 10p, tỷ lệ đúng >90%. │
│                                              │
│ Quick gut: □ No AI □ Rule □ Workflow         │
│            ■ Agent □ Chưa biết               │
└──────────────────────────────────────────────┘
```
Draft Workflow #1:

```text
Current State (45 phút): 
[Mở VOD: 2'] 
→ [Tua tìm mốc biến động: 10'] 
→ [Ghi nhận bề nổi: 10'] 
→ [Suy đoán lý do bối cảnh: 15'] (Bottleneck) 
→ [Ghi chép: 8']
```
```text
Future State (9 phút): 
[Nhập URL: 1'] 
→ [Agent quét bối cảnh: 3'] 
→ [Agent phân tích logic: 2'] 
→ [Human đọc báo cáo: 3'] (Human Boundary)
```
### Problem Card #2
```text
┌──────────────────────────────────────────────┐
│ PROBLEM CARD #2: Cập nhật Meta TFT            │
│                                              │
│ Problem 1 câu: Mỗi bản update phải cày nát   │
│ MXH (TikTok, Youtube, Threads) để tự chắt    │
│ lọc ra đội hình meta nào đang mạnh nhất.     │
│                                              │
│ Ai đang đau? Game thủ TFT.                   │
│                                              │
│ Bước nghẽn nhất: Đọc patch note và đối chiếu │
│ để loại suy các đội hình bị nerf (30-45p).    │
│                                              │
│ Đo thành công bằng gì? Rút ngắn thời gian    │
│ nắm bắt meta mới xuống còn 5 phút đọc tóm tắt│
│                                              │
│ Quick gut: □ No AI □ Rule ■ Workflow         │
│            □ Agent □ Chưa biết               │
└──────────────────────────────────────────────┘
```
Draft Workflow #2:

```text
Current State (45 phút): 
[Đọc patch note: 15'] (Bottleneck) 
→ [Lướt MXH/Web tft xem đội hình: 20'] 
→ [Lưu ảnh/mã đội hình: 10']
```
```text
Future State (5 phút): 
[AI crawl dữ liệu MXH + Patch note: 2'] 
→ [AI xuất danh sách Tier list: 1'] 
→ [Human xem và chọn bài: 2'] (Human Boundary)
```
### Problem Card #3
```text
┌──────────────────────────────────────────────┐
│ PROBLEM CARD #3: Tra cứu Item mới            │
│                                              │
│ Problem 1 câu: Gặp Item mới/lạ trong trận,    │
│ phải tabbing ra ngoài xem wiki/discord làm   │
│ mất thời gian và dễ thao tác lỗi trong game. │
│                                              │
│ Ai đang đau? Người chơi D&D.                 │
│                                              │
│ Bước nghẽn nhất: Rời mắt khỏi bàn chơi để gõ  │
│ search keyword trên Wiki (1-2 phút/vòng).    │
│                                              │
│ Đo thành công bằng gì? Thời gian nhận diện    │
│ và biết cách sử dụng item < 10 giây.         │
│                                              │
│ Quick gut: □ No AI ■ Rule □ Workflow         │
│            □ Agent □ Chưa biết               │
└──────────────────────────────────────────────┘
```
Draft Workflow #3:

```text
Current State (2 phút/vòng): 
[Thấy item lạ] 
→ [Tab ra trình duyệt] 
→ [Search Wiki/Discord] (Bottleneck) 
→ [Tab vào game] 
→ [Sử dụng đồ]
```
```text
Future State (10 giây): 
[Cài tool] 
→ [Hover chuột vào item] 
→ [Hiển thị thông tin đồ ngay trên màn hình] (Non-AI/Rule is enough)
```
## 3. Lý do pitch Card #1 và Câu hỏi challenge
Vì sao pitch: 
```text
Vấn đề 2 (Meta) và 3 (Item) đã có nhiều web tĩnh (như tftactics) giải quyết được phần lớn. Vấn đề 1 (VOD Review) chưa có tool tự động hóa triệt để, tốn cực nhiều thời gian mỗi tuần và có dư địa ứng dụng AI (Computer Vision + Reasoning) rất rõ ràng.
```

Câu hỏi muốn nhóm challenge: 
```text
Liệu rào cản chi phí tính toán GPU cho việc scan luồng video 40 phút có làm giải pháp này trở nên bất khả thi để scale không?
```