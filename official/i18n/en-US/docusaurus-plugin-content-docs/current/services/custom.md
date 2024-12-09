# Custom Interface Translation

## ImmersiveL

[Immersive Translate Model](https://github.com/immersive-translate/ImmersiveL) has support for custom interfaces

Turn on **Enable Beta Testing Features** in `Options > Developer settings`.
![](https://s.immersivetranslate.com/assets/turn_on_beta_en.jpeg)

Then select **Custom API** in `Options > General` to open the configuration page.
![](https://s.immersivetranslate.com/assets/select_custon_api_en.jpeg)

## Requesting

- method: POST
- content-type: application/json
- body
  - source_lang: language code
  - target_lang: language code
  - text_list: array of translated text strings

## Responsive

- response
  - translations: array
    - detected_source_lang: language code
    - text: translated text

## Reserved Placeholder

The purpose is to placeholder the non-text content in the translation of the web page and keep the special symbol after translation, we will restore the corresponding non-text content after the translation is completed.

### Specification

string array

- 0: Left of pairwise separator
- 1: Right side of pairwise separators
- 2: Tag Separator

#### (for) instance

- Example 1: ['{', '}']

```
            Original: 😁 Hallo 👏🏻 Welt
Placeholder Original: {0} Hallo {1} Welt

Placeholder Translation: {0} hello {1} world
            Translation: 😁 hello 👏🏻 wrold
```

- Example 2: ['', '', 'b']

```
            Original: 😁 Hallo 👏🏻 Welt
Placeholder Original: <b0></b0> Hallo <b1></b1> Welt

Placeholder Translation: <b0></b0> hello <b1></b1> world
            Translation: 😁 hello 👏🏻 wrold
```

## Language Code

```bash
auto: Detect Language
af: Afrikaans
am: Amharic
ar: Arabic
az: Azerbaijani
be: Belarusian
bg: Bulgarian
tn: Zana
bn: Bengali
bs: Bosnian
ca: Catalan
ceb: Cebuano
co: Corsican
cs: Czech
cy: Welsh
da: Danish
de: German
el: Greek
en: English
eo: Esperanto
es: Spanish
et: Estonian
eu: Basque
fa: Farsi
fi: Finnish
fil: Filipino
fj: Fijian
fr: French
fy: Frisian
ga: Irish
gd: Scottish Gaelic
gl: Galician
gu: Gujarati
ha: Hausa
haw: Hawaiian
he: Hebrew
hi: Hindi
hmn: Hmong
hr: Croatian
ht: Haitian Creole
hu: Hungarian
hy: Armenian
id: Indonesian
ig: Igbo
is: Icelandic
it: Italian
ja: 日本語
jw: Javanese
ka: Georgian
kk: Kazakh
km: Khmer
kn: Kannada
ko: Korean
ku: Kurdish
ky: Kyrgyz
la: Latin
lb: Luxembourgish
lo: Lao
lt: Lithuanian
lv: Latvian
mg: Malagash
mi: Maori
mk: Macedonian
ml: Malayalam
mn: Mongolian
mr: Marathi
ms: Malay
mt: Maltese
mww: Bai Miao
my: Burmese
ne: Nepali
nl: Dutch
no: Norwegian
ny: Nyanz(Chichewa)
otq: Querétaro Otomi
pa: Punjabi
pl: Polish
ps: Afghan/Pashto
pt: Portuguese(Portugal,Brazil)
ro: Romanian
ru: Russian
sd: Sindhi
si: Sinhala
sk: Slovak
sl: Slovenian
sm: Samoan
sn: Shona
so: Somali
sq: Albanian
sr: Serbian
sr-Cyrl: Serbia(Cyrillic)
sr-Latn: Serbia(Latin)
st: Sesotho
su: Sundanese
sv: Swedish
sw: Swahili
ta: Tamil
te: Telugu
tg: Tajik
th: Thai
tlh: Klingon
tlh-Qaak: Klingo(piqaD)
to: Tongan
tr: Turkish
ty: Tahiti
ug: Uyghur
uk: Ukrainian
ur: Urdu
uz: Uzbek
vi: Vietnamese
wyw: Classical Chinese
xh: Bantu
yi: Yiddish
yo: Yoruba
yua: Yucatan Mayan
yue: Cantones(Traditional)
zh-CN: Chinese(Simplified)
zh-TW: Chinese(Traditional)
zu: Zulu
```
