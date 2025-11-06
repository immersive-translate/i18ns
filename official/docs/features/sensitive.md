---
sidebar_position: 7
---

# 隐私模式（Beta）

## 敏感信息脱敏说明

> 该功能在插件 1.23.1+ 支持。

当您启用了内置或自定义 [OneAIFW](https://github.com/funstory-ai/aifw) 后，插件会在翻译过程中自动识别并脱敏敏感信息（如邮箱、手机号、身份证号等），以保护您的隐私安全。本文档将指导您如何查看翻译过程中哪些敏感信息被识别并脱敏。

### 查看脱敏日志

#### 步骤 1：启用日志功能

1. 打开插件的 [**开发者设置页**](https://dash.immersivetranslate.com/#advanced)
2. 启用 **「控制条打开日志」** 选项

#### 步骤 2：打开开发者控制台

1. 在网页上按 `F12` 键（或右键点击页面，选择「检查」/「审查元素」）
2. 切换到「Console」（控制台）标签页

#### 步骤 3：过滤脱敏日志

在控制台的过滤框中输入 `sensitive-`，即可过滤出所有与敏感信息脱敏相关的日志。

### 日志格式说明

在控制台中，您会看到如下格式的日志：

```
[sensitive-encode] "邮箱：tester.cn+alias@example.com" -> "邮箱：__PII_EMAIL_ADDRESS_1__"

[sensitive-decode] "邮箱：__PII_EMAIL_ADDRESS_1__" -> "邮箱：tester.cn+alias@example.com"
```

#### 日志含义

- **`[sensitive-encode]`**：表示敏感信息被识别并脱敏的过程
  - 左侧是原始文本（包含敏感信息）
  - 右侧是脱敏后的文本（`__PII_*` 为脱敏占位符）

- **`[sensitive-decode]`**：表示脱敏后的文本被还原的过程
  - 左侧是脱敏后的文本（包含占位符）
  - 右侧是还原后的原始文本

#### 占位符说明

`__PII_*` 格式的占位符表示被脱敏的敏感信息类型，例如：
- `__PII_EMAIL_ADDRESS_1__`：邮箱地址
- `__PII_PHONE_NUMBER_1__`：手机号码
- `__PII_ID_CARD_1__`：身份证号
- 等等...

### 脱敏原理

关于敏感信息脱敏的具体原理和实现细节，您可以查看 [OneAIFW 项目](https://github.com/funstory-ai/aifw) 的文档和代码。

### 注意事项

- 本功能目前处于 **Beta 测试阶段**，可能会存在识别不准确或脱敏失败的情况
- 如果您遇到脱敏失败或识别错误的问题，欢迎在 [GitHub Issues](https://github.com/funstory-ai/aifw/issues) 提交问题反馈，我们会持续迭代优化

