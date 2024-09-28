# Traduzione dell'Interfaccia Personalizzata

## ImmersiveL

[Modello di Traduzione Immersiva](https://github.com/immersive-translate/ImmersiveL) supporta interfacce personalizzate

Attiva **Abilita Funzionalità di Test Beta** in `Opzioni > Impostazioni sviluppatore`.
![](https://s.immersivetranslate.com/assets/turn_on_beta_en.jpeg)

Quindi seleziona **API Personalizzata** in `Opzioni > Generale` per aprire la pagina di configurazione.
![](https://s.immersivetranslate.com/assets/select_custon_api_en.jpeg)

## Richiesta

- metodo: POST
- content-type: application/json
- corpo
  - source_lang: codice lingua
  - target_lang: codice lingua
  - text_list: array di stringhe di testo tradotte

## Risposta

- risposta
  - translations: array
    - detected_source_lang: codice lingua
    - text: testo tradotto

## Segnaposto Riservato

Lo scopo è di segnaposto il contenuto non testuale nella traduzione della pagina web e mantenere il simbolo speciale dopo la traduzione, ripristineremo il corrispondente contenuto non testuale dopo che la traduzione è completata.

### Specifica

array di stringhe

- 0: Lato sinistro del separatore di coppia
- 1: Lato destro dei separatori di coppia
- 2: Separatore di Tag

#### (per) esempio

- Esempio 1: ['{', '}']

```
            Originale: 😁 Hallo 👏🏻 Welt
Placeholder Originale: {0} Hallo {1} Welt

Traduzione Placeholder: {0} ciao {1} mondo
            Traduzione: 😁 ciao 👏🏻 mondo
```

- Esempio 2: ['', '', 'b']

```
            Originale: 😁 Hallo 👏🏻 Welt
Placeholder Originale: <b0></b0> Hallo <b1></b1> Welt

Traduzione Placeholder: <b0></b0> ciao <b1></b1> mondo
            Traduzione: 😁 ciao 👏🏻 mondo
```

## Codice Lingua

```bash
auto: Rileva Lingua
af: Afrikaans
am: Amarico
ar: Arabo
az: Azero
be: Bielorusso
bg: Bulgaro
tn: Zana
bn: Bengalese
bs: Bosniaco
ca: Catalano
ceb: Cebuano
co: Corso
cs: Ceco
cy: Gallese
da: Danese
de: Tedesco
el: Greco
en: Inglese
eo: Esperanto
es: Spagnolo
et: Estone
eu: Basco
fa: Persiano
fi: Finlandese
fil: Filippino
fj: Figiano
fr: Francese
fy: Frisone
ga: Irlandese
gd: Gaelico Scozzese
gl: Galiziano
gu: Gujarati
ha: Hausa
haw: Hawaiano
he: Ebraico
hi: Hindi
hmn: Hmong
hr: Croato
ht: Creolo Haitiano
hu: Ungherese
hy: Armeno
id: Indonesiano
ig: Igbo
is: Islandese
it: Italiano
ja: Giapponese
jw: Giavanese
ka: Georgiano
kk: Kazako
km: Khmer
kn: Kannada
ko: Coreano
ku: Curdo
ky: Kirghiso
la: Latino
lb: Lussemburghese
lo: Lao
lt: Lituano
lv: Lettone
mg: Malgascio
mi: Maori
mk: Macedone
ml: Malayalam
mn: Mongolo
mr: Marathi
ms: Malese
mt: Maltese
mww: Bai Miao
my: Birmano
ne: Nepalese
nl: Olandese
no: Norvegese
ny: Nyanz(Chichewa)
otq: Otomi di Querétaro
pa: Punjabi
pl: Polacco
ps: Pashto
pt: Portoghese (Portogallo, Brasile)
ro: Rumeno
ru: Russo
sd: Sindhi
si: Singalese
sk: Slovacco
sl: Sloveno
sm: Samoano
sn: Shona
so: Somalo
sq: Albanese
sr: Serbo
sr-Cyrl: Serbia (Cirillico)
sr-Latn: Serbia (Latino)
st: Sesotho
su: Sundanese
sv: Svedese
sw: Swahili
ta: Tamil
te: Telugu
tg: Tagico
th: Tailandese
tlh: Klingon
tlh-Qaak: Klingo(piqaD)
to: Tongano
tr: Turco
ty: Tahitiano
ug: Uiguro
uk: Ucraino
ur: Urdu
uz: Uzbeco
vi: Vietnamita
wyw: Cinese Classico
xh: Bantu
yi: Yiddish
yo: Yoruba
yua: Maya dello Yucatan
yue: Cantonese (Tradizionale)
zh-CN: Cinese (Semplificato)
zh-TW: Cinese (Tradizionale)
zu: Zulu
```
