# 百樂居家呼吸照護所 - FAQ 管理系統

## 📋 系統說明

這是一個為百樂居家呼吸照護所設計的 FAQ 管理與查詢系統，包含：

1. **系統管理網頁** (`admin.html`) - FAQ 資料管理
2. **使用者查詢網頁** (`index.html`) - 民眾查詢介面
3. **PWA 支援** - 可安裝至手機/電腦，支援離線查詢

## 🚀 功能特色

### 系統管理網頁 (admin.html)

- ✅ FAQ 新增/編輯/刪除
- ✅ 分類管理
- ✅ CSV 檔案上傳/下載
- ✅ 與 GitHub 同步（自動存檔）
- ✅ 無需登入，直接使用

### 使用者查詢網頁 (index.html)

- ✅ 文字輸入查詢
- ✅ 語音輸入（麥克風）
- ✅ 語音播放答案
- ✅ 智慧搜尋 FAQ 資料庫
- ✅ Claude API 整合（FAQ 無答案時使用）
- ✅ PWA 支援（可離線使用）
- ✅ 響應式設計（手機/平板/電腦）

## 📦 檔案結構

```
health/
├── admin.html          # 系統管理網頁
├── index.html          # 使用者查詢網頁
├── manifest.json       # PWA 設定檔
├── sw.js              # Service Worker（離線支援）
├── FAQ.csv            # FAQ 資料（由系統產生）
├── class.csv          # 分類資料（由系統產生）
└── README.md          # 說明文件
```

## 🔧 部署到 GitHub Pages

### 1. 上傳檔案到 GitHub

將所有檔案上傳至您的 GitHub Repository：
- Repository: `shui1133/health`

### 2. 啟用 GitHub Pages

1. 進入 Repository 設定
2. 左側選單點選 "Pages"
3. Source 選擇 "main" 分支
4. 資料夾選擇 "/ (root)"
5. 點選 "Save"

### 3. 訪問網站

等待約 1-2 分鐘後，您的網站將可在以下網址訪問：

- **系統管理**: `https://shui1133.github.io/health/admin.html`
- **使用者查詢**: `https://shui1133.github.io/health/index.html`

## 🎯 使用說明

### 系統管理員

1. 開啟 `admin.html`
2. 在「FAQ 管理」分頁：
   - 點選「新增 FAQ」新增問答
   - 或上傳 CSV 檔案批次匯入
   - 編輯完成後點選「儲存至 GitHub」
3. 在「分類管理」分頁：
   - 管理 FAQ 分類選項

### 一般使用者

1. 開啟 `index.html`
2. 輸入問題或點選麥克風使用語音
3. 系統自動搜尋 FAQ 資料庫
4. 若 FAQ 無答案且有設定 API Key，將使用 Claude AI 回答
5. 可點選「語音播放最後回答」聆聽答案

### Claude API 設定（選填）

如需使用 AI 智慧回答功能：

1. 前往 [Anthropic Console](https://console.anthropic.com/)
2. 取得 API Key
3. 在查詢網頁輸入 API Key
4. API Key 將儲存於瀏覽器本地

**注意**：API Key 僅在 FAQ 資料庫找不到答案時才會使用。

## 📱 PWA 安裝

### Android / Chrome

1. 開啟 `index.html`
2. 點選瀏覽器選單的「新增至主畫面」
3. 確認安裝

### iOS / Safari

1. 開啟 `index.html`
2. 點選分享按鈕
3. 選擇「加入主畫面」

## 🔒 安全性說明

- ✅ FAQ 資料不含敏感資訊，無需加密
- ✅ GitHub Token 用於系統存檔，已內建於程式碼
- ⚠️ Claude API Key 由使用者自行輸入，儲存於瀏覽器本地
- ⚠️ 建議定期更換 GitHub Token

## 🛠️ 技術規格

- **前端框架**: 純 HTML/CSS/JavaScript
- **語音功能**: Web Speech API
- **儲存方式**: GitHub API
- **AI 整合**: Anthropic Claude API
- **PWA 支援**: Service Worker + Manifest
- **瀏覽器支援**: Chrome / Edge / Safari（建議 Chrome）

## 📊 資料格式

### FAQ.csv 格式

```csv
項次,分類,問題說明,答案內容
1,"健保給付","呼吸器租用健保有給付嗎？","是的，符合條件者健保有給付..."
2,"補助申請","如何申請氧氣機補助？","申請流程如下：1. 備妥醫師診斷證明..."
```

### class.csv 格式

```csv
分類名稱
健保給付
補助申請
居家照護
設備租用
```

## 🆘 常見問題

### Q: FAQ 資料無法載入？
A: 請確認 GitHub Repository 中有 `FAQ.csv` 檔案，並已正確設定。

### Q: 語音功能無法使用？
A: 請確認：
- 使用 Chrome 或 Edge 瀏覽器
- 已允許網站使用麥克風權限
- 網站使用 HTTPS 連線

### Q: Claude API 無法使用？
A: 請確認：
- API Key 正確無誤
- API Key 有足夠額度
- 網路連線正常

## 📞 聯絡資訊

**百樂居家呼吸照護所**

如有任何問題或建議，歡迎聯繫系統管理員。

---

**版本**: 1.0.0  
**最後更新**: 2026-02-01
