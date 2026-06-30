# Tổng Hợp Nhóm: So Sánh Risk Profile Giữa Các Ngành

## 1. Bảng So Sánh Risk Profile
| Ngành | Harm dễ gặp nhất | Failure mode hay lặp lại | Layer hay bắt đầu lỗi | Risk profile tổng thể | Vì sao? |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **HR / Tuyển dụng** | Opportunity loss (Mất cơ hội việc làm), Bias. | Bias / Fairness. | Model training data. | Medium-High | Dữ liệu lịch sử chứa định kiến. AI tự động loại CV gây bất công xã hội và rủi ro kiện tụng. |
| **Y tế / Health Assistant** | Injury (Tổn hại sức khỏe), Chẩn đoán sai. | Harmful advice, Hallucination. | Safety, Grounding. | Critical | Trực tiếp đe dọa sinh mạng người bệnh nếu AI đưa ra đơn thuốc sai. Dữ liệu là y lệnh. |
| **Mobility / Autonomous** | Physical Injury, Hư hỏng tài sản. | Edge-case failure, Escalation failure. | Model (Computer Vision), System. | Critical | Ô tô tự lái nếu nhận diện sai biển báo hoặc vật cản sẽ gây tai nạn chết người ngay lập tức. |
| **Media / News / Social** | Misinformation, Mất uy tín, Thao túng. | Misuse, Over-reliance, Hallucination. | Safety policy, UX (thiếu minh bạch). | High | Tin giả lan truyền cấp số nhân. Rất khó vãn hồi niềm tin (Blast radius cực kỳ cao). |

## 2. Đoạn tổng hợp ngắn về Risk Profile giữa các ngành
Qua thảo luận nhóm, chúng tôi nhận thấy các ngành có sự khác biệt rõ rệt về loại hình rủi ro. **Y tế và Mobility** mang rủi ro chí mạng về thể chất (Severity: Critical), đòi hỏi bar "được ship" và Human-in-the-loop cực kỳ khắt khe. Ngược lại, **Media và HR** ít gây hại thể chất hơn nhưng có **Scale (Quy mô) lan rộng cực lớn**. Báo chí đối mặt với sự thao túng tập thể và lan truyền tin giả (Misinformation), trong khi HR phải đối mặt với sự phân biệt đối xử có hệ thống (Bias). Điểm chung duy nhất là AI hiện tại chưa đủ khả năng tự trị hoàn toàn (autonomous) trong bất kỳ ngành nào mà thiếu sự giám sát từ con người.

---

## [Bonus] AI Product Manager POV — Giải Pháp "AI News Guard"
Sau khi nghiên cứu Risk Profile của ngành Media, nhóm đề xuất xây dựng hệ thống **AI News Guard** nhằm phát hiện Deepfake và cảnh báo Hallucination cho tòa soạn:

- **Module Fact-checking:** Cross-check số liệu bài viết với Reuters/Bloomberg để lọc các ảo giác tài chính (khắc phục vụ CNET).
- **Module Deepfake Detector:** Quét metadata của ảnh/âm thanh tác giả và tin tức đính kèm để chống Fake Author (khắc phục vụ Sports Illustrated).
- **Workflow:** Gắn nhãn màu (Xanh: An toàn, Đỏ: Cần duyệt). Bài bị gắn cờ "Đỏ" bắt buộc phải có OTP từ Tổng biên tập mới được phép publish.
