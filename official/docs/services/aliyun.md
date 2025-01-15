# 阿里云翻译

## 简要说明

1. 官方网站：[机器翻译*阿里 AI 翻译*文档图片翻译 - 阿里云](https://www.aliyun.com/product/ai/alimt)
2. 官方资费说明：[机器翻译的付费模式及具体定价\_机器翻译 - 阿里云帮助中心](https://help.aliyun.com/document_detail/197134.html)
3. 机器翻译通用版每月的前 100 万字符免费，超出的部分会按照 50 元 / 百万字符收取费用；机器翻译专业版每月的前 100 万字符免费，超出的部分会按照 60 元 / 百万字符收取费用。请关注使用额度，以免意外扣费。

## 申请步骤

1. 打开 [阿里云官网](https://www.aliyun.com/) 并登录。
2. 打开 [机器翻译*阿里 AI 翻译*文档图片翻译 - 阿里云](https://www.aliyun.com/product/ai/alimt)，点击“立即开通”按钮。登录之后，会进入阿里云机器翻译服务控制台。
3. 选择开通“通用版翻译”和“专业版翻译”。
4. 创建访问密钥。将鼠标悬停在网页右上角的头像上，然后选择 [AccessKey 管理](https://ram.console.aliyun.com/manage/ak)，最好不要直接创建密钥，因为主账号创建的密钥可以访问调用你账号里的所有资源，因此保险起见选择创建一个子账号，子账号访问方式为“OpenAPI 调用方式”。
5. 成功创建后，会看到这个子账户的“AccessKey ID”和“AccessKey Secret”。将其填入本扩展！
6. 子账号授权，点击子账号“用户登录名称”，选择“权限管理” “新增授权” ，在“选择权限” “系统策略”进行搜索“机器翻译”，选“管理机器翻译 (alimt) 的权限”这一项
7. 完成🎉，如有疑惑的地方，请在 [这里](https://github.com/immersive-translate/immersive-translate/issues/137) 反馈。
