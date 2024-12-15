---
sidebar_position: 6
---

# Change Log

## 1.12.3 (2024-12-13)

- 新增：AI智能上下文翻译，可以提高专业内容翻译的准确性。（仅Pro会员可用）【**设置**】->【**基本设置**】->【**启用AI智能上下文翻译**】。
- 修复：推特多行翻译效果下的部分 bug。
- 修复：富文本导致部分公式翻译的问题。
- 优化：在推特翻译时，有字幕的视频会自动翻译双语字幕。
- 优化：无字幕视频显示翻译图标，并告知无法翻译的原因。

## 1.11.7 (2024-11-25)

- 新增：Bing/google支持柬埔寨语（高棉语）。
- 新增：允许未翻译完成的ePub文件在再次导入时从上次停止处继续翻译。
- 修复：在 Safari 浏览器中无法翻译推特图片的问题。
- 修复：在开启或关闭【**鼠标悬停翻译**】功能时，快捷键失效的问题。
- 优化：改进Twitter,Youtube多行双语对照翻译的显示效果。
- 优化：在双语模式下，默认关闭富文本翻译以提升翻译质量。
- ~~优化：【**进阶设置**】中添加了自定义【**侧边栏和导航条翻译**】的选项。~~
- 优化：在【**鼠标悬停-直接翻译该段**】模式下，不再翻译图片。

## 1.11.4 (2024-11-16)

- 修复：1.11.2版本中"Twitter翻译改进"引起的公式翻译的问题。

## 1.11.2 (2024-11-13)

- 修复：Facebook在仅译文模式下，点击seemore后导致内容消失的问题。
- ~~优化：改进Twitter多行双语对照翻译的显示效果。~~
- 优化：改进面板中翻译服务下拉列表的UI。

## 1.11.1 (2024-11-05)

- 新增：实时会议的【字幕翻译】新增悬浮球触发支持，适用于Zoom、Google Meet和Microsoft Teams。
- 修复：YouTube【字幕翻译】在观看广告后时间轴不同步的问题。
- 修复：MacOS 15 Safari浏览器中右键翻译菜单显示异常的问题。
- 修复：部分网站【输入框增强】的Ctrl+Z撤销操作无效的问题。

## 1.10.6 (2024-10-25)

- 修复：【输入增强】快捷键无法触发的问题
- 优化：减小安装包大小
- 优化：奈飞字幕显示方案调优

## 1.10.5 (2024-10-23)

- 新增：当源语言和目标语言一致时显示警告提示
- 修复：富文本空白字符翻译问题 [#2175](https://github.com/immersive-translate/immersive-translate/issues/2175)
- 优化：网页内嵌iframe里的输入增强和鼠标悬停功能

## 1.10.2 (2024-10-11)

- 新增：图片翻译Beta版 (仅支持会员可用，非油猴版本)，在【设置】->【开发者】-> 【开启beta】
- 新增：仅鼠标模式（仅当平板设备的鼠标hover功能失效时才需开启此功能）【设置】->【进阶设置】->【启用仅鼠标模式】
- 新增：视频字幕翻译失败后，显示错误信息
- 修复：富文本翻译问题 [#2163](https://github.com/immersive-translate/immersive-translate/issues/2163)
- 优化：PDF翻译时可能出现的翻译按钮失效的问题
- 优化：提升译文中公式的渲染效果
- 优化：语言选择列表

## 1.9.8 (2024-09-28)

- 新增：翻译服务“智谱GLM翻译”
- 移除：“SiliconCloud翻译”模型qwen1.5-7B-chat（由于官方不再支持）
- 修复：解决 macOS 15 上 Safari 插件的登录兼容性问题

## 1.9.7 (2024-09-20)

- 输入增强支持百度，gmail等输入框
- 支持 claude Anthropic API 的 anthropic-dangerous-direct-browser-access 请求头
- 支持 hulu、bloomberg、domestika 视频字幕下载
- deepx 支持富文本翻译
- 修复自定义AI专家无法同步

## 1.9.6 (2024-09-13)

- [PDF Pro](https://app.immersivetranslate.com/pdf-pro/) 支持公式复制（在公式上右键即可看到复制的菜单）
- 修复推特同一网页多个视频的双语字幕显示问题
- 修复一些 Bug

## 1.9.3 (2024-09-05)

- 双语对照/仅显示译文设置项迁移到通用设置中
- 默认将会记住在面板中点击图标切换双语对照模式/仅显示译文默认，如需临时切换，需要点击面板中的【更多】 -> 【切换为仅显示译文】
- 默认情况下，简体中文翻译为繁体中文，繁体中文翻译为简体中文将使用仅显示译文模式，而不是双语对照模式
- 修复一些 Bug

## 1.9.1 (2024-09-03)

- 支持为双语对照或仅译文模式配置例外的语言和网站（在设置页面->进阶设置中配置）。比如：如果您的默认翻译模式是双语对照，但是您并不希望繁体中文也使用双语对照，此时您可以在双语对照的例外语言中添加繁体中文，这样繁体中文将会使用仅译文模式翻译。同理，如果您的默认翻译模式是仅译文，但是您希望某个语言或网站使用双语对照模式，您也可以在例外语言中添加这个语言或网站。
- 修复 Tiktok 私信界面输入框翻译出错问题
- 修复 Read Comic Online 漫画无法翻译问题
- 修复 【进阶设置 -> 翻译段落所需的最少字符数】 在部分情况下不生效的问题

## 1.8.4 (2024-08-30)

- DeepL 翻译服务正式支持繁体中文作为目标语言（此前 DeepL 翻译为繁体中文有额外的第三方简体转繁体过程）
- 优化富文本翻译性能

## 1.8.3

- Google Meet 实时会议支持双语字幕：现在，您可以在 Google Meet 会议中享受双语字幕功能。只需打开会议链接，并在沉浸式翻译面板中激活双语字幕，然后刷新页面即可体验。
- 在面板的更多选项里新增【反馈当前网页的翻译问题】选项，新增【快捷开启/关闭悬浮球】选项
- 调整 YouTube 双语字幕位置后，系统将自动记住新位置
- 优化插件的缓存逻辑，现在会自动清除超过 30 天的缓存数据
- 对段落中出现的代码块进行了优化，以更准确地还原原文
- 改进了高级设置中“不翻译词语”的处理

## 1.8.2

- 现在可以用右键翻译输入框里的文本了：选中任何网页上的输入框文本，右键选择翻译，沉浸式翻译会自动将选中的文本翻译为输入框的目标语言，方便快速将输入框里的母语翻译为其他语言。
- 现在可以在沉浸式翻译的悬浮球里快速反馈网页的翻译问题了，翻译网页后，如果有问题，可以点击悬浮球右侧的【反馈】按钮，填写问题描述，我们会尽快处理。
- Epub 文件现在支持富文本翻译了（即可以保留每个段落原文的格式，比如链接，粗体等）
- 支持 Microsoft Teams 网页版视频会议的实时双语字幕了（打开 Teams 会议链接，在沉浸式翻译面板开启双语字幕后再次刷新即可）
- 优化英文版爱奇艺 (iq.com) 的双语字幕
- 为 arxiv 上更多的论文提供排版优化的双语翻译
- 由于 Youtube 网站限制，Chrome 油猴脚本不再支持 Youtube 双语字幕，请使用[插件版](https://immersivetranslate.com/)。

## 1.8.1

- 修复油猴脚本 SiliconCloud 翻译问题
- Claude 翻译新支持藏语，支持配置 Temperature 参数
- AI 专家详情页展示专家使用的 Prompt
- 快捷键设置中可以为任意翻译服务指定独立的快捷键翻译了
- 优化 arxiv 论文翻译的检测

## 1.7.9

- 修复 Google, DeepL 等翻译服务的富文本翻译问题（如页面直接显示 `<button>` 等）
- 修复 YouTube 视频双语快捷方式无法关闭的问题

## 1.7.8

- DeepL, 微软翻译, Google 翻译，OpenAI，Claude， Gemini 等翻译服务支持译文保留原文格式（比如链接，粗体等）
- 选中文本后，右键菜单会变为【翻译该文本】，点击即可自动跳转到沉浸式翻译文本翻译页面
- 新增大模型免费翻译服务：SiliconCloud ，所有用户可用。
- 新增零一万物大模型翻译，可在零一万物平台注册后填写 API Key 使用。
- 漫画翻译新增用户反馈按钮（漫画翻译后，点击悬浮球右侧的【反馈】按钮，可以反馈翻译质量问题）

## 1.7.7

- 针对 YouTube 自动生成的英文字幕采用 AI 智能分句算法 【Pro 可用】
- 优化右键翻译为”翻译为xx目标语言“
- 支持第三方网站集成沉浸式 [JS SDK](https://immersivetranslate.com/docs/js-sdk/)
- 优化 hulu 字幕显示
- 支持 ZOOM 网页版会议字幕翻译

## 1.7.6

- 支持自定义 AI 专家，入口在【设置】->【AI 专家】页面最下方。
- TED 站点优化字幕加载
- 插件语言支持葡萄牙语（巴西）
- 漫画翻译新增支持站点
  - [Antbyw](https://www.antbyw.com)
  - [Zerobywzz](https://www.zerobywzz.com)
  - [动漫之家](https://www.idmzj.com)
  - [Jmanga](https://jmanga.org)

## 1.7.5

- Youtube 字幕显示允许复制
- 优化部分视频站点的字幕显示
- 优化漫画翻译速度

## 1.7.2

- 修复火狐浏览器漫画翻译失败

## 1.7.1

- 漫画翻译优化翻译速度
- 漫画翻译新增支持站点
  - [ShonenJumpPlus](https://shonenjumpplus.com)
  - [Heros Web](https://viewer.heros-web.com/)
  - [Comic Days](https://comic-days.com/)
  - [ComicWalker](https://comic-walker.com/)
  - [Web Ace](https://web-ace.jp/)
  - [Omega Scans](https://omegascans.org/)

## 1.6.6

- 漫画翻译新增支持站点
  - [Mangabuddy](https://mangabuddy.com/)
  - [Hitomi](https://hitomi.la)
  - [Yamibo](https://www.yamibo.com)
  - [Copymanga](https://www.copymanga.site/)
- Youtube 双语字幕支持智能分句（Beta）（仅在【设置】-【视频字幕】中手动启用沉浸式翻译翻译Youtube字幕，且原视频字幕为自动生成的英文字幕才生效）
- 翻译服务新增腾讯[【混元大模型】](https://immersivetranslate.com/docs/services/tencent-hunyuan/)

## 1.6.5

- 修复漫画翻译目标语言为拉丁语系的文字排版问题
- 漫画翻译新增支持站点
  - [COMIC FUZ](https://comic-fuz.com/)
  - [MangaDex](https://mangadex.org/)
  - [快看漫画](https://www.kuaikanmanhua.com/)
- 修复自定义 AI 服务无法选中 AI 专家

## 1.6.4

- 当 AI 专家为【智能选择】时，可以为不同网站自定义不同的 AI 专家，在【设置】->【AI专家】->【进入任何一个专家】设置
- 修复 YouTube【仅译文】模式下，字幕不显示的问题
- 修复 Mubi 双语字幕失效问题
- 兼容 Adobe Acrobat 插件打开的 PDF
- 所有用户可以[在线贡献](https://weblate.immersivetranslate.com/projects/immersive-translate/extension/)沉浸式翻译界面的多语言翻译

## 1.6.3

- 新功能：漫画翻译（Beta），在支持的漫画网站里，网页快捷翻译悬浮球下方会出现一个漫画翻译的按钮，点击即可开启漫画翻译，该功能为 Pro 会员可用（每月 500 张，更多可购买加量包），当前支持以下网站：
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)
  - [seiga.nicovideo](https://seiga.nicovideo.jp/?cmnhd_ref=device=pc&site=seiga&pos=header_servicelink)
- 新特性：AI 翻译支持[豆包大模型](https://www.volcengine.com/product/doubao)
- 新特性： 支持译文在先，原文随后的双语对照模式，可在设置页面->进阶设置中启用。
- 自定义 AI 模型列表支持 `-all` 语法，可以删除预置的所有模型。
- 视频双语字幕中，当目标语言是简体中文，原文是繁体中文时，会自动将原文转为简体中文，反之亦然。
- 修复 iOS 18 下悬浮球快捷方式无法翻译的问题。
- 修复自定义 Prompt 过多时不生效的问题。

## 1.6.2

- 支持百度千帆大模型平台，阿里百炼大模型平台，DeepSeek 大模型平台
- 修复 popup 面板修改目标语言等设置，点击悬浮球翻译会被重置
- PDF 翻译页面 UI 优化
- Youtube 视频繁体字幕自动转为简体，简体字幕自动转为繁体

## 1.5.8

- AI 专家支持【智能选择】模式，系统会根据当前网站自动选择最适合的 AI 专家（比如 The Verge， Hacker News 会自动选择科技类，推特会自动选择推特翻译增强）。

## 1.5.7

- 支持添加 OpenAI 适配的自定义 AI 翻译服务，入口在【设置】->【翻译服务】页面最下方。
- 所有译文样式支持设置斜体和字体粗细
- 修复 Safari 下 Domestika 视频平台双语字幕不生效问题

## 1.5.6

- 大幅优化了大网页，ePub 制作，字幕文件的翻译性能
- 修复 Pro 多设备同步的 Bug

## 1.5.5

- 修复仅译文模式下部分段落被丢失的问题。

## 1.5.4

- Pro 会员支持开箱即用的 Claude, Gemini 翻译服务 (Beta)
- Youtube 双语字幕支持字体、字重设置
- 修复长段落换行的单词边界问题 [#86](https://github.com/immersive-translate/immersive-translate/issues/86)
- 修复日韩语言识别
- 修复移动端 Reddit 页面滑动不翻译
- 修复部分页面 DeepL 漏翻
- 修复 Pro 用户配置多设备同步时间不同步
- 优化云同步设置的覆盖问题
- 优化 AI 翻译服务的提示词

## 1.5.2

- 修复通用专家提示词变动覆盖指定 AI 专家提示词 [#1692](https://github.com/immersive-translate/immersive-translate/issues/1692)
- AI 自定义模型名称支持高级语法, 使用 + 增加一个模型，使用 - 来隐藏一个模型，使用 模型名=展示名 来自定义模型的展示名，如: +gpt-3.5-turbo,-gpt-4,gpt-4-turbo=gpt-4-super
- 修复 Gemini 异常返回的报错
- 打印页面时隐藏悬浮球
- 修复 YouTube 全屏时字体大小没有等比例缩放 [#1681](https://github.com/immersive-translate/immersive-translate/issues/1681)

## 1.5.1

- 支持 AI 类翻译服务设置【AI 专家】以指定翻译策略，当前为 Beta 特性，可在 [开发者设置](https://dash.immersivetranslate.com/#developer) 启用 Beta 后，刷新后可以看到【AI 专家】菜单。
- AI 类翻译服务现在可以自定义模型列表了，比如 【OpenAI】，系统只内置了最常用的几个模型，点击模型下拉列表，可以看到最后一项是【设置更多模型】，设置之后以后后自动记住，方便用户测试不同的自定义模型。
- 优化部分情况下译文排版高低不一致的情况。
- Youtube 字幕样式添加重置按钮，可以快速恢复到默认样式。
- 修复 Youtube 中文字幕无法下载的问题。
- 优化繁体中文界面文案。

## 1.4.12

- 修复 reddit 页面打开消息对话框未翻译问题
- 面板【更多】入口添加临时开启译文编辑功能
- 修复 YouTube Shorts 没有字幕的视频总是会显示之前视频的字幕
  [#1655](https://github.com/immersive-translate/immersive-translate/issues/1655)
- 修复 YouTube 双语字幕全屏时无法上下调节字幕的位置
  [#1654](https://github.com/immersive-translate/immersive-translate/issues/1654)
- 支持 [VK Video](https://vk.com/video) 双语字幕
- 支持 YouTube 视频双语字幕的独立开启设置功能（新用户默认开启）
- 优化翻译本地双语字幕错误提示

## 1.4.11

- 兼容 Bing Copilot 页面的输入框翻译
- Youtube 字幕样式控制支持边缘样式
- 支持在设置->翻译服务页面选择默认翻译服务
- 修复 OpenAI SystemPrompt 占位符替换
- 修复自定义用户规则合并问题
- 修复 Netflix 部分视频字幕显示异常
  [#1630](https://github.com/immersive-translate/immersive-translate/issues/1630)
- 修复频繁通过色盘修改译文颜色失效
  [#1628](https://github.com/immersive-translate/immersive-translate/issues/1628)

## 1.4.9

- 将翻译服务单独作为一个
  Tab，现在你可以整体预览所有的翻译服务，并且可以自定义显示哪些翻译服务，默认情况下只展示较少的翻译服务，你可在[更多服务](https://dash.immersivetranslate.com/#services)
  中自定义要显示的翻译服务。
- 设置页支持 [YouTube 字幕样式](https://dash.immersivetranslate.com/#subtitle)
  调节
- 优化了当用户在 Youtube
  网站上设置了字幕语言为中文时，沉浸式翻译双语字幕不显示的问题。
- 支持了新的快捷键，临时翻译
  Claude，可在[快捷键设置页](https://dash.immersivetranslate.com/#shortcuts)中设置

## 1.4.8

- 优化 pdf-pro 大文件翻译性能
- 实现页面文档跳转时的国际化支持（i18n）
- YouTube 新增功能，可临时启用双语字幕
- YouTube 支持双语字幕的下载（限会员）
- 移动端新增手势操作，通过[快捷键设置](https://dash.immersivetranslate.com/#shortcuts)实现输入增强
- 支持 Google Docs 双语翻译

## 1.4.7

- 修复 OpenAI 自定义切换 Pro 在测试按钮下点击翻译失败问题
- 修复 YouTube 字幕快捷图标未显示问题
- 优化扩展语言识别

## 1.4.6

- 修复用户自定义提示词无效问题
- Youtube 字幕字号大小新增50%,150%选项

## 1.4.5

- 修复 Youtube 字幕样式变动未保存问题
- 修复 iOS Safari 全屏字幕消失问题
- 进一步优化 Youtube 字幕翻译速度
- 面板的更多选项支持[文本翻译入口](https://app.immersivetranslate.com/text/)

## 1.4.2

- 支持 Claude 翻译服务
- 优化 OpenAI 多段提示词，支持 YAML 格式，提高了配置的灵活性和易用性
- 大幅优化 Youtube
  字幕翻译速度，并新增支持中英顺序切换、自定义字体颜色及字号大小等功能
- 视频字幕平台支持
  [University of Southampton](https://southampton.cloud.panopto.eu)
- Udemy 双语字幕兼容移动端显示
- 默认隐藏 Gemini
  翻译服务，可在[开发者设置](https://dash.immersivetranslate.com/#developer)中启用
  beta 显示该翻译服务

## 1.3.4

- 支持 Yandex 免费翻译服务
- 优化 Gemini 提示词
- 视频字幕支持设置双语/仅译文显示
- 支持 OpenAI 翻译结果中英文之间空格
- 面板切换仅译文按钮修改为仅在当前页面生效

## 1.3.3

- 优化了Twitter CC视频字幕的翻译显示问题。
- DeepL 服务新增了对阿拉伯语的支持。
- 彩云小译服务现已支持韩语、西班牙语、法语和俄语。
- OpenAI 服务新增了对东北话的支持。
- 面板的自动检测支持显示原文语言。
- 对移动端面板的快捷键描述进行了调整。

## 1.3.2

- 修复移动端无法关闭控制面板

## 1.3.1

- 视频字幕平台支持 [DeepLearning.ai](https://learn.deeplearning.ai)
- 支持网页翻译和视频字幕翻译阿拉伯语、希伯来语等语言的 rtl 显示问题
- 修复 Gemini 翻译希伯来语
- 修复 YouTube 部分繁体中文字幕无法正常显示问题
- 修复 Twitter 字幕在 Safari 上的显示问题
- 修复立即翻译到页面底部快捷键

## 1.2.4

- 修复 ePub 制作占位符未正常替换问题
- 视频字幕翻译支持 [Unreal Sensei](https://www.unrealsenseiacademy.com/)

## 1.2.3

- 优化翻译服务请求频率控制
- 近期微软翻译服务国内请求不稳定，当出错时，自动探测当前可用的翻译服务,用户可以快速切换。
- 优化网络错误文案提示
- 修复配置文本颜色不支持 RGBA
  预览[#1435](https://github.com/immersive-translate/immersive-translate/issues/1435)
- 修复 Safari 插件版本升级总是弹出安装成功页面
- 微软添加支持越南语
- 修复 edx 站点翻译字幕不显示问题

## 1.2.2

- 视频字幕翻译支持
  [pluto](https://pluto.tv/)、[STARZ](https://www.starz.com/)、[Paramount Plus](https://www.paramountplus.com/)、[Rotten Tomatoes](https://www.rottentomatoes.com/)、[Dailymotion](https://www.dailymotion.com/)、[FMovies](https://fmoviesz.to/)、[AniWatch](https://aniwatch.to/)、[iQIYI](https://www.iq.com/)、[Youku](https://www.youku.tv/)、[movie-web](https://movie-web.app/)。同时支持
  Twitter 部分 CC 字幕视频的翻译
- 优化错误弹窗，网络问题错误弹窗自动检测有效免费翻译服务
- 修复沉浸式 iOS APP 支持 YouTube 全屏播放
- 修复 Perplexity.ai 段落翻译问题
  [#707](https://github.com/immersive-translate/immersive-translate/issues/707)

## 1.2.1

- 视频字幕翻译支持
  [Kanopy](https://www.kanopy.com/)、[RachelsEnglishAcademy](https://www.rachelsenglishacademy.com/)、[Hulu](https://www.hulu.com/)、[Three.js Journey](https://threejs-journey.com/)
- 修复部分 Pro 用户在 Chrome 浏览器中无法修改设置的问题
- 支持 YouTube 在 iOS 全屏模式下显示双语字幕

## 1.2.0

- 视频字幕翻译支持
  [LinkedIn](https://www.linkedin.com/)、[Viu](https://www.viu.com/) 平台
- 增加更多平台的视频字幕快捷入口
- 支持指定网站/语言设置仅译文显示
- 修复部分情况下 Safari 打开设置页一直显示 loading
- 支持 input 标签节点翻译
- 优化错误弹窗 UI

## 1.1.9

- 字幕翻译支持 YouTube 直播，[Mubi](https://mubi.com/) 平台
- 优化：设置页面， URL 列表交互 UI（避免歧义，默认不展示复选框）
- 仅译文模式翻译时支持设置译文字体
- 针对 Netflix, Ted，Bloomberg, Udemy, Coursera 添加视频字幕快捷启用入口
- 修复：Safari 部分译文样式（波浪线等）不生效的问题。
- 修复：页面翻译时，鼠标悬停没有重翻的问题

## 1.1.8

- 子翻译服务新增选项跟随主翻译服务
- 双语字幕支持 [Amazon Prime Video](https://www.primevideo.com)
- 进一步优化 Sci-Hub 的内嵌 PDF 翻译功能
- 修复在线 PDF 打开异常问题
- 修复 Netflix 双语字幕连续播放问题

## 1.1.7

- 现在你可以在设置页面-> 【基本设置】 -> 【译文样式】为译文配置指定的字体
- 移动端悬浮球面板新增【翻译指定段落】的快捷配置
- 优化鼠标悬停 Ctrl 的检测灵敏度，避免 `Ctrl+C` 也被认为是 `Ctrl`
- 支持里一个新的快捷键设置，可以快速切换视频字幕是否使用自带的机器翻译字幕
- 在 Sci-Hub 网站里，点击悬浮球即可翻译网页中内嵌的PDF

## 1.1.6

- **移动端支持翻译指定的段落：**
  移动端现在支持对指定段落进行翻译，并新增了多种快捷操作，包括左滑、右滑、双击、三击以及多指同时触控的触发手势，默认未启用，需要用户主动在设置页面
  【鼠标悬停】里选择触发的手势
- **Gemini默认版本更新：** 现在默认为 `v1beta` 版本。
- **修复文言文翻译：** 修复了微软和OpenAI的文言文翻译功能。
- **日语翻译优化：** 对OpenAI的日语翻译进行了进一步优化，以提高准确性和流畅性。
- **沉浸式翻译体验：**
  为了更好地适应用户习惯，我们将YouTube平台全屏模式下的双语字幕快捷方式移至左侧。

## 1.1.5

- 修复 Windows 下黑暗模式下拉框没有颜色的问题。
- 修复 Windows 更多没有左对齐的问题。

## 1.1.4

- **Popup 面板 UI 升级：** 新版设计旨在提升易用性和可理解性。本次更新包括：

  - **一级菜单新增功能：**
    - **双语/仅译文模式切换：**
      现在可以直接在一级菜单中切换“双语翻译模式”和“仅译文翻译模式”，位置在翻译按钮的左侧。
    - **文档翻译入口：**
      “PDF/ePub/字幕文件”的翻译入口已移至一级菜单，方便快速访问。
    - **视频翻译设置：** “视频翻译”的设置入口也被置于一级菜单，以便快速调整。
    - **新增使用说明文档入口：** 提供详细的操作指南和帮助文档。

- **文档翻译入口整合：** 现在，您可以通过一个统一的上传入口来翻译 PDF、ePub
  和字幕文件等。只需点击 Popup 面板里的【PDF/ePub】按钮，无需再选择【更多】。

- **新增对5个视频网站的支持：**
  - 对 Youtube Music 的播客字幕提供支持。
  - 新增支持 iview.abc.net.au 网站。
  - 新增支持 www.nma.art 网站。
  - 新增支持 creativecloud.adobe.com 网站。
  - 新增支持 www.masterclass.com 网站。

## 1.1.3

- 修复了移动版插件在打开PDF页面时出现的显示异常问题。
- 对GPT对话翻译效果进行了优化。
- 针对百度翻译支持了领域翻译。
- 设置页面新增了仅译文翻译模式。
- 在快捷键切换翻译模式时增加了提醒功能。
- 修复了输入框翻译含网址内容时仅部分翻译的问题。

## 1.1.2

- 修复：当页面尚未翻译时，切换翻译服务不生效的问题。
- 优化：在Epub和PDF翻译过程中，如果部分内容翻译失败，现在可以在面板上切换到另一种翻译服务而不会重启整个翻译过程（之前的逻辑是立即使用新的翻译服务重新翻译整本书）。这意味着在翻译进行到一半时，您可以切换到不同的翻译服务，并点击【重试所有错误的段落】，之后系统将使用新的翻译服务继续翻译。
- 优化：调整翻译错误提示的字体大小，以提升可读性。

## 1.1.1

- 修复 Youtube 双语字幕快捷方式英文文案过长的问题。

## 1.1.0

### 新增功能

- **快捷键设置**：新增了一级菜单【快捷键】以及以下可自定义的快捷键功能：

  - 指定组合键以翻译当前输入框内容，补充之前的快速连击3次空格键。
  - 指定组合键以在页面上临时开启“鼠标悬停直接翻译”，再次按下则取消。
  - 新增6个翻译服务（如DeepL, OpenAI, Google, 微软, Gemini,
    腾讯交互翻译）的专用快捷键，方便临时切换翻译服务。

- **插件设置页面UI更新**：

  - 【进阶设置】新增选项，支持用户指定某些单词（如“LLM”）不被翻译。
  - 【进阶设置】新增选项，支持配置翻译段落所需的最少字符数，默认是 4
    个字符，可以设置多一点（比如 20），这样，只有较长的段落才会被翻译。
  - 新增新手教程，涵盖悬浮球设置、视频字幕设置及鼠标悬停设置。

- **YouTube双语字幕**：在YouTube视频播放窗口新增快捷入口，用于开启或隐藏双语字幕（可关闭该功能）

- **Deepl语言支持**：新增对葡萄牙语（巴西）的支持。

- **新用户引导**：新用户首次打开非目标语言页面时，展示悬浮球帮助指引气泡。

### 优化与修复

- **UI优化**：重新设计了页面翻译错误的提示UI，使其更易于理解。当错误较多时，会主动弹窗提示用户。

- **问题修复**：

  - 解决了页面失去焦点时鼠标悬停翻译失效的问题。
  - 修复输入框增强功能中少于3个字符不被翻译的问题。
  - 修复Epub双语制作时部分目录未翻译的问题。

- **功能移除**：删除了双语信息增强功能（在谷歌搜索页面同时展示英语的搜索结果）。

### 其他更新

- **openAI配置更新**：现在支持每秒配置次数的小数设置，比如 0.5，表示 2秒请求1次

## 0.12.14

- 修复：首次安装后，部分机器的默认目标语言识别问题
- 优化： 网页标题默认顺序改为【中文 - 英文】

## 0.12.13

- 修复： 部分情况下 OpenAI 长段落翻译拼接问题。
  [#1276](https://github.com/immersive-translate/immersive-translate/issues/1276)
- 优化：当使用鼠标悬停的时候，页面失去焦点时，再次触发无效的问题。
- 修复： OpenAI 修改 prompt/model 之后，缓存依然还在的问题。

## 0.12.12

- 更新：优化弹窗面板，移除当前网站的部分选项。
- 优化：改进人工字幕合并流程。
- 优化：根据浏览器语言自动设置目标语言。
- 新增：为 [ArtStation](https://www.artstation.com/learning) 学习平台和
  [ZDF](https://www.zdf.de/) 增加双语字幕支持。
- 修复：解决 jstor 列表页标题不翻译的问题
  [#1268](https://github.com/immersive-translate/immersive-translate/issues/1268)。
- 修复：修复 Hacknews 上仅译文部分内容消失的问题
  [#1264](https://github.com/immersive-translate/immersive-translate/issues/1264)。

## 0.12.11

- 双语字幕增加支持
  [HBO Max](https://play.max.com/)、[BBC](https://www.bbc.com/)、[Disney+](https://www.disneyplus.com)、[ARD Mediathek](https://www.ardmediathek.de/)、[ITV](https://www.itv.com/)、[Domestika](https://www.domestika.org)
  平台

## 0.12.10

- 修复了在油猴脚本下的 Gemini 域名授权问题。
- 支持了 Twitter Space 的实时字幕翻译。
- 针对旧版本的油猴脚本，现在在设置页面中添加了更新提示。

## 0.12.9

- 新增支持 Gemini 翻译
- 修复了部分情况下，网页滚动到中间位置时翻译没有及时响应的问题
- 修复了部分视频网站上字幕切换导致译文重复显示的 bug
- 修复了鼠标悬停在某些情况下没有按住快捷键时持续翻译的问题
- 在 macOS 上，优化了面板快捷键的显示名称

## 0.12.8

- 修复在“当前网站设置为永不翻译”时原视频字幕不显示
- 修复与部分插件冲突导致页面无限重翻
- 修复开启长段落换行后部分段落不翻译
- 修复[临时开启网页翻译时长，点击面板【总是翻译该网站】无法取消总是翻译 #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)

## 0.12.7

- 双语字幕增加支持 [TED](https://www.ted.com)、
  [Frontend Masters](https://frontendmasters.com/) 、
  [edx](https://www.edx.org/)、
  [CodeWithChris](https://learn.codewithchris.com/enrollments)、
  [Skillshare](https://www.skillshare.com/) 平台
- 视频全屏的时候，现在默认会隐藏悬浮球。
- 修复 firefox 页面悬浮球操作面板点击抖动问题。
- 支持 pubmed.ncbi.nlm.nih.gov 站点下和 scholarscope 插件协作
- 修复 reddit 输入框翻译页面抖动问题

## 0.12.6

- 修复 YouTube/Web of Science 等网站在切换 tab 时翻译不灵敏的问题。
- 移动端悬浮球现在支持长按操作了，短按时翻译，长按则打开面板。
- 翻译双语电子书现在会把目录也翻译了。
- 搜索增强（谷歌搜索的部分页面展示双语搜索结果）特性现在默认不启用，下个版本将移除该功能。

## 0.12.5

- 修复 Epub 制作电子书从面板点击翻译无效的问题

## 0.12.4

- 在面板上开启双语字幕后，会首先自动刷新一下页面（为了能更准确的显示双语字幕），部分网站依然需要用户手动点击网站上的“CC”按钮以开启字幕。
- 优化油猴、Safari 语言检测
- 为 [Arxiv](https://arxiv.org/abs/1910.06709)
  论文网站所有的论文提供双语版本的快捷入口。
- [悬浮球支持配置成固定在左边 #1168](https://github.com/immersive-translate/immersive-translate/issues/1168)
- [修复学习模式显示问题 #1180](https://github.com/immersive-translate/immersive-translate/issues/1180)
- [临时开启网页翻译时长无法取消总是翻译 #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)
- 优化 PDF 文件初始化问题

## 0.12.3

- 修复【永久禁用视频字幕】功能不生效的问题
  [#1175](https://github.com/immersive-translate/immersive-translate/issues/1175)

## 0.12.2

- 为更多视频平台提供了双语字幕支持，目前已经支持这些平台：
  [Youtube](https://www.youtube.com/)、[Netflix](https://www.netflix.com)、
  [Udemy](https://www.udemy.com/)、
  [Khanacademy](https://www.khanacademy.org/)、
  [Coursera](https://www.coursera.org/)、 [Vimeo](https://vimeo.com/)、
  [Nebula](https://nebula.tv)、[Bloomberg](https://www.bloomberg.com)、[Bilibili](https://www.bilibili.com/)
  等视频网站，（注意：由于技术限制，部分网站在首次开启双语字幕后需要重新刷新页面，或者需等待翻译完成以显示双语字幕）
- 大幅优化插件压缩包大小，比原来减少了一半，下载和更新都更快了。
- 修复扩展 PDF 下载问题
- 在 [Arxiv](https://arxiv.org/abs/1910.06709) 论文网站右侧添加了一个快捷翻译
  PDF 的入口，会跳转到一个干净的 HTML
  页面（只有部分论文支持，因为需要原作者提交源码，所以大概会有 50%
  的论文会显示这个入口）
- 无 .pdf 后缀的在线 PDF 网页，现在可以通过点击页面上的悬浮球直接跳转到 PDF
  翻译页面
- 修复 Safari 下部分输入框增强问题
- 优化 油猴和 Safari 的语言检测

## 0.11.6

- 新增了11种插件和官网的界面语言，现在支持的界面语言达到14种，包括中文简体，中文繁体，英语，日语，韩语，俄语，西班牙语，葡萄牙语，印度语，意大利语，德语，法语，阿拉伯语，波斯语。
- 将上个版本新增的双语分享（清爽模式）修改为双语页面快照分享，这样分享的内容更加原汁原味，以及适配性更广。
- 修复推特输入框末尾表情包无法翻译的情况
- 修复部分场景下翻译了第三方插件内容的情况
- 修复在线 pdf 悬浮球点击无反应

## 0.11.5

- 你现在可以为沉浸式翻译翻译后的双语页面生成一个公开的链接了。
  - [点击](/docs/share/)沉浸式翻译分享图标即可一键生成
- 解决了部分平台无法识别是否支持鼠标的问题
  - 有一些同时支持触摸屏和鼠标的桌面浏览器，沉浸式翻译在技术上无法检测这类平台是否支持鼠标，所以我们在【鼠标悬停】设置里增加了【强制启用鼠标支持】的选项

## 0.11.2-0.11.4

- 优化体验，修复一些 Bug

## 0.11.1

- OpenAI 翻译的模型默认是: GPT3.5-turbo-1106 了
- 优化了OpenAI 的中文Prompt，现在更不容易出现幻觉了
- 减少了OpenAI 的 prompt 长度，从之前的 90 减少到 40，更省流量了。

## 0.11.0

- 修复页面悬浮球点击抖动的问题
- 修复 Azure 翻译的问题

## 0.10.9

- 修复一些小问题

## 0.10.8

- 支持设置悬浮球快捷翻译按钮（PC/移动端都支持）
- 优化油猴语言判断
- 修复 txt 文件翻译

## 0.10.7

- 鼠标悬停支持再次按下Ctrl显示原文
- 鼠标悬停忽略永不翻译语言
- Youtube 双语字幕优化

## 0.10.6

- Youtube 字幕支持仅译文展示
- 新增油猴低版本更新提示
- 修复本地 txt 文件无法翻译问题

## 0.10.5

- 修复 Youtube 偶尔回到首页问题

## 0.10.4

- 修复 Youtube 字幕与 Dual 字幕插件冲突的问题（当检测到 Youtube Dual
  插件存在的时候，则不启用沉浸式翻译的Youtube 字幕翻译，避免冲突）
- 新增【永久禁用视频字幕功能】，如果还有别的冲突的问题，而你又不想用沉浸式翻译来开启双语字幕功能的话。
- 优化字幕断句问题

## 0.10.3

- 修复 自定义 DeppL Auth Key 翻译问题

## 0.10.3

- 完美支持 Youtube 视频双语字幕🎉
- 对于文章页面，现在会优先翻译正文部分，然后再翻译其他侧边栏内容
- 优化 DeepL 翻译上下文联系
- 优化 OpenAI 翻译字幕文件联系上下文

## 0.10.1

- 提高正文翻译优先级，优化翻译体验
- 修复 ins 点击更多文本未翻译问题

## 0.9.8

- 优化体验，修复一些bug

## 0.9.7

- 修复 readwise 高亮的时候自动翻译

## 0.9.6

- 修复清除缓存的时候，退出了用户的登录状态。

## 0.9.5

- 在线电子书 bug 修复

## 0.9.4

- 优化输入增强检测，减少误触
- 电子书及字幕翻译在线化

## 0.9.3

- 输入框翻译：首次使用的时候展示一个弹窗提醒，用户可以选择本次禁用或者永久禁用，避免误触。
- PDF 仅译文导出速度优化，如果选择仅译文导出，目前是直接可以调用系统的 PDF
  预览去导出，速度更快。
- Deeplx 支持多个 URL, 用,分割即可。

## 0.9.2

- PDF 翻译工具迁移到在线版： https://app.immersivetranslate.com/pdf/ ,
  这样油猴，Safari 都可以使用 PDF 翻译，并且出现问题也更好迭代，不需要发版解决。
- POPUP UI 优化，面板更漂亮了！

## 0.9.1

- 修复 Epub 电子书制作的文件名问题

## 0.8.8

- pdf 支持行间距和字间距调节重新识别段落
- epub 在线阅读移动端自动滚动问题修复

## 0.8.7

- pdf 支持仅译文下载
- 修复 safari Google 登录问题

## 0.8.2 - 0.8.6

- 允许设置输入增强连击触发的间隔时间
- 修复一些 Bug

## 0.8.1

- 语言检测优化
- Beta 特性：自定义 API （在开发者设置中开启 Beta 可体验）
- 支持阿里云翻译
- 修复了一些 Bug

## 0.8.0

- 支持用户系统
- 支持[开通 Pro 会员](/pricing)，开通会员后，用户可以畅享 Deepl 和 OpenAI
  翻译和云同步设置
- 鼠标悬停翻译服务可以单独设置
- 输入框翻译服务可以单独设置
- PDF 翻译优化
- 修复了一些 Bug

## 0.7.16

- PDF 翻译新增快捷控制译文样式的选项（PDF
  文件千奇百怪，开启这些选项可能对某些格式较乱的 PDF 文件有用）
- iOS 和 macOS 版本重新上架苹果商店国区

## 0.7.15

- 接苹果通知，在 iOS 和 macOS 版本暂时下架 OpenAI 翻译，尝试重新上架国区。

## 0.7.11- 0.7.14

- 修复：Gmail 翻译全部区域问题
- 由于 Safari 对插件下载的限制（Bug），暂时禁用 Safari 的 PDF 导出功能
- 修复一些其他问题

## 0.7.10

- Popup 浏览器图标面板 UI 升级，更有设计感一点～
- 修复部分日语段落不翻译的问题

## 0.7.9

- PDF 终于支持导出双语版了！你可以点击【保存】按钮导出翻译后的双语 PDF 文件
- 自定义规则支持与默认内置规则合并了，如：`{"id":"youtube","selectors.add":["#test"]}`
  表示在原有的 selectors 基础上新增一个 `#test`, `selectors`
  表示覆盖默认的，`selectors.remove` 表示删除默认的 selectors 中的某一项。
- 更新 Safari 图标, 更大一点。
- 其他 Bug 修复

## 0.7.8

- Bug 修复

## 0.7.7

- 适配 Safari 的系统风格，Safari 的扩展图标改为透明轮廓
- 增加浏览器图标状态变化，当某个网页已翻译时，浏览器图标右下角自动增加一个 ✅
- 为新用户自动开启常用英文网站翻译
- 修复 https://claude.ai/ 的翻译问题

## 0.7.6

- 输入增强支持翻译结果 ctrl+z 撤销
- 支持飞书文档阅读模式下翻译
- 适配 https://pi.ai/talk

## 0.7.5

- 修复油猴图标不显示的问题
- 修复若干问题

## 0.7.4

- 修复若干问题
- 设置页面支持全选 url 进行批量删除
- 支持启用/关闭 Youtube 字幕翻译，防止与其他相关插件冲突。
- 有道翻译支持设置领域和术语 id

## 0.7.2

- 输入框增强：允许省略前缀//，直接 3
  个空格即可触发翻译整个输入框的内容，也可以在设置页面关闭此选项。

## 0.7.1

- 支持搜索增强啦，启用后，在谷歌/谷歌新闻用中文搜索时，右边栏自动显示对应英文关键词的搜索结果，默认为启用状态。
  - 原因：我们发现，在谷歌搜索里，中文关键词和英文关键词的搜索结果会有非常大的不同，在启用沉浸式翻译搜索增强功能后，我们会自动用英文为你搜索同样的关键词并展示在右侧。如果你不需要该功能的话，可以选择禁用它。
  - Safari 浏览器由于 API 限制，暂不支持。

## 0.6.20

- 修改默认设置：由于大量用户反馈安装后不会使用，他们对翻译工具的预期是装了之后就能自动翻译英语网页，所以从该版本起，对于中文用户，开启了默认翻译英文页面的选项（如果用户之前有过设置总是翻译的语言，那么会尊重用户的设置，该变更只修改了扩展的初始设置），需要取消的话，可以很方便的在
  [Popup 面板或者设置页面取消](/docs/faq/#%E5%A6%82%E4%BD%95%E5%85%B3%E9%97%AD%E8%87%AA%E5%8A%A8%E7%BF%BB%E8%AF%91)

## 0.6.19

- 修复 PDF Bug
- 修复 web of science Bug
- 适配 feeder.com
- 修复 epub 不翻译部分书籍

## 0.6.18

- 修复 Safari Popup 弹窗宽度溢出的问题
- 构建流程优化

## 0.6.17

- 优化错误提示
- 优化目标语言选择，现在只会展示对应翻译服务支持的语言了
- PDF 译文优化
- 适配 Good Reads 网站，亚马逊和南华早报网站

## 0.6.16

- 增加 PDF 无权限页面显示
- 修复 PDF 正文列表段落的显示
- 调大 PDF 小字体的在 chrome 和 safari 上的缩放比列

## 0.6.15

- 修复打开 PDF 文件的时候，扩展面板上提示没有权限的问题。
- 修复当网站被设为永不翻译的时候，输入框增强功能无法启用的问题。

## 0.6.14

- PDF 翻译优化，译文区域现在可以编辑/拖动/删除了
  - 左上角拖动，右上角删除，右下角改变大小
- Windows 下拉框左对齐
- 支持繁体中文和简体中文互翻

## 0.6.13

- 修复鼠标悬停重复翻译的问题
- PDF 译文支持拖动改变大小以及编辑译文的内容

## 0.6.12

- 修复部分浏览器 Epub 翻译图片变小的问题
- 优化输入框翻译，现在在 Bard 中流畅的使用了

## 0.6.10

- OpenAI 默认模型改为 0613 版本
- 修复部分输入框样式
- 更智能的判断是否为导航区域，如果是的话，则不进行翻译
- 修复可能的 XSS 注入攻击

## 0.6.8

- 扩展面板现在可以对不支持的页面进行提示（比如没有权限的页面和非 HTML 页面）
- 输入框增强支持翻译中展示 Loading 状态
- 更新默认的翻译中 loading 颜色
- 当输入框配置为无前缀时，支持 `ja 你好`翻译为日语，`英文 你好`翻译为英文

## 0.6.6

- 修复： 部分区域不翻译的问题（quora）

## 0.6.5

- Google Bard 优化
- 输入框翻译支持无需前缀直接翻译整个文本框
- 优化 OpenAI 翻译无脑加句号的问题，（如果在原文里检测不到句号，如果 openai
  返回了句号，那就去掉）
- safari 字幕文件不识别的问题

## 0.6.3

输入框翻译的默认语言可以省略空格了，也就是 //你好世界 也可以被翻译了。

## 0.6.2

最令人兴奋的输入框增强功能来了：

- 在任何网页中的输入框输入： // 你好世界，然后三连击空格键，即可将该段翻译为英文
- 你也可以指定翻译为某语言： /ja
  你好世界，然后三连击空格键，即可将该段翻译为日文

[点此查看 30 秒快速介绍](/docs/input/)

## 0.6.0

- 6
  月的第一个版本，从之前的个人子域名<https://immersive-translate.owenyoung.com>迁移到了新的域名
  <https://immersivetranslate.com/>
- 功能方面基本没有变化(下一个版本将会有新特性！)

## 0.5.17

- 修复： 双语电子书导出后没有图片的问题

## 0.5.16

- 修复： openai 翻译繁体中文问题

## 0.5.15

- 优化： 最短触发翻译的段落字数修改为最小 4
  个字符，以减少困惑，同时利用其他特征避免翻译网站的导航和尾部区域。
- 修复： Github details 展开之后无法翻译的问题。

## 0.5.14

- 修复： 部分网页的图片复制后变大的问题
- 修复： medium 评论区不翻译的问题
- 修复： 部分网页的图片被错误的复制问题

## 0.5.12

- 特性： 分割线译文样式增加单行译文的垂直分割线
- 修复： 极少数情况下段落分割的问题。
- 为 iOS 新用户提供了一个很好的初次设置引导页面。

## 0.5.11

- 字幕翻译支持导出仅译文
- 修复： 鼠标悬停部分元素不识别
- 修复：推特部分换行不识别问题
- 修复：电子书制作样式不生效问题

## 0.5.10

- 修复： 推特换行无法识别的问题
- 修复： Reddit 详情页返回部分段落无法翻译的问题
- 修复： 部分 Code 标签未正确识别的问题

## 0.5.9

- 修复： 部分情况下段落分段问题
- 修复： 油猴脚本切换仅显示译文
- 修复： 电子书在线阅读的样式不生效问题

## 0.5.8

- 修复： 临时设置网站翻译时长不生效问题。

## 0.5.7

- 超多更新！
- 仅显示译文功能来了！ 点击【更多】->【切换为仅显示译文】
  - 支持自定义快捷键，在界面设置-> 快捷键设置中设置
- 优化 OpenAI 请求频率限制问题
- ChatGPT 默认改为 mobile 模型，更快！
- 网页核心解析重构，这意味着：
  - 大型网页秒翻译
    - 比如： <https://pve.proxmox.com/pve-docs/pve-admin-guide.html>, 之前需要
      30 秒，现在秒翻
  - 复杂网页占用内存超低
    - 比如：
      <https://www.wsj.com/articles/global-stocks-markets-dow-news-05-05-2023-cb142c76?mod=hp_lead_pos1>
  - 对更多网站的适配
- 支持了所有 ShadowRoot 的网站翻译
  - 比如： <https://bugs.chromium.org/p/chromium/issues/detail?id=418987>
  - 比如：
    <https://news.yahoo.com/gma/virginia-mom-facing-charges-6-190600893.html>
    的评论区
- 修复之前 Next.js 等具有水合作用的网站翻译后白屏的问题
  - 比如： <https://webpack.js.org/>
- 修复了修改鼠标悬停的快捷键需要刷新页面才生效的问题
- 修复了 TXT 文件 换行识别的问题。

- Lots of updates!
- The 'Show Translation Only' feature has arrived! Click on 'More' -> 'Switch to
  Show Translations Only'.
  - Supports custom shortcuts, which can be set in 'Interface Settings' ->
    'Shortcut Settings'
- Optimized for OpenAI request rate limit issue
- Web core parsing has been rebuilt, which means:
  - Instant translation for large websites
  - Minimal memory usage for complex web pages
  - Better compatibility with more websites
- Now supports translations for all websites with ShadowRoot
- Fixed the white screen issue after translating websites with hydration, such
  as Next.js
- Fixed the issue where changing the mouse hover shortcut required a page
  refresh to take effect
- Fixed the issue with recognizing line breaks in TXT files.

## 0.5.6

- Fix: macOS new tab popup issue.
- Feat: New guide page for new user.

## 0.5.5

- Fix: Mouse over area issue.

## 0.5.4

- Fix: Spa Page duplicate

## 0.5.3

- Fix: Mouse hover hotkey listener.
- Fix: PDF document translate
- Feat: Add new client guide page

## 0.5.2

- Fix: userscript mouse hover shortcuts settings

## 0.5.1

- Fix: OpenAI API not works.

## 0.5.0

- Feat: Translate the current paragraph when mouse hover.
- Feat: Refactor PDF translation, now you can translate most PDFs with Immersive
  Translate
- Fix: Disable Context Menu not working
  [#428](https://github.com/immersive-translate/immersive-translate/issues/428)
- Fix: Avoid Content Security Policy for [Mastondon](https://mastodon.social/)

## 0.4.11

- Fix: userscript permission (only for userscript).

## 0.4.8

- Feat: Bing Translate to Microsoft Translate for more stable quality.
- Fix: Pure TXT web page like
  [this](https://edoras.sdsu.edu/~vinge/misc/singularity.html)
- Performance: Exclude some child advertising pages in the website, and the
  performance has improved a little

## 0.4.7

- Fix: Firefox Userscript popup missing.

## 0.4.6

- Feat: Allow third party send document event to call `toggleTranslatePage`
- Feat: iOS app add enable extension button and communities link
- UI: OpenAI settings field model use select instead of text input box.

## 0.4.5

- Fix: iOS 15.0 safari extension issue.
- Fix: macOS safari extension shortcuts
- Fix: content security policy popup for extension, and partly for userscript.

## 0.4.4

- Chore: Remove console.log

## 0.4.3

- Fix: sup, sub tag whitespace detection.
- Feat: support ChatGPT Plus Website as Translation Service, This is a beta
  feature, so you can access it by enabling Beta Feature on developer settings.
  This is very slow, cause chatgpt can only send one request at once. Make sure
  you have ChatGPT Plus Account, cause there are more limit on Free Account, and
  I'm not sure if this bring risk for your account, be careful to use it.

## 0.4.1

- Fix: firefox context menu dispeared after restart.
- Support Azure openai

## 0.4.0

- Feat: Support Translate Local Subtitle File (.srt,.ass,etc.)

## 0.3.17

- Feat: Support translate local .txt file.
- Fix: Context Menu may not avaliable sometimes.
  [#273](https://github.com/immersive-translate/immersive-translate/issues/273)

## 0.3.16

- Fix: keep &nbsp; as whitespace.
- Remove: Take down Papago, as
  [the service is down](https://github.com/immersive-translate/immersive-translate/issues/310)

## 0.3.15

- UI: allow no API key for openai
- UI: allow Open AI reset to the default settings

## 0.3.14

- Dependence: Upgrade pdf.js to the latest version
- Fix: pdf selection background color
- Fix: whitespace detect

## 0.3.13

- Fix: ebook builder specific character issue, like some chapter path is
  `xxx' xxxx`
- UI: fold openai custom options by default.
- UI: Add exporting status for epub export.
- Fix: Gpt4 default prompt

## 0.3.12

- Feat: We can custom Marker translation theme background color now.
- Fix: postMessage when init page broke somesites, now we will do this only when
  we really translate pages
- Fix: ebook progress issue.
- Fix: better for split long paragraph, 1.5 billion, 25.5%, Mr. will not be
  considered as a boundary

## 0.3.11

- Fix: ebook reader dark mode text color
- Fix: openAI prompt

## 0.3.10

- Better: detect Japanese/Korean container.
- Fix: Ebook Builder Progress 99% stopped.

## 0.3.9

- Fix: Options UI switch translation services input state not changed.

## 0.3.8

- UI: loading color more transparent
- Fix: Detect Ebook Language.
- Feat: Add translate progress for ebook builder, and a beautiful confetti after
  success.
- Feat: Add retry all failed paragraphs for retry button.
- Fix: Deepl Error handle

## 0.3.7

- Fix: ebook reader can not load images on Chrome.

## 0.3.6

- UI: better for make ebook page UI

## 0.3.5

- Fix: userscript ebook export
- Feat: add custom API endpoint for OpenAI
- Feat: add temp translate website time options on `Advanced Settings`

## 0.3.4

- CI: Build failed

## 0.3.3

- Fix: ebook maker for Kindle
- Change: Loading icon color, from black to blue, for adapt the dark mode web
  page.
- Feat: Support local html translate for extension

## 0.3.2

- Fix: Options Form Input cursor moving.
- Feat: OpenAI support custom apiUrl for develope settings.

## 0.3.1

- Feat: update dark icon to transparency.
- Fix: Wrong order for long paragraph

## 0.3.0

- Version: From now on, we will change the minor version number once a month,
  for example, now in March, the version will start from 0.3.0, in April, the
  version number will start from 0.4.0, next April, the version number will be
  1.4.0, and so on. This is because it does not make sense for extensions to
  follow semantics, but standardizing version numbers according to the laws of
  time is motivation for development to keep updating, and for users to find
  problems more easily.
- Feat: Support dark icon for firefox

## 0.2.86

- Add max text length option for per request with Open AI
- Fix: ebook identifier duplicated
- Feat: Support txt web page translation

## 0.2.85

- Fix: some epub file can not be found.

## 0.2.84

- Feat: Support Ebook Reader and Maker

## 0.2.83

- Feat: Allow password input Form show password.

## 0.2.82

- Fix: Some site use `span` for styles, so we use `font` instead of span for
  translation target wrapper
- Fix: OpenAI max tokens limit, change max chars from 1500 to 1300.

## 0.2.81

- Fix: m.youtube.com
- Fix: options form UI
- Fix: Open AI prompt
- Feat: Support OpenAI multiple keys, use `,` split them.

## 0.2.80

- Feat: Add Enable/Disable Menu for popup -> more
- Fix: DingTalk Message conflict

## 0.2.79

- Fix: Open AI for space paragraph

## 0.2.78

- Feat: support OpenAI CHATGPT 3.5 (支持 OpenAI ChatGPT 3.5 接口)
- Feat: Add new theme Solid Border (新增新主题，实线边框)

## 0.2.77

- Fix: multiple code tag
  error.[#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.76

- Fix: multiple code tag error
  [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.75

- Feat: Support custom immediate translation text count for different
  translation service.

## 0.2.74

- Feat: Support Tencent (alpha)
- Fix: openai translation
- Fix: unknown tags inline check

## 0.2.73

- Feat: Support Grey Translation Theme
- Fix: Github Trending Page

## 0.2.72

- Fix: firefox mobile verify translation service net issue.

## 0.2.71

- Fix: Open AI userscript permission

## 0.2.70

- Fix: Open AI placeholder

## 0.2.69

- Feat: Support Open AI as translation service.
- Feat: Support verify translation service on options.html
- Feat: Support custom main frame cuase some site is not using body as the main
  frame

## 0.2.68

- Support Caiyun (Alpha)
- Fix unknow block tags

## 0.2.67

- Feat: Add `<all>` for always translate languages, so now you can use it to
  translate all language except the target language, and never translate
  languages
- Fix: Allow config custom google API
- Better: Deepl Free support
- Fix: hight memory use for userscripts and extension (by removing opencc zh-CN
  to zh-TW, instead with Google translate)
- Fix: Relingo
  [#159](https://github.com/immersive-translate/immersive-translate/issues/159)
- Fix: Azure translate setup but still show (need setup)

## 0.2.66

- Fix: PDF file translation failed, Bug from 0.2.60 for supporting deepl from
  zh-CN to zh-TW

## 0.2.65

- Support throttle request for multiple frame
- Do not translate page title when in iframe

## 0.2.64

- Fix: openl choose translation services
- Feat: Support is translate title option

## 0.2.63

- Feat: Support Azure Translate Service
- Feat: Support Papago Translate Service
- Fix: native firefox android google drive sync.
- Fix: change transparency from 0.4 to 0.618
  [#147](https://github.com/immersive-translate/immersive-translate/pull/147)
- Fix: popup shortcuts tips
- Performance: serial to cocurrency requests
- Better for detect Japanese count

## 0.2.62

- Feat: Add waitForSelectors rule, for fixing some sites like reddit

## 0.2.61

- Fix: userscript is too big for greasy fork
- Better: reduce file size

## 0.2.60

- Feat: Support zh-CN to zh-TW for Deepl
- Feat: Immersive Translate Deepl Feature
- Feat: Support custom font size zoom
- Fix: Steam forum style
- Fix: global style not changed after dynamic elements generated
- Fix: promote exclude priority
- UI: about page change
- Fix: some math element stayoriginal

## 0.2.59

- Fix: Unkowntags Block Element
- Fix: translate=no element overide
- Fix: url match with multiple \*

## 0.2.58

- Feat: Support custom translation text color, border color.

## 0.2.57

- No changes, rebuild

## 0.2.56

- Fix duplicate translate for inline elements with code element.
- Fix unknown tags inline/block check
- Feat: support injected css on developer board
- Feat: trim authKey, appid appSecret
- Better: open settings page on new tab (but not for Stay)

## 0.2.55

- Try fix deepl api charset

## 0.2.54

- Remove tabs permission for chrome store rejection
- Fix translate the whole page, footer is ignored
- Add notes to about page
- Support custom url from buildin Config

## 0.2.53

- Fix userscript google drive sync error.

## 0.2.52

### Code

- Use the latest esbuild
- Use the latest deno version
- CI: submit source code to firefox

## 0.2.51

- Fix Google Auth Need Login on Chrome/Firefox
- Replace translation service links
- Better for permission.
- remove minify.

## 0.2.50

- Fix google drive upload issue (really)
  [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.49

- Remove shortcuts alt+d, alt+s cause may conflict with native shortcuts.
- Fix google drive upload issue
  [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.48

- Better for speed, by add minLength to 50 for language detecting.
- Fix Google Drive token validate.

## 0.2.47

- Fix deepl api

## 0.2.46

- fix block mark

## 0.2.45

- Fix element innerText is undefined
- Fix caiyun translation undefined source language

## 0.2.44

- Fix userscript toggle mask
- Fix toggle mask logic

## 0.2.43

- Fix userscript toggle mask with touch event.
- Fix speed (by remove sleep(300))

## 0.2.42

- Fix mask hover when toggle mask again.
- Add mask shortcuts for mobile
- Fix userscript cloud sync issue
- Move advanced option page to left menu.
- Add retry logic to translation service

## 0.2.41

- Fix userscript niu translation
- Fix xhtml translate

## 0.2.40

- Fix beta feature show
- Fix popup setting page on new tab page
- Fix translation placeholder replace

## 0.2.39

- Support shortcuts for show mask translation
- Support enable beta feature at develper panel
- Fix shortcuts in mobile extension

## 0.2.38

- Support loading theme
- Fix getpocket.com
- Fix aside footer for body area
- Fix import/export icon

## 0.2.37

- Fix frame exclude mark

## 0.2.36

- Support sync to Google Drive

## 0.2.35

- Fix japanese rb, rt tag ignore.
- Better for popup ui more
- Better for bad userscript tips
- Add contribution to about page
- Fix volc translate for auto detect language

## 0.2.34

- Fix multiple language speed

## 0.2.33

- Support vertical writing mode, like Japanese.
- Add 3 themes
- Add Niu translation service

## 0.2.32

- Fix PDF basic translation
- Fix popup select a not configed service, go to options page.
- Fix stay open settings.
- Fix multiple language detect speed

## 0.2.31

- Fix dynamic iframe css inject

## 0.2.30

- Support userscript inline iframe translation.
- Support shadowroot translation. For example:
  <https://www.foxnews.com/politics/minnesota-senate-passes-abortion-bill-opponents-call-most-extreme-nation>
  Conversation area.
- also check sync rule on popup

## 0.2.29

- Fix Facebook translation
- Support show context menu option.

## 0.2.28

- Remove not standard match for userscript

## 0.2.27

- Support inline iframe translation. (Only for extension, not avaliable for
  userscript)
- Fix multiple language translation

## 0.2.26

- Fix firefox android addon
- Add advanced settings for translation newline

## 0.2.25

- Support iframe translate, like QQ mail, emebed tweet.

## 0.2.24

- Add temp translate site for a while
- Fix stay.app userscript browser API
- Fix stay.app options page

## 0.2.23

- Fix multiple language page translation

## 0.2.22

- Fix userscript build

## 0.2.21

- Fix firefox online pdf translate

## 0.2.20

- Fix macaque request issue
- Fix mark highlihgt line heigh

## 0.2.19

- Fix tencent smart japanese
- Fix haikuo world browser

## 0.2.18

- Fix client url change, auto remain the translate state.
- Remove aside container as the translate container.
- Refactor popup position.

## 0.2.17

- Change highlight to mark
- Add hightlight translation theme

## 0.2.16

- Macaque compatibility

## 0.2.15

- Fix touch bounce issue

## 0.2.14

- Fix safari globalThis.GM not working

## 0.2.13

- Support Userscript Popup Draging
- Support There Fingers on Touch device to trigger toogle translate pages
- Support Hiding the userscript popup icon.

## 0.2.12

- Better for inoreader

## 0.2.11

- Fix
  [#28](https://github.com/immersive-translate/immersive-translate/issues/28)
  Annas archive 页面主要内容无法被翻译

## 0.2.10

- Fix pdf lineheight distance

## 0.2.9

- Fix exclude elements mark
- Fix deno type check
- remove importmap
- Fix context menus translation
- restore page when never translate this site enabled
- Add description for add url

## 0.2.8

- Detect the user agent language for interface language
- Fix line break bug.

## 0.2.7

- Fix grease monkey request

## 0.2.6

- Fix
  [#30](https://github.com/immersive-translate/immersive-translate/issues/30),
  file url match issue

## 0.2.5

- bump version for ci test

## 0.2.4

- catch message connection error for popup.

## 0.2.3

- Fix
  [#26](https://github.com/immersive-translate/immersive-translate/issues/26)
  create context multiple times

## 0.2.2

- Fix PDF sample file
- Fix Firefox pdf local file
- Fix pdf shortcuts

## 0.2.1

- Support Grease Monkey Shortcuts manager.
- Fix match regex
- Fix youtube comments.
- Fix reddit mobile compact version
- Fix fulltext translate issue

## 0.2.0

- Fix PDF two column.
- Fix Chrome/Edge Store version bug.
- Fix
  [#21](https://github.com/immersive-translate/immersive-translate/issues/21)

## 0.1.2

- Publish to Firefox addon
- Publish to Edge
- fix pdf margin.
- Change sample pdf file

## 0.0.62

- Fix pdf format, indent.
- Fix telegra.ph prevent element change

## 0.0.61

- Fix span element close.
- Fix permission for early browser

## 0.0.60

- Fix Chrome PDF

## 0.0.59

- Initial Support for PDF

## 0.0.58

- Edit translation theme description

## 0.0.57

- Change popup ui, for more easy use

## 0.0.56

- Fix chrome timeout
- Fix split sentence error.

## 0.0.55

- Fix display none element show.
- refactor element mark

## 0.0.54

- Support line break for X characters.

## 0.0.53

- use sendMessage insteadof connect, cause chrome will disconnect the port after
  5 minites
- better for detect text containers

## 0.0.52

- Do not translate the paragraph that only has placeholders elements, for
  [example](https://github.com/nank1ro/solidart), the first line.
- Better for detect child elements.

## 0.0.51

- Fix cache issue
  [#12](https://github.com/immersive-translate/next-immersive-translate/issues/12),
  [#7](https://github.com/immersive-translate/next-immersive-translate/issues/7)
- Fix options UI font size

## 0.0.50

- Fix block img be translated.

## 0.0.49

- Fix firefox extension

## 0.0.48

- Fix chrome extension

## 0.0.47

- rewriting message with background, use connect instead of sendMessage
- add reddit mobile support
- fix pre white space for some article

## 0.0.46

- Format userscript meta info

## 0.0.45

- userscript use one file.
- add timeout for cache request

## 0.0.44

- Fix split tencent error.
- Fix inline sup element error.
- Better for twitter

## 0.0.43

- Fix tweet br
- Fix global translate.

## 0.0.42

- Fix BR tag
- treat block tags to rules

## 0.0.41

- Fix inline element check
- Add developer debug log option

## 0.0.39

- Fix translation service contains mock2

## 0.0.38

- Support Cache result for userscript
- Add Options UI
- Support detect more content containers

## 0.0.37

- Fix change popup translation service not work
- Fix reddit mobile post content translate.

## 0.0.36

- Fix Wikipedia special character
  [#6](https://github.com/immersive-translate/next-immersive-translate/issues/6)
- Fix userscript icon size.
- enable all sites to detect paragraph language.

## 0.0.35

- Fix youtube go to next page
- Support Youtube search page.
- Fix options advanced switch.
- Fix img tag , hiddent tag
  [#5](https://github.com/immersive-translate/next-immersive-translate/issues/5)
- Fix Google Search Force refresh
  [#4](https://github.com/immersive-translate/next-immersive-translate/issues/4)
- Support Table result of Google
  [#3](https://github.com/immersive-translate/next-immersive-translate/issues/3)
- Fix Wikipedia blank
  [#2](https://github.com/immersive-translate/next-immersive-translate/issues/2)

## 0.0.34

### Break Changes

- The Default Hot Key to toggle translate has been changed to `alt+A`, cause
  it's the most convinient key to type.

### Others

- Support set immediate translation mode, so you can let the web page translate
  as quick as possible.
- Support set page area that need to translate. so you can translate more area.
- Support set the first x text count to translate immediately.
- Fix translate duplicately when change translate
- Better popup UI

## 0.0.33

- Support more languages, zh-TW, en

## 0.0.32

- Fix translate local file after saved. Fixed
  [#1](https://github.com/immersive-translate/next-immersive-translate/issues/1)
- Add dist js file to public repo

## 0.0.31

- Support Translate the Whole Page
- Support Translate page immediatlly
- More Config UI
- Reflect the theme
- Add new icon
- Add new translation theme dashedBorder

## 0.0.30

- Better for dashed theme

## 0.0.29

- Fix paragraph valid.
- Add dotted, thinDashed theme
- Better for dashed, highlight theme

## 0.0.28

- Fix underline
- Add dashed, paper theme
- Fix header detected

## 0.0.27

- Support translationTheme

## 0.0.26

- Fix volc alpha userscript connect permission.
- Fix version clickable.

## 0.0.25

- Support selectorMatches, so we can match all manstondon now.
- Fix Firefox userscript error.

## 0.0.23

- Better for Chinese detect
- Fix reddit innerText issue

## 0.0.22

- Support deeplx
- Fix multiple translation when switch service

## 0.0.21

- Fix some span tag is block element

## 0.0.20

- Support not translate hash tag like #hash , at tag like @xxx, $tag, like $APPL
- Support block element

## 0.0.18

- Support deepl, bing,baidu,youdao, volc, openl, caiyun.

## 0.0.13

- Support userscript

## 0.0.4.8

- Fix code order.
- Support basic popup ui

## 0.0.4.6

- Support check new version

## 0.0.3

- Support local files

## 0.0.2

- Support Dynamic Elements
- Support visible translate
