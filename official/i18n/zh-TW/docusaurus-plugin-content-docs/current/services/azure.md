# 微軟 Azure 翻譯

## 簡要說明

1. 官方網站：[微軟 Azure 翻譯](https://learn.microsoft.com/zh-cn/azure/cognitive-services/translator/text-translation-overview)
2. 官方說明：每月翻譯 200 萬字之內都是免費的，如果您每月超過 200 萬字，我們會按照 10 美元 / 100 萬字 的費率收費。詳情參考 [定價說明](https://azure.microsoft.com/zh-cn/pricing/details/cognitive-services/translator/)

## 註冊流程

註冊流程相比其他翻譯服務較為繁瑣，需耐心操作。

參考鏈接：[微軟 Azure 翻譯入門文檔](https://learn.microsoft.com/zh-cn/azure/cognitive-services/translator/document-translation/quickstarts/get-started-with-rest-api?pivots=programming-language-csharp)

## 註冊 Azure 帳戶

第一步，註冊 [Azure](https://azure.microsoft.com/zh-cn/free/cognitive-services/) 帳戶，要求必須綁定國際信用卡(Visa/Master)。如果沒有，將無法註冊。## 註冊 Azure Blob 存儲帳戶

第二步，註冊 [Azure Blob](https://portal.azure.com/#create/Microsoft.StorageAccount) 存儲帳戶。

1. 新建資源組，填寫存儲帳戶名稱
2. 區域選擇一個離你最近的地區，比如香港區域就是 `East Asia`。
3. 剩下的流程只需直接下一步即可。在最後一頁，部署完成後，點擊左下方的藍色按鈕"創建"。

## 創建翻譯工具

第三步，創建 [翻譯工具](https://portal.azure.com/#create/Microsoft.CognitiveServicesTextTranslation)  
1. 區域選擇一個離你最近的地區，比如香港區域就是 `East Asia`。
2. 定價層根據需要選擇，免費用戶可選擇 `Free F0`。免費層不支持文檔翻譯。如有需要可以使用標準 S1 試用。
3. 剩下的流程只需直接下一步即可。在最後一頁，部署完成後，點擊左下方的藍色按鈕"創建"。## 訪問密鑰

部署成功後，進入[Azure儀表板](https://portal.azure.com/#home)，進入**翻譯工具**的頁面，在左側菜單-資源管理-`密鑰和終結點` 找到密鑰。微軟會提供 2 個密鑰，任選其一，將密鑰填入沉浸式擴展-微軟翻譯的 `APIKEY` 裡。

密鑰下方還有一個 `位置/區域` 資訊，例如 `eastasia`，也需要填入沉浸式擴展-微軟翻譯的 `region` 裡。

## 常見問題

如有疑惑的地方，請在 [這裡](https://github.com/immersive-translate/immersive-translate/issues/137) 反饋。