# Tradução de Interface Personalizada

## ImmersiveL

O [Modelo Immersive Translate](https://github.com/immersive-translate/ImmersiveL) possui suporte para interfaces personalizadas.

Ative **Habilitar Recursos de Teste Beta** em `Opções > Configurações do desenvolvedor`.
![](https://s.immersivetranslate.com/assets/turn_on_beta_en.jpeg)

Em seguida, selecione **API Personalizada** em `Opções > Geral` para abrir a página de configuração.
![](https://s.immersivetranslate.com/assets/select_custon_api_en.jpeg)

## Requisição

- método: POST
- content-type: application/json
- body
 - source_lang: código do idioma
 - target_lang: código do idioma
 - text_list: array de strings de texto traduzidas

## Resposta

- response
 - translations: array
  - detected_source_lang: código do idioma
  - text: texto traduzido

## Placeholder Reservado

O objetivo é reservar o conteúdo que não é texto na tradução da página da web e manter o símbolo especial após a tradução. Restauraremos o conteúdo que não é texto correspondente após a conclusão da tradução.

### Especificação

array de strings

- 0: Lado esquerdo do separador de pares
- 1: Lado direito do separador de pares
- 2: Separador de Tag

#### Exemplo

- Exemplo 1: ['{', '}']

```
            Original: 😁 Hallo 👏🏻 Welt
Placeholder Original: {0} Hallo {1} Welt

Placeholder Translation: {0} hello {1} world
            Translation: 😁 hello 👏🏻 world
```

- Exemplo 2: ['', '', 'b']

```
            Original: 😁 Hallo 👏🏻 Welt
Placeholder Original: <b0></b0> Hallo <b1></b1> Welt

Placeholder Translation: <b0></b0> hello <b1></b1> world
            Translation: 😁 hello 👏🏻 world
```

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
co: Corso
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
ha: Hauçá
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
lo: Laosiano
lt: Lituano
lv: Letão
mg: Malgaxe
mi: Maori
mk: Macedônio
ml: Malaiala
mn: Mongol
mr: Marati
ms: Malaio
mt: Maltês
mww: Bai Miao
my: Birmanês
ne: Nepalês
nl: Holandês
no: Norueguês
ny: Nyanja (Chichewa)
otq: Otomi de Querétaro
pa: Punjabi
pl: Polonês
ps: Pashto
pt: Português (Portugal, Brasil)
ro: Romeno
ru: Russo
sd: Sindi
si: Cingalês
sk: Eslovaco
sl: Esloveno
sm: Samoano
sn: Shona
so: Somali
sq: Albanês
sr: Sérvio
sr-Cyrl: Sérvio (Cirílico)
sr-Latn: Sérvio (Latim)
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
xh: Bantu
yi: Iídiche
yo: Iorubá
yua: Maia Iucateco
yue: Cantonês (Tradicional)
zh-CN: Chinês (Simplificado)
zh-TW: Chinês (Tradicional)
zu: Zulu
```