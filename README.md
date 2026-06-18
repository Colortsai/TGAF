# 臺北生成藝術節 — 太空母艦線上藝廊

科技感 / 星空主題的線上藝廊網站。首頁太空母艦浮動視覺,線上藝廊以星座式錯落排列三個年度主視覺,點入各年度作品列表,再進入單件作品頁(支援圖像、漫畫條漫閱讀器、YouTube 影片嵌入、可播放音樂播放器)。

## 頁面結構

| 檔案 | 說明 |
|------|------|
| `index.html` | 入口(自動導向首頁) |
| `Banner.dc.html` | 首頁 Banner(太空母艦) |
| `Gallery.dc.html` | 線上藝廊(年度主視覺錯落排列) |
| `Year2024.dc.html` | 2024 年度作品列表(海報設計) |
| `Year2025.dc.html` | 2025 年度作品列表(四格漫畫／貼圖／卡面) |
| `Year2026.dc.html` | 2026 年度作品列表(漫畫／圖像／影片／音樂) |
| `Artwork.dc.html` | 單件作品頁(依 `?year=&type=` 切換版型) |
| `support.js` | 頁面執行runtime |
| `assets/` | 圖片、字型、音檔等素材 |

## 部署到 GitHub Pages

1. 建立新 repo,將本資料夾所有檔案上傳到根目錄。
2. Repo → **Settings → Pages** → Source 選 `main` 分支 `/ (root)` → Save。
3. 稍候片刻,網站會發佈於 `https://<帳號>.github.io/<repo 名>/`。

> 已包含 `.nojekyll`,確保所有檔案正常提供。

## 本機預覽

需透過本機伺服器(勿直接雙擊 file://):

```bash
python3 -m http.server
# 開啟 http://localhost:8000
```

## 內容替換

- 各年度作品圖:作品框目前為示意預留位,可換上實際海報/封面。
- 影片:於 `Artwork.dc.html` 的 `YT_ID` 換成參賽影片的 YouTube 影片 ID。
- 音樂:替換 `assets/` 內的封面與 mp3。
- 漫畫條漫:替換 `assets/manga-strip.jpg`(建議寬 800px、長度不限)。
