# Traduction de l'interface personnalisée

## ImmersiveL

[Modèle de Traduction Immersive](https://github.com/immersive-translate/ImmersiveL) prend en charge les interfaces personnalisées

Activez **Activer les fonctionnalités de test bêta** dans `Options > Paramètres développeur`.
![](https://s.immersivetranslate.com/assets/turn_on_beta_en.jpeg)

Puis sélectionnez **API personnalisée** dans `Options > Général` pour ouvrir la page de configuration.
![](https://s.immersivetranslate.com/assets/select_custon_api_en.jpeg)

## Requête

- méthode : POST
- type de contenu : application/json
- corps
  - source_lang : code de langue
  - target_lang : code de langue
  - text_list : tableau de chaînes de texte traduit

## Réponse

- réponse
  - translations : tableau
    - detected_source_lang : code de langue
    - text : texte traduit

## Placeholder Réservé

Le but est de placer un espace réservé pour le contenu non textuel dans la traduction de la page web et de conserver le symbole spécial après la traduction, nous restaurerons le contenu non textuel correspondant après que la traduction soit terminée.

### Spécification

tableau de chaînes

- 0 : À gauche du séparateur par paire
- 1 : Côté droit des séparateurs par paire
- 2 : Séparateur de balise

#### (par) exemple

- Exemple 1 : ['{', '}']

```
            Original : 😁 Hallo 👏🏻 Welt
Original avec placeholders : {0} Hallo {1} Welt

Traduction avec placeholders : {0} bonjour {1} monde
            Traduction : 😁 bonjour 👏🏻 monde
```

- Exemple 2 : ['', '', 'b']

```
            Original : 😁 Hallo 👏🏻 Welt
Original avec placeholders : <b0></b0> Hallo <b1></b1> Welt

Traduction avec placeholders : <b0></b0> bonjour <b1></b1> monde
            Traduction : 😁 bonjour 👏🏻 monde
```

## Code de langue

```bash
auto : Détecter la langue
af : Afrikaans
am : Amharique
ar : Arabe
az : Azéri
be : Biélorusse
bg : Bulgare
tn : Zana
bn : Bengali
bs : Bosniaque
ca : Catalan
ceb : Cebuano
co : Corse
cs : Tchèque
cy : Gallois
da : Danois
de : Allemand
el : Grec
en : Anglais
eo : Espéranto
es : Espagnol
et : Estonien
eu : Basque
fa : Persan
fi : Finnois
fil : Philippin
fj : Fidjien
fr : Français
fy : Frison
ga : Irlandais
gd : Gaélique écossais
gl : Galicien
gu : Gujarati
ha : Haoussa
haw : Hawaïen
he : Hébreu
hi : Hindi
hmn : Hmong
hr : Croate
ht : Créole haïtien
hu : Hongrois
hy : Arménien
id : Indonésien
ig : Igbo
is : Islandais
it : Italien
ja : Japonais
jw : Javanais
ka : Géorgien
kk : Kazakh
km : Khmer
kn : Kannada
ko : Coréen
ku : Kurde
ky : Kirghize
la : Latin
lb : Luxembourgeois
lo : Laotien
lt : Lituanien
lv : Letton
mg : Malgache
mi : Maori
mk : Macédonien
ml : Malayalam
mn : Mongol
mr : Marathi
ms : Malais
mt : Maltais
mww : Hmong Daw
my : Birman
ne : Népalais
nl : Néerlandais
no : Norvégien
ny : Nyanja (Chichewa)
otq : Otomi de Querétaro
pa : Pendjabi
pl : Polonais
ps : Pachto
pt : Portugais (Portugal, Brésil)
ro : Roumain
ru : Russe
sd : Sindhi
si : Cinghalais
sk : Slovaque
sl : Slovène
sm : Samoan
sn : Shona
so : Somali
sq : Albanais
sr : Serbe
sr-Cyrl : Serbie (Cyrillique)
sr-Latn : Serbie (Latin)
st : Sotho
su : Soundanais
sv : Suédois
sw : Swahili
ta : Tamoul
te : Télougou
tg : Tadjik
th : Thaï
tlh : Klingon
tlh-Qaak : Klingon (piqaD)
to : Tongien
tr : Turc
ty : Tahitien
ug : Ouïghour
uk : Ukrainien
ur : Ourdou
uz : Ouzbek
vi : Vietnamien
wyw : Chinois classique
xh : Bantou
yi : Yiddish
yo : Yorouba
yua : Maya du Yucatan
yue : Cantonais (Traditionnel)
zh-CN : Chinois (Simplifié)
zh-TW : Chinois (Traditionnel)
zu : Zoulou
```