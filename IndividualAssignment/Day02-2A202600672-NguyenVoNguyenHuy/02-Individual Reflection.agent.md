# 03 — Individual Reflection

## Tôi đã tham gia vào phần nào?

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| Scan cá nhân | Đưa ra 10 problems tập trung vào mảng Sản xuất & Quản lý chất lượng (QC). | Nhóm có thêm góc nhìn về các bài toán ngoài môi trường văn phòng/software truyền thống. |
| Pitch Problem Card | Pitch bài toán "Lục tìm hồ sơ truy vết lỗi" với số liệu downtime thực tế. | Thuyết phục được nhóm đưa bài này vào shortlist vì metric (thời gian dừng máy) có sức nặng lớn. |
| Challenge bài của bạn khác | Đặt câu hỏi cho bài "Tóm tắt meeting notes" của thành viên khác: "Nếu AI nghe sai thuật ngữ chuyên ngành thì sao?" | Nhóm nhận ra rủi ro Hallucination cao và loại bài đó khỏi top 1. |
| Workflow nhóm | Vẽ chi tiết các bước QC phải chạy đi tìm file cứng và log máy như thế nào. | Chốt được bottleneck nằm ở khâu "gom dữ liệu đa nguồn" chứ không phải khâu "viết báo cáo". |
| Rule / Workflow / Agent | Lập luận chọn Workflow (RAG) thay vì Agent. | Nhóm thống nhất không để AI tự phán đoán nguyên nhân lỗi rồi gửi đi (quá rủi ro cho nhà máy), con người phải là ranh giới cuối (human boundary). |

## Bảng dùng AI trong reflection

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Nhờ AI cấu trúc lại câu chữ cho 10 problems ban đầu. | Giúp bảng scan nhìn gọn gàng, chia lăng kính rõ ràng. | AI gợi ý một số lỗi sai kiểu "hệ thống tự động sửa máy". | Tôi gạch bỏ vì sai thực tế nhà máy; giữ lại việc AI chỉ hỗ trợ tìm thông tin cho QC. |
| Problem Card | Đưa Problem Card nhờ AI phản biện (đóng vai QA Manager). | Đặt câu hỏi rất hay về tình trạng "dữ liệu rác" của log máy. | Đề xuất giải pháp bằng Agent quá phức tạp. | Tôi chủ động hạ xuống mức Workflow (AI gom data + tóm tắt), QC tự chốt quyết định. |
| Workflow | Nhờ định dạng lại before/after flow cho dễ nhìn. | Tiết kiệm thời gian gõ phím. | Không có. | Căn chỉnh lại thời gian (phút) cho sát với thực tế xưởng. |

## Reflection câu hỏi mở

- **Tôi học được gì khi nghe top 3 problems của các bạn khác?** Mình nhận ra đa số mọi người hay bị vướng ở khâu "tổng hợp dữ liệu từ nhiều nguồn khác nhau", dù làm ở văn phòng hay dưới xưởng.
- **Nhóm có lúc nào bị solution-first không?** Có, lúc đầu nhóm rất háo hức muốn tạo một Agent "chỉ cần chụp hình sản phẩm lỗi là tự ra nguyên nhân". Mình đã kéo nhóm lại bằng cách phân tích workflow: phải tìm log máy, tìm hồ sơ lô hàng, chứ AI không thể nhìn hình mà đoán được bên trong máy chạy thông số gì.
- **Điều khó nhất khi viết Problem Statement là gì?** Là việc xác định "Boundary" (ranh giới). Ban đầu viết rất mông lung, sau phải chốt rõ ràng: "AI chỉ tóm tắt timeline lỗi, KHÔNG tự đưa ra kết luận nguyên nhân gốc rễ".
- **Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?** Sẽ xoáy sâu hơn vào phần "Non-AI alternative". Ở nhà máy, đôi khi chỉ cần làm chuẩn 5S văn bản giấy tờ hoặc nhập data lên chung 1 sheet là xong, chưa chắc đã cần đến AI.

## Tự kiểm cuối bài

- [x] [12đ cá nhân] Cá nhân có 5+ problems và top 3 Problem Cards.
- [x] [12đ cá nhân] Tôi đã pitch rõ và challenge nhóm đúng trọng tâm.
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài (Phần này nằm trong repo nhóm).
- [x] [15đ nhóm] Nhóm có workflow trước/sau.
- [x] [20đ nhóm] Nhóm có Problem Statement v0/v1 với metric và boundary rõ.
- [x] [15đ nhóm] Nhóm có so sánh No AI / Rule / Workflow / Agent.
- [x] [10đ nhóm] Nhóm có Go / Not Yet / No-Go và lý do rõ.
- [x] [10đ cá nhân] Reflection cá nhân có nói rõ vai trò trong nhóm, cách dùng AI, điều học được và nếu làm lại sẽ đổi gì.
- [x] [6đ cá nhân] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp với AI.