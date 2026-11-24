# 03 — AI Agents, Skills, MCP và tự động hóa

## Khái niệm

- **Prompt:** yêu cầu bằng ngôn ngữ tự nhiên.
- **Skill:** bộ hướng dẫn chuyên môn dùng lại nhiều lần.
- **Agent:** tác nhân có nhiệm vụ, công cụ và ranh giới quyền hạn.
- **MCP:** chuẩn kết nối AI với công cụ/dịch vụ bên ngoài.
- **Hook:** tác vụ được kích hoạt tại một sự kiện; có thể chạy lệnh và cần kiểm tra cẩn thận.
- **Checkpoint:** khả năng quay về trạng thái trước khi đổi.

## Quy trình tạo một Agent an toàn

1. Xác định một nhiệm vụ có đầu ra cụ thể.
2. Chỉ cấp đúng quyền cần thiết; giai đoạn đầu ưu tiên **chỉ đọc**.
3. Chỉ định nguồn dữ liệu và giới hạn bảo mật.
4. Thử trên dữ liệu giả lập, xem log/đầu ra thực tế.
5. Bổ sung cơ chế duyệt trước khi ghi, xóa, gửi dữ liệu hoặc Push.
6. Theo dõi lỗi và cải tiến từng phiên bản.

## Mẫu có sẵn

- [Agent phân tích yêu cầu](agents/requirements-analyst.md) — chỉ đọc, không viết mã.
- [Skill xác định phạm vi công việc](skills/task-triage/SKILL.md) — xác định mục tiêu, đầu vào, rủi ro và đầu ra.
- [Skills cho Google Antigravity (Gemini)](antigravity-skills.md) — kho skill mạnh, Superpowers, cách cài trên Windows.

## Cách dùng

Các file ở đây chỉ là **mẫu**. Với Claude Code, hãy rà soát tương thích rồi sao chép mẫu Agent vào `.claude/agents/` và Skill vào `.claude/skills/<tên-skill>/SKILL.md` trong **dự án riêng**. Khi dùng ChatGPT/Gemini, cần chuyển đổi hướng dẫn theo tính năng công cụ đó; không thể giả định tự chạy giống Claude Code.

Không chạy `06-hooks` trong giáo trình gốc hoặc tạo GitHub token chỉ để thử nghiệm.
