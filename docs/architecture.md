# 網站架構說明（Architecture）

**專案名稱：** 音樂公司官方網站  
**文件類型：** 網站架構說明  
**更新日期：** 2026-04-19

---

## 1. 專案概述

本專案為 Inizio 音樂公司官方網站之前端整理版本，原始內容來自 WordPress 匯出頁面，後續將版面、資源與檔案結構重新整理為較乾淨的靜態前端架構。

專案主要目標包含：

- 建立清晰的前端專案結構
- 整理多語系頁面
- 優化靜態資源管理
- 建立響應式畫面展示
- 作為前端作品集展示專案

網站主要用途包含：

- 公司品牌形象展示
- 音樂品牌與藝人介紹
- 服務項目說明
- 商業合作夥伴展示
- 聯絡資訊提供

---

## 2. 網站整體架構（Site Map）

```text
Home
├── About
├── Music Label
├── Artist
├── Service
├── Our Partner
└── Contact Us
```

---

## 3. 網站頁面說明

| 頁面 | 說明 |
|------|------|
| Home | 首頁主視覺與品牌導覽 |
| About | 公司介紹與品牌理念 |
| Music Label | 音樂品牌與內容展示 |
| Artist | 藝人資訊與形象展示 |
| Service | 公司服務項目介紹 |
| Our Partner | 合作夥伴展示 |
| Contact Us | 聯絡資訊與聯絡方式 |

---

## 4. 多語系架構

本專案包含多語系頁面：

- 中文（zh）
- 英文（eng）
- 日文（jp）

### 語系管理策略

- 各語系採獨立 HTML 管理
- 降低動態切換造成的複雜度
- 保持靜態頁面結構清晰
- 方便後續轉換為 i18n 架構

---

## 5. 頁面與語系對應

| 頁面名稱 | 中文 | 英文 | 日文 |
|----------|------|------|------|
| Home | ✓ | ✓ | ✓ |
| About | ✓ | ✓ | ✓ |
| Music Label | ✓ | ✓ | ✓ |
| Artist | ✓ | - | - |
| Service | ✓ | ✓ | ✓ |
| Our Partner | ✓ | - | - |
| Contact Us | ✓ | - | - |

---

## 6. 專案資料夾結構

```bash
inizio/
│
├── assets/                        # 靜態資源
│   │
│   ├── fonts/                     # 字型資源
│   │
│   ├── images/                    # 網站圖片素材
│   │
│   ├── wireframes/                # Figma 響應式畫面整理與 UI 參考檔
│   │   ├── desktop.pdf
│   │   ├── tablet.pdf
│   │   └── mobile.pdf
│   │
│   └── screenshots/               # 專案畫面截圖
│       │
│       ├── desktop/               # Desktop 響應式截圖
│       │   ├── about/
│       │   ├── artist/
│       │   ├── contact-us/
│       │   ├── home/
│       │   ├── music-label/
│       │   ├── our-partner/
│       │   └── service/
│       │
│       ├── tablet/                # Tablet 響應式截圖
│       │   ├── about/
│       │   ├── artist/
│       │   ├── contact-us/
│       │   ├── home/
│       │   ├── music-label/
│       │   ├── our-partner/
│       │   └── service/
│       │
│       └── mobile/                # Mobile 響應式截圖
│           ├── about/
│           ├── artist/
│           ├── contact-us/
│           ├── home/
│           ├── music-label/
│           ├── our-partner/
│           └── service/
│
├── src/                           # 前端原始碼
│   │
│   ├── css/                       # CSS 樣式檔案
│   │   ├── plover-animation.css
│   │   ├── plover-elements-button.css
│   │   ├── plover-theme-button.css
│   │   ├── wp-core-columns.css
│   │   ├── plover-dark-mode.css
│   │   ├── plover-animation-flip.css
│   │   ├── post-views-counter.css
│   │   ├── magic-liquidizer-table.css
│   │   ├── vexis-theme.css
│   │   ├── wp-block-cover.css
│   │   └── wp-block-gallery.css
│   │
│   ├── javascript/                # JavaScript 功能腳本
│   │   ├── jquery.min.js
│   │   ├── jquery-migrate.min.js
│   │   ├── magic-liquidizer-table.min.js
│   │   ├── plover-particles-effect.min.js
│   │   ├── plover-scroll-observer.min.js
│   │   ├── plover-entrance-animation.min.js
│   │   └── wp-dom-ready.min.js
│   │
│   └── html/                      # HTML 頁面
│       │
│       ├── about/
│       │   ├── about-zh.html
│       │   ├── about-eng.html
│       │   └── about-jp.html
│       │
│       ├── artist/
│       │   └── artist.html
│       │
│       ├── contact-us/
│       │   └── contact-us.html
│       │
│       ├── home/
│       │   ├── home-zh.html
│       │   ├── home-eng.html
│       │   └── home-jp.html
│       │
│       ├── music-label/
│       │   ├── music-label-zh.html
│       │   ├── music-label-eng.html
│       │   └── music-label-jp.html
│       │
│       ├── our-partner/
│       │   └── our-partner.html
│       │
│       └── service/
│           ├── service-zh.html
│           ├── service-eng.html
│           └── service-jp.html
│
├── docs/                          # 專案文件
│   ├── architecture.md            # 網站架構說明
│   ├── design-concept.md          # 設計概念
│   ├── optimization.md            # 優化紀錄
│   ├── performance.md             # 效能分析
│   ├── qa-report.md               # 測試報告
│   ├── lighthouse-report.html     # Lighthouse HTML 報告
│   └── lighthouse-report.pdf      # Lighthouse PDF 報告
│
└── README.md                      # 專案總說明
```

---

## 7. 響應式設計（Responsive Design）

本專案包含多裝置畫面整理與展示：

| 裝置類型 | 說明 |
|----------|------|
| Desktop | 桌面版畫面 |
| Tablet | 平板版畫面 |
| Mobile | 手機版畫面 |

### 響應式整理方式

- 各頁面依裝置類型分類截圖
- 保留完整頁面與區塊畫面
- 方便後續 UI / UX 檢視與比較

---

## 8. Wireframe 架構

專案包含不同裝置版本的 Wireframe：

- Desktop Wireframe
- Tablet Wireframe
- Mobile Wireframe

主要作為：

- 版面規劃參考
- 響應式結構整理
- UI 架構分析

---

## 9. 前端結構設計

### 9.1 HTML 結構

- 以頁面為單位拆分 HTML
- 各語系獨立管理
- 保持靜態結構可讀性

### 9.2 CSS 結構

目前 CSS 主要保留 WordPress 匯出樣式，後續將逐步整理：

- 共用樣式
- 響應式樣式
- 元件化樣式

### 9.3 JavaScript 結構

目前保留原始 JavaScript 功能腳本，後續將逐步整理：

- 導覽功能
- 動畫效果
- 響應式互動功能

---

## 10. 架構設計原則

本專案整理過程中遵循以下原則：

### 可讀性（Readable）
- 移除過多 WordPress 殘留結構
- 保持資料夾命名一致性

### 可維護性（Maintainable）
- 依頁面分類管理
- 靜態資源獨立整理

### 可擴展性（Scalable）
- 保留未來元件化可能
- 可逐步轉換為 React / Next.js 架構

### 資源集中管理（Organized Assets）
- 圖片與截圖統一整理
- Wireframe 與文件集中管理

---

## 11. 後續優化方向

後續可持續優化項目包含：

- 重構 CSS 架構
- 清理 WordPress 殘留 class
- 建立共用元件（Header / Footer）
- 增加模組化 JavaScript
- 優化 Lighthouse 效能
- 增加 SEO 與 Accessibility 優化
- 導入 Component-based 架構

---

## 12. 專案文件說明

| 文件名稱 | 說明 |
|----------|------|
| architecture.md | 網站架構說明 |
| design-concept.md | 設計理念與版面概念 |
| optimization.md | 網站優化紀錄 |
| performance.md | 效能分析 |
| qa-report.md | 測試與檢查報告 |
| lighthouse-report.html / lighthouse-report.pdf | Lighthouse 效能報告 |

---

## 13. 備註

本專案目前以靜態前端整理與作品集展示為主，主要目標為：

1. 重整 WordPress 匯出內容
2. 建立清晰專案架構
3. 建立多語系與響應式整理
4. 作為前端作品集展示專案
5. 提升前端專案管理與文件化能力
