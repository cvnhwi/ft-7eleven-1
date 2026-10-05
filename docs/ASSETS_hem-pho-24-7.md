# 7-Eleven — "Hẻm Phố Thu Nhỏ Trong Trạm Dừng 24/7" · Asset Pack v1

Model: **Seedream 5.0 Pro** (Higgsfield) · 1.5K (2048×1152) · 16:9 · 19 asset

## Style Bible (khóa tone màu toàn dự án)

| Vai trò | Màu | Hex |
|---|---|---|
| Neon brand – cam | 7-Eleven Orange | `#F4811F` |
| Neon brand – xanh | 7-Eleven Green | `#008163` |
| Neon brand – đỏ | 7-Eleven Red | `#EE2526` |
| Lễ hội – đèn lồng | Crimson | `#C8102E` |
| Lễ hội – kim tuyến | Gold | `#E8B04A` |
| Bóng đêm | Deep teal-blue | `#0E2A33` |
| Key light | Tungsten amber 2700K | — |

- **Grade:** teal-and-amber, Kodak Vision3 500T (grain mịn + halation quanh nguồn sáng), 35mm anamorphic, haze nhẹ, bề mặt ướt phản chiếu.
- **Mood reference:** đêm neon kiểu điện ảnh Hồng Kông thập niên 90 × phố lồng đèn Lương Nhữ Học (Chợ Lớn, Q.5) — vừa tạnh mưa.
- **Sheet (CH/Prop):** nền seamless xám ấm, key ấm 3200K trước-trái + rim teal phía sau → cùng hệ sáng với BG.
- **Consistency chain:** BG03 gen từ BG02 (giữ bố cục cho shot biến hình); BG04, BG05 lấy BG01 làm ref tone.
- **Logo/chữ:** không gen bằng AI — biển hiệu chừa trống, composite logo thật ở hậu kỳ.

## Background (plate trống, góc 3/4 toàn cảnh)

| ID | Nội dung | Shot | Job ID |
|---|---|---|---|
| BG01 | Mặt tiền cửa hàng, phố Chợ Lớn sau mưa, đèn lồng | 1 | `59070e4a-82f5-4925-bd49-b5b16b3fdd17` |
| BG02 | Lối đi trong cửa hàng (trạng thái A) | 2 | `75223818-a10d-44d9-95ca-a8041e517a01` |
| BG03 | Lối đi đã biến thành hẻm ẩm thực (trạng thái B, ref BG02) | 2 | `3bb5a6ac-d029-42fe-85e4-7832b8971341` |
| BG04 | Góc quầy đồ nóng + lò vi sóng | 3 | `4dd5f7c1-5fb5-4f94-b618-aa4b8fc10d6b` |
| BG05 | Quầy bên cửa kính, pháo hoa xa | 4 | `e5e78c1a-4c07-4258-9199-b609f6c57dad` |

## Character sheet (front / 3/4 / back + chest-up)

| ID | Nhân vật | Màu chủ đạo | Job ID |
|---|---|---|---|
| CH01 | Nữ chính – áo dài cách tân đỏ gấc, túi xanh ngọc | Crimson + Green | `62060764-3aae-4981-8b37-285d1ecd2433` |
| CH02 | Nam – bomber xanh ngọc thêu cá chép, kính tròn | Green | `d496f65b-69ef-49c0-8b9d-6e46c8ddcad5` |
| CH03 | Nữ – tóc bob nâu đồng, cardigan cam | Orange | v1 `f16654ad-d47a-4db0-871d-a336408942b9` (bị look 3D, loại) → v2A `d66f2aac-8b41-4007-89fd-2a8aa2a35857` / v2B `f0b0a341-00b6-4737-a7c7-304c35bcc062` (ref style CH02) → **v3 đổi mặt**: A `c4a10f9a-a7e7-44d7-a5c9-d81c67c39cc7` (da sáng, nốt ruồi dưới mắt) / B `adfacea1-525f-4e1f-b14e-71f420e0ada0` (da rám, gò má cao, mắt một mí) |
| CH04 | Nam – tóc xoăn, overshirt kem + hoodie đỏ đô | Burgundy | `66029270-e361-4471-8221-96af675a79b4` |

Áo của 4 nhân vật được phối theo bảng màu brand + lễ hội để khi đứng chung ở shot 4 vẫn đúng tone dự án.

## Prop sheet

| ID | Prop | Shot | Job ID |
|---|---|---|---|
| P01 | Biển lightbox sọc cam-xanh-đỏ (chừa trống logo) | 1, 5 | `ef21525d-7ebc-46f0-abfd-fd95b93338fc` |
| P02 | Bộ đèn lồng (trống, ông sao, cá chép, Hội An) | 1–4 | `efb7cafa-6df1-4eee-ad32-baabcc024f5d` |
| P03 | Kệ hàng hiện đại | 2 | `5ffb9e4c-ae58-40c1-aa10-fe72d040aa70` |
| P04 | Sạp ẩm thực gỗ truyền thống | 2 | `52707527-06c1-422a-ae48-c90c3d10987a` |
| P05 | Lò vi sóng (không logo) | 3 | `5816b12d-795a-4cde-ace9-acc2aee01f45` |
| P06 | Xôi gấc | 3, 4 | `771c4683-1df7-449b-9a55-5268db562005` |
| P07 | Bánh chưng mini (+ mặt cắt) | 3 | `85462cf6-360c-4272-8389-2a809c75a602` |
| P08 | Bộ 3 bát street food (cá viên chiên, bột chiên, bò bía) | 4 | `3778bb9b-a2a1-4f6c-a0f4-1002c678fbe7` |
| P09 | Ly nóng + ly đá sọc brand | 4 | `44580764-5783-47f7-ab9c-f0e66f128663` |
| P11 | Lẩu cá viên mini (bổ sung theo concept) | 4 | `46eab0dc-f79d-4908-aefd-7853fe619935` |

P10 (áo dài) nằm trong sheet CH01, không tách riêng.
