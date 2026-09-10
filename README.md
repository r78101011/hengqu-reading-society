# 橫渠閱人社網站

橫渠閱人社的公開介紹網站，使用 Astro 建置並部署至 GitHub Pages。

## 本機開發

```bash
npm install
npm run dev
```

## 建置

```bash
npm run build
```

靜態檔案會產生於 `dist/`。

## 部署

將這個 repository 推送至 GitHub 後，在 repository 的 **Settings → Pages → Build and deployment** 選擇 **GitHub Actions**。之後每次推送到 `main`，`.github/workflows/deploy.yml` 會自動建置並發佈網站。

目前的正式網站網址為：

```text
https://xbridge.maxosoft.com/
```

GitHub Pages 的預設網址仍可使用：

```text
https://r78101011.github.io/hengqu-reading-society/
```

`public/CNAME` 記錄 custom domain，請不要移除；這能讓後續 GitHub Actions 發佈保留網域設定。

Repository: https://github.com/r78101011/hengqu-reading-society

內部資料由外層的 private repository 管理，不應提交到此 public repository。

## 網站內容維護

- 首頁內容與參與常見問題位於 `src/pages/index.astro`。
- 目前活動資訊仍以籌備中呈現。活動時間、頻率、地點、參加對象與報名方式定案後，需同步更新「參與前想知道的事」及 LINE 公告。
- 分享圖為 `public/social-card.png`，SVG 為同版向量來源。更新分享圖時，也要更新首頁的 `socialImageUrl` 版本參數。
- 目前對外身分維持「發起於成功大學 · 社團申請籌備中」；正式核准後需同步調整頁面、分享圖與圖片替代文字。

2026-09-10 已調整桌面欄位排列、手機標題與導覽、首頁加入入口及三種閱讀引言，並新增原生可展開的參與常見問題。
