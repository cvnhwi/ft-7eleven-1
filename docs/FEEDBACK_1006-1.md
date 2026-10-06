# Feedback round 1: video `1006-1.mp4` (30s)

Nguồn: slide "INPUT 711" của khách. Review dựa trên các frame trong slide (chưa xem được full video).

## Brand spec của khách

| Màu | Hex | Pantone |
|---|---|---|
| Green | `#007350` | 336 C |
| Orange | `#FF6C00` | 1505 XGC |
| Red | `#EC0F2A` | 2347 C |

3 stripes ngang trên nền trắng, từ trên xuống: **cam → xanh → đỏ**. Logo 7-ELEVEN đặt giữa fascia (xem ảnh tham chiếu ở slide 2).

## Bảng feedback → hướng sửa

| TC | Feedback | Nguyên nhân | Hướng sửa | Cách làm |
|---|---|---|---|---|
| Toàn bộ | Cửa hàng ở toàn cảnh và trung cận không đồng bộ | 0:02 và 0:03 gen độc lập: toàn cảnh là căn góc phố hẹp, trung cận là mặt tiền phẳng với vỉa hè rộng, kiến trúc khác hẳn | Tạo 1 **storefront master** duy nhất. Toàn cảnh = outpaint từ master; trung cận = crop/upscale từ master. Gen lại 0–5s bằng first/last frame (đầu = toàn cảnh, cuối = trung cận), hoặc gộp thành 1 cú push-in liền | Regen |
| 0:02, 0:03 | Add logo, cân màu 3 stripes | AI tự chế stripes: sai thứ tự, sai tỷ lệ, sai màu; không có logo | Master storefront: fascia trắng + 3 stripes đúng thứ tự, để trống vị trí logo. Logo thật composite bằng planar track. Màu stripes chỉnh về đúng hex bằng qualifier trong grade | Regen + Post |
| 0:06 | Chỉnh 3 stripes theo branding | Header kệ thành các khối xanh/đỏ rời rạc, thiếu cam | Header kệ = dải trắng có 3 stripes liền mạch chạy dọc lối đi. Đưa vào BG lối đi (image 3) rồi gen lại shot | Regen |
| 0:11 | Chỉnh logo 711 kèm text trên signboard | AI render chữ rác ("VNII-ĐGO") | Gen signboard trống (blank white panel), sau đó composite artwork logo + text chính thức và track theo chuyển động máy | Post (hoặc inpaint + post) |
| 0:13 | Add food: tô xôi gấc khớp với cảnh sau | Lò vi sóng trống, chỉ có hơi nước | Đặt **đúng tô xôi gấc của shot 13.5s** lên đĩa xoay. Dùng frame đầu shot 13.5s làm ref để khớp tô, màu xôi, hơi nước | Regen |
| 0:23 | Logo trên ly; đổi sang inox/thủy tinh vì SFX giấy chưa hợp | Ly giấy trơn; tiếng "cạch" không khớp chất liệu | Xem phần phản biện bên dưới. Ly trơn khi gen, logo composite sau, ít nhất trên 1 ly hero quay mặt ra máy | Regen + Post |
| 0:25 | Signboard cam đổi thành 3 stripes | Dải trên cửa sổ là mảng cam đặc; tủ và quầy cũng cam, làm loãng brand | Dải trên cửa sổ = trắng + 3 stripes. Giảm mảng cam trên tủ/kệ về trắng/xám bạc để stripes nổi lên | Regen (BG image 6) |
| 0:30 | Cân màu branding + add logo | Logo badge đặt tạm; store trong end card lại là 1 kiểu kiến trúc khác; stripes sai | End card dùng toàn cảnh từ storefront master (đồng bộ với 0:02). Logo chính thức là file vector, không gen | Regen + Post |

## Phản biện / cần chốt với khách

1. **Ly inox/thủy tinh** khớp SFX nhưng không đúng thực tế cửa hàng tiện lợi (7-Eleven bán đồ uống ly nhựa/giấy). Đề xuất thay thế: **ly nhựa trong có logo + đá viên**. Tiếng đá va vào thành ly rất "đã tai", giữ được tính thật của sản phẩm, và ly trong dễ composite logo hơn. Nếu khách vẫn muốn thủy tinh thì làm theo.
2. **Tagline end card đang là tiếng Anh**, trong khi thị trường VN và kịch bản gốc dùng câu tiếng Việt ("Trạm Dừng Văn Hóa – Đậm Vị Lễ Hội"). Cần khách chốt ngôn ngữ và copy cuối.
3. **Logo/text không gen bằng AI.** Mọi vị trí có logo (fascia, signboard 0:11, ly, end card) đều làm ở hậu kỳ, từ file logo chính thức. Đây là cách duy nhất để đúng 100% brand guideline. Nên báo khách khi họ hỏi vì sao logo không có ngay trong bản gen.
4. Mã hex chỉ chính xác tuyệt đối trên artwork phẳng (logo, end card). Trên video có ánh sáng và phản chiếu, stripes được grade về gần đúng hex ở vùng sáng chuẩn.

## Thứ tự làm

1. Storefront master (ảnh tĩnh) → khách duyệt trước khi gen video. Đây là bước chặn: chưa chốt master thì không gen lại các shot liên quan.
2. Cập nhật BG image 3 (lối đi) và image 6 (quầy cửa sổ) với stripes đúng.
3. Gen lại: 0–5s, 6–10s, 12–13.5s, 22–24s, 24–30s.
4. Hậu kỳ: planar track logo (fascia, signboard, ly), grade stripes, end card.

## Prompt fragments

**Storefront master (image edit, ref = ảnh mặt tiền ở slide 2 + logo):**
```
Photorealistic Vietnamese street-corner 7-Eleven style convenience store on a busy Ho Chi Minh City alley, bright sunny late afternoon, Tet decorations (red lanterns, hoa mai). Store design exactly as the reference photo: white fascia with three continuous horizontal stripes, top to bottom orange #FF6C00, green #007350, red #EC0F2A, equal thickness, a clean blank white square in the centre of the fascia for the logo, full-height glass front and sliding glass doors. No text, no letters, no logos anywhere.
```

**12–13.5s microwave:**
```
Macro, static camera, at the hot-food counter of image 5. A plain white microwave with no logo; its door pops open toward camera revealing, on the glass turntable, the same bowl of xoi gac as image 11 — bright orange-red sticky rice, same bowl. Hot steam spills out over the bowl. Bowl, rice colour and steam match image 11 exactly.
```

**22–24s cups (đề xuất ly nhựa trong + đá):**
```
Close-up at table height, static camera. Four clear plastic cups of iced tea with ice cubes rise into frame from four sides and clink together in the centre; ice knocks against the walls and a few drops splash. Cups are plain and blank, no print. Warm sunny bokeh background.
```

**24–26s window counter:**
```
... Above the window, a white fascia band with three continuous horizontal stripes, top to bottom orange, green, red, no text. Fridges and counter in white and brushed steel, not orange.
```
