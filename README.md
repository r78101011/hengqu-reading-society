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

這個專案預設部署為 GitHub project site；網址格式為：

```text
https://<GitHub 帳號>.github.io/<repository 名稱>/
```

內部資料由外層的 private repository 管理，不應提交到此 public repository。
