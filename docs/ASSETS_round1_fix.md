# Round 1 fix: asset sau feedback (Seedream 5.0 Pro, 2K 16:9)

Ảnh gốc 2K lưu trên Higgsfield (link CloudFront bên dưới, mở trực tiếp để tải). Ảnh tham chiếu đầu vào nằm ở `refs/r1/`.
Quy trình: sửa trực tiếp frame của video 1006-1 → relight pass (khớp hướng nắng, nhiệt màu, DOF, grain; giảm độ rực stripes).

## Bộ ảnh chốt (dùng cho video)

| # | Shot | Job ID (chốt) | Link 2K |
|---|---|---|---|
| 1 | Toàn cảnh phố + store (0–2.5s) | `bf6f5953-a658-4b5f-82a7-c6982dc4ec62` | [png](https://d8j0ntlcm91z4.cloudfront.net/user_3IOz7tFscQRUWCyOIu2UK9CE8RJ/hf_20261006_135921_bf6f5953-a658-4b5f-82a7-c6982dc4ec62.png) |
| 2 | Trung cận mặt tiền, Linh vào cửa (2.5–5s) | `e9eaa967-e3ab-46d2-97fd-b2607a62ccd5` | [png](https://d8j0ntlcm91z4.cloudfront.net/user_3IOz7tFscQRUWCyOIu2UK9CE8RJ/hf_20261006_135922_e9eaa967-e3ab-46d2-97fd-b2607a62ccd5.png) |
| 3 | Lối đi, header 3 stripes + logo (5–10s) | `be9cd0c2-02ab-433f-9ecd-22fc9e332d2f` | [png](https://d8j0ntlcm91z4.cloudfront.net/user_3IOz7tFscQRUWCyOIu2UK9CE8RJ/hf_20261006_140339_be9cd0c2-02ab-433f-9ecd-22fc9e332d2f.png) |
| 4 | Hẻm ẩm thực, signboard logo (10–12s) | `5de7e668-dde5-4b3f-ae7b-1b559fc3fabf` | [png](https://d8j0ntlcm91z4.cloudfront.net/user_3IOz7tFscQRUWCyOIu2UK9CE8RJ/hf_20261006_135919_5de7e668-dde5-4b3f-ae7b-1b559fc3fabf.png) |
| 5 | Lò vi sóng + tô xôi gấc (12–15.5s) | `73d6b8b3-8996-4412-8b88-16e3c84eb742` | [png](https://d8j0ntlcm91z4.cloudfront.net/user_3IOz7tFscQRUWCyOIu2UK9CE8RJ/hf_20261006_134946_73d6b8b3-8996-4412-8b88-16e3c84eb742.png) |
| 6 | Quầy cửa sổ, fascia 3 stripes + logo (18–20s) | `fb1fb05d-dd8d-4c14-9ff7-38819651154a` | [png](https://d8j0ntlcm91z4.cloudfront.net/user_3IOz7tFscQRUWCyOIu2UK9CE8RJ/hf_20261006_135920_fb1fb05d-dd8d-4c14-9ff7-38819651154a.png) |
| 7 | Ly thủy tinh có logo, cụng ly (22–24s) | `c5558e1c-a195-4da9-8915-ae754cd269eb` (tay áo theo 4 nhân vật) / fallback `c27bab45-3f05-42bb-8867-396bdb2c0a2e` | Higgsfield |
| 8 | End card logo + tagline (26–30s) | `e39869f7-a35f-4af2-8e2c-603635617135` | [png](https://d8j0ntlcm91z4.cloudfront.net/user_3IOz7tFscQRUWCyOIu2UK9CE8RJ/hf_20261006_135920_e39869f7-a35f-4af2-8e2c-603635617135.png) |

## Loại bỏ
- Ly nhựa (`1ea99c71…`, `b5fae046…`): logo bị lặp/vỡ → không dùng.
- Aisle relight `b3fc6ecd…`: model trả lại khối màu cũ → không dùng.
- Pass 1 (chưa relight, logo nổi như dán): `5e4f8786…`, `a9f8fc5e…`, `54d9c303…`, `44a5f015…`, `14a5b452…`, `de64e87a…`, `e29daa23…`.

## Nhân vật
Linh (chính): áo dài trắng viền đỏ thêu mai vàng, kẹp hoa vàng, túi xanh lá. Mai: tóc bob nâu mái bằng, kẹp đỏ, áo len xanh lá + cardigan trắng, chân váy jean xếp ly, giày Mary Jane đỏ.
Bảo: dáng đầy đặn, tóc xoăn, mũ bucket kem, polo đỏ viền trắng, quần short jean, hộp quà đỏ-vàng. Khang: undercut, sơ mi cam họa tiết cá koi trắng, áo thun trắng, quần kaki be, đồng hồ bạc.
Sheet nhân vật chưa có trên Higgsfield; draft video dùng mô tả text cho Mai/Bảo/Khang.
