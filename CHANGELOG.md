# 📝 Journal des modifications

Studio : ORIKAMI.

## 0.77 ⭐

- Cases du plateau : les dessins indirects (enregistrements écrits par le GPU) sont maintenant exécutés.

## 0.76

- Passages à fond noir aux changements de scène corrigés : courte saccade à la place, le temps que les shaders se compilent.

## 0.75

- Plantage au lancement d'un mini-jeu corrigé (fonctions de base manquantes : atof, qsort, bsearch).

## 0.74 ⭐

- Personnages aplatis corrigés (lecture des matrices d'os).
- Fin d'une fausse vérification « format de sommet inconnu ».

## 0.73

- LOG enrichi (attributs et flux de sommets de chaque dessin).

## 0.72

- Mémoire partagée avec le GPU : un mot réécrit par le jeu n'est plus écrasé par une ancienne relecture.
- LOG enrichi.

## 0.71

- Plus de plantage quand l'appli passe en arrière-plan.
- LOG enrichi.

## 0.70 ⭐

- Personnages, PNJ et Bowser en couleur (cache de shaders complété ; l'ancien cache est remplacé automatiquement).

## 0.69

- Gel au chargement du plateau corrigé : le rendu n'attend plus les shaders préparés.
- Dernier shader non traduit corrigé (LEA).

## 0.68

- Blocage au lancement d'une partie corrigé.
- Instruction ATOM des shaders de skinning ; rapport de blocage plus complet.

## 0.67

- Couleurs corrigées sur la place, la carte de l'île et le choix du mode (tables de couleurs 3D).

## 0.66

- Écran blanc au chargement d'une sauvegarde corrigé (compilation en arrière-plan).
- Instruction VOTE traduite ; rapport de blocage dans le journal.

## 0.65

- Personnages enfin calculés (vertex shaders de calcul exécutés dans une passe dédiée).
- Zones mémoire partagées qui se chevauchent fusionnées.

## 0.64 ⭐

- Personnages animés par la carte graphique enfin dessinés (transform feedback).
- Image de débogage complète dans le journal.

## 0.63

- Personnages et objets animés par le GPU dessinés avec leurs vrais sommets (ils étaient étirés en triangles ou absents).

## 0.62

- Jusqu'à 64 textures par shader (personnages et rendu système).
- Attributs indexés traduits.
- Journal : nouvelles vérifications et ligne de statistiques des sommets toutes les 30 s.

## 0.61

- Personnages aplatis ou clignotants : listes de dessin stockées hors de la mémoire du jeu.
- Dessins des programmes du cache à nouveau affichés (absents depuis la 0.58).
- Fausses couleurs : entrées interpolées correctement à l'écran.
- Rapport des capacités graphiques au démarrage ; cache de pipelines protégé quand le stockage est plein.

## 0.59

Le pilote graphique s'affiche en jeu.

- L'ATH affiche sur une deuxième ligne le pilote graphique utilisé et sa version (pilote système ou Turnip installé, version Vulkan).

## 0.58

Des vérifications dans les journaux et un plantage de moins.

- Le journal contient maintenant des lignes `[vérif]` (anomalies du rendu) et une ligne `[santé]` toutes les 30 secondes (mémoire, threads, file du rendu).
- Le rapport de plantage est plus complet (tous les registres, contexte du rendu, pile élargie).
- Plantage sur une texture sans mémoire après plusieurs changements de plateau corrigé.

## 0.57

Fin d'un plantage au chargement des plateaux.

- Plantage au chargement d'un plateau (après la Chance Time) corrigé : les copies de programmes graphiques ne sont plus réécrites au-delà de 2048.
- Le mail de plantage ne s'ouvre plus par-dessus le jeu au lancement : le bouton LOG l'ouvre, l'appui suivant redonne le journal.

## 0.56

Correctif du sol, des personnages et des textes, plus un mini-jeu qui ne plante plus.

- Les shaders ne demandent l'extension GLSL `shadow_lod` que si elle sert (le sol, les personnages et les textes avaient disparu).
- Mini-jeu mg0107 : 19 fonctions de la libc++ des modules ajoutées, fin du plantage.
- Conversions de texte UTF alignées sur le SDK (noms des joueurs).

## 0.55

Textures des shaders d'éclairage, noms des joueurs et mail après plantage.

- Textures des shaders d'éclairage par lumière (7 771 étages sur 7 802 traduits).
- Noms des joueurs affichés.
- Après un plantage, un mail prêt avec rapport et journal joints.
- Le rapport donne la raison de fin indiquée par Android.

## 0.52 ⭐

Chargements rapides et nouvelle manette tactile.

- Gestion de la mémoire du jeu en O(log n) : chargements de 35 s à 46 ms.
- Nouvelle manette tactile au thème fête, mêmes tailles sur les deux écrans du pliable.
- Bouton x2 pour accélérer le jeu ; compteur d'images par seconde discret avec températures.

## 0.49 ⭐

Les décors 3D apparaissent.

- Les listes de commandes en cache ne s'écrasent plus (0.48).
- Les shaders de sommets du décor écrivent enfin leur position (0.49).

## 0.33 ⭐

Le son arrive.

- Audio : mixage des voix et lecture via AAudio.
- Bouton LOG : journal du runtime sur disque, partageable.
- Plusieurs shaders (calcul, textures bindless) traduits en plus.

## 0.22

Sélection des personnages atteinte.

- Profil utilisateur par défaut pour que le jeu charge sa sauvegarde.
- Lecteur vidéo en échec propre quand aucune vidéo n'est décodée.
- Sous-titres de l'intro retirés de l'écran titre.
- Manette tactile affichée par-dessus le jeu.

## 0.15 ⭐

Écran titre et menu principal.

- Le jeu démarre, passe l'intro et atteint l'écran titre.
- Après un plantage, le rapport du lancement précédent est écrit dans `rapport.txt` et proposé au partage.
- Manettes physiques 1 à 4 reconnues.
