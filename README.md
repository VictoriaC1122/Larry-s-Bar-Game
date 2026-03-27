# 賴瑞的調酒研究室

這個 repo 已整理成可直接部署到 GitHub Pages 的靜態網頁遊戲版本。

## 結構

- `public/index.html`: 遊戲首頁
- `public/assets/`: 前端腳本、樣式與封面
- `public/data/game.xml`: 劇本資料
- `.github/workflows/deploy-pages.yml`: GitHub Pages 自動部署

## 發布到 GitHub Pages

1. 把這份專案推到 `main` 分支。
2. 到 GitHub repo 的 `Settings > Pages`。
3. 在 `Build and deployment` 選 `GitHub Actions`。
4. 等待 `Deploy GitHub Pages` workflow 跑完。

## 本地預覽

需要用靜態伺服器開啟，不能直接雙擊 `index.html`，因為遊戲會讀取 `data/game.xml`。

範例：

```bash
cd public
python3 -m http.server 4173
```

然後打開 `http://localhost:4173`。

## 目前版本的注意事項

- 這版已移除原平台留言區、廣告與平台導流，只保留遊戲本體與簡化控制。
- 快速存讀檔使用瀏覽器本地儲存，不會跨裝置同步。
- 劇情素材目前仍由 `bassadv.com` 載入；如果你要完全獨立、不依賴原平台，下一步需要把 XML 內引用的所有圖片與音樂批次下載到 repo 內。
