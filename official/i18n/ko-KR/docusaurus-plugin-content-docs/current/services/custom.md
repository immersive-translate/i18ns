# 사용자 정의 인터페이스 번역

## ImmersiveL

[몰입형 번역 모델](https://github.com/immersive-translate/ImmersiveL)은 사용자 정의 인터페이스를 지원합니다.

【설정】페이지에서 개발자 모드를 활성화하고【Beta】기능을 사용하면 번역 서비스에서 다음을 볼 수 있습니다:

![](https://s.immersivetranslate.com/assets/20231026-125902.jpeg)

## 요청

- method: POST
- content-type: application/json
- body
  - source_lang: 소스 \{언어 코드\}
  - target_lang: 대상 \{언어 코드\}
  - text_list: 번역할 텍스트 문자열 배열

## 응답

- response
  - translations: 배열
    - detected_source_lang: 감지된 소스 텍스트 \{언어 코드\}
    - text: 번역된 텍스트

## 플레이스홀더 유지

목적은 웹 페이지 번역 중 텍스트가 아닌 내용에 대해 플레이스홀더를 사용하여 번역 후에도 이러한 특수 기호를 유지하고, 번역이 완료된 후 해당 비텍스트 내용을 복원하는 것입니다.

### 형식

문자열 배열

- 0: 짝을 이루는 구분 기호의 왼쪽
- 1: 짝을 이루는 구분 기호의 오른쪽
- 2: 태그 구분 기호

#### 예시

- 예시 1: ['{', '}']

```
   원문: 😁 hello 👏🏻 world
플레이스홀더 원문: {0} hello {1} world

플레이스홀더 번역문: {0} 안녕하세요 {1} 세계
   번역문: 😁 안녕하세요 👏🏻 세계
```

- 예시 2: ['', '', 'b']

````
   원문: 😁 hello 👏🏻 world
플레이스홀더 원문: <b0></b0> hello <b1></b1> world

플레이스홀더 번역문: <b0></b0> 안녕하세요 <b1></b1> 세계
   번역문: 😁 안녕하세요 👏🏻 세계

## 언어 코드

```bash
auto: 자동 언어 감지, Detect Language
af: 아프리칸스어, Afrikaans
am: 암하라어, Amharic
ar: 아랍어, Arabic
az: 아제르바이잔어, Azerbaijani
be: 벨라루스어, Belarusian
bg: 불가리아어, Bulgarian
tn: 제나어, Zana
bn: 벵골어, Bengali
bs: 보스니아어, Bosnian
ca: 카탈로니아어, Catalan
ceb: 세부아노어, Cebuano
co: 코르시카어, Corsican
cs: 체코어, Czech
cy: 웨일스어, Welsh
da: 덴마크어, Danish
de: 독일어, German
el: 그리스어, Greek
en: 영어, English
eo: 에스페란토어, Esperanto
es: 스페인어, Spanish
et: 에스토니아어, Estonian
eu: 바스크어, Basque
fa: 페르시아어, Farsi
fi: 핀란드어, Finnish
fil: 필리핀어, Filipino
fj: 피지어, Fijian
fr: 프랑스어, French
fy: 프리지아어, Frisian
ga: 아일랜드어, Irish
gd: 스코틀랜드 게일어, Scottish Gaelic
gl: 갈리시아어, Galician
gu: 구자라트어, Gujarati
ha: 하우사어, Hausa
haw: 하와이어, Hawaiian
he: 히브리어, Hebrew
hi: 힌디어, Hindi
hmn: 몽어, Hmong
hr: 크로아티아어, Croatian
ht: 아이티 크리올어, Haitian Creole
hu: 헝가리어, Hungarian
hy: 아르메니아어, Armenian
id: 인도네시아어, Indonesian
ig: 이그보어, Igbo
is: 아이슬란드어, Icelandic
it: 이탈리아어, Italian
ja: 일본어, 日本語
jw: 자바어, Javanese
ka: 조지아어, Georgian
kk: 카자흐어, Kazakh
km: 크메르어, Khmer
kn: 칸나다어, Kannada
ko: 한국어, Korean
ku: 쿠르드어, Kurdish
ky: 키르기스어, Kyrgyz
la: 라틴어, Latin
lb: 룩셈부르크어, Luxembourgish
lo: 라오어, Lao
lt: 리투아니아어, Lithuanian
lv: 라트비아어, Latvian
mg: 마다가스카르어, Malagash
mi: 마오리어, Maori
mk: 마케도니아어, Macedonian
ml: 말라얄람어, Malayalam
mn: 몽골어, Mongolian
mr: 마라티어, Marathi
ms: 말레이어, Malay
mt: 몰타어, Maltese
mww: 백모어, Bai Miao
my: 버마어, Burmese
ne: 네팔어, Nepali
nl: 네덜란드어, Dutch
no: 노르웨이어, Norwegian
ny: 치체와어, Nyanz(Chichewa)
otq: 케레타로 오토미어, Querétaro Otomi
pa: 펀자브어, Punjabi
pl: 폴란드어, Polish
ps: 파슈토어, Afghan/Pashto
pt: 포르투갈어 (Portugal,Brazil)
ro: 루마니아어, Romanian
ru: 러시아어, Russian
sd: 신디어, Sindhi
si: 싱할라어, Sinhala
sk: 슬로바키아어, Slovak
sl: 슬로베니아어, Slovenian
sm: 사모아어, Samoan
sn: 쇼나어, Shona
so: 소말리아어, Somali
sq: 알바니아어, Albanian
sr: 세르비아어, Serbian
sr-Cyrl: 세르비아어 (키릴 문자), Serbia(Cyrillic)
sr-Latn: 세르비아어 (라틴 문자), Serbia(Latin)
st: 세소토어, Sesotho
su: 순다어, Sundanese
sv: 스웨덴어, Swedish
sw: 스와힐리어, Swahili
ta: 타밀어, Tamil
te: 텔루구어, Telugu
tg: 타지크어, Tajik
th: 태국어, Thai
tlh: 클링곤어, Klingon
tlh-Qaak: 클링곤어 (piqaD), Klingo(piqaD)
to: 통가어, Tongan
tr: 터키어, Turkish
ty: 타히티어, Tahiti
ug: 위구르어, Uyghur
uk: 우크라이나어, Ukrainian
ur: 우르두어, Urdu
uz: 우즈베크어, Uzbek
vi: 베트남어, Vietnamese
wyw: 문언문, 文言文
xh: 반투어, Bantu
yi: 이디시어, Yiddish
yo: 요루바어, Yoruba
yua: 유카탄 마야어, Yucatan Mayan
yue: 광동어 (전통), Cantones(Traditional)
zh-CN: 간체 중국어, 简体中文
zh-TW: 번체 중국어, 繁體中文
zu: 줄루어, Zulu
````
