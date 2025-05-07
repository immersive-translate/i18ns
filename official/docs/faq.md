---
sidebar_position: 9
---

# 常见问题

## 安全相关

### 1. Android App，悬浮球消失

原因是旧版本的附加组件被禁用。

请卸载后前往 [官网](https://immersivetranslate.com/) 安装最新版本。


## 安装相关

### 1. 如何更新扩展

一般来说，在浏览器商店安装的扩展都会在新版发布后的一天之内自动进行更新。如果你想立刻更新到最新版本的话，可以在浏览器的**扩展管理**页面，打开**开发者模式**，然后点击最上面的**更新**，即可立即更新到商店的最新版本。

![](https://s.immersivetranslate.com/assets/r2-uploads/Update_Extension-As1DgZMw0hcbe5kh.gif)

### 2. 沉浸式翻译油猴脚本支持的浏览器

iOS 系统：

- [Tampermonkey 浏览器](https://www.tampermonkey.net/)
- 安装油猴扩展后的 Safari 浏览器，可安装的油猴扩展：
  - [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)
  - [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171)：建议直接在 Stay 自带的商店里搜索沉浸式翻译优化脚本下载（针对 Stay 做了特殊优化）。

Android 系统：

- [Firefox 最新版本](https://www.firefox.com.cn/download/#product-android-release)：安装完成后，再安装 [Tamper Monkey](https://www.tampermonkey.net/) 扩展。
- [X 浏览器](https://www.xbext.com/?ref=immersive-translate)：安装后，直接打开[沉浸式翻译油猴脚本地址](https://download.immersivetranslate.com/immersive-translate.user.js) 即可安装。

已知不支持的油猴扩展的浏览器（此类浏览器缺乏必要的油猴 API）：

- 安卓 Via 浏览器
- iOS Alook 浏览器

### 3. 在 chrome 上安装插件安装包报错

如果收到报错信息 `invalid value for web_accessible_resource[0]`

需要 Chromium 版本大于 88 才能支持 manifest_version 3。

### 4. 360 浏览器如何安装

沉浸式翻译插件只支持 **360 极速浏览器 x** （产品名中带有 x）。你可以前往谷歌浏览器扩展商店安装插件，或者 [手动安装](/docs/installation/#%E6%89%8B%E5%8A%A8%E5%AE%89%E8%A3%85-%E8%BF%BD%E8%B8%AA%E6%9C%80%E6%96%B0%E5%BC%80%E5%8F%91%E7%89%B9%E6%80%A7)。

### 5. Opera 浏览器不生效

在 google.com 等搜索页面不生效，插件显示`请先刷新当前页面，再开始翻译`且刷新页面仍提示该信息：需要在 Opera 插件设置中找到【沉浸式翻译】，开启【允许访问搜索页面结果】选项。

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(7)-UqvTUexInGVTf3X2.png)

### 6. 在 iOS 设备上无法启用扩展

如果您在 iOS 设备上无法启用扩展，请按照以下步骤操作操作：

1. 打开【设置】应用
2. 滑动并点击【屏幕使用时间】
3. 选择【内容和隐私访问限制】
4. 点击进入【内容访问限制】
5. 选择【网页内容】，并将其设置为【无限制】

如果您不需要使用内容和隐私访问限制的其他功能，您也可以选择直接关闭内容和隐私访问限制：

1. 打开【设置】应用
2. 选择【屏幕使用时间】
3. 禁用【内容和隐私访问限制】

### 7. Safari 打开设置页面 一直显示 loading

打开 Safari 浏览器-> 设置 -> 网站 -> 沉浸式翻译 -> 找到 immersivetranslate.com 相关域名并删除。

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(8)-O7IPyq2aF6WhbgMO.png)

### 8. iOS 18 安装后进入设置页面登录时跳转到空白页面

长按悬浮球，点击头像并登录账号。

### 9. 下载的离线版插件文件拖拽至浏览器扩展程序，显示文件不存在

需要先解压压缩包，再单独拖拽其中的  `.CRX` 文件。

### 10. crx 下载为什么安装是 1.13.5 而不是最新版

因为系统检测您的浏览器 Chromium 内核低于 115 版本，不支持插件部分高级特性，所以自动降级为 1.13.5 版本。

## 基础翻译相关

### 1. Youtube, Facebook 等网站主要内容翻了，但是部分侧边栏没法，想翻译全部

出于页面可读性和体验的考量，沉浸式翻译默认只翻译主要内容区域。

如果想翻译全部区域，请打开插件面板 (移动端长按悬浮球) -> 点击右下角**更多** -> 选择 **「切换为翻译全部区域」**。

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(9)-p0X8p6YHUUIy7A-K.png)

### 2. 手机 App 中不显示悬浮球

- 沉浸式翻译插件为浏览器插件，**只能在浏览器**中运行，无法在其他 app 中使用，不支持其他 App 内部翻译。

- 浏览器与相应安装过的插件一一对应，**无法跨浏览器**（如在 Safari 内安装不可以在 Chrome 内使用插件）

### 3. iOS 浏览器上点击 YouTube 直接打开 App，无法进入网页翻译

长按 YouTube 链接弹出悬浮窗选择网页打开。

### 4. 如何关闭自动翻译

- 在 Popup 面板或者设置页面取消。

- 或者通过设置页面修改

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(10)-27sbOakCfjAGn1E0.png)

### 5. 暂无权限翻译当前页面

- 浏览器默认页无法翻译 (地址栏无地址)
- 第三方插件页面无法翻译
- 谷歌插件禁止了谷歌商店页面的翻译

### 6. 如何不显示原文

点击沉浸式翻译图标，打开扩展面板，点击【更多】，【切换到仅译文模式】。请查看视频演示：

<div style={{textAlign: "center"}}>
  <video
    controls
    muted
    style={{width:"100%", maxWidth:500}}
    poster="https://s.immersivetranslate.com/assets/r2-uploads/004_切换双语-封面-AHSpIxvmD713B8sh.jpg"
    src="https://s.immersivetranslate.com/assets/r2-uploads/004_切换双语-EKS6H03tEOg-EhDt.mp4">
  </video>
</div>

### 7. 页面出现感叹号

页面出现感叹号，说明翻译服务遇到问题，返回了错误，可以将鼠标移动到感叹号上查看具体错误。

#### 例如：429 错误

这是最常见的错误之一，429 表示请求的频率过快。网页翻译中有较多的段落需要翻译，尽管我们已经做了极大的优化，但是有的时候依然有一些翻译服务不堪重负，返回 429 频率限制的错误。

这一问题通常可通过暂时切换到其他翻译服务解决，或者稍后再试。

如果你在使用 Google 服务时遇到 429 错误，通常是谷歌针对你所使用的节点做了限流，建议切换节点。

### 8. 怎么切换翻译源与目标语言

移动端长按悬浮球，电脑端鼠标移动至悬浮球唤出设置，选择其他翻译服务/其他目标语言。

![](https://s.immersivetranslate.com/assets/r2-uploads/Toggle_AI_Models-6hIHVHagHMK7wr92.gif)

### 9. 谷歌翻译接口被墙问题

请将`translate.googleapis.com` 域名加入到代理规则中。

### 10. OpenAI 封禁中国地区 API Key 对会员使用 AI 服务是否有影响

没有影响，产品使用 Azure 企业版 OpenAI，不受 API 地区限制。

### 11. 彩云翻译报错

点开`?`号的报错信息显示"Unsupported trans_type"。可以手段选择自动检测语言为指定语言。

### 12. 微信读书无法翻译

微信读书针对内容做了特殊处理，禁止通过第三方手段获取内容，所以无法翻译。

### 13. 网页部分内容未翻译

一般是网站管理者通过 `translate="no"` 或者 `notranslate class` 来约定翻译插件不翻译这块区域。

可以通过以下方式解决：

1. 启用鼠标悬停功能
2. 通过鼠标悬停来强制翻译该区域段落内容

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(4)-_JbXNlBLSe-tVmjt.png)

### 14. 触发翻译不生效

当出某个网站不能翻译，而其他网页翻译正常时

- 如果这个网站访问人比较少
  - 建议通过鼠标悬停来翻译段落
  - 如果需要翻译整篇网站可以通过 [用户规则](/docs/advanced/#用户规则合并增强) 适配

- 如果这个网站有很多人用
  - 可以先通过鼠标悬停翻译使用
  - 在用户群中报错，我们的技术人员会稍后安排适配

### 15. 网页翻译有问题，如何保存网页反馈

请在网页中右键点击“存储为”或者 ctrl+s 快捷键，保存选项选择单个文件，最后文件格式为.mht/.mhtml。然后将文件发送至 support@immersivetranslate.com。

![save mht](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(11)-z1OWfJqCqHri1mFp.png)

### 16. 查看调试日志

1. 开启调试日志：打开面板 -> 设置 -> 开发者设置 -> 启用”在控制台打印调试日志“。
2. 打开网站的控制台：右键打开审查 -> 右边栏目顶部切换到控制台 -> 执行操作就可以看到日志。

### 17. 如何关闭悬浮球

- 在当前页隐藏：设置为【永不翻译该网站】即可
- 在所有页面隐藏：打开【设置】-【悬浮球】，关闭【启用悬浮球】即可

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(12)-mBXqJ4yCmbSbpzcz.png)

### 18. 鼠标悬停 + 快捷键翻译功能无效

要启用鼠标悬停加快捷键的翻译功能，页面必须首先获得焦点。如果您发现该功能未能触发，请尝试以下步骤：

1. 在页面 **任意位置点击一次**，以确保页面获得焦点。
2. 再次尝试同时使用鼠标悬停和快捷键进行翻译。
3. 如果翻译功能仍然不响应，**请确认您的快捷键设置是否正确**。

### 19. 如何更新最新规则

扩展程序会在使用过程中定时自动同步官方最新的网页适配规则。

如果需要手动同步，请点击浏览器中的沉浸式翻译扩展图标，插件卡片打开后，扩展程序将自动检测并更新到最新适配规则。

使用油猴脚本的用户，同样支持规则的自动检测与同步。

### 20. 翻译失败 / 翻译一直转圈

1. 查看失败原因：

   - 如**额度达到限制**，说明你的会员当月该翻译源额度用尽
   - 如翻译显示网络错误，请先检查节点/网络状态

2. 切换翻译服务，长按悬浮球或点击插件图标，在弹出面板中选择其他翻译服务。

### 21. Pro 会员翻译额度与用量如何查询

- Pro 会员每月可享受 2000 万 Token 的基础翻译额度。该额度可用于所有翻译服务，无论是全部用于 DeepL（相当于 2000 万字符）、全部用于 OpenAI（2000 万 Token），还是混合使用多个服务，您都可以根据实际需求自由分配额度

  > OpenAI 的定价是基于 token 的，对于英文文本，1 个 token 大约是 4 个字符或 0.75 个单词。通常 1000 个 Token 约等于 750 个英文单词或者 400~500 个汉字。

- 用量查询地址： [https://immersivetranslate.com/accounts/usage](https://immersivetranslate.com/accounts/usage)

### 22. 为什么插件谷歌翻译质量不如谷歌网页翻译

目前扩展使用的是谷歌翻译的免费 API，该接口属于谷歌早期提供的旧版服务，已不再持续维护。相比之下，谷歌官方网站上的翻译功能仍在持续优化，因此理论上翻译质量会更高。

近期，由于谷歌免费 API 的翻译质量明显下降，我们建议用户考虑切换至其他可用的翻译服务。与此同时，我们也在积极评估和寻找更优质的替代方案。

了解更多讨论内容：[#2574](https://github.com/immersive-translate/immersive-translate/issues/2547)

### 23. 鼠标模式下确显示触摸模式

在[进阶设置](https://dash.immersivetranslate.com/#advanced)中，开启仅鼠标模式即可。

1.14.9 版本已优化这个模式判断。

### 24. Edge 无法朗读译文

Edge 浏览器的朗读功能会根据原网页的语言自动选择对应的语音模型。由于这些语音模型是针对单一语言设计的，因此当页面包含译文时，默认选择的语音模型无法正确朗读译文内容。

解决方法：您可以在 Edge 朗读功能的工具栏中，点击【语音选项】，然后手动选择与译文语言相匹配的语音模型。这样就能正确朗读译文内容了。

## 视频翻译相关

### 1. Youtube 字幕设置样式

可以直接点击 Youtube 自带的字幕设置，[Options], 然后就可以调整大小，颜色等。

![](https://s.immersivetranslate.com/assets/r2-uploads/Subtitle_options-wyH3JJ2rghmaz7OJ.gif)

### 2. YouTube 双语字幕繁体中文不显示
YouTube 自带机翻字幕，繁体中文会出现格式错误，导致所有字幕在开始的时候会弹出一大段字幕，基于此场景，建议在【设置】【视频字幕】中开启【使用沉浸式翻译来翻译字幕】选项。

### 3. Bilibili 如何开启字幕翻译

在翻译 Bilibili 视频字幕时，请按以下步骤操作：

1. 先开启 Bilibili 内置字幕，点击播放器右下角的“字幕”按钮即可。如果视频没有字幕按钮或字幕内容，则不支持双语字幕。
2. 点击播放器中的“沉浸式翻译”图标，开启双语字幕功能。

使用时需注意：

1. 确保已经开启 Bilibili 的内置字幕。
2. 确保沉浸式翻译的目标语言与 Bilibili 内置字幕的语言不同，以触发翻译功能。

### 4. Netflix 字幕翻译用原始字幕样式

- 当前 Netflix 采用渐进式翻译方案，字幕样式自托管，不支持人工字幕。
- 旧方案，需要等到所有字幕翻译完才会显示字幕，支持人工字幕。

**如何回退至旧方案**

进入【[开发者设置](https://dash.immersivetranslate.com/#developer)】找到`Edit User Rules`
添加如下规则

```json
[
  {
    "id": "netflix",
    "subtitleRule.add": {
      "attachRule": {
        "appendSelector": ""
      }
    }
  }
]
```

## 文件翻译相关

### 1. 如何翻译本地文件

- 方法一：进入[沉浸式翻译文件翻译官网](https://app.immersivetranslate.com/)，也可以点击沉浸式翻译扩展图标，点击【文件翻译】进入。

- 方法二：如果使用的是类 Chrome 浏览器，如（Chrome，Arc，Edge 浏览器），还有另一种办法，就是在浏览器中打开扩展管理页面`chrome://extensions`,找到【沉浸式翻译】插件，【允许该扩展访问本地文件】，之后直接在浏览器中打开本地的 HTML 或本地的 PDF 文件，就可以直接右键【翻译】了。

![](https://s.immersivetranslate.com/assets/r2-uploads/翻译本地文档设置-N2yTVc8X7HvXw3uJ.gif)

**注意**：Safari 浏览器对扩展访问本地文件有严格限制，Safari 用户请直接前往[沉浸式翻译文件翻译官网](https://app.immersivetranslate.com/)来翻译本地文件。

### 2. 页数过多时 PDF 文件翻译过慢

建议裁剪为多个 100 页以下的部分再进行翻译，翻译完成后再进行合并

### 3. PDF 翻译译文重复重叠

这是由源文件自身识别问题造成的，建议手动点击该部分，删除多余文本框。我们会持续优化 PDF 翻译效果。

### 4. 是否有术语表 / 某些词汇特殊翻译或不翻译

1.16.1+ 支持 [AI 术语库](https://dash.immersivetranslate.com/#terms) 功能。

AI 术语库默认不支持谷歌/微软这类机器翻译术语

机器翻译模型采用的是占位符替换，使用术语库可能会导致翻译质量下降。

强制开启方法：

【[开发者设置](https://dash.immersivetranslate.com/#developer)】 -> 【Edit Full User Config】

```
{
  ....
  "enableMachineTranslateTerms":true,
  ...
}
```


### 5. Word 文件翻译后无法导出为 Word 格式

目前 word 文件导出存在一定技术问题，建议保持现有格式。我们正在优化这一功能。

### 6. PDF 如何调整最小字号

PDF 翻译字体取决于浏览器设置，你可以将调整浏览器字体到最小。以 chrome 为例：点击 [chrome 字号设置](chrome://settings/fonts?search=%E5%AD%97%E5%8F%B7)进行设置，或参考以下方式：

![](https://s.immersivetranslate.com/assets/r2-uploads/调整最小字体-KR8tw_2LkGHkrAlZ.gif)


## 输入框翻译相关

### 1. 输入框增强不生效

- 请确认你使用的不是明确不支持的浏览器：详见 [输入框翻译](https://immersivetranslate.com/docs/input/) 兼容性部分
- 在网址栏或浏览器初始页无法翻译，仅支持搜索栏，可至 https://www.bing.com/ 测试
- 加快空格连击速度

## 支付相关

### 1. 是否能用微信支付

微信支付需要私信群内工作人员并备注“微信支付”。

在工作人员提供收款码之后付款，并将相应的付款详情提供给工作人员。

工作人员会提供所需的年/月会员兑换码。

你可以在 [兑换会员页](https://immersivetranslate.com/exchange/) 中兑换。

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(15)-Hy0trH9XQNzTPr7A.png)

### 2. 是否能开发票

目前仅支持年费会员开具发票。

已经支付的用户需要发票请私信群内工作人员并备注“发票问题”，未支付的用户可查看：[年会员开票须知](https://immersivetranslate.com/bill/)

## 更多问题（非常见）

### 油猴脚本如何清空缓存？

由于油猴脚本的 API 限制，沉浸式翻译油猴脚本的缓存会保存在对应网站的缓存里。

所以，如果要清除的话，可以在浏览器打开相应网站的开发者工具面板，然后清空该网站的缓存。

### 油猴脚本自定义接口地址请求失败？

油猴脚本要求脚本的所有请求都需要在脚本的开头声明权限，比如：`@connect api.google.com`，所以，如果你需要新增一个非默认的域名，请在油猴脚本开头仿照其他域名进行声明。

### Edge 浏览器插件打开空白，且浏览器报错 MANIFEST-000001

打开【[文件快速查找应用 (Everything)](https://www.voidtools.com/zh-cn/downloads/)】应用，搜索 `amkbmndfnliijdhojkpoglbnaaahippg` 沉浸式的扩展 id 浏览器的存储文件夹，删除之后，然后再去卸载重装插件

### 双语字幕如何下载 / 其他网站双语字幕能否下载？

- 目前仅支持在电脑端进行字幕下载。
- 包括 Youtube，当有字幕下载按钮时，当前网站即可支持双语字幕下载。
![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(16)-T-SJ6jJfA9zG7w5a.png)
