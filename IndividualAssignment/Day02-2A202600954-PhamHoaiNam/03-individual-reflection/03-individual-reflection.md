# 03 — Individual Reflection

## 1. Đóng góp của cá nhân trong dự án nhóm

Dưới đây là chi tiết các đóng góp của tôi trong quá trình làm việc nhóm để hoàn thành bản báo cáo:

| Hoạt động | Công việc cụ thể của tôi | Kết quả & Ảnh hưởng đối với sản phẩm nhóm |
| :--- | :--- | :--- |
| **Quét vấn đề (Scan)** | Đóng góp 8 đề xuất vấn đề cá nhân đa dạng lĩnh vực (TFT, dọn dẹp dữ liệu nghiên cứu Gnuplot, nhập liệu tài chính). | Giúp nhóm có nhiều chất liệu thực tế để phân loại (cluster) và chấm điểm. |
| **Trình bày (Pitching)** | Thuyết trình và bảo vệ đề xuất **"Phân tích VOD TFT"**. Giải thích rõ quy trình hiện tại bị nghẽn ở bước tự suy luận chiến thuật mất 15-20 phút. | Thuyết phục nhóm đưa đề xuất này vào danh sách chấm điểm và cuối cùng đạt điểm số cao nhất (34 điểm) để nhóm chọn. |
| **Tranh biện (Challenge)** | - Đưa ra phản biện cho bài **Gnuplot**: rủi ro ảo giác (hallucination) số thập phân trong nghiên cứu khoa học là cực kỳ nguy hiểm, đề xuất đưa về giải pháp phi-AI (Python Script cứng).<br>- Phản biện bài **Biển báo**: rủi ro an toàn khi thử nghiệm ngoài đời thật quá cao.<br>- Phản biện bài **Nhập liệu tài chính**: rào cản bảo mật dữ liệu nhạy cảm (Privacy) và bài toán "Cold start". | Giúp nhóm loại bỏ các ý tưởng có độ rủi ro cao hoặc quy mô quá rộng, tập trung nguồn lực vào bài toán khả thi nhất. |
| **Kiểm chứng (Validation)** | Trực tiếp đăng tin khảo sát và phỏng vấn nhanh 5 người chơi TFT trên Discord. | Nhận về 4/5 phản hồi xác nhận nỗi đau xem VOD, phát hiện 1 phản hồi trái chiều về việc chỉ cần xem highlight YouTube. Từ đó nhóm bổ sung phần phản biện cho giải pháp phi-AI. |
| **Nghiên cứu (Research)** | Tìm kiếm và phân tích 3 công cụ: **Insights.gg** (bookmarking), **Mobalytics** (API stats) và **Trophi.ai** (AI Coach). | Rút ra bài học: Không nên làm auto-clipper thông thường mà phải tập trung vào lớp suy luận logic (Reasoning Engine) để lý giải "Tại sao". |
| **Xây dựng Quy trình (Workflow)** | Phác thảo quy trình Before (45 phút) và After (9 phút) cho VOD TFT. Đề xuất điểm Human Boundary kiểm soát chất lượng. | Tạo ra sơ đồ trực quan và xác định rõ AI sẽ can thiệp ở bước nào (Thay thế bước tua tay và tự suy đoán bối cảnh). |
| **Tuyên bố bài toán (Problem Statement)** | Dự thảo phần Tuyên bố bài toán v0 và v1, đặc biệt là phần ranh giới hoạt động (Boundary) và điểm can thiệp của AI. | Giúp nhóm định hình rõ ràng phạm vi dự án: AI chỉ viết báo cáo và cắt video timestamp, con người vẫn là người duyệt cuối. |
| **Đánh giá Công nghệ (R/W/A)** | Phân tích lý do vì sao bài toán TFT cần dùng **Agent** (phối hợp Computer Vision và LLM reasoning để xử lý logic mờ) chứ không thể dừng lại ở Rule hay Workflow. | Định hình hướng tiếp cận kỹ thuật cho dự án và thuyết phục nhóm đồng thuận chọn Agent. |
| **Quyết định cuối (Decision)** | Lập luận chọn phương án **GO (với pilot nhỏ)**. Đề xuất phạm vi thử nghiệm tối giản: Chỉ phân tích vòng đấu 3-2. | Giúp nhóm tránh tình trạng ôm đồm (scope creep) và thiết lập được phương án rút lui (rollback) an toàn. |

---

## 2. Nhật ký sử dụng AI hỗ trợ trong quá trình làm bài

Trong suốt Lab 2, tôi đã sử dụng AI làm trợ lý tư duy theo các nguyên tắc đã thống nhất. Dưới đây là đánh giá trung thực về quá trình này:

| Giai đoạn | Tôi dùng AI để làm gì? | AI hữu ích ở điểm nào? | AI bị hời hợt/sai lệch ở điểm nào? | Tôi đã điều chỉnh gì dựa trên nhận định cá nhân? |
| :--- | :--- | :--- | :--- | :--- |
| **Scan vấn đề cá nhân** | Nhờ AI gợi ý các vấn đề lặp lại hoặc tốn thời gian dựa trên bối cảnh sinh viên nghiên cứu và game thủ. | Gợi ý được ý tưởng tìm kiếm tài liệu trên Discord bị trôi và soạn code boilerplate cho Gnuplot. | Đưa ra các gợi ý quá rộng kiểu "trợ lý học tập thông minh" không có workflow rõ ràng. | Tôi bỏ qua các ý tưởng vĩ mô, tự viết lại các vấn đề cụ thể gắn liền với trải nghiệm của bản thân (TFT VOD, log Gnuplot). |
| **Thiết kế Quy trình (Workflow)** | Nhờ AI hỗ trợ viết cú pháp Mermaid cho quy trình Before/After. | Tiết kiệm thời gian tự gõ cú pháp đồ họa Mermaid, giúp flow hiển thị trực quan và đẹp mắt. | AI tự động gộp bước "đọc báo cáo" và "tự đối chiếu video" làm một, bỏ qua vai trò kiểm soát của con người. | Tôi tách riêng bước Đọc báo cáo và quy định đây là **Human Boundary** bắt buộc để kiểm soát rủi ro ảo giác. |
| **Nghiên cứu giải pháp (Research)** | Sử dụng AI/Search để quét các phần mềm phân tích game hiện có. | Phát hiện nhanh ra 3 công cụ Insights.gg, Mobalytics và Trophi.ai mà tôi chưa từng biết trước đó. | AI đưa ra một số số liệu thống kê thời gian tiết kiệm được rất chung chung (ví dụ "tiết kiệm 50% thời gian") mà không có nguồn gốc kiểm chứng rõ ràng. | Tôi chủ động loại bỏ các số liệu vô căn cứ, chỉ trích dẫn tính năng thực tế từ trang chủ chính thức của các công cụ đó. |
| **Lựa chọn công nghệ (Rule/Workflow/Agent)** | Đưa ma trận đánh giá cho AI và yêu cầu phản biện việc chọn Agent. | AI chỉ ra các rủi ro lớn khi dùng Agent như chi phí GPU cao khi xử lý video thời gian thực và độ trễ phản hồi. | AI liên tục khuyên nên xây dựng Agent tự động chơi game luôn để tối ưu trải nghiệm người dùng. | Tôi bác bỏ ý kiến của AI vì việc Agent tự chơi game đã vi phạm trực tiếp vào **Boundary** của bài toán (chỉ hỗ trợ học chiến thuật) và phạm vi của Lab. |

---

## 3. Phản tư sâu (Deep Reflection)

*   **Tôi học được gì khi nghe top 3 problems của các bạn khác?**
    Nghe các bạn trình bày giúp tôi nhận ra rằng nỗi đau (pain point) có ở khắp mọi nơi, từ việc xếp lịch học tín chỉ cho đến định dạng ảnh Gnuplot. Tuy nhiên, không phải vấn đề nào cũng cần AI. Có những bài toán như Gnuplot, việc dùng Python script thuần túy (Rule) mang lại hiệu quả 100% và an toàn hơn hẳn so với việc cố gắng đưa AI Agent vào xử lý dữ liệu thô.
*   **Nhóm có lúc nào bị tình trạng Solution-first (nghĩ về giải pháp trước vấn đề) không?**
    Có. Lúc đầu khi chọn bài toán TFT, nhóm lập tức bàn về việc "dùng mô hình thị giác máy tính nào", "train model ra sao". Tôi đã phải kéo nhóm quay lại bằng cách hỏi: *"Hiện tại bước nào đang làm người chơi tốn thời gian nhất và mất bao nhiêu phút?"*. Nhờ vậy nhóm mới xác định được bottleneck thực sự là bước **suy luận logic bối cảnh**, chứ không phải bước thu thập số liệu.
*   **Tôi có thay đổi ý kiến sau khi bị challenge không?**
    Có. Ban đầu tôi nghĩ AI có thể tự động viết báo cáo phân tích toàn bộ trận đấu TFT dài 40 phút. Nhưng sau khi nhóm challenge về chi phí chạy GPU cho video dài và rủi ro người dùng lười không kiểm tra lại dẫn đến tin vào phân tích sai của AI, tôi đã đồng ý giới hạn **Boundary** (AI bắt buộc phải cắt clip 10s đính kèm báo cáo) và thiết kế **Pilot** cực nhỏ (chỉ phân tích vòng 3-2).
*   **Điều khó nhất khi viết Problem Statement là gì?**
    Đó là việc định lượng **Success Metric** và khoanh vùng **Boundary**. Rất dễ để viết "giúp phân tích nhanh hơn", nhưng để viết rõ "giảm từ 45 phút xuống dưới 9 phút" và "AI không được tự ý quyết định lối chơi thay game thủ" đòi hỏi nhóm phải tư duy cực kỳ chặt chẽ về mặt vận hành.
*   **Nếu làm lại từ đầu, tôi sẽ làm gì khác đi?**
    Tôi sẽ thúc đẩy nhóm đi phỏng vấn nhiều người chơi hơn (khoảng 10-15 người) thay vì chỉ hỏi nhanh 5 bạn trên Discord, để số liệu baseline (45 phút) và các ý kiến phản bác về YouTube highlight có thêm độ tin cậy thống kê cao hơn.
