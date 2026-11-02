# 하루 한국어

韓文初級複習網站，原生 HTML/CSS/JavaScript，無需 npm 安裝。

## 啟動

在專案資料夾執行：

```bash
python -m http.server 8000
```

瀏覽 http://localhost:8000 。不要直接雙擊 index.html，因為瀏覽器可能禁止從 file:// 讀取 JSON。

## 部署 GitHub Pages

把 `index.html` 和 `data/questions.json` 上傳至 GitHub repository 根目錄，前往 Settings → Pages → Build and deployment → Deploy from a branch → main / (root) → Save。

## 題庫

`data/questions.json` 包含 vocabulary 和 sentences 兩個陣列。每題有 id、lesson、category、zh、ko、alternatives。可透過網站匯入 JSON 或 CSV，匯入的題庫會取代目前題庫並儲存於本機瀏覽器。CSV 的 type 使用 vocabulary 或 sentences；alternatives 以 `|` 分隔。示範題庫是原創練習素材，非教材原文。

## 注意

- 答題紀錄和自訂題庫使用 localStorage，僅限目前瀏覽器，清除網站資料後會消失。
- 朗讀需瀏覽器支援 Web Speech API 且裝置具備韓文語音。
- 翻譯採用題庫列出的標準答案與可接受答案，不會自動辨識所有語意相同的自由翻譯。
