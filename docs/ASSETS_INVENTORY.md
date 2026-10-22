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


## W03 服務總覽圖片與頁尾紋飾

- 14 張服務總覽圖片已正式部署；所有原始 JPG 保留於 `web/` 根目錄。
- W02 WebP 重用 6 張：`03-service-hand-nail-care.webp`、`04-service-toe-nail-trim.webp`、`05-service-foot-skin-care.webp`、`06-service-nail-buffing.webp`、`07-service-single-color-gel.webp`、`08-service-gel-removal.webp`。
- W03 新轉 WebP 8 張，路徑均在 `web/assets/images/photos/`：`01-services-hero.webp`、`08-service-body-massage.webp`、`09-service-foot-massage-shoulder.webp`、`10-service-gua-sha-relaxation.webp`、`11-service-cupping-relaxation.webp`、`12-service-body-exfoliation.webp`、`13-service-facial-cleansing-mask.webp`、`14-service-face-hair-brow.webp`。主圖 1600×900，其餘七張 1200×900；目前合計 770,620 bytes。W04 開工前 GitHub 上兩筆使用者圖片上傳更新了最後一張 WebP（45,614 bytes）及其來源 JPG；W04 已先同步並保留該遠端更新。
- 六張使用者提供的 W03 JPG（檔名 02 至 07）因版位重用 W02 WebP，未另行轉檔，但原始檔仍保留。
- 第 11 張是一般背部放鬆情境，不是拔罐操作；第 12 張為局部肌膚保養示意；第 13 張為美容保養用品氛圍。所有照片均未標為店內實景、顧客成果或療效對比。
- 新增原創 Footer 線紋 `web/assets/brand/footer-ornament.svg`；CSS 與 JS 版本分別為 `w03-polish` 與 `w03-navigation`。
- `.w01_builder.py` 未修改或執行；未來重建網站前，需同步此輪映射與共用視覺。
- 詳細 14 張對應、ALT、尺寸、檔案大小、發布及 RWD 驗收見 `docs/W03_SERVICES_VISUAL_REPORT.md`。

## W04 品牌介紹頁圖片與標題紋飾

- 五張使用者提供的 AI 美容情境 PNG 均保留於 `web/` 根目錄；網站引用的 WebP 統一存於 `web/assets/images/photos/`。照片不代表店內實景、技師實際施工或顧客案例。
- W04 WebP 總計 516,990 bytes；原始 PNG 總計 10,560,147 bytes。Hero 圖 1672×941、優先載入；其餘四張 1200×900、lazy loading；均有 width/height、`object-fit: cover` 與實際情境 ALT。

| 原始 PNG | 用途 | 正式 WebP | 尺寸 | 大小 |
|---|---|---|---:|---:|
| `web/01-about-hero-spa-care.png` | 品牌介紹頁首大圖 | `web/assets/images/photos/01-about-hero-spa-care.webp` | 1672×941 | 108,276 bytes |
| `web/02-about-yating-spa-scene.png` | ABOUT YATING 品牌氛圍圖 | `web/assets/images/photos/02-about-yating-spa-scene.webp` | 1200×900 | 104,788 bytes |
| `web/03-about-our-services-nail-care.png` | 手部修甲服務卡 | `web/assets/images/photos/03-about-our-services-nail-care.webp` | 1200×900 | 96,260 bytes |
| `web/04-about-our-services-foot-spa.png` | 腳底按摩與肩頸服務卡 | `web/assets/images/photos/04-about-our-services-foot-spa.webp` | 1200×900 | 104,490 bytes |
| `web/05-about-our-services-neck-shoulder-relax.png` | 全身指壓與油壓服務卡 | `web/assets/images/photos/05-about-our-services-neck-shoulder-relax.webp` | 1200×900 | 103,176 bytes |

- 原創裝飾檔：`web/assets/brand/about-title-ornament.svg`；空 ALT 並設為裝飾性隱藏，不增加螢幕閱讀器噪音。
- W04 詳細圖片 ALT、連結映射、正式部署及三種螢幕驗收見 `docs/W04_ABOUT_VISUAL_REPORT.md`。
