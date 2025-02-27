# Ollama

> 💡 从插件版本 1.14.16 开始支持

## 简要说明

1. 官方网站：[Ollama](https://github.com/ollama/ollama)
2. 官方资费说明：本地运行的大模型，完全免费

## 使用方法

1. 打开 [Ollama](https://ollama.com) 下载 Ollama
2. 打开 [模型列表](https://ollama.com/library)下载模型，比如可以使用 `ollama pull llama3.3` 下载 llama3.3 模型
3. 启动 Ollama
4. 完成 🎉，如有疑惑的地方，请在 [这里](https://github.com/immersive-translate/immersive-translate/issues/137) 反馈。

## 参考文档

- https://github.com/ollama/ollama/blob/main/docs/api.md
- https://github.com/ollama/ollama/issues/2335

## 常见问题说明
1. 使用局域网的接口地址时出现跨域问题？

   此时允许跨域即可：

   - macOS：命令行执行 `launchctl setenv OLLAMA_ORIGINS "*"`，再启动 App。
   - Windows：控制面板 - 系统属性 - 环境变量 - 用户环境变量新建 2 个环境变量：变量名`OLLAMA_HOST`变量值`0.0.0.0`，变量名`OLLAMA_ORIGINS`变量值`*`，再启动 App。
   - Linux：命令行执行 `OLLAMA_ORIGINS="*" ollama serve`。

2. 使用油猴脚本时，自定义接口地址请求失败？

   油猴脚本要求脚本的所有请求都需要在脚本的开头声明权限，比如：@connect api.google.com，所以，如果你需要新增一个非默认的域名，请在油猴脚本开头仿照其他域名进行声明。
