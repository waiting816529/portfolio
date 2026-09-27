# 任務計畫 - 新增 AI 履歷分析小助手

## 需求
在網站右下角新增一個 AI 聊天小助手，讓 HR 貼上 JD (職缺描述) 後，自動分析與 Waiting 履歷的適配度。

## 執行步驟
1. [ ] 申請 Google Gemini API Key (需由使用者自行執行並設定網域限制)。
2. [x] 修改 `index.html`：
    - 新增懸浮按鈕 (Floating Action Button) 與聊天視窗 (Chat Window) 的 UI。
    - 撰寫 JavaScript 邏輯：
        - `getResumeContent()`: 自動抓取網頁上的經歷與技能文字。
        - `callGeminiAPI(jdText)`: 呼叫 Gemini 1.5 Flash 模型進行分析。
        - **資安機制**: 程式碼中將預留 `YOUR_API_KEY` 欄位，並加上註解指導使用者設定 HTTP Referrer 限制。
3. [x] 驗證 UI 互動與 API 串接流程。

## 技術決策
- **Model**: Gemini 1.5 Flash (速度快、免費額度高)。
- **Security**: 依賴 Google Cloud 的 HTTP Referrer 限制 (Client-side 唯一解法)。
- **Context**: 動態抓取 DOM 文字，確保分析內容與網頁呈現一致。

# 任務計畫 - SEO 與 GEO 優化 (曝光度提升)

## 需求
透過 SEO (針對 Google 搜尋) 與 GEO (針對 AI 搜尋) 原理，提升履歷網站的被搜尋機率與 AI解讀正確性。

## 執行步驟
1. [x] 修改 `index.html` (Meta Tags)：
    - 優化 `<title>` 與 `<meta description>`，加入高價值關鍵字 (Instructional Design, HRD, Gen-AI)。
    - 新增 `<meta name="keywords">`。
2. [x] 修改 `index.html` (JSON-LD 結構化資料)：
    - 加入 `Person` Schema，定義姓名、職稱、學歷 (嘉義大學)、任職公司 (上銀科技) 與技能標籤。
    - 這是為了讓 Google 和 AI 引擎能「理解」實體關係，而不僅僅是讀取文字。
3. [x] 驗證修改結果。

## 技術決策
- **GEO 策略**: 使用 JSON-LD 讓 AI 快速抓取 "Entity" (實體) 資訊。
- **SEO 策略**: 針對 HR 常用關鍵字 (如：教育訓練管理師, 數位教材) 進行埋設。

# 任務計畫 - 加入網頁瀏覽量統計

## 需求
在網頁頁尾加入網頁瀏覽量統計，使用不蒜子 (Busuanzi) 服務。

## 執行步驟
1. [x] 修改 `index.html`：
    - 引入不蒜子腳本。
    - 在 Footer 加入瀏覽量顯示區塊。
2. [x] 驗證修改結果。

## 技術決策
- 使用 Busuanzi 服務，因為它適合靜態網站且易於整合。
- 樣式將配合現有 Footer 設計，保持簡潔。

# 任務計畫 - 完善學歷資訊

## 需求
將學歷資訊補充完整，包含：國立嘉義大學、數位學習設計與管理學系、碩士。

## 執行步驟
1. [x] 修改 `index.html`：
    - 在學歷 (Education) 區塊補充「數位學習設計與管理學系」。
2. [x] 建立或更新 `README.md`。
3. [x] 驗證修改結果。

## 技術決策
- 保持現有 UI 風格，確保文字在行動裝置與桌面端皆能良好呈現。

# 任務計畫 - 上銀科技新增「組織認同與文化體驗」專案

## 需求
在上銀科技 (HIWIN) 的經歷區塊中新增專案「🤝組織認同與文化體驗」，並採用 STAR 原則結構化呈現：
- S (Situation): 既有選拔與表揚作業仰賴過往經驗，跨單位溝通成本高且缺乏標準化依據。
- T (Task): 梳理辦理流程並建立 SOP，統籌模範員工與資深同仁之年度表揚專案。
- A (Action): 優化評選規範與作業細則，主導選拔機制、活動策劃與現場控場，並輸出標準化 SOP。
- R (Result): 圓滿表彰獲獎及資深同仁，活動滿意度達 4.5 分，落實制度化作業標準。

## 執行步驟
1. [ ] 修改 `index.html`：
    - 在 `#content-hiwin` 經歷區塊中加入 Project 3。
    - 採用與 Project 1, 2 一致之卡片與 STAR 結構，並使用 FontAwesome `fa-handshake` 圖示。
    - 強調關鍵成效數據（滿意度 4.5 分）。
2. [ ] 驗證 HTML 語法與樣式完整性。
3. [ ] 更新 `plan.md` 與 `README.md`。

## 技術決策
- 維持與現有專案卡片一致的 Tailwind CSS class 與 STAR 標籤樣式。
- 使用 `fas fa-handshake` 呈現「組織認同與文化體驗」之意象，確保跨裝置圖示渲染品質與一致性。
- 將成果數據（4.5 分）以 `font-extrabold text-brand-600` 樣式標示，呼應其他專案之重點標記規範。

