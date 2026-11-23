---
name: task-triage
description: Phân loại yêu cầu AI, chọn đầu ra và công cụ phù hợp, nhận diện rủi ro trước khi thực hiện.
---

# Xác định phạm vi và phương án xử lý công việc AI

Khi người dùng yêu cầu làm một việc:
1. Tóm tắt mục tiêu bằng một câu, xác định đầu ra thật sự cần (văn bản, bảng tính, mã nguồn, hình ảnh, thao tác trên công cụ...).
2. Ghi nhận tài liệu hiện có, phiên bản, dữ liệu chưa có và các ràng buộc.
3. Phân loại: chỉ cần giải thích / cần phân tích file / cần tạo file / cần can thiệp repository hoặc ứng dụng ngoài.
4. Chỉ chọn công cụ phù hợp với quyền hiện có; không giả định có quyền với Claude/GitHub/dịch vụ chỉ vì tài liệu mô tả kết nối.
5. Nếu có rủi ro ghi đè, lộ dữ liệu hoặc thay đổi không thể hoàn tác, yêu cầu phê duyệt trước bước đó.
6. Đưa kế hoạch ngắn và tiêu chí nghiệm thu; không bịa kết quả.

Mặc định hướng dẫn bằng tiếng Việt, ưu tiên thao tác đơn giản, bảo mật và khả năng phục hồi.
