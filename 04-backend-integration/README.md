# 第四階段：建置免費後台串接（約 5 分鐘）

## 🎯 學習目標
- 了解 Figma Make 可串接的免費後台服務
- 使用 Supabase 建立資料庫
- 讓 AI 生成的介面能讀寫真實資料

## 🛠️ 推薦免費後台方案

| 服務 | 特色 | 免費額度 |
|------|------|---------|
| **Supabase** | PostgreSQL 資料庫 + API，官方推薦 | 500MB / 2個專案 |
| **Firebase** | Google 出品，即時資料庫 | 1GB 儲存 |
| **Airtable** | 試算表式資料庫，操作直覺 | 1,000 筆/Base |
| **PocketBase** | 單檔自架，完全免費 | 無限制（自架） |

---

## 📝 教學步驟：Supabase 串接

### 1. 建立 Supabase 專案
- 前往 [https://supabase.com](https://supabase.com)
- 註冊帳號 → 新增 Project
- 記下 `Project URL` 與 `anon API Key`

### 2. 建立資料表
- 進入 **Table Editor** → New Table
- 範例資料表（以預約系統為例）：
  ```
  appointments
  ├── id (int, primary key)
  ├── patient_name (text)
  ├── doctor (text)
  ├── date (date)
  └── status (text)
  ```

### 3. 在 Figma Make 串接
- 在 Prompt 輸入串接指令：
  ```
  請串接 Supabase 資料庫
  URL: https://xxxxx.supabase.co
  API Key: eyJ...
  從 appointments 資料表讀取預約清單並顯示在畫面上
  ```

### 4. 測試讀寫功能
- 新增一筆資料 → 確認畫面即時更新
- 修改資料表內容 → 確認介面同步

---

## 💡 串接技巧
- API Key 使用 **anon key**（前端公開用），不要用 service key
- 可先在 Supabase 手動新增幾筆假資料，方便測試畫面顯示
- Figma Make 會自動幫你寫 API 呼叫的程式碼

## 📎 參考資源
- [Supabase 官網](https://supabase.com)
- [Supabase 快速入門](https://supabase.com/docs/guides/getting-started)
- [Firebase 官網](https://firebase.google.com)
- [Airtable 官網](https://airtable.com)
