# 網站架構說明（Architecture）

## 1. 專案概述
本專案為音樂公司官方網站之前端整理版本，原始內容來自 WordPress 匯出頁面，後續將版面、資源與結構重新整理為較乾淨的前端展示架構。

網站主要用途包含：
- 公司品牌形象展示
- 音樂品牌與藝人介紹
- 服務項目說明
- 商業合作夥伴展示
- 聯絡資訊提供

---

## 2. 網站整體架構（Site Map）
Home
├── About
├── Music Label
├── Artist
├── Service
├── Partners
└── Contact

---

## 3. 網站頁面說明

| 頁面 | 說明 |
|------|------|
| Home | 主視覺、品牌導覽 |
| About | 公司理念與介紹 |
| Music Label | 音樂品牌展示 |
| Artist | 藝人資訊 |
| Service | 服務項目 |
| Partners | 合作夥伴 |
| Contact | 聯絡資訊 |

---

## 4. 多語系架構

本專案包含多語系頁面：

- 中文（zh）
- 英文（en）
- 日文（jp）

### 語系策略
- 各語系採「獨立 HTML」管理
- 避免動態切換造成結構複雜
- 方便後續轉為 i18n 架構

---

## 5. 頁面與語系對應

| 頁面名稱 | 中文 | 英文 | 日文 |
|----------|------|------|------|
| Home | ✓ | ✓ | ✓ |
| About | ✓ | ✓ | ✓ |
| Music Label | ✓ | ✓ | ✓ |
| Artist | ✓ | - | - |
| Service | ✓ | ✓ | ✓ |
| Partners | ✓ | - | - |
| Contact | ✓ | - | - |

---

## 6. 專案資料夾結構

```bash
project-name/
│
├── src/                     # 前端頁面原始碼
│   ├── home/               # 首頁
│   ├── about/              # 關於我們
│   ├── music-label/        # 音樂品牌
│   ├── artist/             # 藝人
│   ├── service/            # 服務
│   ├── partners/           # 合作夥伴
│   └── contact/            # 聯絡我們
│
├── assets/                 # 靜態資源
│   ├── images/             # 圖片素材
│   └── screenshots/        # 專案截圖
│
├── docs/                   # 專案文件
│   ├── architecture.md
│   ├── qa-report.md
│   ├── performance.md
│   ├── optimization.md
│   └── design.md
│
└── README.md               # 專案說明
