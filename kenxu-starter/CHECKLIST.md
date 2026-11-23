# Checklist trước khi tích hợp cấu hình Claude

## Trước khi cài
- [ ] Đã sao lưu bản `.dotm` / dữ liệu và có nhánh làm việc riêng.
- [ ] Đã xác nhận đây là repository công khai, không có nội dung bí mật.
- [ ] Đã đọc toàn bộ file sẽ sao chép vào dự án; không cài toàn bộ hooks/scripts từ nguồn ngoài.
- [ ] Đã chỉnh `CLAUDE.project-template.md` theo đúng dự án.
- [ ] Đã ghi lại tên module, UserForm, Ribbon callbacks và phiên bản Word.

## Kiểm thử chỉ đọc
- [ ] Yêu cầu agent liệt kê file và phân tích mà không sửa.
- [ ] Đối chiếu lỗi báo cáo với tệp thực tế; tách lỗi chắc chắn và nghi vấn.
- [ ] Không phát sinh chỉnh sửa, commit, push hay quyền mới.

## Trước khi thay đổi mã
- [ ] Mô tả phạm vi sửa và cách khôi phục.
- [ ] Đã được người dùng giao nhiệm vụ chỉnh sửa.
- [ ] Có bản mã đầy đủ, tên vị trí dán và kế hoạch kiểm tra.
- [ ] Kiểm thử chức năng thay đổi và chức năng có liên quan trong Microsoft Word nếu có môi trường.

## Trước khi Push
- [ ] Không có key/token/mật khẩu, dữ liệu nội bộ, file chứa hồ sơ hoặc log bí mật.
- [ ] Đã xem diff, chỉ có file dự kiến.
- [ ] Đã kiểm tra kết quả và thông báo rõ phần chưa kiểm chứng.
- [ ] Không dùng force-push hoặc merge tự động ngoài phạm vi được giao.

## Khi Claude hết hạn
Bạn vẫn có thể xem và chỉnh tài liệu trên GitHub hoặc cùng ChatGPT rà soát các mẫu. Chưa thể xác nhận cấu hình hoạt động trong Claude Code cho tới khi thử thực tế.
