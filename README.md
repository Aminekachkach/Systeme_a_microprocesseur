# Systeme_a_microprocesseur
This project was made by Me and my colleague Etienne PARMENTIER during our engineering studies at ENSEA.

BaudRate de l'USART2: 115200 Bits/ seconds

#TP 1.2 Questions
Q.13)
d'après la documentation technique la broche PB9 permet de permuter entre bootloader interne et externe (provenant de la liaison série).
Il est important de tirer la broche en pull-down afin d'éviter qu'elle détecte un état haut au moment du reset et en consequence decide de passer au chargeur de demarrage interne.

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