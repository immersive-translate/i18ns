---
sidebar_position: 7
---

# 隱私模式 (Beta)

## 敏感資訊脫敏說明

> 該功能在插件 1.23.1+ 支援。

當您啟用了內建或自訂 [OneAIFW](https://github.com/funstory-ai/aifw) 後，插件會在翻譯過程中自動識別並脫敏敏感資訊（如郵箱、手機號、身份證號等），以保護您的隱私安全。本文檔將指導您如何查看翻譯過程中哪些敏感資訊被識別並脫敏。

### 查看脫敏日誌

#### 步驟 1：啟用日誌功能

1. 打開插件的 [**開發者設定頁**](https://dash.immersivetranslate.com/#advanced)
2. 啟用 **「控制條打開日誌」** 選項

#### 步驟 2：打開開發者控制台

1. 在網頁上按 `F12` 鍵（或右鍵點擊頁面，選擇「檢查」/「審查元素」）
2. 切換到「Console」（控制台）標籤頁

#### 步驟 3：過濾脫敏日誌

在控制台的過濾框中輸入 `sensitive-`，即可過濾出所有與敏感資訊脫敏相關的日誌。

### 日誌格式說明

在控制台中，您會看到如下格式的日誌：

```
[sensitive-encode] "郵箱：tester.cn+alias@example.com" -> "郵箱：__PII_EMAIL_ADDRESS_1__"

[sensitive-decode] "郵箱：__PII_EMAIL_ADDRESS_1__" -> "郵箱：tester.cn+alias@example.com"
```

#### 日誌含義

- **`[sensitive-encode]`**：表示敏感資訊被識別並脫敏的過程
  - 左側是原始文字（包含敏感資訊）
  - 右側是脫敏後的文字（`__PII_*` 為脫敏佔位符）

- **`[sensitive-decode]`**：表示脫敏後的文字被還原的過程
  - 左側是脫敏後的文字（包含佔位符）
  - 右側是還原後的原始文字

#### 佔位符說明

`__PII_*` 格式的佔位符表示被脫敏的敏感資訊類型，例如：
- `__PII_EMAIL_ADDRESS_1__`：郵箱地址
- `__PII_PHONE_NUMBER_1__`：手機號碼
- `__PII_ID_CARD_1__`：身份證號
- 等等...

### 脫敏原理

關於敏感資訊脫敏的具體原理和實現細節，您可以查看 [OneAIFW 專案](https://github.com/funstory-ai/aifw) 的文檔和代碼。

### 注意事項

- 本功能目前處於 **Beta 測試階段**，可能會存在識別不準確或脫敏失敗的情況
- 如果您遇到脫敏失敗或識別錯誤的問題，歡迎在 [GitHub Issues](https://github.com/funstory-ai/aifw/issues) 提交問題反饋，我們會持續迭代優化

