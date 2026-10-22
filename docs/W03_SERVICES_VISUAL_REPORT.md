# W03｜服務總覽圖片、全站導覽與頁尾視覺報告

更新日期：2026-10-22

## 發布狀態

- 狀態：已部署並驗證。
- 正式網站：[https://yating-nails.github.io/](https://yating-nails.github.io/)
- 服務總覽：[https://yating-nails.github.io/services/](https://yating-nails.github.io/services/)
- Repository：[yating-nails/yating-nails.github.io](https://github.com/yating-nails/yating-nails.github.io)
- 網站部署 commit：`0c9051dd997765037615fbe4af4c0a7ae769cffe`
- GitHub Actions：Deploy website to GitHub Pages，Run #5，Success；[檢視執行結果](https://github.com/yating-nails/yating-nails.github.io/actions/runs/39734065449)
- 正式站 Sitemap 列出的 22 個網址皆 HTTP 200。服務總覽 14 張圖片、共用 CSS、JS、Footer SVG、首頁、robots.txt 及 sitemap.xml 皆 HTTP 200。
- 本機 39 項 HTTP 檢查皆成功。正式服務總覽 14 張圖片已在瀏覽器逐張完成解碼，沒有破圖。

## 14 個圖片版位與來源

所有新製作 WebP 位於 `web/assets/images/photos/`。14 張使用者提供的來源 JPG 均確認可解碼並保留於 `web/` 根目錄。第 02–07 項依指示沿用 W02 圖片，未再轉換對應的 W03 JPG。

| # | 服務總覽版位 | 使用者提供 JPG | 正式使用圖片 | 尺寸／大小 | ALT |
|---:|---|---|---|---:|---|
| 01 | 服務總覽頁首主圖 | `web/01-services-hero.jpg` | `web/assets/images/photos/01-services-hero.webp` | 1600×900／148,614 bytes | 服務總覽主視覺：足部保養情境搭配毛巾、花材與保養用品。 |
| 02 | 手部修甲與指甲保養 | `web/02-service-hand-nail-care.jpg` | `web/assets/images/photos/03-service-hand-nail-care.webp`（重用 W02） | 1200×900／48,210 bytes | 以修甲工具整理自然指甲的手部修甲情境。 |
| 03 | 足部趾甲日常修整 | `web/03-service-toe-nail-trim.jpg` | `web/assets/images/photos/04-service-toe-nail-trim.webp`（重用 W02） | 1200×900／42,172 bytes | 修整趾甲外觀的足部保養情境，呈現趾甲與修整工具細節。 |
| 04 | 腳皮與足部角質保養 | `web/04-service-foot-skin-care.jpg` | `web/assets/images/photos/05-service-foot-skin-care.webp`（重用 W02） | 1200×900／61,276 bytes | 使用足部磨砂板整理足跟肌膚的日常保養情境。 |
| 05 | 手腳指甲拋光 | `web/05-service-nail-buffing.jpg` | `web/assets/images/photos/06-service-nail-buffing.webp`（重用 W02） | 1200×900／41,276 bytes | 以拋光板整理自然指甲甲面的手部保養情境。 |
| 06 | 單色光療美甲 | `web/06-service-single-color-gel.jpg` | `web/assets/images/photos/07-service-single-color-gel.webp`（重用 W02） | 1200×900／32,752 bytes | 呈現柔和裸色單色甲面的手部美甲情境。 |
| 07 | 光療卸除與指甲整理 | `web/07-service-gel-removal.jpg` | `web/assets/images/photos/08-service-gel-removal.webp`（重用 W02） | 1200×900／42,514 bytes | 以卸除箔包覆指甲的光療卸除情境，呈現工具與指尖細節。 |
| 08 | 全身指壓與油壓 | `web/08-service-body-massage.jpg` | `web/assets/images/photos/08-service-body-massage.webp` | 1200×900／118,206 bytes | 背部按摩與毛巾構成的舒適放鬆情境圖。 |
| 09 | 腳底按摩與肩頸舒緩 | `web/09-service-foot-massage-shoulder.jpg` | `web/assets/images/photos/09-service-foot-massage-shoulder.webp` | 1200×900／110,032 bytes | 足部與肩背休息情境，搭配毛巾及足浴用品。 |
| 10 | 傳統刮痧放鬆服務 | `web/10-service-gua-sha-relaxation.jpg` | `web/assets/images/photos/10-service-gua-sha-relaxation.webp` | 1200×900／107,064 bytes | 以刮痧工具進行肩背日常放鬆的美容情境圖。 |
| 11 | 傳統拔罐服務 | `web/11-service-cupping-relaxation.jpg` | `web/assets/images/photos/11-service-cupping-relaxation.webp` | 1200×900／122,082 bytes | 背部按摩放鬆情境與毛巾的暖色畫面；圖片未呈現拔罐操作。 |
| 12 | 全身肌膚去角質 | `web/12-service-body-exfoliation.jpg` | `web/assets/images/photos/12-service-body-exfoliation.webp` | 1200×900／54,024 bytes | 以刷具塗抹肌膚保養產品的局部情境示意。 |
| 13 | 臉部粉刺清潔及面膜保養 | `web/13-service-facial-cleansing-mask.jpg` | `web/assets/images/photos/13-service-facial-cleansing-mask.webp` | 1200×900／64,984 bytes | 毛巾、白花與美容保養用品構成的氛圍示意，非臉部清潔操作照片。 |
| 14 | 臉部除毛與眉型修整 | `web/14-service-face-hair-brow.jpg` | `web/assets/images/photos/14-service-face-hair-brow.webp` | 1200×900／37,824 bytes | 眉部修整情境圖，呈現眉型與整理工具近照。 |

新增轉換 8 張，合計 762,830 bytes；六張 W02 WebP 重用素材合計 268,200 bytes；服務總覽實際使用 14 張 WebP 合計 1,031,030 bytes。卡片圖片均採 `object-fit: cover`、4:3 版位、正確 `width`／`height` 及延遲載入；頁首圖採 1600×900、高優先級載入。原圖與版位比例相同，桌機及手機皆無拉伸或重要部位裁切。

所有圖片均以可見內容撰寫 ALT，不將情境素材說成店內實景、顧客成果或療效照片。第 11 張是一般背部放鬆情境，沒有拔罐操作；第 12 張為局部肌膚保養示意；第 13 張為保養用品氛圍，不是臉部清潔流程照。W03 六張未採用的來源 JPG 仍保留。

## 全站視覺與相容性

- Sitemap 的 22 個頁面均新增導覽「首頁」，保留品牌、服務、價目、保養知識、位置預約與 LINE 原有連結；404 頁也使用新版共用 CSS。
- 導覽採圓角膠囊、目前分類標示、柔和 hover／鍵盤 focus 效果。Header sticky，支援 16px 毛玻璃並備有奶油白不透明 fallback。手機漢堡選單可展開，Escape 可收合。
- 新增原創 SVG 抽象甲面弧線與植物線紋，僅作 Footer 背景；裝飾不覆蓋文字，桌機透明度 9%，手機降至 4.5–5.5%。原 Footer 文字、電話、地址、LINE、快速連結與 Copyright 保持原樣。
- 尊重 `prefers-reduced-motion`。服務總覽卡片圖片在手機改為單欄全寬 4:3；頁首主圖依 16:9 顯示。

| 瀏覽器視窗 | 實際檢查結果 |
|---:|---|
| 1440 px | 三欄服務卡、主圖及導覽正常；無水平溢出；14 張圖均解碼。 |
| 768 px | 兩欄服務卡、sticky Header 與漢堡選單正常；無水平溢出。 |
| 390 px | 單欄 4:3 全寬照片、觸控選單可展開／Escape 收合、LINE 浮鈕位於安全區內；無水平溢出。 |

## SEO、內容與安全檢查

- 22 頁的 HTML Title、Description、Canonical 與 JSON-LD 均保留原值；SEO/GEO metadata 檢查無差異。
- 13 篇服務文章正文、首頁 W02 九張圖片、價格、電話、LINE 及 Logo／favicon 未改。
- 本輪新增 ALT 與圖片說明不含醫療療效承諾。服務頁文字與既有法律提醒保持原樣。
- 全站共用 CSS／JS 加上新的版本查詢字串以更新快取；Git 差異檢查通過。

## 後續項目

- W03 只替換服務總覽頁的 14 個圖片版位。13 篇獨立服務文章主圖仍維持原版位，本輪未修改文章頁。
- `.w01_builder.py` 未執行或修改。若日後重建網站，需先把 W03 服務總覽圖、全站導覽與 Footer 改動同步進產生器，避免重建時覆回舊版。
- 上述不影響本輪上線；網站已部署並完成正式站驗證。