# QA Report（測試報告）

## Project

Inizio Corporation Website (Frontend Only)

## Date

2026-04-19

## Tester

Kevin

---

# 1. 測試範圍 (Testing Scope)

本次測試針對音樂公司網站前端進行驗證，包含以下範圍：

### 裝置

* Desktop（電腦版）
* Tablet（平板）
* Mobile（手機）

### 語言

* 中文（ZH）
* 英文（EN）
* 日文（JP）

### 測試頁面

* Home
* About
* Music Label
* Artist
* Service
* Our Partner
* Contact Us

---

# 2. 測試項目與結果 (Test Items & Results)

## 2.1 頁面顯示測試 (Page Rendering Test)

| 測試項目   | 說明       | 結果   |
| ------ | -------- | ---- |
| 顯示     | 頁面是否正常載入 | Pass |
| 整體版面   | 無破版、無重疊  | Pass |
| 區塊排版   | 各區塊排列正常  | Pass |
| 圖片顯示載入 | 圖片正常載入   | Pass |
| 文字字體顯示 | 字體與樣式正確  | Pass |

---

## 2.2 響應式測試 (Responsive Test)

| 測試項目       | 說明          | 結果   |
| ---------- | ----------- | ---- |
| Desktop 顯示 | 電腦版顯示正常     | Pass |
| Tablet 顯示  | 平板顯示正常      | Pass |
| Mobile 顯示  | 手機顯示正常      | Pass |
| 區塊自動換行     | 不同螢幕寬度下正常排列 | Pass |
| 圖片等比例縮放    | 圖片不變形       | Pass |

---

## 2.3 連結跳轉測試 (Navigation & Link Test)

| 測試項目              | 說明             | 結果   |
| ----------------- | -------------- | ---- |
| Home 語言切換         | 跳轉至指定語言頁面      | Pass |
| 選單語言切換            | 導覽列語言切換正常      | Pass |
| Sidebar 語言切換      | 側邊欄切換正常        | Pass |
| Footer Logo       | 點擊回首頁（中文版）     | Pass |
| Footer Contact Us | 正常跳轉至聯絡頁       | Pass |
| 社群 Icon           | 正確導向社群平台       | Pass |
| 地址連結              | 導向 Google Maps | Pass |
| Email 連結          | 開啟 mailto      | Pass |
| 電話連結              | 開啟 tel（手機）     | Pass |

---

## 2.4 多語言內容測試 (Multilingual Test)

| 測試項目   | 說明        | 結果   |
| ------ | --------- | ---- |
| 語言頁面對應 | 各語言頁面正確   | Pass |
| 語言切換   | 切換後進入正確頁面 | Pass |
| 語言殘留   | 無混用語言內容   | Pass |
| 排版穩定性  | 不因文字長度破版  | Pass |
| 英日換行   | 換行自然      | Pass |
| 文案一致性  | 按鈕與圖片文字一致 | Pass |

---

## 2.5 圖片與媒體測試 (Image & Media Test)

| 測試項目        | 說明       | 結果   |
| ----------- | -------- | ---- |
| 公司 Logo     | 正常顯示     | Pass |
| Hero Banner | 正常載入     | Pass |
| 社群 Icon     | 正常顯示     | Pass |
| 圖片載入        | 無破圖      | Pass |
| 圖片比例        | 顯示正常     | Pass |
| Lazy Load   | 載入後正常顯示  | Pass |
| Alt 設定      | 已設定圖片描述  | Pass |
| 背景圖裁切       | 不同裝置顯示合理 | Pass |

---

## 2.6 瀏覽器相容性測試 (Browser Compatibility Test)

| 瀏覽器     | 結果   |
| ------- | ---- |
| Chrome  | Pass |
| Safari  | Pass |
| Edge    | Pass |
| Firefox | Pass |

補充：

* 字型、間距、按鈕樣式於各瀏覽器顯示一致

---

## 2.7 效能與載入測試 (Performance Test)

| 測試項目              | 說明                         | 結果   |
|----------------------|------------------------------|--------|
| 首頁載入速度          | 載入時間正常                 | Pass   |
| 圖片壓縮              | 無過大圖片                   | Pass   |
| 首屏延遲              | 無明顯延遲                   | Pass   |
| 頁面切換              | 流暢無卡頓                   | Pass   |
| JS / CSS            | 無明顯冗餘                   | Pass   |
| Lighthouse Performance | 效能評分 99                 | Pass   |
| Lighthouse Accessibility | 無障礙評分 93             | Pass   |
| Lighthouse Best Practices | 最佳實務評分 77          | Pass   |
| Lighthouse SEO        | SEO 評分 100                | Pass   |

### Lighthouse 測試結果說明

本專案使用 Chrome DevTools Lighthouse 進行效能分析，測試結果如下：

- **Performance：99**
- **Accessibility：93**
- **Best Practices：77**
- **SEO：100**

核心指標表現：
- First Contentful Paint (FCP)：0.7 秒
- Largest Contentful Paint (LCP)：0.7 秒
- Total Blocking Time (TBT)：0 ms
- Cumulative Layout Shift (CLS)：0.003

測試結果顯示：
- 頁面載入速度表現優良
- 無明顯阻塞或延遲問題
- 版面穩定性良好（CLS 表現佳）
- SEO 結構完整且符合最佳實務

備註：
- Best Practices 分數尚有優化空間，後續可針對安全性與資源載入策略進行進一步改善
- 完整 Lighthouse 報告請參考 `/docs/lighthouse-report.html`

## 2.8 內容校對測試 (Content Verification Test)

| 測試項目   | 說明                | 結果   |
| ------ | ----------------- | ---- |
| 公司名稱   | 一致正確              | Pass |
| 聯絡資訊   | 電話 / Email / 地址正確 | Pass |
| 服務內容   | 描述正確              | Pass |
| 合作夥伴   | 名稱正確              | Pass |
| 拼字檢查   | 無明顯錯誤             | Pass |
| 多語言一致性 | 中英日內容一致           | Pass |

---

# 3. 測試結果總結 (Summary)

本次測試涵蓋：

* 多裝置（Desktop / Tablet / Mobile）
* 多語言（ZH / EN / JP）
* 多頁面（共 7 個主要頁面）

測試結果：

* 所有測試項目皆為 **Pass**
* 未發現重大 UI / UX 問題
* 響應式設計與多語言切換運作正常
* 導覽與連結功能皆符合預期

---

# 4. 待補充項目 (Pending Items)

無

相關優化建議請參考：
`/docs/optimization.md`

---

# 5. 結論 (Conclusion)

本音樂公司網站前端已完成基本 QA 測試，整體表現穩定：

* 頁面顯示正常
* 響應式設計良好
* 多語言內容一致
* 使用體驗符合預期


