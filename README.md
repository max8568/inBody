# inBody 身體指標追蹤

個人身體組成數據追蹤 App，紀錄每次量測結果並以圖表呈現趨勢。

**Live：** https://max8568.github.io/inBody/

## 功能

- Google 帳號登入（OAuth）
- 新增量測紀錄（體重、BMI、體脂、肌肉量、推定骨量、內臟脂肪、基礎代謝、體內年齡）
- 自動帶入上次數值，方便快速輸入
- 8 項指標折線圖，視覺化趨勢
- 最近 14 筆紀錄列表
- 資料儲存於 Google 試算表

## 技術架構

- **Frontend**：React 19 + Vite
- **樣式**：Tailwind CSS 4
- **圖表**：Recharts
- **資料儲存**：Google Sheets API
- **登入**：Google Identity Services (OAuth 2.0)
- **寫入**：Google Apps Script Web App（不需 OAuth token）
- **部署**：GitHub Pages

## 本地開發

```bash
npm install
npm run dev
```

在 `.env` 設定以下變數：

```
VITE_GOOGLE_CLIENT_ID=...
VITE_SPREADSHEET_ID=...
VITE_SHEETS_RANGE=2026!A:I
VITE_APPS_SCRIPT_URL=...
```

## 部署

```bash
npm run deploy
```

自動 build 並推送至 `gh-pages` branch。
