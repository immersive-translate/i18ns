---
sidebar_position: 7
---

# Privacy Mode (Beta)

## Sensitive Information Desensitization Guide

> This feature is supported in plugin version 1.23.1+.

After enabling the built-in or custom [OneAIFW](https://github.com/funstory-ai/aifw), the plugin will automatically identify and desensitize sensitive information (such as email addresses, phone numbers, ID card numbers, etc.) during translation to protect your privacy and security. This guide will show you how to view which sensitive information has been identified and desensitized during translation.

### Viewing Desensitization Logs

#### Step 1: Enable Logging

1. Open the plugin's [**Developer Settings Page**](https://dash.immersivetranslate.com/#advanced)
2. Enable the **"Enable Console Logging"** option

#### Step 2: Open Developer Console

1. Press `F12` on the webpage (or right-click the page and select "Inspect" / "Inspect Element")
2. Switch to the "Console" tab

#### Step 3: Filter Desensitization Logs

Enter `sensitive-` in the console filter box to filter all logs related to sensitive information desensitization.

### Log Format Explanation

In the console, you will see logs in the following format:

```
[sensitive-encode] "Email: tester.cn+alias@example.com" -> "Email: __PII_EMAIL_ADDRESS_1__"

[sensitive-decode] "Email: __PII_EMAIL_ADDRESS_1__" -> "Email: tester.cn+alias@example.com"
```

#### Log Meanings

- **`[sensitive-encode]`**: Indicates the process of identifying and desensitizing sensitive information
  - Left side is the original text (containing sensitive information)
  - Right side is the desensitized text (`__PII_*` is the desensitization placeholder)

- **`[sensitive-decode]`**: Indicates the process of restoring desensitized text
  - Left side is the desensitized text (containing placeholders)
  - Right side is the restored original text

#### Placeholder Explanation

Placeholders in the `__PII_*` format represent the type of sensitive information that has been desensitized, for example:
- `__PII_EMAIL_ADDRESS_1__`: Email address
- `__PII_PHONE_NUMBER_1__`: Phone number
- `__PII_ID_CARD_1__`: ID card number
- etc.

### Desensitization Principles

For specific principles and implementation details of sensitive information desensitization, you can refer to the [OneAIFW project](https://github.com/funstory-ai/aifw) documentation and code.

### Notes

- This feature is currently in **Beta testing phase**, and there may be cases of inaccurate identification or desensitization failures
- If you encounter desensitization failures or identification errors, please submit feedback via [GitHub Issues](https://github.com/funstory-ai/aifw/issues), and we will continue to iterate and optimize
