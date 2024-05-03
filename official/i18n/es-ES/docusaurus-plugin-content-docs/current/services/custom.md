# Traducción de Interfaz Personalizada

## ImmersiveL

[Modelo de Immersive Translate](https://github.com/immersive-translate/ImmersiveL) tiene soporte para interfaces personalizadas

Activa **Habilitar Características de Pruebas Beta** en `Opciones > Configuración de desarrollador`.
![](https://s.immersivetranslate.com/assets/turn_on_beta_en.jpeg)

Luego selecciona **API Personalizada** en `Opciones > General` para abrir la página de configuración.
![](https://s.immersivetranslate.com/assets/select_custon_api_en.jpeg)

## Solicitando

- método: POST
- tipo de contenido: application/json
- cuerpo
  - source_lang: código de idioma
  - target_lang: código de idioma
  - text_list: arreglo de cadenas de texto traducidas

## Responsivo

- respuesta
  - translations: arreglo
    - detected_source_lang: código de idioma
    - text: texto traducido

## Marcador de Posición Reservado

El propósito es reservar el contenido no textual en la traducción de la página web y mantener el símbolo especial después de la traducción, restauraremos el contenido no textual correspondiente después de que la traducción esté completa.

### Especificación

arreglo de cadenas

- 0: Izquierda del separador por pares
- 1: Derecha de los separadores por pares
- 2: Separador de Etiquetas

#### (por) ejemplo

- Ejemplo 1: ['{', '}']

```
            Original: 😁 Hallo 👏🏻 Welt
Placeholder Original: {0} Hola {1} Mundo

Placeholder Translation: {0} hola {1} mundo
            Translation: 😁 hola 👏🏻 mundo
```

- Ejemplo 2: ['', '', 'b']

```
            Original: 😁 Hallo 👏🏻 Welt
Placeholder Original: <b0></b0> Hola <b1></b1> Mundo

Placeholder Translation: <b0></b0> hola <b1></b1> mundo
            Translation: 😁 hola 👏🏻 mundo
```

Note: There was a typo in the original English content ("wrold" instead of "world"). I've corrected this in the translation.

## Código de Idioma

```bash
auto: Detectar Idioma
af: Afrikáans
am: Amárico
ar: Árabe
az: Azerbaiyano
be: Bielorruso
bg: Búlgaro
tn: Zana
bn: Bengalí
bs: Bosnio
ca: Catalán
ceb: Cebuano
co: Corso
cs: Checo
cy: Galés
da: Danés
de: Alemán
el: Griego
en: Inglés
eo: Esperanto
es: Español
et: Estonio
eu: Vasco
fa: Persa
fi: Finés
fil: Filipino
fj: Fiyiano
fr: Francés
fy: Frisón
ga: Irlandés
gd: Gaélico Escocés
gl: Gallego
gu: Guyaratí
ha: Hausa
haw: Hawaiano
he: Hebreo
hi: Hindi
hmn: Hmong
hr: Croata
ht: Criollo Haitiano
hu: Húngaro
hy: Armenio
id: Indonesio
ig: Igbo
is: Islandés
it: Italiano
ja: Japonés
jw: Javanés
ka: Georgiano
kk: Kazajo
km: Jemer
kn: Canarés
ko: Coreano
ku: Kurdo
ky: Kirguís
la: Latín
lb: Luxemburgués
lo: Lao
lt: Lituano
lv: Letón
mg: Malgache
mi: Maorí
mk: Macedonio
ml: Malayalam
mn: Mongol
mr: Maratí
ms: Malayo
mt: Maltés
mww: Bai Miao
my: Birmano
ne: Nepalí
nl: Neerlandés
no: Noruego
ny: Nyanz(Chichewa)
otq: Otomí de Querétaro
pa: Panyabí
pl: Polaco
ps: Pastún
pt: Portugués(Portugal, Brasil)
ro: Rumano
ru: Ruso
sd: Sindhi
si: Cingalés
sk: Eslovaco
sl: Esloveno
sm: Samoano
sn: Shona
so: Somalí
sq: Albanés
sr: Serbio
sr-Cyrl: Serbia(Cirílico)
sr-Latn: Serbia(Latino)
st: Sesotho
su: Sondanés
sv: Sueco
sw: Suajili
ta: Tamil
te: Telugu
tg: Tayiko
th: Tailandés
tlh: Klingon
tlh-Qaak: Klingo(piqaD)
to: Tongano
tr: Turco
ty: Tahitiano
ug: Uigur
uk: Ucraniano
ur: Urdu
uz: Uzbeko
vi: Vietnamita
wyw: Chino Clásico
xh: Bantú
yi: Yidis
yo: Yoruba
yua: Maya Yucateco
yue: Cantones(Tradicional)
zh-CN: Chino(Simplificado)
zh-TW: Chino(Tradicional)
zu: Zulú
```