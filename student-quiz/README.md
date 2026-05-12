# Ngân hàng câu hỏi ôn tập - Khởi nghiệp (Web app sinh viên)

Static web app (HTML/JS thuần) cho sinh viên ôn tập trắc nghiệm 3 chương:

- Chương 1: 90 câu
- Chương 2: 115 câu
- Chương 3: 30 câu
- **Tổng: 235 câu**

## Cấu trúc

- `index.html` — toàn bộ giao diện + logic (1 file, không build).
- `questions.json` — dữ liệu câu hỏi và đáp án đúng.

## Tính năng

- Chọn 1 trong 3 chương → làm trắc nghiệm.
- Tự lưu tiến độ trên trình duyệt (localStorage), có thể đóng tab và quay lại.
- Đánh dấu cờ 🚩 câu nghi ngờ, pager nhảy nhanh đến từng câu.
- Nộp bài → chấm điểm trên 10, xem riêng câu sai hoặc xem toàn bộ đáp án.
- Mobile-friendly.

## Truy cập (sau khi bật GitHub Pages)

Sau khi PR được merge vào `main` và bật Pages cho repo (Settings → Pages → Source: `main`, folder `/`):

```
https://<owner>.github.io/<repo>/student-quiz/
```

Ví dụ cụ thể của repo này:

```
https://thuyhuongctu-cell.github.io/context-mode/student-quiz/
```

## Chạy local

```
cd student-quiz
python3 -m http.server 8000
# mở http://localhost:8000
```

(Phải qua HTTP server vì trang fetch `questions.json`; mở trực tiếp bằng `file://` sẽ không tải được dữ liệu.)

## Cập nhật câu hỏi

Sửa `questions.json` (giữ đúng cấu trúc):

```json
{
  "ch1": [
    { "q": "Câu hỏi?", "options": { "A":"...", "B":"...", "C":"...", "D":"..." }, "answer": "C" }
  ],
  "ch2": [ ... ],
  "ch3": [ ... ]
}
```
