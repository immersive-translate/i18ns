# 火山翻譯

## 簡要說明

1. 官方網站：[機器翻譯 - 火山引擎](https://www.volcengine.com/product/machine-translation)
2. 官方資費說明：[產品計費 機器翻譯 - 火山引擎](https://www.volcengine.com/docs/4640/68515)
3. 火山翻譯每月的前 200 萬字元免費，超出的部分會按照 49 元 / 百萬字元收取費用，具體細節請檢視官方資費說明文件。

## 申請步驟

4. [API 接入流程概覽 機器翻譯 - 火山引擎](https://www.volcengine.com/docs/4640/130872)，跟隨官方指導，完成註冊帳號、實名認證、開通服務這三個步驟。需要在控制檯進行操作，[火山引擎控制檯](https://console.volcengine.com/home)
5. 在第四步取得金鑰中，火山引擎提供了兩個選項：
   1. 繼續建立（使用主帳號建立金鑰，更便捷，這個 key 可以呼叫主帳號資源，不太安全），選擇“繼續建立“後，表格裡會出現一條新的資料，其中就包含我們要用到的“Access Key ID“和“Secret Access Key“。
   2. 去新建子使用者（建議使用子使用者建立金鑰，更安全），取得“Access Key ID“和“Secret Access Key“, 該子帳戶必須擁有`TranslateFullAccess` 權限
6. 開啟沉浸式翻譯的基本設定 - 翻譯服務，找到火山翻譯選項填寫。
7. 完成 🎉，如有疑惑的地方，請在 [這裡](https://github.com/immersive-translate/immersive-translate/issues/137) 回饋。
