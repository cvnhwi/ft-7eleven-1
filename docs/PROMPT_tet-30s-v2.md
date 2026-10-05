# 7-Eleven Tết 30s: Video Prompt v2 (motion rewrite)

Setting paragraph và Audio giữ nguyên từ v1. Chỉ viết lại motion và cách diễn đạt từng beat.

## Prompt

```
30-second fast-paced Vietnamese Tet TV commercial for a convenience store, 16:9, bright sunny late afternoon, high-key, vivid broadcast-safe colors, quick cuts on the beat of an upbeat 120 BPM track. Keep every character's face and outfit exactly as in their reference images. No dialogue, no text, no logos, no letters on any sign.

Editing rule: each timed line is one shot with a hard cut on the beat to the next, except lines marked CONTINUOUS, which are one unbroken camera move with no cut and no fade.

0-1s: Extreme close-up. Fast crash zoom in (lens zoom, camera body stays still) onto a red carp-shaped lantern hanging above the alley street of image 1. The lantern turns slowly on its string, sunlight glowing through its fabric. Ends with the lantern filling the frame.

1-2.5s: Wide shot of the street of image 1. Fast whip-pan from left to right with motion blur, settling for the last half-second on: motorbikes streaming past, a woman carrying a hoa mai branch, a vendor lifting the lid of a steaming pot.

2.5-5s: Street-level wide shot facing the storefront of image 2. Camera pushes forward fast toward the entrance. Linh (image 7) enters from frame left with her back to camera, weaves between pedestrians and reaches the entrance; the glass doors slide open sideways and she steps inside. Ends on her back crossing the threshold.

5-6s: Inside the aisle of image 3, ground-level low angle, lens just above the glossy floor, camera static. Linh's white sneaker steps down into frame, its reflection on the floor. The step matches the timing of her step through the door.

6-10s: CONTINUOUS. Steadicam behind Linh at shoulder height, moving forward at her walking pace down the aisle of image 3. A band of golden sunlight appears at the far end of the aisle and travels toward the camera. As it passes each shelf, that shelf turns into a wooden street-food stall of image 4: packaged products become steaming food, metal becomes wood, ceiling lights become red lanterns. By 10s the whole frame matches image 4.

10-12s: CONTINUOUS from the previous shot. Camera orbits 90 degrees clockwise around Linh, from behind her to her front-left three-quarter, revealing her face. She smiles and turns her head to look at the stalls of image 4 around her.

12-13.5s: Macro, static camera, at the hot-food counter of image 5. A plain microwave door with no logo pops open toward the camera and hot steam spills out.

13.5-15.5s: Macro slow motion, static camera. Thick steam curls upward from a bowl of xoi gac (image 11), glossy red sticky-rice grains, warm backlight making the steam glow.

15.5-18s: Close-up, static camera, shallow depth of field. Focus starts on the steaming xoi gac in the foreground. Linh's hand rises into the blurred background holding a mini banh chung already cut in half (image 12). Focus racks to the banh chung, its green cut cross-section facing the camera.

18-20s: Medium shot inside the store along the window counter of image 6. Camera dollies fast from left to right, parallel to the counter. Linh is already seated at the counter. Khang (image 8), Mai (image 9) and Bao (image 10) rush in from frame right toward her, waving; Bao lifts a red gift box above his shoulder.

20-22s: Top-down, camera directly above the counter, static. On the beat, hands quickly set down xoi gac, mini banh chung, a bowl of fish balls and a small steaming hotpot one after another; on the last beat four pairs of hands reach toward the food at the same time.

22-24s: Close-up at table height, static camera. Four plain paper cups with no logos rise into frame from four sides and clink together in the centre; a few drops splash.

24-26s: Exterior shot from the sunlit street, looking in through the shop window of image 6 at all four friends seated side by side at the window counter, facing the camera and laughing. Camera pushes in slowly. In the foreground, between the camera and the glass, red and gold confetti bursts and balloons float up into the sky (music peak).

26-30s: CONTINUOUS. Camera pulls straight back away from the window and cranes up to a high wide shot of the storefront of image 2 and the busy sunny street. 26-28s the camera is moving; 28-30s the camera is completely still, with the top third of the frame clean, empty blue sky for an end card.

Audio: upbeat modern Vietnamese pop-electronic beat with dan tranh accents, plus diegetic SFX: motorbike whooshes, crowd chatter, sliding door chime, microwave beep, sizzling, cups clinking, confetti pop. No vocals, no voiceover.
```

## Gen theo 3 đoạn (khi model giới hạn thời lượng hoặc số ảnh)

Mỗi đoạn dùng lại nguyên đoạn setting + Editing rule + Audio, chỉ giữ các beat của đoạn đó.
**Phải đánh số lại "image N" theo thứ tự upload của từng đoạn.**

| Đoạn | Beat | Ảnh cần dùng (số ở bản gốc) |
|---|---|---|
| A | 0–10s | 1, 2, 3, 4, 7 |
| B | 10–20s | 4, 5, 6, 7, 8, 9, 10, 11, 12 |
| C | 20–30s | 2, 6, 7, 8, 9, 10 |

Điểm nối: A kết thúc ở 10s và B bắt đầu bằng cú orbit "CONTINUOUS from the previous shot", nên dùng frame cuối của A làm start frame cho B.
