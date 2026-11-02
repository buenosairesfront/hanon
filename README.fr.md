[English](README.md) · [Español](README.es.md) · **Français** · [Deutsch](README.de.md) · [日本語](README.ja.md) · [中文](README.zh.md) · [हिन्दी](README.hi.md)

# U-MA Hanon

Les 60 exercices du *Pianiste virtuose* de Charles-Louis Hanon, dans le navigateur : vous les voyez sur la portée, vous voyez **les deux mains sur le clavier** avec chaque doigt numéroté, vous les écoutez au tempo choisi et, avec un clavier MIDI, l'application vous écoute et analyse votre prise.

**▶ Ouvrir l'application :** https://buenosairesfront.github.io/hanon/

Rien à installer. L'interface est en espagnol.

## Comment ça marche

1. **Choisissez un exercice.** Les 60 exercices sont regroupés selon les trois parties du livre : **I · 1–20** préparatoires (magenta), **II · 21–43** avancés (cyan) et **III · 44–60** virtuosité (jaune). Touchez un numéro sous le clavier, ou le grand numéro en haut pour ouvrir la grille complète 1–60.
2. **Choisissez une variante** quand l'exercice en a : les gammes (39) et les arpèges (41) existent dans les 24 tonalités, dans l'ordre du livre (chaque majeur suivi de son relatif mineur ; mineurs harmonique et mélodique), les gammes chromatiques (40) en 8 intervalles et sens, les notes répétées (45) en 6 doigtés, les tierces ou sixtes piquées (48)…
3. **Lisez la partition.** Deux portées montrent l'exercice : **↑ montée** (cyan) et **↓ descente** (magenta). Sur téléphone, on passe de l'une à l'autre avec des onglets.
4. **Regardez les mains.** Le clavier est le cœur de l'application. Les deux mains sont dessinées sur les touches avec leurs paumes, chaque doigt porte son numéro (1 = pouce … 5 = auriculaire, chacun avec sa couleur) et un contour en pointillés indique **la prochaine position de la main**. Sous le clavier, une ligne par main montre l'ordre des doigts du groupe en cours et allume la note jouée.
5. **Écoutez.**
   - **▶ 2 passes** : une démo courte avec les deux premiers et les deux derniers groupes, pour entendre la forme rapidement.
   - **↑ montée** / **↓ descente** : un seul sens.
   - **↑↓×2** : l'exercice complet, deux fois.
   - **loop** répète jusqu'à **stop**.
6. **Réglez le tempo** de 40 à 160 BPM avec le curseur ou – / +. La bande jaune indique la plage demandée par Hanon (60 → 108) : commencez lentement et montez peu à peu. Le métronome **MET** clignote et sonne dans la mesure de l'exercice (2/4, 3/4, 4/4 ou 6/8), accent en magenta.

## Travailler avec un clavier MIDI

Appuyez sur **MIDI** et autorisez l'accès. Ensuite :

- les touches jouées s'allument en cyan sur le clavier à l'écran ;
- **REC** joue l'exercice comme guide et enregistre ce que vous jouez par-dessus ;
- à la fin apparaît l'**analyse de votre prise** : précision (%), écart moyen (ms), régularité (%) et fausses notes ; un graphique de mise en place (en avance ↓ / en retard ↑ pour chaque note), retard et force par doigt, et dynamique de chaque main (droite en haut, gauche en bas).

Sans MIDI, **nouvelle prise d'exemple** montre à quoi ressemble l'analyse.

## Clair et sombre

Le bouton **clair / sombre** change le thème ; le choix est mémorisé dans ce navigateur.

## Sous le capot

Un seul `index.html` sans dépendances : les exercices ne sont pas stockés note par note, ils sont **générés**. Chacun est une cellule mélodique (en degrés de la gamme) avec son doigté pour chaque main ; le moteur la monte d'un degré par mesure puis la redescend, et écrit chaque note avec la bonne altération (dièses en montant, bémols en descendant pour les chromatiques). Gammes, arpèges et exercices en octaves sont construits dans les 24 tonalités avec les doigtés traditionnels. La partition est dessinée en SVG, le clavier et l'analyse sur `<canvas>`, le son et le métronome avec Web Audio, l'entrée clavier avec Web MIDI.

## Lancer en local

Téléchargez `index.html` et ouvrez-le, ou servez le dossier :

```
python3 -m http.server 8000
```

<!-- u-ma:more -->
**Plus de U-MA :** tous les instruments et outils au même endroit → [vitrine U-MA](https://github.com/buenosairesfront/U-ma/blob/main/README.fr.md)
<!-- /u-ma:more -->

## Crédits

Exercices tirés du *Pianiste virtuose en 60 exercices* de Charles-Louis Hanon (1873, domaine public). Application par U-MA サウンド · [Buenos Aires Front](https://www.instagram.com/buenos.aires.front/).
