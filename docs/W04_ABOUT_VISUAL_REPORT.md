# W04｜品牌介紹頁圖片與精品視覺報告

更新日期：2026-10-22

## 發布狀態

- 狀態：已部署並完成正式站驗證。
- 品牌介紹頁：[https://yating-nails.github.io/about/](https://yating-nails.github.io/about/)
- Repository：[yating-nails/yating-nails.github.io](https://github.com/yating-nails/yating-nails.github.io)
- W04 網站 commit：`71c3bb451f95375438603b2f793f3292ebabdbe7`
- GitHub Actions：Deploy website to GitHub Pages，Run #8，Success；[查看部署執行](https://github.com/yating-nails/yating-nails.github.io/actions/runs/39739019955)
- 推送前先同步並保留 GitHub 上兩筆較新的服務圖片更新（`09cc7a8`、`26d08f8`），再將 W04 提交接續到最新 `main`；沒有強制推送。

## 五張圖片與版位

五張來源 PNG 均存在且可正常解碼，原始檔保留於 `web/` 根目錄。轉檔採 WebP quality 85、Lanczos 等比例縮放；未拉伸圖像。五張 WebP 合計 516,990 bytes，來源 PNG 合計 10,560,147 bytes。

| # | 版位與連結 | 原始 PNG | 正式 WebP | 尺寸／大小 | ALT |
|---:|---|---|---|---:|---|
| 1 | 品牌介紹頁首大圖 | `web/01-about-hero-spa-care.png` | `web/assets/images/photos/01-about-hero-spa-care.webp` | 1672×941／108,276 bytes | 足部日常保養情境示意，雙足置於柔軟毛巾旁，畫面搭配花材、毛巾與保養用品。 |
| 2 | ABOUT YATING 右側品牌圖 | `web/02-about-yating-spa-scene.png` | `web/assets/images/photos/02-about-yating-spa-scene.webp` | 1200×900／104,788 bytes | 人物雙手輕放於腿部，旁有花材與毛巾的品牌氛圍情境圖。 |
| 3 | OUR SERVICES 第 1 張：手部修甲 | `web/03-about-our-services-nail-care.png` | `web/assets/images/photos/03-about-our-services-nail-care.webp` | 1200×900／96,260 bytes | 雙手放在毛巾上，以磨甲工具整理指甲外觀的手部修甲情境示意。 |
| 4 | OUR SERVICES 第 2 張：腳底按摩與肩頸 | `web/04-about-our-services-foot-spa.png` | `web/assets/images/photos/04-about-our-services-foot-spa.webp` | 1200×900／104,490 bytes | 雙足浸於足浴盆，搭配花瓣與毛巾的足部保養情境示意。 |
| 5 | OUR SERVICES 第 3 張：全身指壓與油壓 | `web/05-about-our-services-neck-shoulder-relax.png` | `web/assets/images/photos/05-about-our-services-neck-shoulder-relax.webp` | 1200×900／103,176 bytes | 人物閉眼休息，手部輕觸肩頸的舒適放鬆情境示意。 |

這五張均是使用者提供的 AI 美容情境圖，不標示為店家實景、技師實際施工、顧客真實案例或療效成果。Hero 採 eager/high priority；其餘四張採 lazy loading。圖片標記均提供 `width`、`height`、ALT 與 `object-fit: cover`，卡片比例一致，CSS 依版位設定 `object-position`。

## 服務卡片連結與版面

原 About 頁的三張卡片連結分別為全身指壓與油壓、腳底按摩與肩頸、傳統刮痧，沒有手部修甲卡。為避免把手部修甲照片放到不相關的服務，新增第一張「手部修甲與指甲保養」卡並連到既有 `/services/hand-nail-care/` 頁。其後安排足部照片對應 `/services/foot-massage-shoulder/`，肩頸情境對應 `/services/body-massage/`；原本的刮痧卡保留為第 4 張並沿用原有插畫。既有三條連結及其卡片文字均未更改。

「關於雅婷美甲足體」標題下加入原創 SVG 甲面弧線及香檳金細線，桌機維持水平版、手機置中縮小。裝飾檔為 `web/assets/brand/about-title-ornament.svg`，標記為輔助技術隱藏。Header、Footer、Logo、LINE 浮動按鈕與其他頁面樣式保持原狀。

## 正式站驗收

| 視窗寬度 | 驗收結果 |
|---:|---|
| 1440 px | 四欄服務卡、sticky Header、品牌圖與 Hero 正常；`scrollWidth` 等於可用 `clientWidth`，無水平溢出。 |
| 768 px | 兩欄服務卡、sticky Header 正常；沒有水平溢出。 |
| 390 px | 單欄全寬 4:3 服務照片，主標與紋飾置中；沒有水平溢出。漢堡選單可展開，Escape 可收合，LINE 浮動按鈕位於底部安全區。 |

- 正式站 About HTML、CSS、SVG 及五張 WebP 均 HTTP 200；五張 WebP 在瀏覽器解碼成功。
- 新增的手部修甲頁及原三個服務連結均 HTTP 200。
- 瀏覽器 Console error：0。
- About Title、Description、Canonical、OG/Twitter、JSON-LD、Breadcrumb 與 H1 均與 W04 前版本相同；正文、電話、LINE、價格、robots.txt 及 sitemap.xml 未改。
- W02 首頁 9 張圖片、W03 服務總覽 14 張圖片、其餘 21 個頁面與 13 篇文章未改。

## 產生器與後續

檢查後發現 `.w01_builder.py` 尚保留 About 頁 SVG 舊映射。本輪已將 About 圖片、服務卡映射、標題裝飾與專屬 CSS 同步至本機產生器；建立 `.w01_builder.py.w04.bak` 作為回復副本，沒有執行產生器。此產生器在 Git 中遭既有 `.gitignore` 排除，因此網站部署仍由 `web/` 靜態成品完成。

待後續：W01 圖片規劃中仍有服務文章主圖待製作；不影響 W04 品牌介紹頁上線。

## FIX01｜刮痧服務卡補圖（2026-10-22）

- 將 /about/ 第四張「傳統刮痧放鬆服務」由 gua-sha-relaxation.svg 更換為 06-about-our-services-gua-sha.webp（1200×900）。
- 原始來源 web/06-about-our-services-gua-sha.jpg 保留；WebP ALT 清楚標示為非店家實拍的 AI 情境示意。
- .w01_builder.py 的 About 圖片設定已同步。
- 正式部署及線上驗證以 GitHub Actions 後續結果為準。
