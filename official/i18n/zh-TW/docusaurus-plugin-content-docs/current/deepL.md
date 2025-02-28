# DeepL

目前有 2 種方式使用 DeepL 翻譯服務：

## 1. 透過開通[沉浸式翻譯 Pro 會員](https://immersivetranslate.com/pricing/) 後直接使用 DeepL 翻譯服務（推薦）

[點此查看介紹](https://immersivetranslate.com/pricing/)

## 2. 透過 DeepL 官方獲取 DeepL API

1. 官方介紹：[DeepL API ](https://www.deepl.com/zh/pro#developer)
   - 注意： [DeepL API](https://www.deepl.com/zh/pro#developer) 和 [DeepL Pro](https://www.deepl.com/pro) 是兩種不同的帳戶類型，在沉浸式翻譯裡使用的是 [DeepL API](https://www.deepl.com/zh/pro/select-country#developer) 帳戶。
2. [為什麼](https://www.deepl.com/zh/whydeepl)選擇 DeepL?

   - 英語 ⇄ 中文 5 倍更準確
   - 英語 ⇄ 日語 6 倍更準確
   - 翻譯引擎基於人工智慧技術（神經網路）

3. Deepl API 分為 [Free API 和 Pro API](https://www.deepl.com/zh/pro#developer)

   - 其中 Free API 每月提供 50 萬免費字元額度。
   - Pro API 的[官方費用](https://www.deepl.com/zh/pro#developer)是：每 100 萬字元 25 美元。
   - 對於高頻使用的用戶，一個月消耗的字元量大約是 1000 萬字元，價格大約為：250 美元

4. 註冊帳號和開通 [DeepL API](https://www.deepl.com/zh/pro#developer)，需要提供一張 DeepL [支持的國家或地區](https://support.deepl.com/hc/zh-cn/articles/360020016339-DeepL-Pro%E5%9C%A8%E6%88%91%E6%89%80%E5%9C%A8%E5%9B%BD%E5%AE%B6%E6%97%A0%E6%B3%95%E8%AE%A2%E9%98%85)發行的 VISA 或 MASTER 信用卡，可惜的是，目前國內發行的任何信用卡（包括雙幣卡和外幣卡）均不被支持。

## 自建 DeepL API

我們正在 Beta 特性裡實驗支持自建的 DeeplX 服務（但是經測試，該服務並不太適合作為網頁翻譯的服務。由於網頁翻譯要求的 API 請求量巨大，如果搭建此服務請務必做好負載均衡）,以下為如何開啟該實驗特性的說明：

1. 開發者設定中開啟 Beta 測試特性
2. 翻譯服務中找到 DeepLX(Beta)，輸入自建 DeepL API URL，如 http://your-domain/translate

> Q：如何自建？  
> A：[OwO-Network/DeepLX](https://github.com/OwO-Network/DeepLX#setup-on-immersive-translate)或是[zu1k/deepl](https://github.com/KyleChoy/zotero-pdf-translate/blob/CustomDeepL/README.md)

## 常見問題

### 1. 填入的密鑰不可用。

DeepL API Pro 和 DeepL Pro 是兩種帳戶，可以在沉浸式翻譯裡使用的 Auth Key 是 DeepL API 帳戶，請點擊這裡查看[DeepL API Pro](https://www.deepl.com/zh/pro/select-country#developer)

### 2. 提示 401,403 無權限錯誤

出現這類錯誤可能是因為您使用了錯誤的密鑰類型。請注意：

1. DeepL有兩種不同的產品：DeepL Pro（翻譯服務）和DeepL API（開發接口）
2. DeepL Pro帳戶中看到的密鑰**不適用**於API調用
3. 您需要專門註冊DeepL API帳戶並獲取API密鑰
4. DeepL Free API Key 的標識是以`:fx`結尾的
5. DeepL Pro API Key 的標識沒有`:fx`，就是正常的一串密鑰

請確保您已正確註冊了DeepL API 服務，而不僅僅是DeepL Pro翻譯服務。

### 3. 456, Quota for user has been reached.

使用量已超過 DeepL 官方為每個用戶設定的硬限制上限，你可能已違反了 DeepL 的合理使用政策，最好避免此類行為。如果是付費用戶的話，下個月會自動重置用量。