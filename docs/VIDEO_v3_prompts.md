# 7-Eleven TVC v3 — Video prompts (30s, bright & fast)

## A. One-shot 30s (Seedance 2.5 omni_reference, 12 refs) — dùng làm draft/animatic

Ref order: 1 BG00 · 2 BG01 · 3 BG02 · 4 BG03 · 5 BG04 · 6 BG05 · 7 CH01 Linh · 8 CH02 Khang · 9 CH03 Mai · 10 CH04 Bao · 11 P06 xoi gac · 12 P07 banh chung

```
30-second fast-paced Vietnamese Tet TV commercial for a convenience store, 16:9, bright sunny late afternoon, high-key, vivid broadcast-safe colors, quick cuts on the beat of an upbeat 120 BPM track. Keep every character's face and outfit exactly as in their reference images. No dialogue, no text, no logos, no letters on any sign.

0-1s: Snap-zoom into a red carp lantern spinning in the sunlight above the crowded alley street of image 1.
1-2.5s: Whip-pan across the street of image 1: streams of motorbikes, people carrying hoa mai branches, vendors steaming pots.
2.5-5s: Fast push-in on the storefront of image 2; Linh (image 7) weaves through the crowd and the glass doors slide open for her.
5-6s: Low-angle cut on action: her white sneaker lands on the glossy floor of the aisle in image 3.
6-10s: Steadicam follows Linh down the aisle of image 3; a wave of golden sunlight sweeps from far to near, transforming the shelves into the sunlit street-food alley of image 4 in one continuous move.
10-12s: Fast 90-degree arc revealing the lively food alley of image 4, Linh smiling and looking around.
12-13.5s: Macro static: a microwave door pops open at the hot-food counter of image 5.
13.5-15.5s: Macro slow motion: steam rising from xoi gac (image 11).
15.5-18s: Rack focus: Linh's hand lifts a mini banh chung (image 12), revealing its green cut cross-section.
18-20s: Fast lateral dolly along the window counter of image 6 as Khang (image 8), Mai (image 9) and Bao (image 10) burst in waving; Bao holds up his red gift box.
20-22s: Top-down: the counter fills with xoi gac, mini banh chung, fish balls and a small hotpot, four pairs of hands reaching in at once.
22-24s: Close-up: four cups clink together.
24-26s: Push-in on all four friends laughing; outside the sunlit window red and gold confetti and balloons burst into the air (music peak).
26-30s: Pull-back and crane-up out through the doors to the storefront of image 2 and the busy sunny street; camera locks still for the final 2 seconds with clean empty sky space at the top for an end card.

Audio: upbeat modern Vietnamese pop-electronic beat with dan tranh accents, plus diegetic SFX: motorbike whooshes, crowd chatter, sliding door chime, microwave beep, sizzling, cups clinking, confetti pop. No vocals, no voiceover.
```

Rủi ro: 14 cut trong 1 lần gen → model hay gộp/bỏ cut, lệch mặt, sinh logo giả ở cuối. Dùng làm animatic duyệt nhịp với KH; bản phát sóng dùng B.

## B. Từng cut (Kling 3.0 Pro, image-to-video) — bản final

Mỗi cut gen 5s (cut ngắn gen 3s nếu tool cho), trim theo cột Dur rồi dựng theo nhạc. Sound OFF, nhạc + SFX mix hậu kỳ.

| Cut | Dur | Start frame |
|---|---|---|
| 1a | 1.0s | BG00 (hoặc crop CU đèn lồng) |
| 1b | 1.5s | BG00 |
| 1c | 2.5s | Keyframe: BG01 + CH01 (Linh trên vỉa hè) |
| 2a | 1.0s | BG02 (low angle sàn) |
| 2b | 4.0s | start K2a · end K2b |
| 2c | 2.0s | BG03 + Linh (hoặc frame cuối 2b) |
| 3a | 1.5s | BG04 (CU lò vi sóng) |
| 3b | 2.0s | P06 xoi gac đặt trên quầy BG04 |
| 3c | 2.5s | P07 banh chung + tay Linh |
| 4a | 2.0s | Keyframe: BG05 + CH02, CH03, CH04 |
| 4b | 2.0s | Top-down bàn với P06/P07/P08/P11 |
| 4c | 2.0s | CU 4 ly (P09) trên quầy BG05 |
| 4d | 2.0s | K4 |
| 5 | 4.0s | BG01 |

### Cut 1a · 1.0s · start: BG00 (hoặc crop CU đèn lồng)
```
Fast snap-zoom in onto a red carp lantern spinning gently in the sunlight above the crowded street, background crowd and motorbikes softly out of focus and moving. Bright sunny afternoon, high-key exposure, vivid broadcast-safe colors, crisp commercial look. Keep faces, outfits and environment exactly as the start frame. No text, no logos, no letters, no morphing or distortion.
```

### Cut 1b · 1.5s · start: BG00
```
Fast whip-pan from left to right across the crowded alley street: streams of motorbikes rushing past with motion blur, people carrying hoa mai branches, vendors stirring steaming pots, lanterns swaying. Bright sunny afternoon, high-key exposure, vivid broadcast-safe colors, crisp commercial look. Keep faces, outfits and environment exactly as the start frame. No text, no logos, no letters, no morphing or distortion.
```

### Cut 1c · 2.5s · start: Keyframe: BG01 + CH01 (Linh trên vỉa hè)
```
Fast push-in toward the storefront as Linh weaves quickly through the passing crowd with a bright smile, the glass sliding doors open for her as she steps inside. Pedestrians and motorbikes keep moving around her. Bright sunny afternoon, high-key exposure, vivid broadcast-safe colors, crisp commercial look. Keep faces, outfits and environment exactly as the start frame. No text, no logos, no letters, no morphing or distortion.
```

### Cut 2a · 1.0s · start: BG02 (low angle sàn)
```
Low-angle static shot at floor level in the bright store aisle: Linh's white sneaker steps firmly onto the glossy floor in the foreground, slight reflection, energetic cut-on-action feel. Bright sunny afternoon, high-key exposure, vivid broadcast-safe colors, crisp commercial look. Keep faces, outfits and environment exactly as the start frame. No text, no logos, no letters, no morphing or distortion.
```

### Cut 2b · 4.0s · start: start K2a · end K2b
```
Steadicam follows Linh from behind as she walks down the aisle; a wave of warm golden sunlight sweeps from the far end toward the camera, and as it passes, the shelves turn into wooden street-food stalls with steam, lanterns and diners. One continuous smooth move, Linh keeps the same pace. Bright sunny afternoon, high-key exposure, vivid broadcast-safe colors, crisp commercial look. Keep faces, outfits and environment exactly as the start frame. No text, no logos, no letters, no morphing or distortion.
```

### Cut 2c · 2.0s · start: BG03 + Linh (hoặc frame cuối 2b)
```
Fast 90-degree arc around Linh revealing the lively sunlit street-food alley inside the store, vendors and diners moving, lanterns swaying, Linh looking around delighted. Bright sunny afternoon, high-key exposure, vivid broadcast-safe colors, crisp commercial look. Keep faces, outfits and environment exactly as the start frame. No text, no logos, no letters, no morphing or distortion.
```

### Cut 3a · 1.5s · start: BG04 (CU lò vi sóng)
```
Macro static shot of a microwave oven at the bright hot-food counter: the door pops open with a puff of steam, warm light inside. Bright sunny afternoon, high-key exposure, vivid broadcast-safe colors, crisp commercial look. Keep faces, outfits and environment exactly as the start frame. No text, no logos, no letters, no morphing or distortion.
```

### Cut 3b · 2.0s · start: P06 xoi gac đặt trên quầy BG04
```
Macro slow motion: thick wisps of steam rise from glossy red xoi gac sticky rice in a bowl, backlit by warm sunlight, grains glistening. Camera static. Bright sunny afternoon, high-key exposure, vivid broadcast-safe colors, crisp commercial look. Keep faces, outfits and environment exactly as the start frame. No text, no logos, no letters, no morphing or distortion.
```

### Cut 3c · 2.5s · start: P07 banh chung + tay Linh
```
Rack focus from the steam to Linh's hand lifting a mini banh chung, revealing its green-and-yellow cut cross-section, slow and appetizing. Camera nearly static. Bright sunny afternoon, high-key exposure, vivid broadcast-safe colors, crisp commercial look. Keep faces, outfits and environment exactly as the start frame. No text, no logos, no letters, no morphing or distortion.
```

### Cut 4a · 2.0s · start: Keyframe: BG05 + CH02, CH03, CH04
```
Fast lateral dolly along the window counter as Khang, Mai and Bao burst in waving excitedly, Bao holding up a red-and-gold gift box, sunlit crowded street visible through the glass. Bright sunny afternoon, high-key exposure, vivid broadcast-safe colors, crisp commercial look. Keep faces, outfits and environment exactly as the start frame. No text, no logos, no letters, no morphing or distortion.
```

### Cut 4b · 2.0s · start: Top-down bàn với P06/P07/P08/P11
```
Top-down static shot of the counter as dishes slide in quickly: xoi gac, mini banh chung, fish balls and a small steaming hotpot; four pairs of hands reach in at the same time with chopsticks. Bright sunny afternoon, high-key exposure, vivid broadcast-safe colors, crisp commercial look. Keep faces, outfits and environment exactly as the start frame. No text, no logos, no letters, no morphing or distortion.
```

### Cut 4c · 2.0s · start: CU 4 ly (P09) trên quầy BG05
```
Close-up of four cups lifted into frame and clinking together in the center, drops of drink sparkling in the sunlight, sunlit window behind softly out of focus. Bright sunny afternoon, high-key exposure, vivid broadcast-safe colors, crisp commercial look. Keep faces, outfits and environment exactly as the start frame. No text, no logos, no letters, no morphing or distortion.
```

### Cut 4d · 2.0s · start: K4
```
Slow push-in on the four friends laughing together at the window counter; outside the window red and gold confetti and balloons burst into the bright sky. Joyful peak moment. Bright sunny afternoon, high-key exposure, vivid broadcast-safe colors, crisp commercial look. Keep faces, outfits and environment exactly as the start frame. No text, no logos, no letters, no morphing or distortion.
```

### Cut 5 · 4.0s · start: BG01
```
Pull-back and crane-up from the storefront to reveal the busy sunny street full of people and motorbikes; for the final 2 seconds the camera locks completely still, leaving clean empty sky at the top of frame for an end card. Bright sunny afternoon, high-key exposure, vivid broadcast-safe colors, crisp commercial look. Keep faces, outfits and environment exactly as the start frame. No text, no logos, no letters, no morphing or distortion.
```

## C. Multi-shot 30s một lần gen + transition effect (Seedance 2.5 omni_reference)

Gộp 14 cut → 9 shot nối bằng transition có động cơ (whip-pan, match cut, light-wipe, steam-wipe, confetti-wipe): nhịp vẫn nhanh nhưng model ít phải "nhảy cảnh" hơn → ít lệch mặt/bỏ shot.
Ref: 1 BG00 · 2 BG01 · 3 BG02 · 4 BG03 · 5 BG04 · 6 BG05 · 7 CH01 Linh · 8 CH02 Khang · 9 CH03 Mai · 10 CH04 Bao · 11 P06 · 12 P07

```
A 30-second multi-shot Vietnamese Tet TV commercial for a convenience store, 16:9, 9 shots connected by energetic motivated transitions, cut on the beat of an upbeat 120 BPM track. Bright sunny late afternoon around 4-5pm, high-key exposure, open shadows, crisp clean whites, vivid broadcast-safe colors, brand accents orange, green and red, red and gold lanterns and yellow hoa mai blossoms everywhere. Keep every character's face, hair and outfit exactly as in their reference images in every shot. No dialogue, no on-screen text, no logos, no letters on any sign.

SHOT 1 (0-2.5s) — Image 1. Snap-zoom into a red carp lantern spinning in the sunlight, then a fast whip-pan across the crowded alley street: streams of motorbikes with motion blur, people carrying hoa mai branches, vendors stirring steaming pots.
TRANSITION: whip-pan motion blur carries straight into the next shot.

SHOT 2 (2.5-5s) — Image 2. Fast push-in on the bright storefront; Linh (image 7) weaves through the passing crowd with a big smile and the glass doors slide open for her.
TRANSITION: match cut on action — her foot crosses the threshold and lands inside.

SHOT 3 (5-6s) — Image 3. Low-angle at floor level: Linh's white sneaker lands on the glossy aisle floor.

SHOT 4 (6-11s) — Image 3 into image 4. Steadicam follows Linh down the bright aisle. TRANSITION EFFECT: a glowing wave of golden sunlight with sparkling dust sweeps from the far end toward the camera; everywhere it passes, the shelves transform into the sunlit street-food alley of image 4 with wooden stalls, steam, lanterns and diners. One continuous move, then a fast 90-degree arc around Linh as she looks around delighted.
TRANSITION: a puff of steam from a food stall fills the frame and clears to reveal the next shot (steam wipe).

SHOT 5 (11-14s) — Image 5. Macro: a microwave door pops open with a burst of steam; slow-motion steam rising from glossy red xoi gac (image 11), backlit by sunlight.

SHOT 6 (14-17s) — Image 5. Rack focus from the steam to Linh's hand lifting a mini banh chung (image 12), revealing its green cut cross-section.
TRANSITION: the banh chung swings toward the lens and fills the frame (object wipe), revealing the next shot.

SHOT 7 (17-20s) — Image 6. Fast lateral dolly along the sunlit window counter as Khang (image 8), Mai (image 9) and Bao (image 10) burst in waving; Bao holds up a red-and-gold gift box; Linh turns and laughs.
TRANSITION: quick whip-tilt down to the counter.

SHOT 8 (20-26s) — Image 6. Top-down: dishes slide in fast — xoi gac, mini banh chung, fish balls, a small steaming hotpot — four pairs of hands reach in at once. Cut on the beat to a close-up of four cups clinking, then push-in on all four friends laughing while red and gold confetti and balloons burst outside the sunlit window (music peak).
TRANSITION: a shower of red and gold confetti sweeps across the lens (confetti wipe).

SHOT 9 (26-30s) — Image 2. Pull-back and crane-up from the storefront to the busy sunny street full of people and motorbikes; for the last 2 seconds the camera locks completely still, with clean empty blue sky at the top of frame for an end card.

Audio: upbeat modern Vietnamese pop-electronic beat with dan tranh accents, each transition hit with a whoosh or riser; diegetic SFX: motorbike whooshes, crowd chatter, door chime, microwave beep, sizzling, cups clinking, confetti pop. No vocals, no voiceover.
```
