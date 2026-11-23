# Bộ khởi động AI lập trình VBA và ứng dụng văn phòng (Tiếng Việt)

**Dành cho:** người học lập trình và phát triển tiện ích Word VBA, Excel, ứng dụng Windows offline.  
**Trạng thái:** bộ mẫu để xem xét và tùy chỉnh; **chưa cài đặt** vào Claude Code hoặc dự án đang chạy.

> Kho này là bản Fork công khai của `luongnv89/claude-howto`. Không lưu văn bản nội bộ, thông tin đảng viên, dữ liệu nhân sự, hồ sơ đất đai, khóa API, mật khẩu, token hoặc tệp bí mật tại đây.

## Có những gì?

- [`templates/CLAUDE.project-template.md`](templates/CLAUDE.project-template.md): mẫu quy tắc dự án cho Claude Code; **không** ghi đè `CLAUDE.md` của kho tài liệu.
- [`agents/vba-reviewer.md`](agents/vba-reviewer.md): tác nhân chuyên rà soát VBA theo chế độ chỉ đọc.
- [`skills/vba-office-review/SKILL.md`](skills/vba-office-review/SKILL.md): quy trình kiểm tra an toàn thay đổi Word VBA.
- [`CHECKLIST.md`](CHECKLIST.md): các bước kiểm tra trước khi tích hợp hoặc Push GitHub.

## Cách sử dụng về sau (khi có Claude Code)

1. Tạo bản sao lưu dự án, mở nhánh phát triển riêng, không chỉnh sửa bản đang dùng.
2. Đọc và **điền thông tin dự án** trong mẫu `templates/CLAUDE.project-template.md`.
3. Lưu bản đã chỉnh thành `CLAUDE.md` **ở thư mục gốc của dự án cần phát triển** (không phải thư mục gốc của `claude-howto`).
4. Sau khi duyệt nội dung, có thể sao chép `agents/vba-reviewer.md` vào `.claude/agents/vba-reviewer.md`, và thư mục `skills/vba-office-review` vào `.claude/skills/vba-office-review` **trong dự án riêng**.
5. Mở Claude Code trong thư mục dự án, yêu cầu: “Chỉ đọc và báo cáo lỗi, không sửa tệp, không Commit hoặc Push”.
6. Đối chiếu kết quả với checklist trước khi cho phép bất kỳ chỉnh sửa nào.

**Nếu chưa có Claude:** có thể đọc tài liệu, tham khảo quy trình với ChatGPT hoặc dùng GitHub để lưu cấu hình. Việc có file trên GitHub **không** đồng nghĩa Claude.ai/Claude Code tự động nhận và áp dụng.

## Các nguyên tắc tối thiểu

- Bảo mật dữ liệu trước tiên. Chỉ xử lý dữ liệu mẫu hoặc đã được phép công khai.
- Không tự giả định mã nguồn đã chạy tốt; chỉ đánh dấu “đã kiểm chứng” khi có bằng chứng.
- Không tự sửa, xóa, tái cấu trúc, Commit, Push, Merge, bật hook hoặc cài plugin khi chưa có yêu cầu rõ.
- Với Word VBA: cần xác minh Ribbon callbacks, UserForm control names, tên module và cấu trúc `.dotm` trước khi thay đổi.
- Nếu phát hiện vấn đề rủi ro, mô tả nguyên nhân và hướng khắc phục, ưu tiên không mất dữ liệu.

## Bản quyền và nguồn

Tài liệu gốc: [luongnv89/claude-howto](https://github.com/luongnv89/claude-howto). Các mẫu mới trong thư mục này được bổ sung độc lập, không thay thế tài liệu gốc. Giữ nguyên `LICENSE` (MIT) của repository.
