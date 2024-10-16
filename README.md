# 測試內容

請先將此專案 fork 到自己的 GitHub 上，再進行修改。

baseUrl 將由面試官提供。

文檔網址為 ${baseUrl}/swagger/index.html。

## 測試內容

1. 完成 `BFormControls.vue` 輸入組件的封裝。
2. 用戶資料只有在首次進入畫面時可以去請求。
3. 其餘請依照 `App.vue` 的要求完成。
4. 若發生 500 錯誤，請立即回報，但請先確認你傳送的資料是正確的，而並非是 id 不存在等。

## BFormControls.vue 要求

1. 能使用 v-model 做雙向綁定 (vue3.4 以下作法優先)
2. type參數: 類型String, 預設為text
3. id 不可重複，但允許用戶自行設置


## 額外內容

1. 請將您的專案透過自動化構建方式部屬 如(cloudflare pages、github pages、netlify、vercel 等)
