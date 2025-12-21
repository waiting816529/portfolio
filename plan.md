# 任務計畫 - 更新競賽獎項顏色

## 需求
將「全國大專院校 StoryMap 競賽」的「優選」與「國際華文暨教育盃電子書創作大賽」的「佳作」文字顏色改為與「全國大專院校倫理個案分析」的「第三名」一致的藍色 (`text-brand-600`)。

## 執行步驟
1. [x] 讀取 `index.html` 尋找目標元素。
2. [x] 在 `plan.md` 中記錄執行計畫。
3. [x] 修改 `index.html`：
    - 將 `全國大專院校StoryMap競賽` 下方的 `優選` 類別從 `text-slate-400` 改為 `text-brand-600`。
    - 將 `國際華文暨教育盃電子書創作大賽` 下方的 `佳作` 類別從 `text-slate-400` 改為 `text-brand-600`。
4. [x] 驗證修改結果。
5. [x] 移除 `index.html` 中的 AI 履歷助手 (HTML & JavaScript)。

## 技術決策
- 使用 Tailwind CSS 類別 `text-brand-600` 來確保顏色一致性。
- `text-brand-600` 在 `portfolioConfig` 中定義為 `#0284c7`。
