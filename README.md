# Vietnamese Invoice Recognition

Hệ thống AI Agent hỗ trợ nhận dạng và trích xuất thông tin từ hóa đơn tiếng Việt. Dự án hướng tới việc để người dùng tải ảnh hóa đơn, đặt câu hỏi bằng ngôn ngữ tự nhiên và nhận câu trả lời dưới dạng văn bản hoặc JSON.

## Mục tiêu

- Đọc và hiểu nội dung tiếng Việt trực tiếp từ ảnh hóa đơn.
- Trả lời câu hỏi về hóa đơn và trích xuất thông tin theo yêu cầu.
- Tạo kết quả có cấu trúc để thuận tiện cho việc sử dụng tiếp.
- Ghi lại các phiên tương tác nhằm hỗ trợ đánh giá và tái lập thí nghiệm.

## Hướng tiếp cận

Dự án đề xuất một quy trình OCR-free, không yêu cầu huấn luyện mô hình hoặc chuẩn bị dữ liệu gán nhãn. Mô hình đa phương thức **Vintern-1B-v2** đóng vai trò AI Agent trung tâm, xử lý ảnh và câu hỏi của người dùng. Prompt hướng mô hình trả kết quả theo schema JSON; các thông tin không chắc chắn được biểu diễn bằng `null`.

Luồng xử lý dự kiến:

1. Người dùng tải ảnh hóa đơn lên.
2. Người dùng nhập câu hỏi hoặc yêu cầu trích xuất.
3. AI Agent phân tích ảnh cùng câu hỏi.
4. Hệ thống trả về câu trả lời dạng văn bản hoặc JSON.
5. Phiên tương tác được ghi log phục vụ đánh giá.

## Giao diện và môi trường

Báo cáo mô tả giao diện xây dựng bằng **Gradio** và môi trường thử nghiệm **Google Colab với GPU T4**, sử dụng Python. Giao diện cho phép tải ảnh, nhập câu hỏi và xem kết quả.

Thông tin log được mô tả gồm ảnh đầu vào, câu hỏi, prompt gửi tới mô hình, câu trả lời, thời gian xử lý và thông tin mô hình.

## Tài liệu

Báo cáo Project III: [Project_III___Phùng_Hữu_Phú___11-1.pdf](./Project_III___Phùng_Hữu_Phú___11-1.pdf)

## Phạm vi repository

Repository hiện lưu báo cáo dự án và README. Mã nguồn triển khai, notebook và trọng số mô hình không nằm trong repository này; vì vậy chưa có hướng dẫn cài đặt hoặc chạy ứng dụng.
