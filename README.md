# Thư viện Hyan

Thư viện token thiết kế cá nhân: mỗi màu, độ nhạt chữ, kiểu chữ, hiệu ứng, khung, icon, bố cục và quy tắc đều có **mã** riêng và **giá trị chính xác**.

- `index.html`: trang web xem trước trực quan, chọn token như đi shopping, cho vào giỏ rồi copy spec dán cho AI.
- `data/`: nguồn dữ liệu duy nhất (JSON). Sửa ở đây thì trang web tự cập nhật.

## Hệ thống mã (v0.2: danh mục key visual)

| Thư mục | Nhóm | Mã | File |
|---|---|---|---|
| Định hướng | Tông cảm xúc | MO01… | data/moods.json |
| | Phong cách thiết kế | S01… | data/styles.json |
| | Kiểu hình ảnh | H01… | data/imagery.json |
| Màu sắc | Bảng màu 5 màu | P01… | data/palettes.json |
| | Màu Hyan (nền, nhấn, mực) | N0–N3, B01–B04, M0 | data/colors.json |
| | Thang đậm nhạt 50–900 | V01… | data/scales.json |
| | Độ nhạt chữ | D1–D5 | data/text.json |
| Chữ | Font | F01… | data/fonts.json |
| | Cặp font | FP01… | data/pairings.json |
| | Cỡ chữ | Z01… | data/typescales.json |
| | Kiểu chữ Hyan | T01… | data/typography.json |
| Hình khối | Bo góc | G01… | data/radius.json |
| | Nút | BT01… | data/buttons.json |
| | Khung & viền | K01… | data/frames.json |
| | Icon | I01… | data/icons.json |
| Hiệu ứng & nền | Hiệu ứng | E01… | data/effects.json |
| | Nền & hoạ tiết | BG01… | data/backgrounds.json |
| Bố cục & khổ | Bố cục | L01… | data/layouts.json |
| | Khổ ảnh | A01… | data/formats.json |
| Quy tắc | Quy tắc | R01… | data/rules.json |

Thư mục và thứ tự nằm trong `data/library.json`. Bản dịch tiếng Anh nằm trong `data/i18n.en.json` (theo mã món); nút VIE/EN trên trang đổi cả giao diện lẫn nội dung brief. Mục có trường `ai` là từ khoá tiếng Anh để dán vào công cụ tạo ảnh AI. Mục có trường `html` là hình minh hoạ dựng sẵn bằng HTML/CSS.

## Thêm token mới

Thêm một mục vào `items` của file tương ứng, ví dụ:

```json
{ "id": "E07", "code": "E07", "name": "Viền phát sáng", "value": "1px B01 50%", "css": "border: 1px solid rgba(61,156,240,.5)" }
```

## Cho AI đọc

Gửi kèm link file thô trên GitHub (raw) của thư mục `data/`, AI đọc JSON trực tiếp được. Trang web dùng để người xem và chọn.

## Link

- Trang xem trước (công khai): https://thudonggg25.github.io/designshop/
- Bản riêng trên Claude: https://claude.ai/artifact/GNUUQZMREDGpbmFQ9D929g
- Dữ liệu JSON: https://github.com/thudonggg25/designshop/tree/main/data
- File thô cho AI: https://raw.githubusercontent.com/thudonggg25/designshop/main/data/library.json (liệt kê các file còn lại)
