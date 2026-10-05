# 7-Eleven Video v2 — Plan (bright look + clean transition)

Tham chiếu độ sáng: storyboard KH gửi (chỉ tham khảo mood/exposure, không dùng làm ref).
Look mới: high-key night, lifted shadows, interior sáng ấm, neon đa sắc (cyan/magenta) + đèn lồng đỏ-vàng, cá chép & ông sao, mặt đường ướt phản chiếu.

## Background v2 (đang gen)
| ID | Job | Ghi chú |
|---|---|---|
| BG01v2 Mặt tiền sáng | `d119e8b9-a51d-4780-9381-f8c88007d246` | thay BG01 |
| BG02v2 Aisle sáng | `19eaf36b-7d80-435c-bb0b-a5609d286a8b` | thay BG02 |
| BG03v2 Hẻm ẩm thực | (ref BG02v2) | cùng layout BG02v2 |
| BG04v2 Quầy đồ nóng | (ref BG01v2 tone) | |
| BG05v2 Quầy cửa kính + pháo hoa | (ref BG01v2 tone) | |

## Pipeline mới — gen từng shot rồi ghép (thay vì 1 lần 30s)
| Shot | Dur | Input | Camera |
|---|---|---|---|
| 1 | 5s | start_image = BG01v2 | push-in chậm, cửa trượt mở |
| 2 | 7s | **start = K2a** (CH01 trong aisle) · **end = K2b** (CH01 cùng tư thế trong hẻm) | steadicam theo sau + làn sóng ánh sáng vàng quét kệ → sạp gỗ |
| 3 | 6s | start = K3 (macro lò vi sóng) + ref P06/P07 | macro slow-mo, steam, rack focus |
| 4 | 8s | start = K4 (nhóm 4 người ở BG05v2) | lateral dolly → push-in |
| 5 | 4s | start = BG01v2 | pull-back + crane-up, không chữ |

**Chống nháy shot 2:** start/end keyframe cùng bố cục & tư thế → model chỉ nội suy, không tự "bịa" môi trường giữa chừng; transition dạng *light-wipe* (làn sáng quét từ xa → gần) thay vì morph toàn khung.
**Audio:** clip gen chỉ SFX; nhạc nền lofi + đàn tranh tái dùng track 30s của v1 (đúng nhịp shot) — mix trong sandbox.
**Chống logo giả:** prompt cấm chữ/logo, QA từng clip, cắt nếu cần.
