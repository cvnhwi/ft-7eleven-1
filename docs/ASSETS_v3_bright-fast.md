# 7-Eleven TVC v3 — Bright & Fast (asset prompts)

Script giữ nguyên 5 beat / 30s của `VIDEO_DRAFT_v1.md`. Thay đổi so với v2:
- **Giờ: chiều nắng ~16–17h** (không còn đêm/chạng vạng) → cảnh tươi sáng thật sự; trong cửa hàng sáng trắng daylight.
- **Pháo hoa → pháo giấy kim tuyến + bóng bay đỏ-vàng** (pháo hoa ban ngày lên hình nhạt, mất điểm nhấn).
- **Nhịp:** mỗi beat 2–4 cut ngắn (1–2.5s) → ~14 cut.
- **Đường phố/hẻm:** đông xe máy, hàng rong, người sắm Tết, motion blur nhẹ.
- **Màu broadcast:** high-key, không vùng tối, trắng sạch, bão hòa cao nhưng broadcast-safe.
- **Tái dùng** CH01–CH04, P01–P11 (sheet nền trung tính). Keyframe có nhân vật: đính kèm sheet CH tương ứng làm ref.

Model: Seedream 5.0 Pro · 2K · 16:9.

## Style block (dán cuối MỌI prompt)

```
STYLE: bright sunny late-afternoon Vietnamese TV commercial look, around 4-5pm, warm soft sunlight and clear bright blue sky, high-key exposure, open shadows filled with bounce light, no dark areas, crisp clean whites, fresh vivid saturated but broadcast-safe colors, convenience store interior lit bright daylight-white, brand accents orange #F4811F, green #008163, red #EE2526, red and gold Tet lanterns and yellow apricot blossoms, crisp sharp detail, clean commercial gloss, ARRI Alexa 35 look, 35mm lens. All signage blank: no text, no letters, no logos, no watermark.
```

## Negative (nếu tool có ô negative)

```
night, dusk, dark, moody, low-key, rain, wet ground, heavy shadows, teal and orange grade, film grain, haze, fog, gloomy, desaturated, neon-noir, text, letters, logo, watermark, distorted faces
```

## Background v3.1

**BG00 — Phố hẻm đông** (shot 1a, 1b)
```
Wide establishing background plate, eye-level 3/4 view: a bustling crowded alley street in Cho Lon, Saigon, on a sunny afternoon before Tet. Dense streams of motorbikes with light motion blur, people carrying hoa mai branches and shopping bags, street-food vendors with carts and steaming pots, kids in colorful ao dai, pastel yellow, mint and pink shophouses with balconies full of plants, red and gold lanterns and carp lanterns strung across the street catching the sunlight. At the end of the street a bright modern convenience store corner with an orange-green-red striped sign that is completely blank. Energetic, joyful, fast-paced city rhythm.
```

**BG01v3 — Mặt tiền 7-Eleven** (shot 1c, 5) · ref layout BG01v2 `d119e8b9-a51d-4780-9381-f8c88007d246`
```
Use the reference only for the storefront layout and camera angle; completely re-light it as a sunny afternoon. 3/4 wide shot of the convenience store facade on a busy street corner in Cho Lon: spotless glass sliding doors, bright white interior clearly visible through the glass, orange-green-red striped fascia and lightbox left completely blank, potted yellow hoa mai trees flanking the entrance, red and gold lanterns hanging under the awning, many people walking past with shopping bags, motorbikes passing with slight motion blur, a street vendor cart nearby. Dry sunlit pavement, clear blue sky. Busy, cheerful, inviting.
```

**BG02v3 — Lối đi trong cửa hàng** (shot 2a, 2b start) · ref layout BG02v2 `19eaf36b-7d80-435c-bb0b-a5609d286a8b`
```
Use the reference only for the aisle layout and centered camera angle. Interior of a modern convenience store in the afternoon, view straight down the central aisle, very bright daylight-white ceiling light, sunlight streaming in through the front glass, glossy white floor, shelves packed with colorful snacks and drinks whose packaging has no readable text, small red and gold lanterns and hoa mai branches hanging above, orange-green-red brand stripe along the top of the shelves, a few shoppers at the far end with slight motion blur. Airy, fresh, spotless, high-key.
```

**BG03v3 — Hẻm ẩm thực** (shot 2b end, 2c) · ref BẮT BUỘC = BG02v3 (giữ layout cho light-wipe)
```
Keep the exact same camera angle, perspective and aisle layout as the reference. The shelves have transformed into a lively, sunlit Cho Lon street-food alley: colorful wooden food stalls with steaming pots, banh mi cart, fish-ball fryer, red plastic stools, many smiling diners and vendors in motion, a canopy of red, gold and carp lanterns overhead, warm afternoon sunlight pouring in from above. Same bright high-key exposure and white balance as the reference.
```

**BG04v3 — Quầy đồ nóng** (shot 3a–3c)
```
Background plate, 3/4 medium-wide view of the hot-food counter corner inside a bright modern convenience store: stainless steel warmer display, a row of microwave ovens with no logos, soft steam rising, trays of xoi gac (red sticky rice) and mini banh chung on a clean white counter, white tiled wall, sunlight from a side window, small red and gold lanterns and a hoa mai branch above, orange-green-red brand stripe trim. Bright, appetizing, glossy and clean.
```

**BG05v3 — Quầy cửa kính** (shot 4a–4d)
```
Background plate, 3/4 view of a long window bar counter with stools inside a bright convenience store, facing a big sunlit glass window. Outside the window: a crowded festive street on a sunny afternoon, streams of motorbikes in light motion blur, people carrying hoa mai and gifts, red and gold lanterns strung across, red and gold balloons and confetti in the air. The counter is empty and clean, ready for people and food. Bright interior, lively exterior, joyful Tet energy.
```

## Keyframe (đính kèm sheet nhân vật làm ref)

**K2a** — ref: BG02v3 + CH01 v2
```
Place the woman from the character reference (keep her face, hair and white-red ao dai exactly) walking down the center of the aisle from the background reference, seen from behind at a slight 3/4 angle, mid-stride, one hand reaching toward the shelf, joyful energy. Keep the background, camera angle and bright lighting exactly as the background reference.
```

**K2b** — ref: BG03v3 + K2a
```
Same woman, same pose, same position and same camera angle as the first reference, but the environment is now the sunlit street-food alley from the second reference. Bright, joyful, consistent lighting.
```

**K4v3** — ref: BG05v3 + CH01, CH02, CH03 v3-B, CH04
```
The four young friends from the character references (keep each face and outfit exactly) gathered at the window counter from the background reference, laughing and clinking cups, bowls of xoi gac, mini banh chung, fish balls and a small hotpot on the counter, confetti and balloons outside the sunlit window. Medium-wide, eye level, bright high-key, everyone clearly lit, no dark areas.
```

## Đã gen (bản chạng vạng, cần gen lại theo style mới)
- BG00 `72a13c4d-11de-4a5b-98d6-1b8ebad56b36` — blue hour → gen lại
- BG04 `742ebe8a-dc09-4690-b269-effb0b1f5e81` — interior, có thể giữ nếu đủ sáng

## Fast cut list (đúng 5 beat script)

| Beat | Cut | Dur | Nội dung | Start frame | Camera |
|---|---|---|---|---|---|
| 1 Establishing 0–5s | 1a | 1.0 | CU đèn lồng cá chép xoay trong nắng, phố đông out-focus | BG00 | snap-zoom in |
| | 1b | 1.5 | Dòng xe máy + người ôm cành mai lướt qua | BG00 | whip-pan trái→phải |
| | 1c | 2.5 | CH01 len qua đám đông, cửa trượt mở | BG01v3 + CH01 | push-in nhanh |
| 2 Transformation 5–12s | 2a | 1.0 | Giày chạm sàn bóng (cut on action) | BG02v3 | low-angle tĩnh |
| | 2b | 4.0 | Light-wipe nắng quét kệ → sạp gỗ | start K2a · end K2b | steadicam theo sau |
| | 2c | 2.0 | Reveal hẻm ẩm thực đông vui | BG03v3 | arc 90° nhanh |
| 3 Food hero 12–18s | 3a | 1.5 | Cửa lò vi sóng bật mở | BG04v3 | macro tĩnh |
| | 3b | 2.0 | Hơi nóng trên xôi gấc | P06 + BG04v3 | macro slow-mo |
| | 3c | 2.5 | Tay lấy bánh chưng mini, mặt cắt | P07 + BG04v3 | rack focus |
| 4 Sharing 18–26s | 4a | 2.0 | CH02–04 ùa vào, vẫy tay | BG05v3 + CH02–04 | lateral dolly nhanh |
| | 4b | 2.0 | Top-down bàn đầy món, tay gắp đồng loạt | P06/P07/P08/P11 | top-down |
| | 4c | 2.0 | Cụng ly (P09) | BG05v3 + P09 | CU tĩnh |
| | 4d | 2.0 | Cả nhóm cười, pháo giấy + bóng bay ngoài kính (đỉnh nhạc) | K4v3 | push-in |
| 5 End card 26–30s | 5 | 4.0 | Pull-back ra phố nắng đông người, khóa máy 2s cuối | BG01v3 | crane-up → lock |

Video: Kling 3.0 Pro (start/end frame) cho cut ≥2s; cut 1–1.5s gen 3s rồi trim. Nhạc ~120 BPM, cắt trên phách.
