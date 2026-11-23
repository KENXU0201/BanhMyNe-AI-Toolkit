# HƯỚNG DẪN LÀM VIỆC VỚI DỰ ÁN (MẪU — CẦN TÙY CHỈNH)

> Sao chép tệp **sau khi đã xem xét** thành `CLAUDE.md` trong thư mục gốc **dự án riêng**. Không sử dụng nguyên văn trong kho `claude-howto`. Thay các ô [ĐIỀN ...] trước khi áp dụng.

## Tổng quan

- Tên dự án: [ĐIỀN TÊN DỰ ÁN]
- Công nghệ: [Word VBA / Python / công nghệ khác]
- Phiên bản phần mềm: [ĐIỀN PHIÊN BẢN]
- Điểm vào và thành phần chính: [ĐIỀN THƯ MỤC, MODULE, USERFORM, RIBBON]
- Mục tiêu: [ĐIỀN MỤC TIÊU]
- Tệp bản chuẩn/bản sao lưu đã xác minh: [ĐIỀN THÔNG TIN KHÔNG NHẠY CẢM]

## Cách giao tiếp

- Trả lời bằng tiếng Việt rõ ràng, giải thích từ chuyên môn khi mới xuất hiện.
- Trình bày theo thứ tự: hiện trạng → nguyên nhân → cách xử lý → bước kiểm chứng.
- Nếu đề xuất VBA, đưa **mã đầy đủ** cho thành phần cần thay, hướng dẫn chính xác vị trí dán và cách kiểm tra; không cắt bỏ mã quan trọng.

## Giới hạn thay đổi

- Mặc định **chỉ đọc**; không tự ý sửa file, Commit, Push, Merge, xóa module, đổi cấu trúc, cài package hay chạy script.
- Muốn chỉnh sửa phải mô tả: file bị ảnh hưởng, tác động dự kiến, phương án sao lưu, cách hoàn nguyên; chỉ tiến hành sau khi được yêu cầu.
- Không sửa trực tiếp file `.dotm` đang sử dụng. Luôn làm trên bản sao/nhánh phát triển; sao lưu `.dotm` và xuất các thành phần VBA trước khi sửa.
- Hạn chế thêm module mới hoặc đổi tên public procedure nếu chưa chứng minh cần thiết.
- Không tự bịa kết quả kiểm thử, ảnh chụp hay dữ liệu nghiệp vụ.

## Word VBA và Ribbon

1. Kiểm tra tham chiếu Ribbon XML, tên callback và các khai báo `Public Sub/Function`.
2. Kiểm tra UserForm: tên control, sự kiện Click/Change/Initialize, tình trạng control trùng hoặc bị ẩn.
3. Kiểm tra phụ thuộc giữa các module, xử lý lỗi, Unicode tiếng Việt và tương thích Microsoft 365.
4. Phân biệt lỗi có thể kết luận qua đọc mã với lỗi chỉ phát hiện khi chạy trong Word trên Windows.
5. Ưu tiên hiển thị trạng thái trên UserForm; chỉ thông báo popup khi có lỗi/cảnh báo quan trọng nếu dự án yêu cầu.

## An toàn dữ liệu và quyền riêng tư

- Không lưu tài liệu nội bộ, danh sách nhân sự, đảng viên, hồ sơ đất đai, số căn cước, dữ liệu nhạy cảm, khóa API hoặc token lên GitHub công khai.
- Không ghi dữ liệu bí mật vào log, issue, PR hay ảnh chụp.
- Không chạy lệnh có thể xóa, reset, ghi đè dữ liệu; tránh `git push --force` và `git reset --hard` nếu chưa có chỉ đạo rõ.

## Hoàn thành và bàn giao

- Liệt kê file thay đổi và lý do; chỉ nêu kết quả kiểm thử đã thực sự thực hiện.
- Cho biết những gì chưa kiểm chứng được, đặc biệt thao tác cần Microsoft Word thực tế.
- Cung cấp bước khôi phục nhanh và đề nghị kiểm thử lại các chức năng liên quan.
- Commit/Push/Merge chỉ khi được giao nhiệm vụ cụ thể và được phép với repository tương ứng.
