# Performance Report

## 🔥 Summary

- **Lighthouse Performance: Excellent (<1s load time)**
- 首屏渲染時間 < 1 秒，屬於高效能網站等級
- 使用者幾乎無感載入延遲

---

## 1. 測試目的 (Objective)

本文件用於記錄音樂公司官方網站（https://inizio-corp.com/）之前端效能測試結果，  
透過 Google Lighthouse 分析網站在效能、可存取性、最佳實踐與 SEO 等面向的表現，  
並作為後續優化依據。

---

## 2. 測試工具 (Tools)

- 工具：Google Lighthouse  
- 版本：13.0.2  
- 測試方式：Chrome DevTools  
- 報告格式：HTML 匯出報告  
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

## 4. Lighthouse 測試結果（首頁）

### 4.1 Core Metrics

| 指標 | 數值 | 評級 |
|------|------|------|
| First Contentful Paint (FCP) | 0.7 秒 | ⭐ Excellent |
| Largest Contentful Paint (LCP) | 0.7 秒 | ⭐ Excellent |
| Speed Index | 0.9 秒 | ⭐ Excellent |

👉 整體評估：**載入速度非常優秀（< 1 秒）**

---

### 4.2 Performance Visualization

```text
Performance Metrics

FCP         | ████████████████████ 0.7s
LCP         | ████████████████████ 0.7s
Speed Index | ██████████████████   0.9s
