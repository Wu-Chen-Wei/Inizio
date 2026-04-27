# Performance Report

## 總結 (Summary)

- Lighthouse Performance: Excellent (<1s load time)
- 核心效能指標（FCP、LCP、Speed Index）皆 < 1 秒，屬於高效能網站等級
- 使用者幾乎無感載入延遲

---

## 1. 測試目的 (Objective)

本文件用於記錄音樂公司官方網站之前端效能測試結果，透過 Google Lighthouse 分析網站在效能、可存取性、最佳實踐與 SEO 等面向的表現，並作為後續優化依據。

---

## 2. 測試工具 (Tools)

- 工具：Google Lighthouse  
- 版本：13.0.2  
- 測試方式：Chrome DevTools  
- 報告格式：lighthouse-report.html  
- 測試網址：https://inizio-corp.com/

---

## 3. 測試環境 (Environment)

| 項目 | 說明 |
|------|------|
| 裝置 | Desktop（Mac） |
| 瀏覽器 | Google Chrome |
| User Agent | Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) |
| 測試時間 | 2026-04-19 |
| 網路條件 | Lighthouse 預設模擬 |

---

## 4. Lighthouse 測試結果

| 指標 | 數值 | 評級 |
|------|------|------|
| First Contentful Paint (FCP) | 0.7 秒 | Excellent |
| Largest Contentful Paint (LCP) | 0.7 秒 | Excellent |
| Speed Index | 0.9 秒 | Excellent |

---

## 5. 技術分析 (Technical Analysis)

- FCP 與 LCP 均為 0.7 秒，代表首屏內容與主要視覺元素幾乎同步完成渲染
- Speed Index 為 0.9 秒，顯示頁面內容填充速度良好
- 無明顯渲染延遲或阻塞資源

分析結果：
- Rendering pipeline 表現穩定
- 首屏載入效率高
- 使用者可在極短時間內看到完整內容

---

## 6. 後續優化方向 (Future Improvements)

- 圖片格式優化（WebP / AVIF）
- Lazy loading 非首屏資源
- 字型載入優化（font-display）
