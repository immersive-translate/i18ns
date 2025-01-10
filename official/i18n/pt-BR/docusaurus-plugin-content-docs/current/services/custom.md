# Guia de Implementação da Interface de Tradução Personalizada ImmersiveL

Este guia detalha como implementar a Interface de Tradução Personalizada [ImmersiveL](https://github.com/immersive-translate/ImmersiveL) ao plugin Immersive Translate, permitindo que você utilize seu próprio modelo de tradução para personalizar a experiência de tradução.

## Ativação da Funcionalidade

1. **Configurações do Desenvolvedor:**

   - Acesse as configurações do Immersive Translate em `Opções > Configurações do desenvolvedor`.
   - Ative a opção "Ativar Funcionalidades Experimentais".
     ![](https://s.immersivetranslate.com/assets/turn_on_beta_en.jpeg)

2. **Seleção da API Personalizada:**
   - Em `Opções > Geral`, selecione "API Personalizada" para abrir a página de configuração.
     ![](https://s.immersivetranslate.com/assets/select_custon_api_en.jpeg)

## Especificação da Requisição

- **Método:** POST
- **Content-Type:** application/json
- **Corpo:**
  - `source_lang`: código do idioma de origem (ex: "en").
  - `target_lang`: código do idioma de destino (ex: "pt").
  - `text_list`: array de strings contendo os textos a serem traduzidos.

## Especificação da Resposta

- **Resposta:**
  - `translations`: array contendo os textos traduzidos.
    - `detected_source_lang`: código do idioma de origem detectado (opcional).
    - `text`: texto traduzido.

## Placeholders Reservados

Placeholders são utilizados para preservar conteúdo não textual (emojis, formatação, etc.) durante a tradução.

- **Especificação:** array de strings.

  - 0: Delimitador esquerdo do par (ex: "\{").
  - 1: Delimitador direito do par (ex: "\}").
  - 2: Separador de tag (opcional, ex: "b").

- **Exemplos:**
  1. `['{', '}']`: Preserva emojis e formatação simples.
  - Original: 😁 Hallo 👏🏻 Welt
  - Traduzido: 😁 Olá 👏🏻 Mundo

```
            Original: 😁 Hallo 👏🏻 Welt
Placeholder Original: {0} Hallo {1} Welt

Placeholder Translation: {0} hello {1} world
            Translation: 😁 hello 👏🏻 world
```

2. `['', '', 'b']`: Preserva tags HTML como `<b>`.

   - Original: 😁 **Hallo** 👏🏻 Welt
   - Traduzido: 😁 **Olá** 👏🏻 Mundo

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
ps: Afghan/Pashto
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
