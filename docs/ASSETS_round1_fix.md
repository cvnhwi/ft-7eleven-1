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

## Video draft round 1

- Model: Seedance 2.5, `omni_reference`, 30s, draft 480p, 16:9, audio on. Chi phí: 90 credits.
- Job ID: `7ba08f64-dcf7-4426-b620-48b6f16fe905`
- Refs theo thứ tự: image 1–7 = ảnh chốt #1–#7 ở bảng trên; `end_image` = #8 (end card, khóa frame cuối).
- Prompt: dựa trên `docs/PROMPT_tet-30s-v2.md`, thêm khóa branding + mô tả 4 nhân vật; ly đổi sang thủy tinh, SFX "glass clinks with ice".
- Finalize 1080p: gọi lại Seedance 2.5 với `draft_job_id` = job ID ở trên (trong vòng 7 ngày).

## Update: cảnh phố ít xe, đi đúng chiều

Lưu ý: các job ảnh pass 1–2 ở trên không còn trên Higgsfield ("Generation not found"); video draft `7ba08f64…` vẫn còn.

- Ảnh toàn cảnh mới (làm lại từ `refs/r1/frame_s3.png` + logo + ref mặt tiền, một lượt gồm branding, xe và relight):
  - **Chốt A** `4b549a71-b52e-4723-8e5f-0f207ebcbe71`: khoảng 8 xe; xe tới gần máy ở nửa trái, xe đi xa ở nửa phải (giữ bên phải).
  - B `4fa1ace1-c549-4c7c-bd92-2a26e83ed7af`: khoảng 5 xe; có 1 xe giữa-phải đi ngược chiều → loại.
- Clip riêng cảnh phố: Seedance 2.5, 5s, draft 480p, start_image = A. Job `b4cd7f4c-c447-4e49-9cb0-2a41e60db461`.
- Sheet nhân vật: `refs/chars/{linh,mai,bao,khang}.png`.

## Update: Linh đi vào cửa hàng (đúng location của clip phố)

- Lưu ý: ảnh gen trên Higgsfield bị mất sau một thời gian (job "not found"), video thì còn. Từ giờ ảnh chốt được lưu lại thành media upload cố định.
- Mốc vị trí: frame cuối clip phố `b4cd7f4c…` → media `dfd0c2db-3eaa-48fa-9631-f4ff57b4bdb8`.
- Ảnh trung cận (Seedream, refs: frame cuối + sheet Linh + logo):
  - **Chốt** `2d767577-d203-4b03-9e13-2c1d762b0e8b` → media cố định `2ceee65a-ad6e-45c2-b822-bb4fb6a29a25`.
  - `e1589aa4…`: bị nhân đôi Linh → loại.
- Clip Linh vào cửa: Seedance 2.5, 5s draft 480p, start_image = `2ceee65a…`, ref = sheet Linh. Job `a6ed73f8-c3a5-4246-b830-5e069e31637a`.

## Update: Linh vào cửa (logo chính giữa trên đầu nhân vật)

- Ảnh đầu: media `54b7d77c-7986-424f-ad7b-5c62d2761ef3`. Ảnh cuối: media `f3462198-61d5-411e-9408-ba704a818453` (logo ghép bằng file vector chính thức, vì Seedream render sai chữ "7-LEVEN").
- Clip (start + end frame, 5s draft): [mp4](https://d8j0ntlcm91z4.cloudfront.net/user_3IOz7tFscQRUWCyOIu2UK9CE8RJ/hf_20261006_161146_982a52bd-6fcc-4668-9d9d-1234c1de2b74.mp4). Job `982a52bd…`

## Round 2 feedback (khách)

| Feedback | Xử lý | Ảnh chốt (media cố định) | Clip draft |
|---|---|---|---|
| Lò vi sóng bớt khói | Chỉ còn vài sợi khói mảnh | `867c0242-b587-4cc1-bfd6-22947af1870f` | [mp4](https://d8j0ntlcm91z4.cloudfront.net/user_3IOz7tFscQRUWCyOIu2UK9CE8RJ/hf_20261006_162620_48565027-02f4-4df3-9b72-15001b20a30d.mp4) |
| Hẻm ẩm thực: line dưới thành trắng | Biển dưới nền trắng + logo; stripes chỉ ở dải trên | `0cb22f40-d329-40de-b28a-b96261f35f98` | [mp4](https://d8j0ntlcm91z4.cloudfront.net/user_3IOz7tFscQRUWCyOIu2UK9CE8RJ/hf_20261006_162619_65b534c7-7fe8-478f-a745-d21fa02e6c12.mp4) |
| Đổi sang bánh chưng, đồng bộ món ăn | Bánh chưng vuông lá dong, lạt tre; mặt cắt gạo xanh/đậu xanh/thịt → **mẫu chuẩn cho mọi shot** | `50832884-0467-4eb4-946e-fef4a3da8dcb` | [mp4](https://d8j0ntlcm91z4.cloudfront.net/user_3IOz7tFscQRUWCyOIu2UK9CE8RJ/hf_20261006_162619_ba038bd4-77a4-4e31-9e6d-3c86d1016c67.mp4) |
| (đồng bộ) Bàn ăn top-down | Dùng đúng mẫu bánh chưng + tô xôi gấc ở trên | `be3e95ac-8990-40e6-a146-2ea706b58189` | [mp4](https://d8j0ntlcm91z4.cloudfront.net/user_3IOz7tFscQRUWCyOIu2UK9CE8RJ/hf_20261006_163423_86552827-71b7-446e-97f6-3c7946438970.mp4) |
| Nhóm bạn cùng quẩy; quẩy ngoài cửa kính; sửa Khang | Góc trong nhà nhìn ra quầy cửa kính, 4 bạn quẩy ngoài kính, Khang đúng sheet | `2599b138-4696-4c10-a361-6333eaf7adc6` | job `ba5a0145-b221-40ac-a978-0ae10473f302` |

Loại: quẩy trong nhà (`4d1ee8ca` + clip `ef9c9401`), quẩy trên vỉa hè (`925e5514`, `772df696`, clip `8a150f8a`). Khách chốt góc trong nhà nhìn ra kính.

## Fix: Hẻm ẩm thực, line dưới thành trắng (bản sửa lỗi)

- Lỗi bản trước (`0cb22f40`): stripes là lớp phẳng dán ngang mép trên khung, không nằm trong cảnh → loại (clip `65b534c7` cũng loại).
- Bản chốt: media `0cdba3d3-fff3-4e6f-b86a-be5969d7b43b`. Stripes brand nằm trên dải trần thật, có phối cảnh; biển dưới nền trắng, chỉ có logo. (Bản B `c47fc13f`: logo nhỏ và mờ → loại.)
- Clip 4s draft: job `64dc204d-6602-4f9f-860a-90b5d034bb8e`. Máy push-in nhẹ để biển và logo luôn nằm trong khung.

## Fix: Nhóm bạn quẩy, giữ nguyên location gốc, quẩy ngoài cửa kính

- Base: frame gốc `refs/r1/frame_s9.png` (giữ nguyên cửa sổ, quầy, ghế cam, tủ cam; chỉ đổi biển cam → stripes + logo theo feedback vòng 1).
- Chốt: media `c76556fc-dd47-4d87-9a46-512969b012db` (4 bạn ngoài kính). Bản A `ae0e48f7`: nhóm bạn đứng trong nhà → loại.
- Clip 5s draft: job `68a62529-8bd3-468c-88cc-920e81d20c61`. Các bản trước (`2599b138` + `ba5a0145`) đổi location → loại.
