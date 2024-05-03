# Benutzerdefinierte Schnittstellenübersetzung

## ImmersiveL

[Immersive Übersetzungsmodell](https://github.com/immersive-translate/ImmersiveL) unterstützt benutzerdefinierte Schnittstellen

Aktivieren Sie **Beta-Testfunktionen aktivieren** in `Optionen > Entwicklereinstellungen`.
![](https://s.immersivetranslate.com/assets/turn_on_beta_en.jpeg)

Wählen Sie dann **Benutzerdefinierte API** in `Optionen > Allgemein`, um die Konfigurationsseite zu öffnen.
![](https://s.immersivetranslate.com/assets/select_custon_api_en.jpeg)

## Anfragen

- Methode: POST
- Inhalts-Typ: application/json
- Körper
  - source_lang: Sprachcode
  - target_lang: Sprachcode
  - text_list: Array von übersetzten Textstrings

## Antwort

- Antwort
  - Übersetzungen: Array
    - detected_source_lang: Sprachcode
    - text: übersetzter Text

## Reservierter Platzhalter

Der Zweck ist, den Nicht-Text-Inhalt in der Übersetzung der Webseite zu platzieren und das spezielle Symbol nach der Übersetzung zu behalten, wir werden den entsprechenden Nicht-Text-Inhalt nach der Übersetzung wiederherstellen.

### Spezifikation

String-Array

- 0: Links vom paarweisen Trennzeichen
- 1: Rechte Seite der paarweisen Trennzeichen
- 2: Tag-Trennzeichen

#### (zum) Beispiel

- Beispiel 1: ['{', '}']

```
            Original: 😁 Hallo 👏🏻 Welt
Platzhalter Original: {0} Hallo {1} Welt

Platzhalter Übersetzung: {0} hallo {1} welt
            Übersetzung: 😁 hallo 👏🏻 welt
```

- Beispiel 2: ['', '', 'b']

```
            Original: 😁 Hallo 👏🏻 Welt
Platzhalter Original: <b0></b0> Hallo <b1></b1> Welt

Platzhalter Übersetzung: <b0></b0> hallo <b1></b1> welt
            Übersetzung: 😁 hallo 👏🏻 welt
```

Note: The word "wrold" in your original translation seems to be a typo for "world". I've corrected it to "welt" in the German translation.

## Sprachcode

```bash
auto: Sprache erkennen
af: Afrikaans
am: Amharisch
ar: Arabisch
az: Aserbaidschanisch
be: Weißrussisch
bg: Bulgarisch
tn: Zana
bn: Bengalisch
bs: Bosnisch
ca: Katalanisch
ceb: Cebuano
co: Korsisch
cs: Tschechisch
cy: Walisisch
da: Dänisch
de: Deutsch
el: Griechisch
en: Englisch
eo: Esperanto
es: Spanisch
et: Estnisch
eu: Baskisch
fa: Persisch
fi: Finnisch
fil: Filipino
fj: Fidschianisch
fr: Französisch
fy: Friesisch
ga: Irisch
gd: Schottisches Gälisch
gl: Galizisch
gu: Gujarati
ha: Haussa
haw: Hawaiianisch
he: Hebräisch
hi: Hindi
hmn: Hmong
hr: Kroatisch
ht: Haitianisches Kreolisch
hu: Ungarisch
hy: Armenisch
id: Indonesisch
ig: Igbo
is: Isländisch
it: Italienisch
ja: Japanisch
jw: Javanisch
ka: Georgisch
kk: Kasachisch
km: Khmer
kn: Kannada
ko: Koreanisch
ku: Kurdisch
ky: Kirgisisch
la: Latein
lb: Luxemburgisch
lo: Laotisch
lt: Litauisch
lv: Lettisch
mg: Madagassisch
mi: Maori
mk: Mazedonisch
ml: Malayalam
mn: Mongolisch
mr: Marathi
ms: Malaysisch
mt: Maltesisch
mww: Bai Miao
my: Birmanisch
ne: Nepalesisch
nl: Niederländisch
no: Norwegisch
ny: Nyanz (Chichewa)
otq: Querétaro Otomi
pa: Punjabi
pl: Polnisch
ps: Paschtu
pt: Portugiesisch (Portugal, Brasilien)
ro: Rumänisch
ru: Russisch
sd: Sindhi
si: Singhalesisch
sk: Slowakisch
sl: Slowenisch
sm: Samoanisch
sn: Shona
so: Somali
sq: Albanisch
sr: Serbisch
sr-Cyrl: Serbien (Kyrillisch)
sr-Latn: Serbien (Latein)
st: Sesotho
su: Sundanesisch
sv: Schwedisch
sw: Swahili
ta: Tamilisch
te: Telugu
tg: Tadschikisch
th: Thailändisch
tlh: Klingonisch
tlh-Qaak: Klingo (piqaD)
to: Tongaisch
tr: Türkisch
ty: Tahitisch
ug: Uigurisch
uk: Ukrainisch
ur: Urdu
uz: Usbekisch
vi: Vietnamesisch
wyw: Klassisches Chinesisch
xh: Bantu
yi: Jiddisch
yo: Yoruba
yua: Yucatan Maya
yue: Kantonesisch (Traditionell)
zh-CN: Chinesisch (Vereinfacht)
zh-TW: Chinesisch (Traditionell)
zu: Zulu
```