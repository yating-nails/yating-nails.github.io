# 素材清單

## 品牌與網站圖示

- web/logo.png：使用者提供的橫式品牌 Logo，原比例沿用。
- web/favicon.ico：由完整 Logo 縮放製作 16/32/48px icon。
- web/assets/brand/apple-touch-icon.png：180px；icon-192.png、icon-512.png：Manifest 圖示。
- web/assets/brand/og-cover.jpg：1200×630 分享封面。
- web/assets/images/illustrations/：24 張原創 SVG 仍保留。首頁九個指定位置改用 WebP，其他頁面插畫未改。

## W02 首頁照片

來源為使用者提供的美容情境圖。原始 JPG 保留於 web/ 根目錄並隨 W02 commit 保存；首頁實際引用 web/assets/images/photos/ 的 WebP。這些為 AI 情境素材，不代表店內實景、實際技師施工或顧客成果。

| 原始 JPG | 用途 | WebP 輸出 | 尺寸 | 大小 |
|---|---|---|---:|---:|
| 01-home-hero-spa.jpg | 首頁 Hero 足部舒適放鬆 | 01-home-hero-spa.webp | 1500×1000 | 103,662 bytes |
| 02-home-care-routine.jpg | 手部日常保養品牌圖 | 02-home-care-routine.webp | 1200×900 | 53,372 bytes |
| 03-service-hand-nail-care.jpg | 手部修甲服務卡 | 03-service-hand-nail-care.webp | 1200×900 | 48,210 bytes |
| 04-service-toe-nail-trim.jpg | 足部趾甲整理服務卡 | 04-service-toe-nail-trim.webp | 1200×900 | 42,172 bytes |
| 05-service-foot-skin-care.jpg | 足部角質整理服務卡 | 05-service-foot-skin-care.webp | 1200×900 | 61,276 bytes |
| 06-service-nail-buffing.jpg | 指甲拋光服務卡 | 06-service-nail-buffing.webp | 1200×900 | 41,276 bytes |
| 07-service-single-color-gel.jpg | 單色光療服務卡 | 07-service-single-color-gel.webp | 1200×900 | 32,752 bytes |
| 08-service-gel-removal.jpg | 光療卸除服務卡 | 08-service-gel-removal.webp | 1200×900 | 42,514 bytes |
| 09-home-brand-approach.jpg | 品牌與照顧方式區塊 | 09-home-brand-approach.webp | 1200×900 | 81,612 bytes |

WebP 合計 506,846 bytes；九張原始 JPG 合計 1,582,575 bytes。九張圖均有實際內容 ALT、width/height 與 object-fit: cover。Hero 使用 eager/high 載入，其餘採 lazy 載入。正式站九張 WebP 均 HTTP 200，瀏覽器解碼成功。

## W01 原始商家素材

專案根目錄原有七張 JPG，均保留於網站發布目錄以外：

- 856697146_122220884432046062_7283099217162194371_n.jpg：足部甲面近照，未公開。
- 857201073_122220884306046062_6854939909546444926_n.jpg：舊版價格圖；用於核對待確認價格。
- 857293836_122220884474046062_1027864903991177774_n.jpg：皮膚痕跡類照片，不公開。
- 857397600_122220884372046062_6610125764125978510_n.jpg：手部照片，肖像授權未確認，不公開。
- 857445616_122220884606046062_3433646896503398501_n.jpg：LINE QR 圖，不公開，網站使用指定 URL。
- 857761652_122220884516046062_8797522282049319996_n.jpg：新版價目圖，用於價格核對。
- 858740669_122220884564046062_3602776382457416134_n.jpg：店面照片，使用權未確認，不公開。

## 權利與後續狀態

- W02 九張情境圖由使用者提供並指定用於本網站；公開文案不將其描述成真實店內、服務人員實際操作或顧客成果照。
- W01 既有商家照片的拍攝者授權／出鏡者同意無法由檔案確認，因此維持不公開。
- 21 張初始情境圖規劃中，W02 完成首頁 9 張，尚有 12 張待後續製作；規劃清單見 docs/YATING_IMAGE_PRODUCTION_PLAN.md。
- .w01_builder.py 是本機原始產生器，首頁照片映射與手機卡片規則已同步；既有 .gitignore 排除此檔於 Git 版本控制之外。
