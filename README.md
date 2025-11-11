# 隱私權政策中心 Privacy Policy Hub

這是一個用於管理多個 App 隱私權政策的靜態網站，部署在 GitHub Pages 上。

## 📁 專案結構

```
privacy-policy/
├── index.html          # 首頁（導航頁面）
├── app1-privacy.html   # App 1 隱私政策
├── app2-privacy.html   # App 2 隱私政策（需自行創建）
├── app3-privacy.html   # App 3 隱私政策（需自行創建）
├── style.css           # 通用樣式
└── README.md           # 說明文件
```

## 🚀 部署到 GitHub Pages

### 步驟 1：創建 GitHub 倉庫

1. 到 GitHub 創建一個新倉庫
   - 倉庫名稱建議：`privacy-policies` 或 `app-privacy`
   - 設為 Public（公開）

### 步驟 2：推送代碼

```bash
# 初始化 Git（如果還沒初始化）
git init

# 添加所有檔案
git add .

# 提交
git commit -m "Initial commit: Privacy policy hub"

# 連接到 GitHub 倉庫（替換成你的倉庫 URL）
git remote add origin https://github.com/你的用戶名/倉庫名.git

# 推送到 GitHub
git branch -M main
git push -u origin main
```

### 步驟 3：啟用 GitHub Pages

1. 到你的 GitHub 倉庫頁面
2. 點擊 **Settings**（設定）
3. 在左側菜單找到 **Pages**
4. 在 **Source** 下拉選單中選擇 **main** 分支
5. 資料夾選擇 **/ (root)**
6. 點擊 **Save**
7. 等待幾分鐘，你的網站就會發布在：`https://你的用戶名.github.io/倉庫名/`

## ➕ 如何添加新的 App

### 方法 1：複製現有模板

1. 複製 `app1-privacy.html` 並重新命名（例如：`app4-privacy.html`）
2. 修改內容：
   - 更新 `<title>` 標籤
   - 更新 `<h1>` App 名稱
   - 修改隱私政策內容
   - 更新聯絡資訊

### 方法 2：在首頁添加新卡片

編輯 `index.html`，在 `<main class="app-grid">` 中添加：

```html
<div class="app-card">
    <div class="app-icon">🎯</div>
    <h2 class="app-name">新 App 名稱</h2>
    <p class="app-description">App 簡短描述</p>
    <a href="new-app-privacy.html" class="btn-primary">查看隱私權政策</a>
</div>
```

## 🎨 自訂樣式

所有樣式都在 `style.css` 中，你可以修改：
- 顏色配置（目前使用紫色漸變）
- 字體大小
- 卡片樣式
- 響應式斷點

## 📝 更新隱私政策

1. 編輯對應的 HTML 檔案
2. 修改「最後更新日期」
3. 提交並推送到 GitHub

```bash
git add .
git commit -m "Update privacy policy for App X"
git push
```

## 🔗 網址結構

- 首頁：`https://你的用戶名.github.io/倉庫名/`
- App 1：`https://你的用戶名.github.io/倉庫名/app1-privacy.html`
- App 2：`https://你的用戶名.github.io/倉庫名/app2-privacy.html`

## 📱 圖示建議

你可以更換 `app-icon` 中的 emoji：
- 📱 手機 App
- 🎮 遊戲
- 🎵 音樂
- 📷 相機
- 💬 社交
- 🏃 健康
- 📚 教育
- 🛍️ 購物

## 📞 聯絡資訊

記得在每個隱私政策頁面中更新：
- 電子郵件地址
- 公司地址
- App 名稱
- 最後更新日期
