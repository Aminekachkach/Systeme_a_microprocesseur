# Systeme_a_microprocesseur
This project was made by Me and my colleague Etienne PARMENTIER during our engineering studies at ENSEA.

BaudRate de l'USART2: 115200 Bits/ seconds

#TP 1.2 Questions
Q.13)
d'après la documentation technique la broche PB9 permet de permuter entre "flash program memory" et "system memory(bootloader)".
Il est important de tirer la broche en pull-down afin d'éviter qu'elle détecte un état haut au moment du reset et reflasher le mcu depuis le boot loader.

Q.14): La Bobine L1 et les capacités C5 et C7 forment un filtre de constante de temps T = 800 KHz.
Toutes les fréquences supérieures seront atténuées.

#TP 1.3 Questions
Q.3) On a les valeurs des capacités à la page 4, le schémas d'application à la page 1 permet d'être sûre que nos schémas correspondent.
Q.5) On a les valeurs des capacités à la page 25, avec le schémas qui correspond.
Q.6) La broche CS-barré est le chip select: quand elle est à l'état bas, la puce est active.
Q.7) La broche LDAC-barré synchonise le registre interne et la sortie du convertisseur.
Q.8) La broche MISO du STM32 n'est pas utilisé car aucune information n'est envoyé par le DAC au STM32. Le DAC fait juste des conversions,
Les données ne circule que dans un sens.
Q.10) Les Broches SWD sont standardisés.

#TP 1.4 Questions
Q.3) Les nombres 0805, 0603, 1206 sont les formats des boitiers des composants.
Q.4) LQFP signifie: Low Profile Quad Flat Package: La puce est basse (Low Profile), et plate (flat), et il y a des pins dans les 4 directions (Quad)
SOT-223 est un format de petit boitier pour transistor (Small Outline Transistor).
un SOIC (Small Outline Integrated Circuit) est une puce avec des pins de deux cotés, avec une épaisseur très faible.
-> Tout ces formats de puces sont montés en surface du PCB.

#TP 3.1 Questions
Q.2) Il y a beaucoup moins de fichiers générer, c'est parce-que l'on utilise des fonctions plus bas niveau sans les couches d'abstractions qu'il y a au
dessus.
Il y a beaucoup de fichiers avec __STATIC_INLINE

Q.4) __STATIC_INLINE est une macro qui contient les mots clés 'static' et 'inline'.
'static' indique au compilateur que la fonction n'est pas utilisé ailleurs que dans le fichier qui la contient.
la mise en ligne de fonction est une optimisation qui consiste à copier-coller le code de la fonction marqué 'inline'
à l'intérieur des fonctions qui l'appelle. Cela à plusieurs effets:
    - Les passe d'optimisation qui ont lieu après comme l'élimination du code mort, l'évaluation des constantes, etc... fonctionnent mieux.
    - Le code résultant est donc plus rapide, car on n'a plus besoin de sauvegarder l'état des registres dans la pile quand on appelle la fonction.
    - Dans certains cas, le code générer peut être plus gros, car les même instructions sont répétés plusieurs fois. Mais dans notre cas, les fonctions LL
    sont tellement petites que ça ne devrait pas poser de probléme. Si le compilateur calcule que plus d'instructions seront généré, il ne fera pas d'inlining.

Q.5) Le code est dans un fichier .h car du coup chaque 'compile unit' dois connaître la définition des fonctions à inliner, ce qui n'est pas nécéssaire
quand le code de chaque module est compilé séparement et qu'ils appellent des fonctions selon la convention d'appel standard du langage C.
