---
name: vba-office-review
description: Kiểm tra an toàn mã Word VBA, Ribbon, UserForm và thay đổi trong tiện ích Office trước khi chỉnh sửa.
---

# Kiểm tra an toàn dự án Word VBA

Sử dụng kỹ năng này khi cần xem xét thay đổi VBA hoặc kiểm tra các thành phần trong file Word add-in.

## Đầu vào
- Bản sao mã nguồn `.bas`, `.cls`, `.frm` hoặc tài liệu mô tả, không chứa dữ liệu nhạy cảm.
- Danh sách tên module/UserForm/control, callback Ribbon, phiên bản Word và triệu chứng lỗi.
- Yêu cầu thay đổi cụ thể và kết quả mong đợi.

## Quy trình
1. Kiểm tra phạm vi: file nào, thủ tục nào, có bản sao lưu chưa?
2. Đọc tham chiếu liên quan trước, không sửa theo suy đoán.
3. Xác định nguyên nhân có bằng chứng; đánh dấu phần chưa rõ.
4. Xem ảnh hưởng dây chuyền: Ribbon, UserForm, module phụ, thao tác định dạng và compatibility.
5. Đề xuất bản vá tối thiểu; mô tả cách thay và cách quay lại bản trước.
6. Chỉ thực hiện chỉnh sửa khi người dùng đã yêu cầu rõ; mặc định không chạy lệnh ngoài.
7. Kiểm thử tĩnh nếu có thể; hướng dẫn kiểm thử thực tế trong Word nếu môi trường chưa sẵn.
8. Báo cáo lỗi còn mở, tệp tác động và tình trạng chưa kiểm chứng.

## Mẫu báo cáo
| Vị trí | Mức độ | Bằng chứng | Đề xuất | Kiểm chứng |
|---|---|---|---|---|
| Module / thủ tục | Lỗi / nghi vấn | Mô tả cụ thể | Bản vá nhỏ nhất | Chưa chạy / Đã kiểm thử |

## Cấm thực hiện khi chưa được phép
- Không xóa module, chạy macro không rõ nguồn hoặc sửa file `.dotm` gốc.
- Không bật `bypassPermissions`, auto-approve tác vụ ghi/xóa hoặc hooks lạ.
- Không Commit/Push/Merge hoặc gửi dữ liệu nhạy cảm lên repository công khai.

**Ghi chú:** Đây là Skill hướng dẫn quy trình, không phải công cụ tự chạy hay bảo đảm mã đúng.
