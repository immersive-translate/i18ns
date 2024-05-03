# 火山翻譯

## 簡要說明

1. 官方網站：[機器翻譯-火山引擎](https://www.volcengine.com/product/machine-translation)
2. 官方資費說明：[產品計費 機器翻譯-火山引擎](https://www.volcengine.com/docs/4640/68515)
3. 火山翻譯每月的前 200 萬字符免費，超出的部分會按照 49 元 / 百萬字符收取費用，具體細節請查看官方資費說明文件。## 申請步驟

1. [API 接入流程概覽 機器翻譯-火山引擎](https://www.volcengine.com/docs/4640/130872)，跟隨官方指導，完成註冊帳號、實名認證、開通服務這三個步驟。需要在控制台進行操作，[火山引擎控制台](https://console.volcengine.com/home)
2. 在第四步獲取密鑰中，火山引擎提供了兩個選項：
   1. 繼續創建（使用主帳號創建密鑰，更便捷，這個 key 可以調用主帳號資源，不太安全），選擇“繼續創建“後，表格裡會出現一條新的數據，其中就包含我們要用到的“Access Key ID“和“Secret Access Key“。
   2. 去新建子用戶（建議使用子用戶創建密鑰，更安全），獲取“Access Key ID“和“Secret Access Key“, 該子帳戶必須擁有`TranslateFullAccess` 權限
3. 打開沉浸式翻譯的基本設置 - 翻譯服務，找到火山翻譯選項填寫。
4. 完成 🎉，如有疑惑的地方，請在 [這裡](https://github.com/immersive-translate/immersive-translate/issues/137) 反饋。