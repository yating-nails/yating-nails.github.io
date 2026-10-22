# W02 首頁圖片替換與部署報告

更新日期：2026-10-22

## 完成狀態

- 已部署並驗證：首頁 9/9 個 SVG 圖片位置已改用使用者提供的美容情境影像 WebP。
- 正式網站：https://yating-nails.github.io/
- Repository：https://github.com/yating-nails/yating-nails.github.io
- 網站變更 commit：595e63a74f581621d76ad7095dd620d3249dd205
- GitHub Actions：Deploy website to GitHub Pages Run #4，Success；https://github.com/yating-nails/yating-nails.github.io/actions/runs/39727901395
- 正式首頁、九張 WebP 與快取版本樣式表均回應 HTTP 200；九張圖在正式站瀏覽器逐張解碼成功。
- 本輪未改動其他 21 個可索引頁面、13 篇服務文章、Title、Description、Canonical、Open Graph、JSON-LD、電話或 LINE 連結。

## 圖片對應與輸出

所有 JPG 原始檔仍保留在 web/ 根目錄，並隨網站提交；首頁使用下表 WebP 路徑。影像為使用者提供的 AI 美容情境素材，不代表店內實景、技師實際施工或顧客成果。

| # | 首頁版位 | 原始 JPG | 正式 WebP | 尺寸 | WebP 大小 | ALT |
|---|---|---|---|---:|---:|---|
| 01 | Hero「日常保養 · 舒適放鬆」 | web/01-home-hero-spa.jpg | web/assets/images/photos/01-home-hero-spa.webp | 1500×1000 | 103,662 bytes | 足部浸泡於溫水中，搭配花朵、毛巾與保養用品的舒適放鬆情境。 |
| 02 | 「細緻保養 · 舒適日常」右側 | web/02-home-care-routine.jpg | web/assets/images/photos/02-home-care-routine.webp | 1200×900 | 53,372 bytes | 裸色指甲的手部置於白色花材旁，呈現細緻的日常手部保養情境。 |
| 03 | 手部修甲服務卡 | web/03-service-hand-nail-care.jpg | web/assets/images/photos/03-service-hand-nail-care.webp | 1200×900 | 48,210 bytes | 以修甲工具整理自然指甲的手部修甲情境。 |
| 04 | 足部趾甲修整服務卡 | web/04-service-toe-nail-trim.jpg | web/assets/images/photos/04-service-toe-nail-trim.webp | 1200×900 | 42,172 bytes | 修整趾甲外觀的足部保養情境，呈現趾甲與修整工具細節。 |
| 05 | 足部角質保養服務卡 | web/05-service-foot-skin-care.jpg | web/assets/images/photos/05-service-foot-skin-care.webp | 1200×900 | 61,276 bytes | 使用足部磨砂板整理足跟肌膚的日常保養情境。 |
| 06 | 指甲拋光服務卡 | web/06-service-nail-buffing.jpg | web/assets/images/photos/06-service-nail-buffing.webp | 1200×900 | 41,276 bytes | 以拋光板整理自然指甲甲面的手部保養情境。 |
| 07 | 單色光療服務卡 | web/07-service-single-color-gel.jpg | web/assets/images/photos/07-service-single-color-gel.webp | 1200×900 | 32,752 bytes | 呈現柔和裸色單色甲面的手部美甲情境。 |
| 08 | 光療卸除服務卡 | web/08-service-gel-removal.jpg | web/assets/images/photos/08-service-gel-removal.webp | 1200×900 | 42,514 bytes | 以卸除箔包覆指甲的光療卸除情境，呈現工具與指尖細節。 |
| 09 | 「品牌與照顧方式」左側 | web/09-home-brand-approach.jpg | web/assets/images/photos/09-home-brand-approach.webp | 1200×900 | 81,612 bytes | 摺疊毛巾、香氛蠟燭與白色花朵構成的品牌保養氛圍。 |

WebP 合計 506,846 bytes；原始 JPG 合計 1,582,575 bytes。JPG 原始檔保留，首頁實際載入 WebP。Hero 使用 eager/high 優先載入；其餘八張使用 lazy 載入。全部有正確 width、height、ALT、async 解碼與 object-fit: cover；物件位置依各張構圖設定。

## RWD 與功能驗收

| viewport | 內容寬度 | 服務照版型 | 水平溢出 |
|---:|---:|---|---|
| 1440 px | 1425 px（含垂直捲軸差異） | 3 欄 | 無 |
| 768 px | 753 px（含垂直捲軸差異） | 2 欄 | 無 |
| 390 px | 375 px（含垂直捲軸差異） | 單欄、圖片 4:3 全寬 | 無 |

以上尺寸已在本機與正式站檢查。手機服務卡圖片改成卡片上方 4:3 全寬，手指、趾甲與整理工具在小螢幕更容易辨識；手機選單可正常展開及收合。LINE 連結仍為 https://line.me/ti/p/IFSfLSxlck#~，電話仍為 tel:0981-797-891。

首頁 Title、Description、Canonical、OG 標題／描述與 JSON-LD 對照 W02 前版本一致。桌機與平板卡片網格維持原有排版。

## 產生器與後續素材

本機原始產生器 .w01_builder.py 已同步首頁九張照片、ALT、尺寸及手機卡片樣式，Python 語法檢查通過。此檔依既有 .gitignore 規則排除於 Git 之外，因此只更新本機產生器，未納入部署 commit。

W01 圖片規劃原列 21 張寫實情境圖；本輪完成首頁 9 張，其餘 12 張保留後續製作。下一輪請以 docs/YATING_IMAGE_PRODUCTION_PLAN.md 為清單，並參照本報告避免重做已完成的九張。
