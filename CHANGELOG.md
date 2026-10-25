# 📝 Journal des modifications

Studio : ORIKAMI.

## 0.58

- Vérifications dans les journaux (`[vérif]`, ligne `[santé]` toutes les 30 s, rapport de plantage complet) ; corrige un plantage sur une texture sans mémoire après des changements de plateau (APK 0.58).

## 0.57

- Corrige le plantage au chargement d'un plateau (copies de programmes réécrites au-delà de 2048 : désormais dans des blocs fixes avec une table de hachage) ; le mail de plantage ne s'ouvre plus au lancement, le bouton LOG l'ouvre (APK 0.57).

## 0.56

- Correction du recul de la 0.55 sur le PC de test (extension GLSL shadow_lod demandée seulement si utile : sol, personnages et textes revenus) ; plantage du mini-jeu mg0107 (19 fonctions libc++ des modules liées) ; conversions UTF calées sur le SDK ; `env.txt` pour les réglages de test (APK 0.56).

## 0.55

- Noms des joueurs (conversions UTF-8/UTF-16 de nn::util) ; après un plantage, mail prêt avec rapport et journal joints, l'adresse restant hors du code (APK 0.55).

## 0.54

- Le rapport du lancement précédent donne la raison de fin indiquée par Android (manque de mémoire, ANR…) ; le journal note les températures affichées (APK 0.54).

## 0.53

- Textures des shaders d'éclairage par lumière (poignées bindless indexées, 7 771 étages sur 7 802 traduits) ; température CPU/GPU de l'affichage = moyenne des capteurs (APK 0.53).

## 0.52

- Nouvelle manette tactile (disposition reprise de BOTWRecompAndroid, thème fête, lettres lisses, mêmes tailles sur les deux écrans du pliable) ; bouton x2 qui accélère le jeu (horloge, attentes et vsync émulée) ; compteur plus discret (APK 0.52).

## 0.51

- Chargements accélérés (gestion de la mémoire du jeu en O(log n) au lieu d'un parcours complet, test de 35 s à 46 ms) ; compteur simplifié façon RTSS avec températures CPU et GPU (APK 0.51).

## 0.50

- Le journal relève où travaille le jeu pendant les longues attentes sans image (chargements) ; contient la correction du décor de la 0.49 (APK 0.50).

## 0.49

- Les shaders de sommets du décor écrivent enfin leur position (EXIT conditionnel du tri rapide jamais pris) ; la passe de profondeur n'était plus vide (APK 0.49).

## 0.48

- Les listes de commandes en cache du décor ne s'écrasent plus quand elles débordent (cause probable du décor 3D noir) ; elles continuent dans des blocs du runtime (APK 0.48).

## 0.47

- Journal comparant les listes du décor à l'enregistrement et à l'exécution (enquête 3D noire) (APK 0.47).

## 0.46

- Corrige le plantage de la 0.45 au plateau ; le journal lit les drapeaux « shader prêt » des matériaux (enquête 3D noire) (APK 0.46).

## 0.45

- Journal de la méthode qui prépare le matériau des formes du décor (enquête 3D noire) (APK 0.45).

## 0.44

- Journal de l'objet de rendu qui émet les dessins du décor (enquête sur le décor 3D noir) (APK 0.44).

## 0.43

- Journal de l'exécuteur : d'où vient le programme des grands dessins du décor (liste, appelants, enregistrement qui l'a lié) (APK 0.43).

## 0.42

- Intro passée sans ses sons ni sa musique sur l'écran titre ; appuis très brefs vus par le jeu ; plus de feuille de partage au lancement (rapport rangé dans Téléchargements/Jamboree) ; écran gardé allumé ; journal des programmes nuls liés par le jeu, pour l'enquête sur le décor 3D noir (APK 0.42).

## 0.39

- Journal : programmes définis avec le shader de sommets « triangle écran » (tous les matériaux du décor) et leur chaîne d'appels (APK 0.39).

## 0.38

- Appli : pause quand elle n'est plus au premier plan (jeu, rendu et son) ; journal : programmes liés par le jeu à ses gros dessins, pour l'enquête 3D (APK 0.38).

## 0.37

- 3D : CopyCommands copie réellement les commandes de la source (le jeu réutilise la mémoire aussitôt ; les dessins du décor perdaient leur programme) (APK 0.37).

## 0.36

- 3D : BindProgram enregistre une copie immuable du programme, sans octets supplémentaires dans la mémoire de commandes (corrige le plantage de la 0.35) (APK 0.36).

## 0.35

- 3D : BindProgram lie les étages tels qu'enregistrés (un programme redéfini par SetShaders avant l'exécution n'est plus pris dans sa dernière version) ; journal des SetShaders (APK 0.35).

## 0.34

- 3D : BindProgram ne remplace plus que les étages de son masque (le décor était dessiné avec le shader de sommets plein écran d'un passage de post-traitement) ; programme composite par étage (APK 0.34).

## 0.33

- Son : la structure WaveBuffer du jeu est copiée à l'ajout (le plantage de la 0.32 dans le décodeur ADPCM venait d'une structure réécrite par le jeu) (APK 0.33).

## 0.32

- Son : la mise à jour audio du jeu atteint enfin le mixeur (poignée de 16 octets lue en x2) et états publics des pools mémoire ; les programmes de shader traduits vides sont journalisés automatiquement (APK 0.32).

## 0.31

- Bouton LOG : dans l'image déboguée, les premiers octets de chaque programme de shader et les tampons liés aux étages (enquête sur les décors invisibles : programme traduit sans attributs ni constantes) (APK 0.31).

## 0.30

- Son : veille toutes les 5 s depuis le thread AAudio (thread de mixage figé ? config absente ? compteurs des boucles internes), pour situer le silence persistant (APK 0.30).

## 0.29

- Son : mixage de secours par le thread audio du jeu (le thread de mixage ne rendait jamais de trame) et bilan audio toutes les 5 s ; bouton LOG : planche-contact des passes de l'image déboguée (`passes.png`) jointe au journal (APK 0.29).

## 0.28

- Journal et rapport partagés en fichier `.txt` dans `Téléchargements/Jamboree` (plus de limite de taille) ; repères audio dans le journal : voix, destinations, puits, pic de sortie (APK 0.28).

## 0.27

- Rendu : deux correctifs du pilote Qualcomm repris de BOTWRecompAndroid (MIT, origine dans `runtime/nvn/las/ORIGINE.md`) : une image liée dans deux slots de couleur ne garde que le slot écrit ; lectures sans comparaison via un sampler sans comparaison (APK 0.27).

## 0.26

- Audio : le renderer mixe les voix (PCM, DSP-ADPCM, hauteur, volumes, sous-mixages) et joue le son via AAudio ; `AudioOut` lu directement ; effets non traités, Opus encore muet (APK 0.26).

## 0.25

- Bouton LOG de la manette tactile : journal du runtime sur disque (`journal.txt`), détail d'une image à la demande et partage sans plantage ; décompte des dessins sautés actif sur Android (APK 0.25).

## 0.24

- Shaders de calcul : code après un en-tête de 0x100 octets (les 61 shaders de calcul du jeu étaient refusés) ; mémoire partagée LDS/STS, réductions atomiques RED, LEA.HI (7 096 étages sur 7 799) ; manette tactile refaite (petite, translucide, taille d'après la densité de l'écran) et ligne de statistiques en haut de l'écran ; plein écran sans bordure ; rapport de plantage avec les adresses du runtime nommées (APK 0.24).

## 0.23

- NVN : textures bindless (handle remonté jusqu'à sa constante), TLD4/TLD/TMML/TXQ.B, HSETP2/HSET2 constante et immédiat ; 7 064 étages de shaders sur 7 799 traduits (2 502 avant) ; les shaders refusés sont listés dans le rapport de lancement (APK 0.23).

## 0.22

- Intro sans vidéo : les sous-titres ne restent plus affichés sur l'écran titre (appel de mise à jour des sous-titres remplacé par un appel vide tant qu'il n'y a pas de décodeur ; APK 0.22).

## 0.21

- `nn::ro` : un module déchargé ne sert plus à lier les suivants (plantage du menu principal) ; lecteur vidéo : sans décodeur, la position de lecture est la fin de la vidéo (sous-titres de l'intro sur l'écran titre ; APK 0.21).

## 0.20

- Appli : manette tactile de test (boutons de la Switch dessinés par-dessus le jeu, joueur 1) ; réservée aux essais, la feuille de route reste sans manette tactile en mode pliant (APK 0.20).

## 0.19

- `nn::account` : profil utilisateur par défaut « Orikami », pour que le jeu charge sa sauvegarde (APK 0.19).

## 0.18

- Lecteur vidéo : gardes sur l'affichage et la position quand aucune vidéo n'est décodée (APK 0.18).

## 0.17

- Lecteur vidéo : le jeu ne plante plus à l'écran titre quand aucune vidéo n'est décodée (garde sur le rendu vidéo absent ; APK 0.17).

## 0.16

- Plantages : deux étages de gestion (le jeu → notre rapport, les threads Android → la chaîne d'ART, qui a besoin de ses SIGSEGV pour le code Java) ; le rapport nomme le thread ; `natives.txt` pour nommer les fonctions dans le rapport du lancement suivant (APK 0.16).

## 0.15

- Tests sans PC : au lancement, le rapport du lancement précédent (plantage + boîte noire décodée) est écrit dans `rapport.txt` et proposé au partage Android (APK 0.15).

## 0.14

- Plantages : gestionnaire installé sans libsigchain (le gestionnaire d'ART replantait avant le nôtre quand le jeu plante avec sa propre TLS) ; rapport par appels système directs (APK 0.14).

## 0.13

- Correctif : le passage journalisé de la boîte noire sautait via la PLT et plantait au démarrage de la 0.12 (APK 0.13).

## 0.12

- Boîte noire : les derniers appels du jeu vers le runtime sont gardés dans `blackbox.bin`, lisible après un plantage ; fichier `crashtest` pour tester le rapport de plantage (APK 0.12).

## 0.11

- Plantages : le rapport est aussi écrit dans `crash.txt` (à côté de `romfs`) par appel système direct, pour qu'il survive même quand la libc ou logcat plantent (APK 0.11).

## Avant la 0.11 : fondations et premiers essais

- Rapport de plantage écrit directement dans logcat ; l'APK porte enfin son numéro de version (0.10).
- Vidéo d'intro : lecteur sans décodeur compté comme préchargé et terminé (fin de la boucle de la scène titre) ; correctifs de code à signature courte (6 mots au plus).
- Sonde « fibres en attente » dans le journal ; correctif de préchargement vidéo basé sur l'état du lecteur, qui remplace celui de la PR #47 (la scène de l'écran titre ne boucle plus).
- Intro désactivée : la scène de l'écran titre n'attend plus un préchargement vidéo qui ne venait jamais (fin de l'écran blanc).
- Vidéo d'intro sautée (correctif de code vérifié avant application : le jeu ne reste plus sur un écran blanc), verrous pthread du jeu, cadence limitée à 60 images/s .
- Le jeu atteint la vidéo d'introduction sur le téléphone ; lecteur vidéo `movie::` en échec propre (vidéo passée) au lieu d'une fermeture silencieuse .
- Appli Android : image étirée sur toute la surface des deux écrans, échelle de rendu plafonnée à 1080p (12–20 → fluide au chargement), plantage au lancement écran éteint corrigé .
- Affichage plein écran (mode TV 1080p par défaut), icône adaptative recadrée, nom de l'appli complet. Premier affichage réel du jeu sur le téléphone (écran-titre, ≈ 38 images/s).
- Appli Android : manettes physiques reliées à `nn::hid` (joueurs 1 à 4, disposition Switch des boutons, sticks, gâchettes, croix).
- Appli Android : `NativeActivity` paysage reliée à la couche NVN → Vulkan, journaux vers logcat, jeu lancé par `smpj_run_main` ; construction de l'APK sans Gradle (`scripts/build-apk.sh`, `scripts/make_icon.py`), fichiers du jeu dans `Android/data/dev.orikami.smpj/files/smpj` (`android/README.md`, PR #35). Premier APK construit (4,1 Mo) ; installation sur le téléphone à suivre.
- NVN → Vulkan : couche reprise de LASRecomp-Android-Plus (MIT) adaptée au runtime (`runtime/nvn/las`, `docs/NVN_VULKAN.md`, PR #33) : 535/535 fonctions, rendu hors écran, mode sans GPU pour qemu ; test d'image rendue sur lavapipe ; `NVNsamplerBuilder` ramené à 64 octets. Sous qemu, le jeu présente ses images via la nouvelle couche et atteint le chargement des personnages. Origine et licences des fichiers repris : `runtime/nvn/las/ORIGINE.md`, `third_party/`. Pour construire : shaderc est compilé à part (`SMPJ_SHADERC_LIB`, `SMPJ_SHADERC_INCLUDE`, voir `docs/NVN_VULKAN.md` §5).
- Exceptions C++ du jeu propagées à travers le runtime, finaliseurs des modules NRO au déchargement et état des fibres conforme au SDK : le jeu passe le démarrage et entre dans l'intro sans planter . Prochaine étape : affichage NVN vers Vulkan.
- `nn::hid` : manettes 1 à 8, écran tactile, capteurs, vibrations, choix des manettes ; `IntrusiveDicNode::FindRefBit` conforme au SDK (archives chargées de nouveau inscrites) .
- Minuteries `nn::os` (une fois, périodique) ; constantes du SDK (`nn::util`, `nn::hid`) lues au lancement dans le module `sdk` du jeu ; variables importées introuvables remplacées par des zéros au lieu de thunks .
- HLE : fibres `nn::os` (changement de contexte coopératif AArch64), traduction de `FE_DFL_ENV` pour `fesetenv` ; le jeu lance son moteur de flux et demande `flow~boot` .
- HLE : moteur de polices `nn::fontll` sur FreeType (sous-module `third_party/freetype`, licence FTL ; cloner avec `git submodule update --init`), déchiffrement BFTTF, zone des thunks exécutable pendant le chargement des NRO ; le jeu charge ses polices et son premier module NRO .
- HLE : passage du jeu avec les vrais modules et archives ; `nn::util` (fichiers binaires, IntrusiveDic, NumberLineAllocator), `nn::pl` (polices partagées), correctifs NotNullImpl et NVN SamplerBuilder ; le jeu tourne jusqu'au moteur de police `nn::fontll` .
- HLE `nn::ro` : chargement des modules NRO par l'éditeur de liens du runtime . Validation avec les vrais modules à suivre.
- HLE audio muet (`nn::audio`, `nn::codec`), MultiWait/MessageQueue, allocateur sur la région du jeu avec régions emboîtées, `smpj-run --trace-natives` .
- NVN : squelette des 535 fonctions, dorsale nulle, conception NVN → Vulkan (`runtime/nvn`, `docs/NVN_VULKAN.md`, PR #14). Sous qemu, le jeu crée son `NVNdevice` et lit ses capacités, puis s'arrête dans `nn::audio` (prochaine étape).
- Threads du jeu en natif (`nn::os::CreateThread` et suivants, PR #12). Tests : 3/3 sur l'hôte, `hle_tests` sous qemu.
- Services natifs `nn::os`, `nn::fs` et `nn::oe` : `nnMain` lit la RomFS et atteint l'initialisation graphique (`nvnBootstrapLoader`) . Les 3 suites de tests passent. Pas encore testé sur téléphone ; prochaine étape : NVN vers Vulkan.
- Services natifs mémoire et libc++ (`runtime/hle`) : les constructeurs globaux s'exécutent et `nnMain` démarre, jusqu'à la lecture de la RomFS . Tests : 3/3 sur l'hôte, `cpu_tests` sous qemu. Pas encore testé sur téléphone.
- Couche CPU (`runtime/cpu`, TLS et thunks AArch64) et lanceur `smpj-run` : le code du jeu s'exécute nativement jusqu'à `nninitStartup` . Testé sur hôte et sous qemu-aarch64, pas encore sur téléphone. Prochaine étape : services `nn::` (mémoire, allocateurs).
- Ossature du dépôt : README, licence GPLv3, `docs/ARCHITECTURE.md`, rapport d'analyse, `.gitignore` strict, chargeur NSO/NRO .
- Outils d'extraction : `tools/ncaromfs`, `tools/nsosyms`, `scripts/extract_nsp.ps1`.
- Garde-fou CI contre les clés et les données du jeu, modèle de PR, feuille de route.
- Exigence ajoutée à la feuille de route : compatibilité et optimisation pour les smartphones pliants.
- Feuille de route : prise en charge des manettes physiques (USB et Bluetooth).
