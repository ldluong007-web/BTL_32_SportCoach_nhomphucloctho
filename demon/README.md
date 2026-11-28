# 🏅 SportCoach — Hệ thống Giáo dục Thể chất

> **Môn học:** CSE122 — Bài tập lớn  
> **Nhóm:** Nhóm Phúc Lộc Thọ (BTL 32) · 3 thành viên  
> **Lĩnh vực:** Giáo dục phổ thông / Giảng dạy và học tập Giáo dục thể chất

---

## 📖 Giới thiệu

**SportCoach** là hệ thống hỗ trợ giảng dạy và học tập môn Giáo dục thể chất dành cho trường phổ thông.  
Sản phẩm giải quyết các vấn đề thực tế:

| Vấn đề | Giải pháp SportCoach |
|--------|----------------------|
| Học sinh không có kênh ôn lại động tác giữa các buổi | Thư viện video động tác với player tốc độ tùy chỉnh |
| Giáo án, video rải rác, khó quản lý | Hệ thống giáo án theo tuần tích hợp video |
| Chấm điểm kỹ thuật thiếu khách quan | Rubric 4 tiêu chí, lưu điểm và phản hồi |
| Học sinh khó theo dõi tiến bộ thể lực | Nhật ký luyện tập + biểu đồ tiến độ Canvas |

---

## 👥 Vai trò trong hệ thống

| Vai trò | Trách nhiệm chính |
|---------|------------------|
| 🧑‍💼 **Khách** | Xem giới thiệu môn thể chất và video động tác công khai |
| 🎓 **Học sinh** | Học giáo án, ôn video, ghi nhật ký, theo dõi thể lực |
| 🧑‍🏫 **Giáo viên** | Soạn giáo án, quản lý video, chấm điểm kỹ thuật, tổ chức thi đấu |
| 🛡️ **Quản trị viên** | Quản lý tài khoản, khối/lớp, môn thể thao, cấu hình hệ thống |

---

## 🗂️ Danh sách giao diện

### Giao diện dùng chung

| Tệp | Giao diện | Mô tả |
|-----|-----------|-------|
| `index.html` | Landing Page | Trang chủ giới thiệu hệ thống |
| `login.html` | Đăng nhập | Đăng nhập theo vai trò |
| `register.html` | Đăng ký | Tạo tài khoản mới |
| `forgot-password.html` | Quên mật khẩu | Khôi phục tài khoản |
| `profile.html` | Hồ sơ | Thông tin cá nhân |
| `settings.html` | Cài đặt | Tuỳ chỉnh tài khoản |
| `notifications.html` | Thông báo | Danh sách thông báo |
| `403.html` | Lỗi 403 | Không có quyền truy cập |
| `404.html` | Lỗi 404 | Trang không tồn tại |

### Vai trò Khách (SV1)

| Tệp | Giao diện | CRUD | Chức năng |
|-----|-----------|------|-----------|
| `visitor-sport-overview.html` | Sport Overview | R | Xem giới thiệu các môn thể chất |
| `visitor-clip-preview.html` | Clip Preview | R | Xem thử video động tác công khai |
| `visitor-sport-feedback.html` | Sport Feedback | C/R | Góp ý môn thể thao hoặc bài tập |

### Vai trò Học sinh (SV1)

| Tệp | Giao diện | CRUD | Chức năng |
|-----|-----------|------|-----------|
| `student-dashboard.html` | Dashboard | R | Tiến độ thể lực, lịch tập, thông báo |
| `student-lesson-view.html` | Lesson View | R | Xem giáo án, video động tác, sơ đồ sân |
| `student-training-log.html` | Training Log | C/R/U | Ghi nhật ký luyện tập, bấm giờ |
| `student-progress.html` | Progress | R | Biểu đồ tiến bộ thể lực bằng Canvas |

### Vai trò Giáo viên (SV2)

| Tệp | Giao diện | CRUD | Chức năng |
|-----|-----------|------|-----------|
| `teacher-dashboard.html` | Dashboard | R | Tổng quan lớp, giáo án, mức độ tập |
| `teacher-lesson-plan.html` | Lesson Plan | C/R/U/D | Soạn giáo án tuần, gắn video, sơ đồ |
| `teacher-move-video.html` | Move Video | C/R/U/D | Quản lý video động tác theo môn |
| `teacher-skill-grading.html` | Skill Grading | R/U | Chấm điểm kỹ thuật, nhận xét |
| `teacher-tournament.html` | Tournament | C/R/U | Tổ chức thi đấu, bảng thành tích |

### Vai trò Quản trị viên (SV3)

| Tệp | Giao diện | CRUD | Chức năng |
|-----|-----------|------|-----------|
| `admin-dashboard.html` | Dashboard | R | Tổng quan hệ thống |
| `admin-user-management.html` | User Management | C/R/U/D | Quản lý tài khoản và khối/lớp |
| `admin-sport-config.html` | Sport Config | R/U | Cấu hình môn thể thao, tiết học |

---

## 🗃️ Cấu trúc thư mục

```
cse122-sportcoach-nhomphucloctho/
│
├── README.md                        ← Tài liệu dự án (file này)
│
├── demon/                           ← Prototype SPA tích hợp (tham khảo)
│   ├── sportcoach.html              ← Demo đầy đủ luồng nghiệp vụ
│   └── README.md                    ← Tài liệu mô tả prototype
│
├── docs/                            ← Tài liệu dự án
│   ├── project-proposal/            ← Đề cương
│   ├── screen-list/                 ← Bảng kiểm kê màn hình
│   ├── team-assignment/             ← Phân công nhóm
│   └── ai-usage-report.md           ← Khai báo sử dụng AI
│
├── design/                          ← Thiết kế
│   ├── figma-link.txt               ← Link Figma/Canva
│   └── mockups/                     ← Ảnh mockup
│
├── pages/                           ← Các tệp HTML theo đề cương
│   ├── index.html
│   ├── login.html
│   ├── register.html
│   ├── forgot-password.html
│   ├── profile.html
│   ├── settings.html
│   ├── notifications.html
│   ├── 403.html
│   ├── 404.html
│   ├── visitor-sport-overview.html
│   ├── visitor-clip-preview.html
│   ├── visitor-sport-feedback.html
│   ├── student-dashboard.html
│   ├── student-lesson-view.html
│   ├── student-training-log.html
│   ├── student-progress.html
│   ├── teacher-dashboard.html
│   ├── teacher-lesson-plan.html
│   ├── teacher-move-video.html
│   ├── teacher-skill-grading.html
│   ├── teacher-tournament.html
│   ├── admin-dashboard.html
│   ├── admin-user-management.html
│   └── admin-sport-config.html
│
├── assets/
│   ├── images/
│   ├── icons/
│   ├── videos/
│   └── data/
│
├── css/
│   ├── style.css                    ← CSS dùng chung
│   └── responsive.css               ← Responsive breakpoints
│
├── js/
│   ├── main.js                      ← Điều hướng & khởi động
│   ├── api.js                       ← Mock API / LocalStorage
│   └── modules/                     ← Các module JS riêng
│
└── db.json                          ← Dữ liệu giả lập (Mock API)
```

---

## 🚀 Hướng dẫn chạy

### Yêu cầu

- Trình duyệt hiện đại (Chrome, Firefox, Edge)
- Không cần cài đặt thêm — toàn bộ là frontend thuần

### Chạy prototype nhanh

```bash
# Mở file demo trực tiếp trong trình duyệt
open demon/sportcoach.html
```

> **Lưu ý:** File `demon/sportcoach.html` là SPA tích hợp dùng để tham khảo và kiểm tra luồng nghiệp vụ. Sản phẩm chính sẽ được tách thành các file riêng trong thư mục `pages/`.

### Chạy với JSON Server (khi có `db.json`)

```bash
# Cài JSON Server
npm install -g json-server

# Chạy Mock API tại cổng 3000
json-server --watch db.json --port 3000

# Mở trang trong trình duyệt
open pages/index.html
```

---

## 🎨 Hệ thống thiết kế (Design System)

### Font chữ

| Mục đích | Font |
|---------|------|
| Nội dung chính | [Be Vietnam Pro](https://fonts.google.com/specimen/Be+Vietnam+Pro) |
| Tiêu đề / Số liệu | [Bungee](https://fonts.google.com/specimen/Bungee) |

### Bảng màu chính

| Tên biến | Mã màu | Dùng cho |
|----------|--------|---------|
| `--green` | `#0e7a3d` | Màu chủ đạo, nút chính |
| `--lime` | `#a3e635` | Nhấn, highlight |
| `--pine` | `#0c2b18` | Sidebar, nền tối |
| `--orange` | `#f4632e` | Nút phụ, cảnh báo |
| `--blue` | `#1d6fe0` | Học sinh, thông tin |
| `--ok` | `#16a34a` | Thành công |
| `--warn` | `#f59e0b` | Cảnh báo, bản nháp |
| `--danger` | `#e11d48` | Lỗi, xoá |

### Responsive Breakpoints

| Màn hình | Kích thước | Thay đổi layout |
|----------|-----------|----------------|
| Desktop | > 1080px | Layout 2 cột đầy đủ |
| Tablet | 921px – 1080px | Layout 1 cột |
| Mobile | ≤ 920px | Sidebar ẩn, hamburger menu |

---

## 📊 Cách truyền đạt kiến thức (≥ 3 cách — bắt buộc)

| # | Cách | Màn hình | Tính năng |
|---|------|----------|-----------|
| 1 | 🎬 **Video động tác từng bước** | `student-lesson-view.html` | Player: dừng, tua, điều chỉnh tốc độ, đếm rep |
| 2 | 🏟️ **Sơ đồ sân tập SVG tương tác** | `student-lesson-view.html`, `teacher-lesson-plan.html` | SVG vị trí đứng, đường chạy, khu vực kỹ thuật, tooltip |
| 3 | 📈 **Biểu đồ tiến độ Canvas** | `student-progress.html` | Line chart, Bar chart, Radar chart theo tuần |
| 4 | ⏱️ **Đồng hồ tập + Nhật ký** | `student-training-log.html` | Bấm giờ, nhập số liệu, validation, phản hồi nhanh |
| 5 | 🃏 **Flashcard trắc nghiệm kỹ thuật** | `student-lesson-view.html` | Thẻ lật, câu đố ngắn về biên độ và nhịp độ |

---

## 🗄️ Dữ liệu giả lập (`db.json`)

| Entity | Mô tả | Số bản ghi mẫu |
|--------|-------|---------------|
| `users` | Tài khoản giáo viên, học sinh, admin | ≥ 5 |
| `sports` | Điền kinh, bóng đá, bơi, thể dục nhịp điệu | 4 |
| `lessonPlans` | Giáo án theo tuần/lớp | ≥ 5 |
| `moves` | Video và mô tả kỹ thuật động tác | ≥ 12 |
| `trainingLogs` | Nhật ký luyện tập theo buổi | ≥ 10 |
| `skillScores` | Điểm kỹ thuật và nhận xét | ≥ 5 |
| `tournaments` | Thi đấu và bảng xếp hạng | ≥ 2 |

> Dữ liệu có thể dùng với **JSON Server**, **MockAPI** hoặc **LocalStorage**.

---

## 👨‍💻 Phân công nhóm

### SV1 — Khách & Học sinh

- **Phụ trách:** Toàn bộ giao diện vai trò Khách và Học sinh.
- **Trách nhiệm chéo:** Giao diện dùng chung, responsive toàn dự án.
- **Màn hình:** `visitor-*.html`, `student-*.html`, `index.html`, `login.html`, `register.html`, trang lỗi.

### SV2 — Giáo viên

- **Phụ trách:** Toàn bộ giao diện vai trò Giáo viên.
- **Trách nhiệm chéo:** JavaScript tương tác, dữ liệu `db.json`, Mock API, review PR.
- **Màn hình:** `teacher-*.html`.

### SV3 — Quản trị viên & Tích hợp

- **Phụ trách:** Toàn bộ giao diện vai trò Quản trị viên.
- **Trách nhiệm chéo:** Tích hợp bố cục, điều hướng, CSS dùng chung, thống nhất design system, phát hành.
- **Màn hình:** `admin-*.html`, `profile.html`, `settings.html`, `notifications.html`.

### Trách nhiệm chéo bắt buộc (cả 3 SV)

- [ ] Hệ thống thiết kế nhất quán (màu, font, component)
- [ ] Điều hướng xuyên suốt giữa các trang
- [ ] Khả năng tiếp cận cơ bản (`aria-label`, HTML ngữ nghĩa)
- [ ] JavaScript và tương tác có ý nghĩa
- [ ] Responsive đa thiết bị
- [ ] Phát hành và đảm bảo chất lượng

---

## 🔄 Quy trình làm việc Git/GitHub

### Nhánh

```
main     ← Sản phẩm ổn định, chỉ merge khi đã kiểm thử
dev      ← Tích hợp nhóm
feature/ ← Phát triển tính năng (mỗi màn hình 1 nhánh)
```

### Quy trình

```
Task → Tạo nhánh feature/... → Code → Commit → Push
     → Pull Request → Review → Merge dev
     → Kiểm thử → Merge main
```

### Quy tắc commit (Conventional Commit)

| Tiền tố | Dùng khi |
|---------|---------|
| `feat:` | Thêm tính năng mới |
| `fix:` | Sửa lỗi |
| `style:` | Chỉnh giao diện, CSS |
| `refactor:` | Tái cấu trúc mã |
| `docs:` | Cập nhật tài liệu |

> ❌ **Không dùng:** `update`, `done`, `final`, `fix code` hoặc spam commit.

---

## 🎥 Video OBS giảng giải

Mỗi màn hình cần **ít nhất 1 video OBS** theo định dạng tên:

```
SV1-01-student-dashboard.mp4
SV2-01-teacher-lesson-plan.mp4
SV3-01-admin-user-management.mp4
```

**Nội dung bắt buộc trong video:**
- Có khuôn mặt và giọng giải thích
- Mở mockup Figma/Canva và giải thích thiết kế
- Mở đúng file HTML/CSS/JavaScript và giải thích logic
- Thực hiện thay đổi nhỏ tại chỗ, chạy lại và commit lên GitHub
- Nêu rõ task, nhánh và commit

---

## ✅ Checklist hoàn thành một màn hình

Một màn hình được tính **hoàn thành** khi đủ tất cả:

- [ ] Bản mô phỏng Figma/Canva
- [ ] HTML ngữ nghĩa (đúng tên file theo đề cương)
- [ ] CSS hoàn chỉnh và responsive
- [ ] Tương tác JavaScript có ý nghĩa (video, canvas, timer, form)
- [ ] Kiểm tra hợp lệ biểu mẫu (validation)
- [ ] Dữ liệu Mock API / `db.json`
- [ ] Trạng thái: rỗng · đang tải · lỗi · thành công
- [ ] Khả năng tiếp cận cơ bản
- [ ] Pull Request đã được review và merge vào `dev`
- [ ] Video OBS giảng giải (tên đúng quy tắc)
- [ ] Chứng minh thao tác làm lại được
- [ ] README / bảng kiểm kê đã cập nhật

---

## 📐 Thang điểm

| Tiêu chí | Tỷ lệ |
|----------|------:|
| Đầy đủ nghiệp vụ và chất lượng frontend | 30% |
| Cách truyền đạt kiến thức trực quan | 25% |
| Video OBS và khả năng làm lại khi bảo vệ | 30% |
| Git/GitHub, Trello/Notion và AI usage disclosure | 15% |

---

## 🤖 Khai báo công cụ AI

Mọi sử dụng AI cần được ghi vào `docs/ai-usage-report.md` bao gồm:
- Công cụ đã dùng (ChatGPT, Claude, Gemini, Copilot,…)
- Prompt chính
- Phần do AI tạo ra — phần sinh viên tự chỉnh sửa
- Lỗi gặp phải và cách kiểm chứng
- Điều đã học được
- Tính năng mock hay tính năng thật

---

*Cập nhật lần cuối: 28/11/2026 · Nhóm Phúc Lộc Thọ — BTL 32 · Môn CSE122*
