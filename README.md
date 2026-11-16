# 我的腦，我會用！｜三民國小「認識自己的大腦」課程資源

一套可直接上架 GitHub Pages / Netlify 的純靜態網站，提供：

- 1–6 年級課程地圖
- 四大核心主題：記憶的秘密、睡眠與大腦、注意力管理、壓力與情緒
- 16 個核心單元教案（以低／中／高年級為發展階段，並提供二、四年級與高年級延伸調整）
- 每單元：學習目標、教師引導語、活動流程、學生學習單、課後練習、評量與延伸
- 手機、平板、電腦響應式版型
- 單元列印版型（瀏覽器 Ctrl/Cmd + P 亦可）

## 為什麼是 16 個核心單元？

需求中同時出現了「1～6 年級」與「每個年級 4 個主題」，若每一個年級的四主題各做一單元，數量會是 24 個單元。為了兼顧「全校課程地圖」與「教師拿到即可使用」的需求，本版本將 16 個單元定位為四大主題 × 四個發展版本：

- 一年級核心版：同時可供二年級做口語與理由深化
- 三年級策略版：同時可供四年級增加記錄與證據
- 五年級自主版：可延伸到六年級
- 六年級整合版：作為畢業前與升國中準備

因此一～六年級都有課程路徑，但教學資源不會因為年級切換而大量重複。

## GitHub + Netlify 部署

### 方式 A｜最簡單
1. 建立一個 GitHub repository，例如 `sanmin-brain-learning`。
2. 將整個資料夾內容上傳。
3. 登入 Netlify → **Add new project / Import an existing project**。
4. 選擇 GitHub repository。
5. Build command 留空。
6. Publish directory 填 `/` 或 repository root。
7. Deploy。

### 方式 B｜Netlify CLI

```bash
npm install -g netlify-cli
netlify login
netlify init
netlify deploy --prod
```

本專案不需要 Node.js、資料庫或後端。

## 檔案

- `index.html`：網站頁面
- `styles.css`：視覺與響應式樣式
- `app.js`：課程資料、篩選、彈窗與列印功能
- `netlify.toml`：Netlify 基本設定

## 後續可擴充

- 加入學校 LOGO 與校色
- 將 16 單元獨立成可分享 URL
- 增加教師備課紀錄與班級使用檢核
- 增加學生版「我的大腦使用說明書」下載版 PDF
- 加入 20 種 SEL 遊戲資源並串接到同一個教師資源入口
