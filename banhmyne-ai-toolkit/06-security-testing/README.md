# 06 — Bảo mật, kiểm thử và chất lượng

## Các nguyên tắc

- Không sao chép mật khẩu, API key, token, hồ sơ nội bộ hoặc dữ liệu nhạy cảm vào prompt, log hay GitHub công khai.
- Các Agent/Skills/Hooks tải từ Internet có thể chứa lệnh bất lợi; luôn đọc nội dung trước khi kích hoạt.
- Chạy thử trên bản sao và dữ liệu giả lập trước.
- Phân loại: đã xác minh qua kiểm thử / nhận định qua đọc mã / chưa kiểm chứng.
- Không bật tự động Push/Merge hoặc bỏ qua bảo vệ chỉ để chạy nhanh.

## Checklist trước khi phát hành

- [ ] Có bản sao lưu và cách phục hồi.
- [ ] Có danh sách file thay đổi và phạm vi cho phép.
- [ ] Đã kiểm tra thông tin nhạy cảm trong thay đổi (kể cả commit history, log).
- [ ] Đã chạy kiểm thử liên quan; ghi kết quả thật, không suy đoán.
- [ ] Đã kiểm tra hoạt động trong đúng hệ điều hành và phiên bản ứng dụng nếu cần.
- [ ] Đã xem diff và yêu cầu người có trách nhiệm phê duyệt.

**Ghi chú:** Các quy trình này giảm rủi ro nhưng không thay thế kiểm toán bảo mật chuyên sâu.
