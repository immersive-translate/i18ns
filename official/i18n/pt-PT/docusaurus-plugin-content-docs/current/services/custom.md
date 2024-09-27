# Tradução de Interface Personalizada

## ImmersiveL

[Modelo de Tradução Imersiva](https://github.com/immersive-translate/ImmersiveL) tem suporte para interfaces personalizadas

Ative **Habilitar Recursos de Teste Beta** em `Opções > Configurações do Desenvolvedor`.
![](https://s.immersivetranslate.com/assets/turn_on_beta_en.jpeg)

Em seguida, selecione **API Personalizada** em `Opções > Geral` para abrir a página de configuração.
![](https://s.immersivetranslate.com/assets/select_custon_api_en.jpeg)

## Solicitando

- método: POST
- tipo de conteúdo: application/json
- corpo
  - source_lang: código do idioma
  - target_lang: código do idioma
  - text_list: array de strings de texto traduzidas

## Responsivo

- resposta
  - translations: array
    - detected_source_lang: código do idioma
    - text: texto traduzido

## Placeholder Reservado

O propósito é reservar o conteúdo não-textual na tradução da página web e manter o símbolo especial após a tradução, nós restauraremos o conteúdo não-textual correspondente após a tradução ser completada.

### Especificação

array de strings

- 0: Esquerda do separador par
- 1: Lado direito dos separadores pares
- 2: Separador de Tag

#### (por) exemplo

- Exemplo 1: ['{', '}']

```
            Original: 😁 Hallo 👏🏻 Welt
Placeholder Original: {0} Hallo {1} Welt

Tradução com Placeholder: {0} olá {1} mundo
            Tradução: 😁 olá 👏🏻 mundo
```

- Exemplo 2: ['', '', 'b']

```
            Original: 😁 Hallo 👏🏻 Welt
Placeholder Original: <b0></b0> Hallo <b1></b1> Welt

Tradução com Placeholder: <b0></b0> olá <b1></b1> mundo
            Tradução: 😁 olá 👏🏻 mundo
```

Note: There was a typo in the original English content ("wrold" instead of "world"). I've corrected it in the Portuguese translation.

## Código de Idioma

```bash
auto: Detectar Idioma
af: Africâner
am: Amárico
ar: Árabe
az: Azerbaijano
be: Bielorrusso
bg: Búlgaro
tn: Zana
bn: Bengali
bs: Bósnio
ca: Catalão
ceb: Cebuano
co: Córsico
cs: Tcheco
cy: Galês
da: Dinamarquês
de: Alemão
el: Grego
en: Inglês
eo: Esperanto
es: Espanhol
et: Estoniano
eu: Basco
fa: Persa
fi: Finlandês
fil: Filipino
fj: Fijiano
fr: Francês
fy: Frísio
ga: Irlandês
gd: Gaélico Escocês
gl: Galego
gu: Gujarati
ha: Hausa
haw: Havaiano
he: Hebraico
hi: Hindi
hmn: Hmong
hr: Croata
ht: Crioulo Haitiano
hu: Húngaro
hy: Armênio
id: Indonésio
ig: Igbo
is: Islandês
it: Italiano
ja: Japonês
jw: Javanês
ka: Georgiano
kk: Cazaque
km: Khmer
kn: Canarês
ko: Coreano
ku: Curdo
ky: Quirguiz
la: Latim
lb: Luxemburguês
lo: Laociano
lt: Lituano
lv: Letão
mg: Malgaxe
mi: Maori
mk: Macedônio
ml: Malaiala
mn: Mongol
mr: Marata
ms: Malaio
mt: Maltês
mww: Bai Miao
my: Birmanês
ne: Nepalês
nl: Holandês
no: Norueguês
ny: Nianja (Chichewa)
otq: Otomi de Querétaro
pa: Punjabi
pl: Polonês
ps: Pashto
pt: Português (Portugal, Brasil)
ro: Romeno
ru: Russo
sd: Sindhi
si: Cingalês
sk: Eslovaco
sl: Esloveno
sm: Samoano
sn: Xona
so: Somali
sq: Albanês
sr: Sérvio
sr-Cyrl: Sérvia (Cirílico)
sr-Latn: Sérvia (Latim)
st: Sesoto
su: Sundanês
sv: Sueco
sw: Suaíli
ta: Tâmil
te: Telugu
tg: Tadjique
th: Tailandês
tlh: Klingon
tlh-Qaak: Klingon (piqaD)
to: Tonganês
tr: Turco
ty: Taitiano
ug: Uigur
uk: Ucraniano
ur: Urdu
uz: Uzbeque
vi: Vietnamita
wyw: Chinês Clássico
xh: Banto
yi: Iídiche
yo: Iorubá
yua: Maia de Yucatan
yue: Cantonês (Tradicional)
zh-CN: Chinês (Simplificado)
zh-TW: Chinês (Tradicional)
zu: Zulu
```
