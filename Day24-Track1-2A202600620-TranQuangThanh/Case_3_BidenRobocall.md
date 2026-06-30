# Case Study 3: Biden Deepfake Robocall

## Brief Case
| Field | Bạn điền gì |
| :--- | :--- |
| **Tên case** | Deepfake Robocall giả giọng TT Biden |
| **Ngành** | Media / news / social / political assistant |
| **Tổ chức / sản phẩm** | Steve Kramer (Political Consultant) / AI Voice Cloning |
| **Use case AI** | Dùng AI nhân bản giọng nói (Voice Cloning) để thao túng chính trị thông qua cuộc gọi tự động (robocall). |
| **Thời điểm** | Tháng 1/2024 |
| **Case xảy ra chuyện gì?** | Một nhà tư vấn chính trị đã dùng AI nhái giọng ông Joe Biden, gọi cho cử tri bang New Hampshire yêu cầu họ KHÔNG đi bầu cử vòng sơ bộ. |
| **Stakeholder bị ảnh hưởng** | Cử tri bang New Hampshire, Quá trình bầu cử dân chủ Mỹ. |
| **Số liệu chính** | FCC đã phạt Steve Kramer **6 triệu USD** và phạt nhà cung cấp viễn thông Lingo Telecom **1 triệu USD**. |
| **Trích nguồn ngắn** | FCC ra mức phạt tổng cộng 7 triệu USD cho việc dùng AI deepfake giọng nói cản trở bầu cử. |
| **Nguồn 1** | FCC.gov (23/05/2024) - [FCC Proposes $6 Million Fine for AI-Generated Deepfake Robocalls](https://www.fcc.gov/document/fcc-proposes-6-million-fine-ai-generated-deepfake-robocalls) |
| **Nguồn 2** | AP News (24/05/2024) - [FCC proposes $6M fine for political consultant...](https://apnews.com/article/biden-ai-deepfake-robocall-fcc-fine-c70e3012c4) |
| **Ghi chú độ tin cậy** | Primary Source (Trang chính phủ FCC). Cực kỳ đáng tin cậy. |

## Harm Map Worksheet
| High-risk moment | Stakeholder bị ảnh hưởng | Failure mode | Layer bắt đầu lỗi | Harm xảy ra là gì? | Harm lens | Severity | Scale | Probability | Frequency | Vì sao? |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Phát tán hàng ngàn cuộc gọi mạo danh chính trị gia sát ngày bầu cử. | Cử tri, Hệ thống dân chủ. | Misuse / Deepfake. | Model / Security. | Tước đoạt quyền lợi bầu cử của công dân do hiểu lầm. | Opportunity loss, Misinformation. | Critical | Medium | High | Low | AI Voice Cloning không có watermarking kết hợp với mạng viễn thông cho phép giả caller ID tạo ra lỗ hổng lớn đe dọa an ninh chính trị. |
