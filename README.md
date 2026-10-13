# AeroRail 旅程決策雛型

正式網站式靜態 Prototype，供 HackRail PN-0026「AeroRail：機捷機場旅程決策助理」展示與截圖使用。

## 目的

- 手機優先展示出境旅程決策卡。
- 同一風格安排入境接續交通情境。
- 顯示建議依據、資料來源、更新時間與推估層級。
- 顯示系統資料資訊流與匿名彙整營運參考。

## 頁面狀態

- `/?view=home`：網站首頁／今天目的選擇
- `/?view=input`：輸入畫面（可搭配 `&mode=inbound` 顯示入境輸入）
- `/?view=outbound`：出境旅程決策卡
- `/?view=evidence`：建議依據檢視
- `/?view=inbound`：入境接續旅程決策卡
- `/?view=flow`：系統資料資訊流
- `/?view=ops`：匿名彙整營運參考

## 本機預覽

本專案是可直接編輯的單一 HTML 原型，CSS、JavaScript 與示範情境都在 `index.html` 中；不需 npm 安裝或建置，也不包含後端 API 或資料庫。

在專案目錄執行（需要 Python 3）：

```bash
python3 -m http.server 8080 --bind 127.0.0.1
```

使用瀏覽器開啟 <http://127.0.0.1:8080/>。

## 檔案

- `index.html`：完整靜態前端原始碼。
- `screenshots/`：既有展示截圖與合成預覽圖。
- `.gitignore`：排除帳密、私鑰、資料庫與開發暫存檔案。

## 注意

目前使用模擬資料與規則式情境切換，不宣稱正式即時營運服務。GPS 按鈕需要瀏覽器支援、使用者授權及安全來源（HTTPS 或 localhost）；一般 HTTP 公開網址可能無法取得定位。

本 repository 不包含自動部署設定；GitHub 更新不會自動修改運行中的展示網站。
