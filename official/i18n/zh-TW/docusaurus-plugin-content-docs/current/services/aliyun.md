# 阿里雲翻譯

## 簡要說明

1. 官方網站：[機器翻譯*阿里AI翻譯*文檔圖片翻譯-阿里雲](https://www.aliyun.com/product/ai/alimt)
2. 官方資費說明：[機器翻譯的付費模式及具體定價\_機器翻譯-阿里雲幫助中心](https://help.aliyun.com/document_detail/197134.html)
3. 機器翻譯通用版每月的前 100 萬字符免費，超出的部分會按照 50 元 / 百萬字符收取費用；機器翻譯專業版每月的前 100 萬字符免費，超出的部分會按照 60 元 / 百萬字符收取費用。請關注使用額度，以免意外扣費。## 申請步驟

4. 打開 [阿里雲官網](https://www.aliyun.com/) 並登錄。
5. 打開 [機器翻譯*阿里AI翻譯*文檔圖片翻譯-阿里雲](https://www.aliyun.com/product/ai/alimt)，點擊“立即開通”按鈕。登錄之後，會進入阿里雲機器翻譯服務控制台。
6. 選擇開通“通用版翻譯”和“專業版翻譯”。
7. 創建訪問密鑰。將鼠標懸停在網頁右上角的頭像上，然後選擇 [AccessKey 管理](https://ram.console.aliyun.com/manage/ak)，最好不要直接創建密鑰，因為主賬號創建的密鑰可以訪問調用你賬號裡的所有資源，因此保險起見選擇創建一個子賬號，子賬號訪問方式為“OpenAPI 調用方式”。
8. 成功創建後，會看到這個子賬戶的“AccessKey ID”和“AccessKey Secret”。將其填入本擴展！
9. 子賬號授權，點擊子賬號“用戶登錄名稱”，選擇“權限管理” “新增授權” ，在“選擇權限” “系統策略” 進行搜索“機器翻譯”，選“管理機器翻譯(alimt)的權限”這一項
10. 完成🎉，如有疑惑的地方，請在 [這裡](https://github.com/immersive-translate/immersive-translate/issues/137) 反饋。
