# Ollama

> 💡 從外掛版本 1.15.1 開始支援

## 簡要說明

1. 官方網站：[Ollama](https://github.com/ollama/ollama)
2. 官方資費說明：本地運行的大模型，完全免費

## 使用方法

1. 打開 [Ollama](https://ollama.com) 下載 Ollama
2. 打開 [模型列表](https://ollama.com/library)下載模型，比如可以使用 `ollama pull llama3.3` 下載 llama3.3 模型
3. APIKEY 使用預設的即可，啟動 Ollama，比如可以使用 `ollama run llama3.3` 啟動 llama3.3
4. 完成 🎉，如有疑惑的地方，請在 [這裡](https://github.com/immersive-translate/immersive-translate/issues/137) 反饋。

## 參考檔案

- https://github.com/ollama/ollama/blob/main/docs/api.md
- https://github.com/ollama/ollama/issues/2335

## 常見問題說明

1. 使用區域網的接口地址時出現跨域問題？

   此時允許跨域即可：

   - macOS：命令行執行 `launchctl setenv OLLAMA_ORIGINS "*"`，再啟動 App。
   - Windows：控制面板 - 系統屬性 - 環境變數 - 使用者環境變數新建 2 個環境變數：變數名`OLLAMA_HOST`變數值`0.0.0.0`，變數名`OLLAMA_ORIGINS`變數值`*`，再啟動 App。
   - Linux：命令行執行 `OLLAMA_ORIGINS="*" ollama serve`。

2. 使用油猴腳本時，自訂接口地址請求失敗？

   油猴腳本要求腳本的所有請求都需要在腳本的開頭聲明權限，比如：`http://localhost:11434`，所以，如果你需要新增一個非預設的域名，請在油猴腳本開頭仿照其他域名進行聲明。