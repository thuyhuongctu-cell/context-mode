# Ngân hàng câu hỏi Khởi nghiệp – Web app cho sinh viên

Web app trắc nghiệm tĩnh, chạy 100% trong trình duyệt. Một file `index.html` duy nhất, nhúng sẵn 235 câu hỏi và đáp án của 3 chương.

## Tính năng

- 235 câu trắc nghiệm:
  - Chương 1: 90 câu (Tổng quan khởi nghiệp)
  - Chương 2: 115 câu (Ý tưởng & cơ hội)
  - Chương 3: 30 câu (Kế hoạch khởi nghiệp)
- 2 chế độ:
  - **Phản hồi tức thì** (mặc định): hiện đúng/sai ngay sau khi chọn.
  - **Kiểm tra**: bỏ tick "Phản hồi tức thì" → bấm "Nộp bài" mới hiện điểm.
- Tuỳ chọn **xáo trộn câu hỏi** và **xáo trộn đáp án**.
- Bảng điều hướng câu (chấm xanh/đỏ trực quan).
- Tự động **lưu tiến trình** trong trình duyệt (localStorage).
- Phím tắt: `←` `→` chuyển câu, `A` `B` `C` `D` hoặc `1` `2` `3` `4` chọn đáp án.
- Giao diện tối, responsive (chạy tốt trên điện thoại).

## Cách chia sẻ cho sinh viên

Đây là static site → có rất nhiều cách deploy miễn phí:

### 1. GitHub Pages (đơn giản nhất, dùng repo này)

1. Vào **Settings → Pages** của repo.
2. Chọn **Source: Deploy from a branch**, **Branch: `main`** (sau khi merge PR), **Folder: `/ (root)`**.
3. Sau 1–2 phút, link sẽ là:
   `https://<user>.github.io/<repo>/quiz/`
4. Gửi link đó cho sinh viên.

### 2. Tải file rồi mở trực tiếp

Tải `index.html` về máy → mở bằng trình duyệt. Không cần internet (đáp án nhúng sẵn).

### 3. Bất kỳ static host nào

Vercel, Netlify, Cloudflare Pages, Surge, Firebase Hosting… kéo thả thư mục `quiz/` là chạy.

## Tuỳ biến nội dung

Toàn bộ câu hỏi nằm trong thẻ `<script id="quiz-data">` trong `index.html`. Sửa JSON ở đó để thêm/sửa câu.
