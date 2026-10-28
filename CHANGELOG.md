# 📝 Journal des modifications

Studio : ORIKAMI.

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
