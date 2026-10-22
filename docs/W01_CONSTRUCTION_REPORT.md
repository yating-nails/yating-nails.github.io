# YATING-W01 網站施工報告

更新日期：2026-10-22

## 本機成品

- 網站根目錄：`D:\2025客站\雅婷美甲足體\web`
- 靜態可索引頁面：22 頁；其中 13 項服務獨立文章：13 篇。
- 主要頁面：首頁、品牌介紹、服務分類、完整價目表、保養知識索引、3 篇保養指南、聯絡預約、13 篇服務頁。
- 網站技術檔案：`web/index.html`、`web/robots.txt`、`web/sitemap.xml`、`web/404.html`、`web/favicon.ico`、`web/logo.png`、`web/site.webmanifest`、`web/.nojekyll`、CSS、JS、OG 圖、Manifest icons、SVG 插畫。
- 每頁提供繁體中文 SEO title、description、唯一 H1、canonical、Open Graph、Twitter/X、JSON-LD 與圖片 ALT。
- SEO Matrix：`docs/SEO_GEO_PAGE_MATRIX.csv`，逐頁列出 title 字數、metadata、schema、內部連結、ALT 與檢查結果。
- RWD 採桌機、平板、手機斷點；LINE 浮動按鈕有安全區距、易觸控尺寸及手機頁尾留白。
- 網站使用 24 張本專案原創 SVG 視覺插畫（21 張服務／品牌規劃圖加 3 張知識指南圖），不以插畫冒稱店家實景；另外有品牌 Logo、favicon、Apple Touch Icon、192/512px Manifest icons 及 OG 圖。

## 價格與事實管理

- 已列出使用者提供的新版價格：手部修甲 400、足部趾甲修整 500、腳皮／足部角質 600、手部拋光 200、足部拋光 250、按摩 60 分 1,000／90 分 1,400、刮痧 500、拔罐 500、全身去角質 1,000、臉部粉刺清潔／面膜 500、臉部除毛／修眉 200、光療卸除 500 元。
- 單色光療舊版手部 700、足部 800 元只記錄為待確認，沒有作為現行價格或 Offer 結構化資料。
- 店家地址、電話、地標及營業時間依使用者提供資料整理；公休日未確認，頁面要求出發前聯絡確認。
- 網站未放入未核實的顧客評價、認證、設備、店史、社群帳號或授權不明顧客照片。

## SEO/GEO 結果

- 頁面數：22；唯一 Title：22/22；唯一 Description：22/22。
- Title 長度範圍：40–45 字元。SEO title 以 40–45 字元為目標；超出者以自然語意為先，逐頁明列於 CSV。
- Canonical 使用正式絕對網址 `https://yating-nails.github.io/`。
- JSON-LD 依頁面使用 WebPage、BreadcrumbList、NailSalon、WebSite、Service、Article、FAQPage；未建立評價、星等、營業日或未確認服務價格。
- `sitemap.xml` 只列出實際生成的 22 個索引頁；robots 允許索引並指向 sitemap；404 設 noindex。

## RWD 與本機驗收

- 桌機 1440、平板 768、手機 390 寬度均以瀏覽器預覽檢視；三種尺寸無水平溢出。768 以下導覽收合，390 手機單欄服務卡片與 LINE 浮動按鈕均正常。
- 手機選單已實際開啟並點入服務分類頁，確認 `aria-expanded` 正確切換、導覽收合及頁面載入。
- 22 頁程式檢查：Title、Description、H1 各頁唯一，Title 全部 40–45 字元；所有 canonical、OG、Twitter 欄位、ALT、JSON-LD 都存在，JSON-LD 可解析。
- 13 篇服務文章正文各約 648–747 字元；內部連結及本地圖片均指向實際存在檔案；24 個 SVG 全部可解析。
- sitemap 含 22 個實際頁面；robots 允許爬取並指向 sitemap；404 頁有 noindex。本地 HTTP 對首頁、主要分類／服務頁、價目、聯絡、sitemap、robots、logo、favicon、manifest、OG 與 404 檔案回應均為 200。
- 全站禁止宣稱字詞掃描未發現違規招攬用語。正文／底色對比高；LINE 綠底白字已調整至約 5.4:1。
- 手機頁已實際核對電話連結、兩個 Google Maps 導航入口、LINE 固定按鈕及拔罐服務內容。正式站部署後再做 HTTP、主要頁及 Actions 驗收。

## GitHub Pages 部署

- 目標 Repository：`https://github.com/yating-nails/yating-nails.github.io`
- 部署方式：GitHub Actions 從 `web/` 上傳 Pages artifact；工作流程可由 main 更新觸發。
- 工作流程：`.github/workflows/pages.yml`，最小 Pages 權限，發佈 artifact 僅取 `web/`。
- 部署狀態、Commit SHA、Actions 執行結果與正式站 HTTP 驗證於推送後補入。

## 圖片狀態與改善項目

- 原創 SVG 已製作：24 張；其中對應 21 張規劃主圖需求，另含 3 張知識指南插畫；寫實攝影／AI 製作圖：0 張；尚欠寫實圖：21 張。
- 圖片逐張需求、提示詞、ALT、尺寸及路徑：`docs/YATING_IMAGE_PRODUCTION_PLAN.md`。
- 待補事項：取得適當授權後製作 2 張 Hero、2 張品牌氛圍、13 張服務主圖、4 張手足保養細節圖，轉 WebP 並人工驗證裁切及授權。
- 待確認價格：單色光療手部與足部現行價格。
