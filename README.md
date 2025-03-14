# LINE App

這是一個使用 LINE LIFF (LINE Front-end Framework) 開發的網頁應用。
這個應用程序可以讓用戶通過 LINE 帳號登入並查看其個人資料。

## 功能特點

- 使用 LINE 登入
- 顯示用戶資料
- 支持在 LINE 應用內和瀏覽器中運行
- 自動部署到 Vercel

## 技術棧

- HTML5
- JavaScript
- LINE LIFF SDK
- Vercel (托管平台)

## 開發設置

1. 克隆倉庫：
```bash
git clone https://github.com/hyder13/lineapp.git
cd lineapp
```

2. 在 [LINE Developers Console](https://developers.line.biz/console/) 設置：
   - 創建一個新的 Provider（如果還沒有）
   - 創建一個新的 Channel
   - 添加 LIFF 應用
   - 設置 Endpoint URL

3. 在 `index.html` 中更新 LIFF ID：
```javascript
await liff.init({ liffId: 'YOUR_LIFF_ID' });
```

## 部署

本項目使用 Vercel 進行自動部署。每次推送到 main 分支時都會自動部署。

訪問地址：[https://lineapp-taupe.vercel.app/](https://lineapp-taupe.vercel.app/)

## 本地開發

建議使用 Live Server 或類似工具來運行本地開發服務器：

1. 使用 VS Code 的 Live Server 擴展
2. 或使用 Python 的簡單 HTTP 服務器：
```bash
python -m http.server 8000
```

## 注意事項

- 確保在 LINE Developers Console 中設置了正確的 Endpoint URL
- 在本地開發時，需要使用 HTTPS 或 localhost
- 記得更新 LIFF ID 為您自己的 ID 