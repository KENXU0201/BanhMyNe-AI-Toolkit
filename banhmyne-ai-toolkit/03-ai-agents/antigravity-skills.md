# Skills cho Google Antigravity (Gemini)

**Kiểm tra ngày:** 24/11/2026. Đã tải và đọc mã nguồn các kho ở mục 2 (chưa chạy thử từng skill trong Antigravity).

## 1. Skill trong Antigravity

- Antigravity dùng **cùng chuẩn `SKILL.md`** với Claude: một skill là một thư mục chứa file `SKILL.md`, có thể kèm `scripts/`, `references/`.
- Skill của Claude (ví dụ mẫu trong thư mục này) chép sang Antigravity là dùng được, không cần sửa.
- Gemini chỉ đọc phần mô tả ngắn của mỗi skill khi mở phiên; khi yêu cầu khớp mới nạp toàn bộ, nên cài nhiều skill không làm chậm.
- Gọi skill: để Gemini tự chọn, hoặc gõ `/<tên-skill>` trong khung chat.

| Phạm vi | Thư mục | Ghi chú |
|---|---|---|
| Một dự án | `<thư mục dự án>/.agents/skills/<tên-skill>/` | Thư mục cũ `.agent/skills` vẫn đọc được |
| Mọi dự án | `~/.gemini/config/skills/<tên-skill>/` | Windows: `C:\Users\<tên>\.gemini\config\skills\` |
| Cài dạng plugin | `~/.gemini/config/plugins/<plugin>/skills/` | Do lệnh `agy plugin install` tạo |

Nguồn: [Antigravity – Agent skills](https://antigravity.google/docs/skills), [Codelab Authoring Antigravity Skills](https://codelabs.developers.google.com/getting-started-with-antigravity-skills).

## 2. Các kho skill đã kiểm tra

| Kho | Nội dung | Giấy phép | Đánh giá |
|---|---|---|---|
| [obra/superpowers](https://github.com/obra/superpowers) | 15 skill quy trình lập trình | MIT | **Nên dùng nhất** – chất lượng cao, hỗ trợ Antigravity chính thức |
| [anthropics/skills](https://github.com/anthropics/skills) | docx, xlsx, pdf, pptx và 15 skill khác | Apache 2.0 (4 skill tài liệu) | Hợp việc văn phòng |
| [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) | Hơn 2.600 skill cộng đồng | MIT | Rộng nhưng chất lượng không đều, chỉ chọn lọc |
| [rominirani/antigravity-skills](https://github.com/rominirani/antigravity-skills) | Skill mẫu của codelab Google | — | Dùng để học tự viết skill |

### Superpowers – 15 skill

| Nhóm | Skill | Khi nào dùng |
|---|---|---|
| Khởi đầu | `using-superpowers` | Tự nạp đầu mỗi cuộc trò chuyện, hướng dẫn Gemini dùng các skill còn lại |
| Ý tưởng, kế hoạch | `brainstorming`, `writing-plans`, `executing-plans` | Trước khi làm tính năng mới |
| Gỡ lỗi | `systematic-debugging`, `verification-before-completion` | Gặp lỗi: tìm nguyên nhân gốc trước khi sửa, kiểm chứng trước khi báo xong |
| Kiểm thử | `test-driven-development` | Viết kiểm thử trước khi viết mã |
| Rà soát | `requesting-code-review`, `receiving-code-review` | Trước khi gộp, khi nhận góp ý |
| Git | `using-git-worktrees`, `finishing-a-development-branch` | Làm nhánh riêng, kết thúc nhánh |
| Nâng cao | `subagent-driven-development`, `dispatching-parallel-agents` | Chia việc cho nhiều tác nhân |
| Khác | `writing-skills`, `diagnosing-superpowers` | Tự viết skill, tìm lý do phiên làm việc chạy sai |

**Kiểm tra an toàn (đã đọc mã):** hook `session-start` chỉ đọc file `skills/using-superpowers/SKILL.md` trên máy, không kết nối mạng, không ghi file. Theo README hiện tại, Antigravity không chạy hook này mà dựa vào mô tả của `using-superpowers`.

## 3. Phù hợp với BanhMyNe

| Ưu tiên | Skill | Dùng cho |
|---|---|---|
| 1 | `systematic-debugging`, `verification-before-completion` | Học Python, sửa lỗi ứng dụng |
| 2 | `brainstorming`, `writing-plans` | Lên ý tưởng, kế hoạch dự án mới |
| 3 | docx, xlsx, pdf (anthropics/skills) | Văn bản, bảng tính, PDF |
| 4 | Skill tự viết: `task-triage`, `vba-office-review`, `python-code-review` | Chép vào thư mục skill toàn cục |
| Bỏ qua | `subagent-driven-development`, `dispatching-parallel-agents`, cài nguyên kho awesome-skills | Quá nâng cao hoặc khó kiểm soát |

## 4. Cài Superpowers trên máy Windows (máy cơ quan)

**Điều kiện:** máy đã cài Google Antigravity và đăng nhập tài khoản Google. Không cần quyền quản trị: mọi thứ cài vào thư mục người dùng. Nếu cơ quan có quy định cài phần mềm, hỏi bộ phận CNTT trước.

### Cách 1 – bằng lệnh (khuyên dùng)

1. Mở Antigravity → menu **Terminal → New Terminal** (hoặc mở **Windows PowerShell**).
2. Gõ lệnh sau rồi Enter:

    ```powershell
    agy plugin install https://github.com/obra/superpowers
    ```

3. Kiểm tra đã cài:

    ```powershell
    agy plugin list
    ```

4. Đóng và mở lại Antigravity.

Nếu báo `agy is not recognized`, máy chưa có Antigravity CLI: dùng cách 2.

### Cách 2 – chép tay

1. Mở [github.com/obra/superpowers](https://github.com/obra/superpowers) → nút **Code → Download ZIP** → giải nén.
2. Mở File Explorer, gõ vào thanh địa chỉ `%USERPROFILE%\.gemini\config` rồi Enter. Nếu chưa có thư mục `skills` thì tạo mới.
3. Chép các thư mục con trong `superpowers-main\skills\` (ví dụ `systematic-debugging`) vào `%USERPROFILE%\.gemini\config\skills\`. Có thể chỉ chép các skill ở mục 3.
4. Đóng và mở lại Antigravity.

### Kiểm tra hoạt động

- Trong khung tác tử (agent) của Antigravity, mở menu **Customizations** để xem danh sách skill đang bật.
- Thử: gõ `/systematic-debugging` hoặc hỏi "Mã Python này báo lỗi KeyError, giúp tôi tìm nguyên nhân". Gemini sẽ hỏi triệu chứng và tìm nguyên nhân gốc trước khi đề xuất sửa.

### Cập nhật và gỡ

- Cập nhật: chạy lại lệnh `agy plugin install` ở cách 1, hoặc chép lại thư mục ở cách 2.
- Gỡ: xoá thư mục superpowers trong `%USERPROFILE%\.gemini\config\plugins\` (cách 1) hoặc các thư mục skill đã chép (cách 2), rồi mở lại Antigravity.

## 5. Nguyên tắc an toàn

- Chỉ cài skill từ kho uy tín; đọc `SKILL.md` và thư mục `scripts/` trước khi cài.
- Không cài nguyên kho hàng nghìn skill lên máy cơ quan.
- Không đưa tài liệu nội bộ, hồ sơ cá nhân vào skill hoặc vào repository công khai này.
