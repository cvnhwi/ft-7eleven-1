# 7-Eleven TVC v3 — Bright & Fast (asset prompts)

Script giữ nguyên 5 beat / 30s của `VIDEO_DRAFT_v1.md`. Thay đổi:
- **Giờ:** chạng vạng ~18h (trời xanh cyan còn sáng, mọi đèn đã bật) thay cho đêm sau mưa → tươi sáng mà vẫn giữ neon + đèn lồng.
- **Nhịp:** mỗi beat chia 2–4 cut ngắn (1–2.5s) → ~14 cut thay vì 5 shot dài.
- **Đường phố/hẻm:** đông xe máy, hàng rong, người đi lễ — motion blur nhẹ để tạo tốc độ.
- **Màu chuẩn phát sóng:** high-key, shadow nâng, không đen bệt, trắng trung tính, bão hòa cao nhưng broadcast-safe.
- **Không gen lại** CH01–CH04 và P01–P11: sheet nền xám trung tính, không phụ thuộc mood → tái dùng (CH01 v2 áo dài trắng-đỏ `49df5c41…`).

Model: Seedream 5.0 Pro · 2K · 16:9.

## Style block (dán cuối mọi prompt BG/keyframe)

```
STYLE: bright high-key Vietnamese TV commercial look, early evening blue hour around 6pm, sky still bright deep cyan-blue, every practical light switched on, lifted shadows, no crushed blacks, clean neutral whites, vivid saturated but broadcast-safe colors, brand accents orange #F4811F, green #008163, red #EE2526, crimson and gold Tet lanterns, crisp sharp detail, ARRI Alexa 35 look, 35mm lens. All signage blank: absolutely no text, no letters, no logos, no watermark.
```

## Background v3

| ID | Ref | Job | Prompt (+ style block) |
|---|---|---|---|
| BG00 Phố hẻm đông | — | `72a13c4d-11de-4a5b-98d6-1b8ebad56b36` | Wide establishing background plate, eye-level 3/4 view: a bustling crowded alley street in Cho Lon, Saigon, at early evening during Tet. Dense streams of motorbikes with light motion blur, street-food vendors with carts and steaming pots, pedestrians in colorful festive clothes, kids holding star lanterns, old yellow and teal shophouses with balconies, a canopy of red-crimson and gold lanterns and carp lanterns strung overhead. At the end of the street a bright modern convenience store corner glows with an orange-green-red striped lightbox sign that is completely blank. Energetic, lively, fast-paced city rhythm. |
| BG01v3 Mặt tiền | BG01v2 `d119e8b9-a51d-4780-9381-f8c88007d246` (layout) | ⏳ hết credit | Use the reference only for the storefront layout and camera angle. Re-light and repopulate it: 3/4 wide shot of the convenience store facade on a busy street corner in Cho Lon at early evening, glass sliding doors, bright clean white interior glowing through the glass, orange-green-red striped lightbox sign left completely blank, many people walking past, motorbikes passing with slight motion blur, parked scooters, street vendor cart nearby, strings of red and gold Tet lanterns crossing the street above. Dry street, no rain. Busy, cheerful, fast-paced. |
| BG02v3 Aisle | BG02v2 `19eaf36b-7d80-435c-bb0b-a5609d286a8b` (layout) | ⏳ hết credit | Use the reference only for the aisle layout and centered camera angle. Interior of a modern convenience store, view straight down the central aisle, very bright clean white LED ceiling light, glossy reflective floor, shelves packed with colorful snacks and drinks whose packaging has no readable text, small red and gold Tet lanterns and peach-blossom branches hanging from the ceiling, orange-green-red brand stripe along the top of the shelves, a few shoppers moving at the far end with slight motion blur. Airy, fresh, cheerful, high-key. |
| BG03v3 Hẻm ẩm thực | **BG02v3** (bắt buộc, giữ layout cho light-wipe) | ⏳ sau BG02v3 | Keep the exact same camera angle, perspective and aisle layout as the reference. The shelves have transformed into a crowded Cho Lon street-food alley: wooden food stalls with steaming pots, banh mi cart, fish-ball fryer, plastic stools, many diners and vendors in motion, dense lantern canopy overhead in red, gold and carp shapes, bright warm-white stall bulbs. Same bright high-key exposure as the reference. |
| BG04v3 Quầy đồ nóng | — | `742ebe8a-dc09-4690-b269-effb0b1f5e81` | Background plate, 3/4 medium-wide view of the hot-food counter corner inside a modern convenience store: stainless steel warmer display with golden lighting, a row of microwave ovens with no logos, steam rising softly, trays of xoi gac and mini banh chung on the counter, clean white tiled wall, small red and gold Tet lanterns above, orange-green-red brand stripe trim. Bright, appetizing, warm-white light, glossy and clean. |
| BG05v3 Quầy cửa kính | — | ⏳ hết credit | Background plate, 3/4 view of a long window bar counter with stools inside a bright convenience store, facing a big glass window. Outside: a crowded festive street at early evening with streams of motorbikes in light motion blur, crowds of people, vendors, red and gold Tet lanterns strung across, and colorful fireworks bursting in the bright cyan-blue sky. The counter is empty and clean. Bright interior, lively exterior, joyful energy. |

## Fast cut list (đúng 5 beat script)

| Beat | Cut | Dur | Nội dung | Start frame | Camera |
|---|---|---|---|---|---|
| 1 Establishing 0–5s | 1a | 1.0 | CU đèn lồng cá chép xoay, phố đông out-focus phía sau | BG00 (crop/keyframe) | snap-zoom in |
| | 1b | 1.5 | Dòng xe máy + hàng rong lướt qua khung | BG00 | whip-pan trái→phải |
| | 1c | 2.5 | CH01 len qua đám đông bước vào, cửa trượt mở | BG01v3 + CH01 | push-in nhanh |
| 2 Transformation 5–12s | 2a | 1.0 | Giày chạm sàn bóng (cut on action) | BG02v3 | low-angle tĩnh |
| | 2b | 4.0 | Light-wipe quét kệ → sạp gỗ, hẻm đông hiện ra | start K2a (BG02v3+CH01) · end K2b (BG03v3+CH01) | steadicam theo sau |
| | 2c | 2.0 | Reveal hẻm ẩm thực đông nghịt trong cửa hàng | BG03v3 | arc 90° nhanh |
| 3 Food hero 12–18s | 3a | 1.5 | Cửa lò vi sóng bật mở | BG04v3 | macro tĩnh |
| | 3b | 2.0 | Hơi nóng bốc trên xôi gấc | P06 + BG04v3 | macro slow-mo |
| | 3c | 2.5 | Tay lấy bánh chưng mini, mặt cắt | P07 + BG04v3 | rack focus |
| 4 Sharing 18–26s | 4a | 2.0 | CH02–04 ùa vào, vẫy tay | BG05v3 + CH02–04 | lateral dolly nhanh |
| | 4b | 2.0 | Top-down bàn đầy món, tay gắp đồng loạt | P06/P07/P08/P11 | top-down, cut nhanh |
| | 4c | 2.0 | Cụng ly (P09) | BG05v3 + P09 | CU tĩnh |
| | 4d | 2.0 | Cả nhóm cười, pháo hoa ngoài kính (đỉnh nhạc) | K4v3 | push-in |
| 5 End card 26–30s | 5 | 4.0 | Pull-back ra phố đông, khóa máy 2s cuối | BG01v3 | crane-up → lock |

Video model đề xuất: Kling 3.0 Pro (start/end frame, camera lock tốt) cho cut ≥2s; cut 1–1.5s gen 3s rồi trim. Nhạc tempo ~120 BPM, cắt trên phách.
