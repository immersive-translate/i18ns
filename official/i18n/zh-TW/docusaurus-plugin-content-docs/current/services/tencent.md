# 騰訊翻譯君

## 簡要說明

1. 官方網站：[機器翻譯\_智能翻譯\_自動翻譯-騰訊雲](https://cloud.tencent.com/product/tmt)
2. 官方資費說明：[機器翻譯 計費概述-購買指南-文檔中心-騰訊雲](https://cloud.tencent.com/document/product/551/35017)
3. 付費版每月的前 500 萬字符免費，超出的部分會按照 58 元 / 百萬字符收取費用，請關注使用額度，以免意外扣費。## 申請步驟

1. 打開 [騰訊雲官網](https://cloud.tencent.com/) 並登錄，登錄成功後，鼠標移動到頁面右上角的頭像上，選擇“賬號信息”進行個人認證。使用騰訊雲機器翻譯必須進行個人認證，已認證過的話可以跳過。
2. 打開 [機器翻譯\_智能翻譯\_自動翻譯-騰訊雲](https://cloud.tencent.com/product/tmt)，點擊“立即使用”按鈕。登錄之後，會進入騰訊機器翻譯服務控制台。
3. 選擇開通付費版。
4. 創建訪問密鑰。將鼠標懸停在網頁右上角的頭像上，然後選擇 [訪問管理](https://console.cloud.tencent.com/cam/overview)，然後在左側菜單選擇 [訪問密鑰 - API 密鑰管理](https://console.cloud.tencent.com/cam/capi)，最好不要直接創建密鑰，因為主賬號創建的密鑰可以訪問調用你賬號裡的所有資源，因此保險起見選擇創建一個子賬號，在“用戶權限”這一項進行搜索“機器翻譯”，只勾選這一項。
5. 成功創建後，會看到這個子賬戶的“SecretId”和“SecretKey”。將其填入本擴展即可！
6. 完成🎉，如有疑惑的地方，請在 [這裡](https://github.com/immersive-translate/immersive-translate/issues/137) 反饋。