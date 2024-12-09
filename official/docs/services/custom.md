# 自定义接口翻译

## ImmersiveL

[沉浸式翻译模型](https://github.com/immersive-translate/ImmersiveL)已支持自定义接口

在【设置】页面，开发者模式中启用【Beta】特性，即可在翻译服务中看到：

![](https://s.immersivetranslate.com/assets/20231026-125902.jpeg)

## 请求

- method: POST
- content-type: application/json
- body
  - source_lang: 源 {语言代码}
  - target_lang: 目标 {语言代码}
  - text_list: 翻译文本字符串的数组

## 响应

- response
  - translations: 数组
    - detected_source_lang: 翻译原文本 {语言代码}
    - text: 已翻译的文本

## 保留占位符

目的是针对网页翻译中的非文本内容进行占位，翻译之后保留该特殊符号，我们会在翻译完成之后将相应的非文本内容进行还原

### 格式

字符串数组

- 0: 成对分隔符的左边
- 1: 成对分隔符的右边
- 2: 标签分隔符

#### 例子

- 例子1: ['{', '}']

```
   原文: 😁 hello 👏🏻 wrold
占位原文: {0} hello {1} world

占位译文: {0} 你好 {1} 世界
   译文: 😁 你好 👏🏻 世界
```

- 例子2: ['', '', 'b']

```
   原文: 😁 hello 👏🏻 wrold
占位原文: <b0></b0> hello <b1></b1> world

占位译文: <b0></b0> 你好 <b1></b1> 世界
   译文: 😁 你好 👏🏻 世界
```

## 语言代码

```bash
auto: 自动检测语言, Detect Language
af: 阿非利卡语, Afrikaans
am: 阿姆哈拉语, Amharic
ar: 阿拉伯语, Arabic
az: 阿塞拜疆语, Azerbaijani
be: 白俄罗斯语, Belarusian
bg: 保加利亚语, Bulgarian
tn: 泽纳语, Zana
bn: 孟加拉语, Bengali
bs: 波斯尼亚语, Bosnian
ca: 加泰罗尼亚语, Catalan
ceb: 宿务语, Cebuano
co: 科西嘉语, Corsican
cs: 捷克语, Czech
cy: 威尔士语, Welsh
da: 丹麦语, Danish
de: 德语, German
el: 希腊语, Greek
en: 英语, English
eo: 世界语, Esperanto
es: 西班牙语, Spanish
et: 爱沙尼亚语, Estonian
eu: 巴斯克语, Basque
fa: 波斯语, Farsi
fi: 芬兰语, Finnish
fil: 菲律宾语, Filipino
fj: 斐济语, Fijian
fr: 法语, French
fy: 弗里斯兰语, Frisian
ga: 爱尔兰语, Irish
gd: 苏格兰盖尔语, Scottish Gaelic
gl: 加利西亚语, Galician
gu: 古吉拉特语, Gujarati
ha: 豪萨语, Hausa
haw: 夏威夷语, Hawaiian
he: 希伯来语, Hebrew
hi: 印地语, Hindi
hmn: 蒙语, Hmong
hr: 克罗地亚语, Croatian
ht: 海地克里奥尔语, Haitian Creole
hu: 匈牙利语, Hungarian
hy: 亚美尼亚语, Armenian
id: 印度尼西亚语, Indonesian
ig: 伊博语, Igbo
is: 冰岛语, Icelandic
it: 意大利语, Italian
ja: 日本语, 日本語
jw: 爪哇语, Javanese
ka: 格鲁吉亚语, Georgian
kk: 哈萨克语, Kazakh
km: 高棉语, Khmer
kn: 卡纳达语, Kannada
ko: 韩语, Korean
ku: 库尔德语, Kurdish
ky: 吉尔吉斯语, Kyrgyz
la: 拉丁语, Latin
lb: 卢森堡语, Luxembourgish
lo: 老挝语, Lao
lt: 立陶宛语, Lithuanian
lv: 拉脱维亚语, Latvian
mg: 马尔加什语, Malagash
mi: 毛利语, Maori
mk: 马其顿语, Macedonian
ml: 马拉雅拉姆语, Malayalam
mn: 蒙古语, Mongolian
mr: 马拉地语, Marathi
ms: 马来语, Malay
mt: 马耳他语, Maltese
mww: 白苗语, Bai Miao
my: 缅甸语, Burmese
ne: 尼泊尔语, Nepali
nl: 荷兰语, Dutch
no: 挪威语, Norwegian
ny: 奇切瓦语, Nyanz(Chichewa)
otq: 奥托米语, Querétaro Otomi
pa: 旁遮普语, Punjabi
pl: 波兰语, Polish
ps: 阿富汗/普什图语, Afghan/Pashto
pt: 葡萄牙语, Portuguese(Portugal,Brazil)
ro: 罗马尼亚语, Romanian
ru: 俄罗斯语, Russian
sd: 信德语, Sindhi
si: 僧伽罗语, Sinhala
sk: 斯洛伐克语, Slovak
sl: 斯洛文尼亚语, Slovenian
sm: 萨摩亚语, Samoan
sn: 修纳语, Shona
so: 索马里语, Somali
sq: 阿尔巴尼亚语, Albanian
sr: 塞尔维亚语, Serbian
sr-Cyrl: 塞尔维亚语（西里尔文）, Serbia(Cyrillic)
sr-Latn: 塞尔维亚语（拉丁文）, Serbia(Latin)
st: 塞索托语, Sesotho
su: 巽他语, Sundanese
sv: 瑞典语, Swedish
sw: 斯瓦希里语, Swahili
ta: 泰米尔语, Tamil
te: 泰卢固语, Telugu
tg: 塔吉克语, Tajik
th: 泰语, Thai
tlh: 克林贡语, Klingon
tlh-Qaak: 克林贡语（piqaD）,Klingo(piqaD)
to: 汤加语, Tongan
tr: 土耳其语, Turkish
ty: 塔希提语, Tahiti
ug: 维吾尔语, Uyghur
uk: 乌克兰语, Ukrainian
ur: 乌尔都语, Urdu
uz: 乌兹别克语, Uzbek
vi: 越南语, Vietnamese
wyw: 文言文, 文言文
xh: 班图语, Bantu
yi: 意第绪语, Yiddish
yo: 约鲁巴语, Yoruba
yua: 尤卡坦玛雅语, Yucatan Mayan
yue: 广东话（传统）, Cantones(Traditional)
zh-CN: 简体中文,, 简体中文
zh-TW: 繁体中文, 繁體中文
zu: 祖鲁语, Zulu
```
