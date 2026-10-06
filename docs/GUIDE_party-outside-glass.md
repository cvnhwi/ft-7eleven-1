# Guide: Cảnh nhóm bạn quẩy NGOÀI cửa kính (giữ nguyên location gốc)

Tool: Higgsfield. Ảnh dùng **Seedream 5.0 Pro** (2K, 16:9). Video dùng **Seedance 2.5** (Omni Reference, draft 480p).

---

## 0. Chuẩn bị reference

| Mã | File | Link (raw GitHub) | Dùng để |
|---|---|---|---|
| R1 | Khung gốc frame_s9 | https://raw.githubusercontent.com/cvnhwi/ft-7eleven-1/bbf0f811cdc6b0a933562180503119ea81aacfd4/refs/r1/frame_s9.png | Khoá location: góc máy, quầy, ghế, tủ |
| R2 | Logo 7-Eleven chính hãng | https://raw.githubusercontent.com/cvnhwi/ft-7eleven-1/bbf0f811cdc6b0a933562180503119ea81aacfd4/refs/r1/logo_7eleven.png | Biển hiệu trắng + sọc cam/xanh/đỏ |
| C1 | Linh (áo dài trắng) | https://raw.githubusercontent.com/cvnhwi/ft-7eleven-1/e8cb17284db841a429e8237d9d366c6eaadf0b89/refs/chars/linh.png | Nhân vật |
| C2 | Mai | https://raw.githubusercontent.com/cvnhwi/ft-7eleven-1/e8cb17284db841a429e8237d9d366c6eaadf0b89/refs/chars/mai.png | Nhân vật |
| C3 | Bảo | https://raw.githubusercontent.com/cvnhwi/ft-7eleven-1/e8cb17284db841a429e8237d9d366c6eaadf0b89/refs/chars/bao.png | Nhân vật |
| C4 | Khang (áo koi cam) | https://raw.githubusercontent.com/cvnhwi/ft-7eleven-1/e8cb17284db841a429e8237d9d366c6eaadf0b89/refs/chars/khang.png | Nhân vật |

Có thể dùng thêm các ảnh đã duyệt làm base nếu còn trên Higgsfield:
- Base nội thất có biển hiệu đã fix: https://d2ol7oe51mr4n9.cloudfront.net/user_3IOz7tFscQRUWCyOIu2UK9CE8RJ/8707ad1d-4b66-46f8-895d-033fe090994f.png (gọi là **B0**).
- Still đề xuất F: https://d2ol7oe51mr4n9.cloudfront.net/user_3IOz7tFscQRUWCyOIu2UK9CE8RJ/1354e0b8-5173-40ec-a9d4-f1da0cd27187.png

Cách đưa ảnh lên: tải file về máy, rồi bấm **Upload** trong ô reference của Higgsfield. Thứ tự upload quyết định ảnh nào là "image 1", "image 2"… nên phải upload đúng thứ tự ghi trong từng bước.

> **Lưu ý quan trọng (phản biện):** Đừng cố ra ảnh trong một lần. Đã test nhiều vòng: prompt một lần thì Seedream luôn kéo nhân vật dính sát kính, nhìn như đứng sau quầy bên trong (các bản A, B, D bị loại). Làm **2 bước** (bước 1 đưa nhân vật ra ngoài, bước 2 trả lại phố Tết) mới ổn định.

---

## BƯỚC 1 — Đưa nhóm bạn ra hẳn ngoài kính

**Reference, upload theo thứ tự:**
1. B0 (hoặc R1 nếu không còn B0).
2. C1.
3. C2.
4. C3.
5. C4.

**Setting:** Seedream 5.0 Pro · 16:9 · 2K · tạo 2–4 ảnh để chọn.

**Prompt:**
```
Edit image 1. Keep the camera, the store interior, the white window counter, the three orange stools, the fridges, the 7-Eleven sign band and the large glass windows EXACTLY the same. Change ONLY where the four friends stand: all four are OUTSIDE the shop, on the sunny outdoor sidewalk about 3 meters beyond the glass, clearly smaller and farther away than the counter. Use the exact identities and outfits from the character sheets: image 2 girl in white ao dai (Linh), image 3 girl in green top and denim skirt (Mai), image 4 boy in red shirt with bucket hat (Bao), image 5 boy in orange koi-print shirt (Khang). Between the glass and the friends, clearly visible: a row of potted yellow hoa mai apricot blossom planters standing on the outside pavement right against the glass, and grey outdoor paving tiles. Through the lower glass below the counter we see only the outside pavement and planter pots, no legs close to the glass. The friends are lit by warm direct outdoor sunlight with shadows on the pavement, a different light from the cool interior lights. Clear glass with faint reflections of the interior ceiling lights and glare streaks, so it is obvious they are seen THROUGH the window from inside. The counter and stools inside are empty. They wave and cheer at the camera, holding a red gift box and sparklers. Photorealistic, cinematic, Tet atmosphere.
```

**Kiểm tra trước khi qua bước 2:**
- [ ] Chậu mai nằm **giữa** kính và nhóm bạn.
- [ ] Không thấy chân người sát kính ở phần kính dưới quầy.
- [ ] Quầy và ghế bên trong trống.
- [ ] Khang mặc áo koi cam, Linh mặc áo dài trắng.

Bước này thường làm nền thành mặt đường trống. Không sao, bước 2 sẽ sửa.

---

## BƯỚC 2 — Trả lại phố Tết, kéo nhân vật lớn hơn

**Reference, upload theo thứ tự:**
1. Ảnh đã chọn ở bước 1.
2. R1 (khung gốc, để lấy không khí phố Tết).

**Setting:** Seedream 5.0 Pro · 16:9 · 2K · tạo 2–4 ảnh.

**Prompt:**
```
Edit image 1. Keep everything inside the shop exactly the same (camera, counter, stools, fridges, 7-Eleven sign band, windows) and keep the low row of yellow apricot blossom planters on the outside pavement against the glass. The four friends stay OUTSIDE on the sidewalk just behind the planters, the planters partly hiding their legs, the friends at medium size (heads around the middle of the window height) and clearly beyond the glass. Background behind them: the bustling Vietnamese Tet street of image 2, shophouses with red lanterns, yellow flowers, banners and balloons, a few distant pedestrians and parked motorbikes, soft depth of field, warm afternoon sunlight. Subtle realistic window glare and reflections of the interior lights over the outside scene. Friends dancing happily, one holds a red gift box, sparklers. Photorealistic, cinematic warm daylight.
```

**Kiểm tra:**
- [ ] Nhóm bạn vẫn ở sau chậu mai, không bị kéo vào trong.
- [ ] Phố Tết có lồng đèn đỏ, người qua lại.
- [ ] Biển hiệu là nền trắng, sọc cam, xanh, đỏ, logo 7-ELEVEN đúng chính tả.

Nếu logo bị sai chính tả, làm lại riêng phần biển hiệu, dùng R2 làm reference: *"replace the sign logo with the exact logo of image 2, matching scene lighting"*.

---

## BƯỚC 3 — Video (Seedance 2.5)

**Setting:**

| Mục | Giá trị |
|---|---|
| Model | Seedance 2.5 |
| Mode | Omni Reference |
| Start frame | Ảnh chốt ở bước 2 |
| End frame | Cũng chính ảnh đó (khoá hình học, chống trôi location; xem ghi chú) |
| Image references | C1, C2, C3, C4 (giữ mặt và trang phục) |
| Duration | 5s |
| Resolution | 480p, Draft ON (duyệt xong mới render 1080p) |
| Audio | Bật nếu muốn tiếng phố Tết; bỏ qua nếu sẽ lồng nhạc sau |
| Preset | Không dùng preset nào. Nếu Higgsfield gợi ý "IN THE DARK" thì bỏ qua. |

**Prompt:**
```
Static locked-off camera inside the 7-Eleven store looking out through the large glass windows, exactly the composition of the start frame. The camera does not move, maybe an extremely subtle slow push-in. The four friends (Linh in white ao dai, Mai in green top and denim skirt, Bao in red shirt and bucket hat, Khang in orange koi-print shirt) stay OUTSIDE on the sunny sidewalk behind the row of yellow apricot blossom planters for the entire shot. They never touch, open or cross the glass and never enter the shop. They party joyfully: jumping, dancing, waving at the camera, Bao lifts the red gift box overhead, Linh and Mai wave sparklers, Khang does a playful little dance, confetti drifts down outside. Background Tet street stays alive: red lanterns swaying gently, distant pedestrians walking, a motorbike passes far away. Inside the shop stays still and empty: counter, stools, fridges and the white 7-Eleven sign band with orange, green and red stripes remain perfectly unchanged. Faint reflections of interior ceiling lights on the glass stay fixed over the moving friends. Photorealistic, warm afternoon sunlight, cinematic Tet commercial, natural motion, no morphing.
```

**Ghi chú về end frame:**
- Dùng cùng một ảnh cho cả start và end frame thì nhân vật sẽ về lại tư thế ban đầu ở cuối clip, giúp cut liền mạch.
- Nếu thấy chuyển động bị "khựng" ở giữa, bỏ end frame và chỉ giữ start frame.
- Bỏ end frame thì phải kiểm tra kỹ 2 giây cuối: Seedance hay đẩy nhân vật lại gần kính.

**Lỗi hay gặp và cách sửa:**

| Lỗi | Sửa |
|---|---|
| Nhân vật đi xuyên kính hoặc vào trong shop | Thêm lại câu *"never cross the glass, never enter the shop"* lên đầu prompt; dùng end frame |
| Biển hiệu, logo méo khi chạy | Giữ camera tĩnh, thêm *"sign band remains perfectly unchanged"* |
| Mặt nhân vật bị đổi | Upload đủ 4 character sheet vào Image references |
| Khói, pháo hoa quá dày che mặt | Bỏ chữ "confetti/sparklers" hoặc thêm *"light, sparse confetti"* |

---

## Thứ tự làm nhanh

1. Bước 1: tạo 4 ảnh, chọn 1 ảnh nhóm bạn ở ngoài rõ nhất.
2. Bước 2: tạo 4 ảnh, chọn 1 ảnh có phố Tết.
3. Gửi ảnh chọn ở bước 2 cho khách duyệt.
4. Bước 3: làm clip nháp 480p, duyệt.
5. Render bản cuối 1080p.
