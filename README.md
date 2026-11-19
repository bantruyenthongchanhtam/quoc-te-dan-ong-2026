# 🎬 19/11 – Hôm Nay Các Anh Là Nhân Vật Chính!

Phim hoạt hình ngắn chúc mừng **Ngày Quốc tế Nam giới 19/11**, tặng anh em
**Học Chúng Chánh Tâm – Tự viện Phước Duyên**: hài hước, ấm áp và đầy yêu thương.

## ▶ Xem phim

Trang đang được lưu trữ tại GitHub Pages:

> https://bantruyenthongchanhtam.github.io/quoc-te-dan-ong-2026/

## ✨ Nội dung

Một "tập phim" hoạt hình 7 cảnh với 4 nhân vật SVG tự dựng khớp:

- **Thầy Nhật Đạo** – người dẫn chuyện
- **Phóng viên Tbh** – đưa tin nóng về ngày 19/11
- **Minh Ý** – triết lý trà đạo (và… rửa chén)
- **Huy Lê (Cậu Út)** – nhảy ra từ bụi cây, hỏi quà 19/11

Kèm nhạc nền & hiệu ứng âm thanh **tổng hợp trực tiếp bằng Web Audio API**
(không cần file mp3); âm thanh được khởi động/khôi phục khi người dùng tương tác và khi quay lại tab,
hỗ trợ Safari trên iPhone. Ngoài ra còn có hộp thoại gõ chữ, camera zoom/pan, pháo giấy và nhiều hiệu ứng khác.

## 🛠 Kỹ thuật

- Toàn bộ nằm trong **một file `index.html`** (~125KB): HTML + CSS + JS, không build step.
- Nhân vật là SVG tách khớp (body/head/arms/legs), chuyển động bằng CSS keyframes;
  vị trí nhân vật dùng `transform: translate3d()` để chạy mượt trên compositor.
- Vòng thời gian của phim dùng `requestAnimationFrame` (tạm dừng, xem lại được).

## 🚀 Deploy lên GitHub Pages

1. Push nhánh `main` lên repo.
2. Vào **Settings → Pages → Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: **main** / thư mục **/(root)**
3. Đợi ~1 phút, mở link ở trên.

## 🎵 Đổi nhạc nền (tuỳ chọn)

Mỗi cảnh có một track trong `SCENE_BGM_PLAYLIST` (trong `index.html`).
Mặc định nhạc được tổng hợp bằng Web Audio; nếu muốn dùng file nhạc thật,
điền đường dẫn vào trường `audioUrl`, ví dụ:

```js
scene1: {
  name: 'Cảnh 1 - Chiều bình yên Phước Duyên',
  audioUrl: 'audio/scene1.mp3', // đặt file trong thư mục audio/
  ...
}
```

---

Chúc các anh em một ngày 19/11 thật vui, bình an và ý nghĩa! 🎉
