# 03 — Individual Reflection Example

## Đóng góp trong nhóm

| Hoạt động | đã làm gì? | Kết quả |
|---|---|---|
| Scan cá nhân | Đưa ra 1 problems | Nhóm có nhiều problem khả thi và quyết định vote chọn 1  |
| Pitch | Pitch VOD TFT | Bài được vào shortlist |
| Challenge | Hỏi nhóm mục đích cuối cùng của AI trong Agent VOD là gì? | Nhóm đưa ra được scope cụ thể là phân tích và giải thích  |
| Research | Tìm hiểu MetaTFT  | Xác định MetaTFT chỉ xử lý dữ liệu tĩnh (API). |
| Rule / Workflow / Agent | So sánh giữa các phương án tiếp cận: Rule-based, Workflow-based, Autonomous Agent. | Nhóm thống nhất lựa chọn giải pháp tối ưu theo hướng Workflow |

## Bảng dùng AI trong reflection

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì |
|---|---|---|---|---|
| Scan | Nhờ AI mở rộng thêm các problem từ vấn đề có sẵn của bản thân.  | Gợi ý thêm các góc nhìn hay về miss data (mất dữ liệu) và các khoản chi ẩn. | Nhảy quá sâu vào phần chi phí phát triển  | Loại bỏ các vấn đề thuộc về chi phí phát triển|
| Workflow | Nhờ AI chuyển mô tả thành hình ảnh trực quan | Nhanh hơn khi vẽ flow | AI gộp gõ thông tin và phân danh mục thành 1  | Tách lại vì gõ thông tin và phân danh mục khác nhau|
| Validation | Nhờ AI phản biện toàn bộ luồng  | Gợi ý thêm trigger để người dùng vào app | AI quá chú tâm vào phần UX | Tập trung về vấn đề bài toán |

## Bài học

- AI có xu hướng nhảy quá nhanh vào phần chi phí phát triển (Development Cost), nhưng bài toán cốt lõi của người dùng phổ thông là Ma sát thao tác và Gánh nặng ghi nhớ (lười gõ tay, quên số lẻ). Khi bẻ hướng phân tích tập trung vào nỗi đau nguyên bản này, bài toán mới thực sự có sức nặng.
- Khi rã nhỏ workflow thành từng giây trải nghiệm, ta sẽ thấy AI hay bị "hời hợt" khi gộp chung bước Gõ thông tin thô và Phân loại danh mục làm một. Việc tách rời hai bước này giúp nhận ra: Người dùng gãy vì ngại mò phím số và mệt não khi đắn đo chọn nhóm Từ đó mới biết AI cần fill ô nào, rule truyền thống xử lý ô nào..
- Pattern thành công của bài toán này là AI điền sẵn Form (Draft) — Người dùng xác nhận (Review).
- Khi nhờ AI phản biện khâu Validation, nó có xu hướng chỉ tập trung sửa lỗi giao diện (UI/UX) mà quên mất cốt lõi bài toán.

Nếu làm lại:

```text
Tôi sẽ mang bản phân tích luồng "Chạm để nhập/Duyệt Form" này đi phỏng vấn sâu với khoảng 5-10 người dùng có đặc tính "siêu lười và hay chi tiêu lặt vặt" giống bạn Chi trước khi chốt thiết kế kịch bản nút bấm. Tôi cần đo lường chính xác xem baseline "tỷ lệ bỏ cuộc tại bước bật bàn phím gõ số lẻ" ngoài đời thực là bao nhiêu %, thay vì chỉ dựa hoàn toàn vào giả định và trải nghiệm lười biếng mang tính cá nhân của riêng tôi.
```

---