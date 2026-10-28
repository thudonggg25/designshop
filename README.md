# Thư viện Hyan

Thư viện token thiết kế cá nhân: mỗi màu, độ nhạt chữ, kiểu chữ, hiệu ứng, khung, icon, bố cục và quy tắc đều có **mã** riêng và **giá trị chính xác**.

- `index.html`: trang web xem trước trực quan, chọn token như đi shopping, cho vào giỏ rồi copy spec dán cho AI.
- `data/`: nguồn dữ liệu duy nhất (JSON). Sửa ở đây thì trang web tự cập nhật.

## Hệ thống mã

| Tiền tố | Nhóm | File |
|---|---|---|
| N0–N3 | Màu nền (Đêm / Ngày) | data/colors.json |
| B01–B04 | Màu nhấn | data/colors.json |
| M0 | Mực (chữ trên khối sáng) | data/colors.json |
| D1–D5 | Độ nhạt chữ | data/text.json |
| T01… | Kiểu chữ | data/typography.json |
| E01… | Hiệu ứng | data/effects.json |
| K01… | Khung | data/frames.json |
| I01… | Icon | data/icons.json |
| L01… | Bố cục | data/layouts.json |
| R01… | Quy tắc dùng | data/rules.json |

## Thêm token mới

Thêm một mục vào `items` của file tương ứng, ví dụ:

```json
{ "id": "E07", "code": "E07", "name": "Viền phát sáng", "value": "1px B01 50%", "css": "border: 1px solid rgba(61,156,240,.5)" }
```

## Cho AI đọc

Gửi kèm link file thô trên GitHub (raw) của thư mục `data/`, AI đọc JSON trực tiếp được. Trang web dùng để người xem và chọn.

## Link

- Trang xem trước (riêng tư, chủ sở hữu mở được): https://claude.ai/artifact/GNUUQZMREDGpbmFQ9D929g
- Dữ liệu JSON: https://github.com/thudonggg25/designshop/tree/main/data
- File thô cho AI: https://raw.githubusercontent.com/thudonggg25/designshop/main/data/library.json (liệt kê các file còn lại)
