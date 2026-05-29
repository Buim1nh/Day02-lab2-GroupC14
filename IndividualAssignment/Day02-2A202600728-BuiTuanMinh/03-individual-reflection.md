# 03 — Individual Reflection (Bùi Tuấn Minh)

## 1. Đóng góp trong nhóm

| Hoạt động | Tôi đã làm gì? | Kết quả / Ảnh hưởng |
|---|---|---|
| Scan cá nhân | Đưa ra list 6 problems kết hợp giữa dev tool và game. Pitch mạch lạc về bài toán VOD TFT. | Nhóm có sự so sánh giữa bài toán công việc và giải trí, cuối cùng đồng thuận chọn bài TFT vì nó sát với năng lực AI Multimodal hiện tại. |
| Thiết kế Workflow | Trực tiếp draft ra Current/Future flow, chỉ ra chính xác nút thắt nằm ở bước "tự suy đoán logic" chứ không chỉ ở việc "tua video". | Giúp nhóm không bị sa đà vào việc xây dựng 1 tool Auto-clipper đơn thuần, mà hướng tới AI Reasoning Agent. |
| Research | Tìm hiểu và tổng hợp thông tin về Insights.gg và Trophi.ai. | Phân định rõ ràng khoảng trống (Gap) của các tool trên thị trường hiện tại. |
| Lập luận Agent | Bảo vệ quan điểm phải dùng Agent thay vì Workflow thông thường. | Xác định rõ AI can thiệp vào tầng suy luận đa biến. |

## 2. Bảng dùng AI trong quá trình làm lab

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan & Pitch | Nhờ AI cấu trúc lại ý tưởng lộn xộn trong đầu thành định dạng Problem Card chuẩn. | Format rất gọn gàng, giúp tôi nhìn rõ bottleneck. | Ban đầu AI viết actor quá rộng kiểu "Tất cả những người chơi game". | Tôi giới hạn lại thành "Game thủ trau dồi kỹ năng/thích học hỏi". |
| Workflow | Yêu cầu AI xuất mã code vẽ biểu đồ SVG cho Current và Future state. | Tạo ra sơ đồ trực quan cực kỳ hữu ích cho việc thuyết trình. | Vẽ mũi tên và fallback chưa đúng chỗ trong lần đầu. | Yêu cầu AI sửa lại boundary rõ ràng giữa người và máy. |
| Validation | Nhờ AI đóng vai "Skeptical PM" để phản biện Problem Statement. | Đặt câu hỏi rất chí mạng về "Metric 90% dựa trên ground truth nào?". | N/A (Câu hỏi phản biện tốt). | Thêm Fallback bắt buộc đính kèm clip gốc để con người đối chiếu. |

## 3. Bài học

* **Bài học lớn nhất:** Không phải bài toán nào cũng cần giải bằng AI, nhưng nếu đã dùng AI, phải đặt nó vào đúng **Bottleneck**. Trước đây tôi nghĩ làm tool tự động cắt highlight là xong, nhưng sau khi phân tích kỹ luồng công việc, tôi nhận ra "pain" thật sự của game thủ là "không hiểu tại sao người ta làm thế", tức là tầng logic (reasoning), chứ không phải tầng hiển thị (visual).
* **Tránh bẫy Solution-first:** Lúc đầu tôi rất hào hứng định build ngay một Agent "nhận diện mọi thứ". Nhưng quá trình vẽ Workflow ép tôi phải đối mặt với rủi ro (chi phí tính toán) và bắt buộc phải khoanh vùng Human Boundary (con người vẫn là người xem cuối cùng).
* **Nếu làm lại:** Tôi sẽ challenge nhóm kỹ hơn về việc làm thế nào để lấy được dataset chuẩn để huấn luyện (hoặc prompt) Agent, vì dữ liệu VOD thường rất nhiễu. Có lẽ nên bắt đầu bằng Pilot đánh giá giao diện tĩnh (ảnh chụp màn hình) trước khi quăng cả luồng video vào Agent.