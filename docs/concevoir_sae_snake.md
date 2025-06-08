# 📚 Portfolio SAE Arkanoid – BUT GEII 1ère Année

## 🔹 Compétence : Concevoir

### 🔸 Contexte
Initialement, notre projet consistait à réaliser une borne d’arcade miniature, mais après analyse des contraintes (transport, esthétique et complexité), nous avons pivoté vers une console portable inspirée de la Game Boy.

### 🔸 Activités réalisées

#### 📋 Cahier des charges et planification
- Analyse des besoins réels et adaptation du projet : abandon de la borne d’arcade pour une console portable.
- Rédaction d’un cahier des charges incluant les composants (PIC16F18877, écran TFT), contraintes techniques (taille, budget) et moyens disponibles à l’IUT.
- Utilisation d’un **diagramme de Gantt** pour organiser les tâches et planifier le projet.

![alt text](<images/Sae snake/diagrame_de_gant.jpg>)


**Apprentissage critique :**
- Adapter un projet aux contraintes techniques et matérielles.
- Maîtriser la gestion de projet pour assurer le respect des délais.

**Lien avec les matières :**
- **Communication & PPP** : présentation et argumentation des choix lors des réunions de suivi.
- **Automatisme & Informatique industrielle** : structuration des tâches et formalisation du cahier des charges.

---

#### 🛠️ Conception mécanique (SolidWorks)
- Conception 3D du boîtier à partir de croquis papier et de mesures précises (pied à coulisse, datasheet).
- Réajustement des dimensions pour intégrer le PCB prototype.
- Création d’un système de fermeture vissé inspiré des calculatrices (impression 3D plus simple à réaliser).


PCB prototype utiliser : 

![alt text](<images/Sae snake/PCB_joystique.png>)

## 📸 Représentations du Projet SAE Snake

| 🔍 Vue technique | 📐 Cotation CAO |
|------------------|------------------|
| ![croquis](<images/Sae snake/Image du croquis.PNG>) | ![cotation solidworks](<images/Sae snake/cotation_pcb_solidworks.png>) |

> 📝 À gauche : le **croquis fonctionnel initial** du projet SAE Arcanoid, illustrant les composants clés et leurs connexions logiques.  
> 🧰 À droite : la **modélisation détaillée sous SolidWorks** avec les **cotes précises du PCB**, utilisée pour la fabrication.



## 🧱 Boîtier final du projet SAE Snake

| 🔲 Vue avant | 🔄 Vue arrière |
|--------------|----------------|
| ![l'avant du boitier](<images/Sae snake/boitier_final.png>) | ![arriere_du_boitier](<images/Sae snake/arriere_boitier.png>) |

Petite  Video ilustrative : 

[![Test du moteur en fonctionnement](https://img.youtube.com/vi/8NDEZ3Jczmg/hqdefault.jpg)](https://youtu.be/8NDEZ3Jczmg)


> 🛠️ Le boîtier a été conçu pour **protéger l’électronique** tout en assurant l’accès aux connecteurs.  
> 🔌 **Vue avant** : interfaces utilisateurs et connecteurs accessibles.  
> 🔧 **Vue arrière** : accès aux bornes d’alimentation et éventuelles aérations.



**Apprentissage critique :**
- Adapter la conception au fur et à mesure des tests et impressions.
- Utiliser les itérations d’impression 3D pour corriger les défauts.

**Lien avec les matières :**
- **Électronique & Systèmes embarqués** : intégration mécanique du PCB.
- **Mathématiques & Physique appliquée** : calculs de dimensions, utilisation du pied à coulisse.


## 🖨️ Utilisation de SuperSlicer pour l'impression 3D du boîtier

Afin de fabriquer notre boîtier conçu sur SolidWorks, j'ai utilisé **SuperSlicer**, un logiciel de **tranchage 3D** (slicer) qui permet de convertir un modèle 3D en **G-code** lisible par l'imprimante 3D.

### ⚙️ Étapes réalisées :

- 🔍 **Chargement du fichier STL** du boîtier (issu de SolidWorks) dans SuperSlicer.
- 🔧 **Paramétrage des réglages d’impression** : hauteur de couche, remplissage, température de buse et plateau.
- 📏 **Ajustement des supports** et de la première couche pour assurer une bonne adhérence.
- 📄 **Génération du fichier G-code** prêt à être transféré sur l’imprimante 3D.
- ✅ **Test d’impression** et vérification des dimensions réelles après fabrication.

### 🖼️ Illustration

| Avant du boîtier | Arrière du boîtier (PCB) |
|------------------|--------------------------|
| 
![alt text](<images/Sae snake/Imprimer vue de face.jpg>)| ![alt text](<images/Sae snake/arriere_imprimer.jpg>) |

---

### 🎓 Liens pédagogiques

#### 🧠 Apprentissage critique
- Comprendre le lien entre **modélisation CAO** et **fabrication réelle**.
- Apprendre à régler les paramètres d’un slicer pour garantir une impression **fiable et précise**.
- Savoir **corriger les erreurs d’adhérence ou de surchauffe** en modifiant le G-code ou les paramètres.

#### 🧩 Lien avec les compétences GEII

| Compétence GEII        | Détail                                                |
|------------------------|--------------------------------------------------------|
| **C1 – Concevoir**     | Transformer une modélisation 3D en objet physique via impression 3D |
| **C4 – Mettre en œuvre** | Configurer une machine à commande numérique (ici l’imprimante) pour produire une pièce |

#### 📚 Lien avec les matières
- **Conception assistée par ordinateur (CAO)** : lien direct avec le logiciel SolidWorks utilisé.
- **Fabrication numérique** : paramétrage, test et validation de l’impression 3D.
- **Projet SAE (Snake ou autres)** : intégration complète du boîtier dans la solution matérielle du projet.

---

📌 *Grâce à cette étape, j’ai compris que concevoir un boîtier fonctionnel ne se limite pas à la modélisation : il faut aussi anticiper les contraintes d’impression comme la dilatation, les jeux mécaniques et la stabilité du modèle pendant l’impression.*



---

#### 🧩 Conception électronique (KiCad)
- Réalisation du schéma électrique complet de la carte son.
- Création des fichiers Gerber et validation auprès du constructeur.
- Résolution d’erreurs de routage (erreurs de fils, problèmes de perçage).


## 🧩 Schémas KiCad – Conception et Contrôle

| 🧠 schéma de carte son (Projet) | 📄 Schéma reçu au contrôle de SAE |
|-------------------------------------|------------------------------------|
| ![kikad_carte_son](<images/Sae snake/kikade_carte_son.png>) | ![alt text](<images/Sae snake/Realisationd'une autre carte son.png>) |


> 🎓 Ce tableau compare :
> - À gauche : le **schéma électrique que j’ai conçu moi-même** sous KiCad, pour la réalisation de la carte son du projet SAE Snake.
> - À droite : le **schéma donné lors de mon contrôle de SAE**, que j’ai dû analyser et corriger en temps limité.
> 
> 🔍 Cet exercice m’a permis de valider ma capacité à :
> - Lire un schéma électronique inconnu rapidement
> - Repérer les incohérences de routage
> - Appliquer la même rigueur que dans mon projet personnel



routage de la carte son : 

![alt text](<images/Sae snake/CARTE SON.png>)


 et creation de fichier gerber avec les fichier percage...

![creation de fichier gerber](<images/Sae snake/Capture d'écran 2025-06-07 140221.png>)

![tracer les fichier gerber](<images/Sae snake/Capture d'écran 2025-06-07 140238.png>)


simulation chez le constructeur :  

![image de la simulation chez le constructeur](<images/Sae snake/Simulation_constructeur.png>)



**Apprentissage critique :**
- Comprendre la chaîne de conception et de validation d’un PCB.
- Apprendre à gérer les erreurs et les contraintes du fabricant.

**Lien avec les matières :**
- **Électronique & Systèmes embarqués** : schéma électrique, routage, validation des fichiers Gerber.
- **Automatisme & Informatique industrielle** : interactions entre le PCB et le microcontrôleur.


### brasure des composant realisation d'une liste avec tout les composant et braser

| Composant       | Référence          | Quantité | Fonction            |
|-----------------|--------------------|----------|---------------------|
| Amplificateur   | LM386N             | 1        | Amplification audio |
| Potentiomètre   | 10kΩ linéaire      | 1        | Contrôle volume     |
| Condensateur   | 10µF électrolytique | 2        | Découplage alimentation |
| Condensateur   | 100nF céramique     | 1        | Filtrage HF         |
| Condensateur   | 47nF céramique      | 1        | Couplage entrée     |
| Condensateur   | 220µF électrolytique| 1        | Filtrage sortie     |
| Résistance     | 10Ω 1/4W            | 1        | Protection sortie   |
| Résistance     | 0Ω (strap)          | 1        | Liaison directe     |
| Interrupteur   | ON/OFF              | 1        | Mise sous tension   |
| Connecteurs    | 2.54mm              | 4        | Liaisons PCB        |

Une fois que on a dresser une liste des composant on est partie braser la carte son sur un poste de soudage : 

on a pue souder les different composant :  

![Pcb carte son](<images/Sae snake/PCB_carte_son.png>)

Apprentissage critique = on a appris a bien braser et detecter les eventuelle panne 

competence : 
lien avec la matiere : ELEN

## 🔧 Réalisation du câblage global et configuration du microcontrôleur

Dans le cadre du projet SAE Snake, j’ai réalisé l’**intégration matérielle** complète entre les différents composants : écran LCD, carte son, PCB joystick, et carte principale. Cette étape repose sur la **configuration du microcontrôleur** via **MCC (MPLAB Code Configurator)** ainsi que sur l’interprétation de **datasheets techniques** pour le câblage.

---

### ⚙️ Configuration des entrées/sorties (MCC)

J’ai commencé par configurer l’ensemble des **broches d’E/S** (entrées/sorties) de mon microcontrôleur pour chaque composant connecté :

| MCC – Affectation des broches |
|-------------------------------|
| ![Grand_pinmodule](<images/Sae snake/pINmodule1.png>) |
| ![SUITE DU PINEMODULE](<images/Sae snake/Pinmodule2suit.png>) |

> 📌 Grâce à ce pin module, j’ai défini les broches à utiliser pour :
> - l’écran LCD (SPI/I2C),
> - le PCB de prototypage (GPIO, alimentation),
> - la carte son (sortie audio),
> - les joysticks et boutons (entrées numériques).

---

### 📚 Câblage basé sur les documentations techniques

Pour garantir un câblage correct, j’ai utilisé les **datasheets** et schémas de référence des composants :

## 🖼️ Schémas de câblage des composants

| 🎮 Joystick Shield – PCB | 🖥️ Écran LCD – I2C |
|--------------------------|--------------------|
| ![Schéma joystick](<images/Sae snake/Capture d'écran 2025-04-24 130112.png>) | ![Schéma écran](<images/Sae snake/Ecran_Cablage.jpg>) |

> 🔧 Ces schémas m’ont permis de :
> - Identifier les **broches de connexion** pour chaque composant.
> - Comprendre les **protocoles utilisés** (I2C, entrées numériques).
> - Réaliser un **câblage fonctionnel et fiable** dans le respect des tensions et niveaux logiques.


> 🔍 Ces documents m'ont permis de repérer les **noms des broches**, leurs **niveaux logiques attendus**, et le **type de communication** utilisé (I2C, SPI, etc.).


Cablage final : 




---

## 🎯 Liens pédagogiques

| Élément travaillé                               | Détail |
|-------------------------------------------------|--------|
| **Compétence visée**                            | C1 – Concevoir une solution technique (matérielle ou logicielle) |
| **Matière associée**                            | Informatique embarquée / TP microcontrôleur |
| **Apprentissage critique**                      | **C1a : Produire une analyse fonctionnelle d’un système** |
| **Justification**                               | J’ai été capable de déterminer les fonctions d’entrées/sorties, les types de signaux, et les connexions entre composants selon les spécifications matérielles. |
| **SAE associée**                                | SAE Snake / Carte embarquée connectée |

---

🎓 *Cette phase de conception m’a permis d’apprendre à lire un schéma technique, configurer un microcontrôleur de façon autonome et concevoir un câblage structuré pour un système électronique embarqué.*



### Choix des composants et gestion énergétique

Dans cette phase, il a été essentiel de **sélectionner des composants** compatibles entre eux et optimisés pour une **consommation énergétique maîtrisée**, en vue d'une alimentation sur batterie rechargeable. Cette démarche a impliqué une réflexion autour des critères suivants :

- Compatibilité en tension (5V ou 3.3V)
- Consommation énergétique des composants
- Disponibilité des modules
- Facilité d’intégration dans le système
- Taille physique des modules

#### 🧮 Tableau estimatif de la consommation par composant :

| Composant                        | Tension (V) | Consommation (mA) | Puissance (W) |
|----------------------------------|-------------|--------------------|---------------|
| Microcontrôleur PIC16F18877     | 5V          | 40                 | 0.20          |
| Écran TFT 2.8" SPI              | 5V          | 60                 | 0.30          |
| Boutons poussoir (x4)          | 5V          | 10                 | 0.05          |
| Joystick 4 directions          | 5V          | 20                 | 0.10          |
| PCB Joystick Shield v1.a       | 5V          | 15                 | 0.075         |
| Module TP4056 (veille)         | 3.7V        | 10                 | 0.037         |
| Carte son (AOP LM386)          | 5V          | 25                 | 0.125         |
| **Total estimé**               | -           | **180 mA**         | **≈ 0.9 W**   |

---

### ⚡ Choix du module de charge et de la batterie

Sur la base du tableau précédent, une consommation moyenne de **180 mA** pour le système complet a été estimée.

#### 🟢 Choix du module de charge : **TP4056**
- Module compact, spécialisé dans la **recharge des batteries Li-ion 3.7V**.
- Intègre la **protection contre les surtensions**, surintensités et court-circuits.
- Prend en charge un courant de charge jusqu’à **1A**, suffisant pour notre batterie et usage.

![alt text](<images/Sae snake/Module de charge.png>)
---

#### 🔋 Choix de la batterie : **Batterie Li-ion 3.7V 1000 mAh**
- Récupérée d’une manette PS4 HS (économie circulaire)
- Donne une autonomie théorique ≈ **5h** (1000 mAh / 180 mA)
- Forme compacte, facile à intégrer dans le boîtier

![alt text](<images/Sae snake/Batteire.png>)
---

### 🧠 Apprentissage critique :
- Savoir **estimer les besoins énergétiques** d’un système embarqué.
- Savoir **dimensionner une source d’énergie** (batterie + module de charge) selon la **consommation réelle**.
- Comprendre **l’équilibre entre puissance, encombrement et autonomie**.
- Maîtriser la **conception électronique sous contraintes physiques et énergétiques**.
- Réutiliser un composant (batterie PS4) de manière responsable, en lien avec une **démarche écoresponsable**.

---

### 📘 Lien avec les matières :

| Matière                                   | Liens concrets dans le projet |
|------------------------------------------|-------------------------------|
| **Électronique & Systèmes embarqués**    | Étude du schéma électrique, calcul de consommation, intégration du TP4056, conception du circuit de charge |
| **Automatisme & Informatique industrielle** | Interaction entre l’alimentation, le microcontrôleur et les entrées/sorties du système |
| **Physique appliquée**                   | Calcul de puissance, estimation d’autonomie, rendement de charge, gestion thermique |
| **Gestion de projet / Développement durable** | Réutilisation de composants, réflexion sur la durabilité du système |

---

### 🔧 Conception du module de charge sous KiCad

Pour valider la solution, le module de charge a été intégré dans le schéma global sous **KiCad**. Cela a nécessité :

- La création du **schéma électrique**
- Le **routage manuel** du PCB
- La **génération des fichiers Gerber** pour fabrication

schema elec : 

![alt text](<images/Sae snake/shcema modulede charge.jpg>)

schema kikad  : 




---
## 💻 Programmation du jeu Arkanoid – SAE Snake

### 🎓 Compétence : C1 – Concevoir une solution matérielle ou logicielle  
### 📚 Matières associées : Informatique embarquée, Automatisme & Interfaces utilisateur  
### 🧠 Apprentissage critique : Transformer un cahier des charges en code fonctionnel, corriger des bugs, organiser une structure logicielle robuste

---

### 🧱 Initialisation des paramètres du jeu

```c
#define SCREEN_WIDTH  320
#define SCREEN_HEIGHT 240
#define ROTATION      1




# 🎮 Analyse complète du code Arkanoid

## 📋 Vue d'ensemble du projet

Ce code implémente un jeu Arkanoid complet sur microcontrôleur PIC avec écran TFT, démontrant une maîtrise des **systèmes embarqués** et de la **programmation en C**.

---

## 🔧 Section 1: Inclusions et définitions globales

```c
#include "mcc_generated_files/mcc.h"
#include "ILI9341.h"
#include "GFX_Library.h"
#include <stdbool.h>
#include <stdio.h>
```

**📸 Photo recommandée :** Vue d'ensemble du projet MPLAB X avec les fichiers d'en-tête

**💡 Explication :**
- Intégration des bibliothèques générées automatiquement par MCC (MPLAB Code Configurator)
- Utilisation de l'écran ILI9341 (320x240 pixels)
- Inclusion des types booléens et fonctions d'affichage

**🎯 Lien compétences :**
- **Automatisme & Informatique industrielle** : Utilisation d'outils de configuration automatique
- **Électronique & Systèmes embarqués** : Interface avec composants externes (écran TFT)

---

## 🖥️ Section 2: Configuration écran et constantes de jeu

```c
// === Écran ===
#define SCREEN_WIDTH  320
#define SCREEN_HEIGHT 240
#define ROTATION      1

// === Raquette ===
#define PADDLE_WIDTH   60
#define PADDLE_HEIGHT  10
#define PADDLE_SPEED   7

// === Balle ===
#define BALL_SIZE      6

// === Briques ===
#define BRICK_ROWS     6
#define BRICK_COLS     10
#define BRICK_WIDTH    30
#define BRICK_HEIGHT   10
```

**📸 Photo recommandée :** Schéma ou dessin montrant les dimensions sur l'écran

**💡 Explication :**
- Définition des constantes pour éviter les "nombres magiques"
- Paramétrage modulaire permettant des ajustements faciles
- Organisation logique par éléments de jeu

**🎯 Lien compétences :**
- **Mathématiques & Physique appliquée** : Calculs dimensionnels, positionnement géométrique
- **Communication & PPP** : Code lisible et bien structuré

---

## 🕹️ Section 3: Lecture des entrées analogiques (Joystick)

```c
uint16_t lireJoystickX() {
    ADPCH = 0x02; // RA2
    ADCON0bits.ADON = 1;
    ADCON0bits.ADGO = 1;
    while (ADCON0bits.ADGO);
    return ((uint16_t)ADRESH << 8) | ADRESL;
}

uint16_t lireJoystickY() {
    ADPCH = 0x09; // RB1 = AN9
    ADCON0bits.ADON = 1;
    ADCON0bits.ADGO = 1;
    while (ADCON0bits.ADGO);
    return ((uint16_t)ADRESH << 8) | ADRESL;
}
```

**📸 Photo recommandée :** Joystick analogique connecté au microcontrôleur

**💡 Explication :**
- Configuration des canaux ADC pour lecture joystick 2 axes
- Gestion des registres de conversion analogique-numérique
- Reconstruction de la valeur 10 bits à partir des registres haut/bas

**🎯 Lien compétences :**
- **Automatisme & Informatique industrielle** : Gestion des entrées/sorties, interfaçage capteurs
- **Électronique & Systèmes embarqués** : Conversion analogique-numérique, registres microcontrôleur

---

## 🎵 Section 4: Système audio et mélodies

```c
int music[12] = {102,108,115,121,129,136,145,153,162,172,182,193};
// Do(C),Do#(C#),Re(D),Re#(D#),Mi(E),Fa(F),Fa#(F#),Sol(G),Sol#(G#),La(A),La#(A#),Si(B)

void playMenuMusic(void) {
    int menuNotes[] = {0, 4, 7, 0}; // Do, Mi, Sol, Do
    for (int i = 0; i < 4; i++) {
        NCO1INC = ((5 + music[menuNotes[i]] * 1.28) / 4);
        __delay_ms(300);
    }
}
```

**📸 Photo recommandée :** Haut-parleur/buzzer connecté, oscilloscope montrant signal audio

**💡 Explication :**
- Utilisation du module NCO (Numerically Controlled Oscillator) pour générer des fréquences
- Tableau de fréquences correspondant aux notes musicales
- Séquences mélodiques différentes selon le contexte (menu, victoire, défaite)

**🎯 Lien compétences :**
- **Mathématiques & Physique appliquée** : Calculs de fréquences, génération de signaux
- **Électronique & Systèmes embarqués** : Modules spécialisés du microcontrôleur (NCO)

---

## 🎨 Section 5: Gestion graphique et palettes

```c
typedef enum {
    PALETTE_CLASSIQUE,
    PALETTE_JUL,
    PALETTE_PASTEL,
    PALETTE_OCEAN,
    PALETTE_FEU
} PaletteType;

const uint16_t palette_classique[6] = {ILI9341_RED, ILI9341_ORANGE, ILI9341_YELLOW, 
                                       ILI9341_GREEN, ILI9341_BLUE, ILI9341_MAGENTA};

void drawBorders(void) {
    fillRect(0, 20, 5, SCREEN_HEIGHT - 20, ILI9341_BLUE);
    fillRect(SCREEN_WIDTH - 5, 20, 5, SCREEN_HEIGHT - 20, ILI9341_BLUE);
    fillRect(0, 20, SCREEN_WIDTH, 5, ILI9341_BLUE);
}
```

**📸 Photo recommandée :** Écran montrant les différentes palettes de couleurs

**💡 Explication :**
- Système de palettes interchangeables pour personnalisation visuelle
- Fonctions de dessin optimisées pour l'affichage TFT
- Interface utilisateur attractive avec bordures et éléments graphiques

**🎯 Lien compétences :**
- **Communication & PPP** : Interface utilisateur intuitive et esthétique
- **Automatisme & Informatique industrielle** : Gestion d'affichage, IHM (Interface Homme-Machine)

---

## 🧱 Section 6: Structure des briques et niveaux

```c
typedef struct {
    uint16_t x, y, width, height;
    bool active;
    uint16_t color;
} Brick;

Brick bricks[BRICK_ROWS][BRICK_COLS];

void initBricks(void) {
    switch(level) {
        case 1:  // Vagues décalées
            for (uint8_t row = 0; row < BRICK_ROWS; row++) {
                for (uint8_t col = 0; col < BRICK_COLS; col++) {
                    if ((col + row) % 2 == 0) bricks[row][col].active = true;
                }
            }
            break;
        
        case 3:  // Cœur
            uint8_t pattern[6][10] = {
                {0,1,0,0,0,0,0,0,1,0},
                {1,1,1,0,0,0,0,1,1,1},
                // ...
            };
            break;
    }
}
```

**📸 Photo recommandée :** Écran montrant différents patterns de briques (cœur, damier, etc.)

**💡 Explication :**
- Structure de données optimisée pour les briques (position, état, couleur)
- Algorithmes de génération de motifs variés selon le niveau
- Système de progression avec difficulté croissante

**🎯 Lien compétences :**
- **Mathématiques & Physique appliquée** : Algorithmique, motifs géométriques, modulo
- **Automatisme & Informatique industrielle** : Structures de données, gestion mémoire

---

## ⚽ Section 7: Physique de la balle et collisions

```c
void updateBall(void) {
    // Effacement position précédente
    drawBall(ballX, ballY, ILI9341_BLACK);
    
    // Calcul nouvelle position
    int16_t newX = ballX + ballSpeedX;
    int16_t newY = ballY + ballSpeedY;
    
    // Collisions avec bordures
    if (newX <= BALL_SIZE || newX >= SCREEN_WIDTH - BALL_SIZE) 
        ballSpeedX = -ballSpeedX;
    if (newY <= BALL_SIZE) 
        ballSpeedY = -ballSpeedY;
    
    // Collision avec raquette
    if (checkCollision(newX, newY, BALL_SIZE*2, BALL_SIZE*2,
                       paddleX, paddleY, PADDLE_WIDTH, PADDLE_HEIGHT)) {
        ballSpeedY = -level;
        int16_t offset = newX - (paddleX + PADDLE_WIDTH / 2);
        ballSpeedX = offset / 6; // Effet directionnel
    }
}
```

**📸 Photo recommandée :** Séquence montrant la balle rebondissant sur la raquette

**💡 Explication :**
- Implémentation de la physique basique : rebonds, vitesse, direction
- Détection de collisions rectangulaires optimisée
- Effet directionnel sur la raquette pour contrôle avancé

**🎯 Lien compétences :**
- **Mathématiques & Physique appliquée** : Vecteurs, cinématique, détection de collisions
- **Automatisme & Informatique industrielle** : Algorithmes temps réel, optimisation

---

## 🎮 Section 8: Contrôle de la raquette

```c
void updatePaddle(void) {
    uint16_t valeurX = lireJoystickX();
    uint16_t valeurY = lireJoystickY();
    
    int16_t newX = paddleX;
    int16_t newY = paddleY;

    // Seuils de détection joystick
    if (valeurX < 400) newX -= PADDLE_SPEED;
    if (valeurX > 624) newX += PADDLE_SPEED;
    
    // Contraintes de mouvement
    if (newX < 0) newX = 0;
    if (newX > SCREEN_WIDTH - PADDLE_WIDTH) 
        newX = SCREEN_WIDTH - PADDLE_WIDTH;
    
    // Mise à jour graphique
    if (newX != paddleX || newY != paddleY) {
        clearPaddle();
        paddleX = newX;
        paddleY = newY;
        drawPaddle();
    }
}
```

**📸 Photo recommandée :** Joystick en action avec raquette se déplaçant à l'écran

**💡 Explication :**
- Conversion des valeurs analogiques en mouvements discrets
- Gestion des limites d'écran et contraintes physiques
- Optimisation graphique (redessinage uniquement si changement)

**🎯 Lien compétences :**
- **Automatisme & Informatique industrielle** : Interface homme-machine, temps réel
- **Mathématiques & Physique appliquée** : Conversion analogique-numérique, seuillage

---

## 📊 Section 9: Interface utilisateur et informations

```c
void drawGameInfo(void) {
    char info[32];
    sprintf(info, "Score: %u  Vies: %u", score, lives);
    
    // Effacement zone d'affichage
    fillRect(0, 0, SCREEN_WIDTH, 20, ILI9341_BLACK);
    
    // Affichage texte
    display_setCursor(10, 5);
    display_setTextColor(ILI9341_WHITE, ILI9341_BLACK);
    for (uint8_t i = 0; info[i]; i++) {
        display_print(info[i]);
    }
    
    // Barre de vie graphique
    for (uint8_t i = 0; i < maxVies; i++) {
        uint16_t color = (i < lives) ? ILI9341_RED : ILI9341_DARKGREY;
        fillRect(baseX + i * (segmentW + spacing), baseY, segmentW, segmentH, color);
    }
}
```

**📸 Photo recommandée :** Interface montrant score, vies et barre d'énergie

**💡 Explication :**
- Affichage temps réel des informations de jeu
- Interface graphique claire avec barres de vie visuelles
- Gestion efficace du rafraîchissement d'écran

**🎯 Lien compétences :**
- **Communication & PPP** : Design d'interface utilisateur claire
- **Automatisme & Informatique industrielle** : IHM, affichage temps réel

---

## 🎯 Section 10: Menu interactif et sélection

```c
void showMenu(void) {
    uint8_t paletteIndex = 0;
    bool confirmed = false;
    level = 1;
    
    const char* paletteNames[] = {
        "Classique", "Jul", "Pastel", "Ocean", "Feu"
    };
    
    while (!confirmed) {
        if (refresh) {
            fillScreen(ILI9341_BLACK);
            drawText(60, 20, "Choix du Niveau", ILI9341_WHITE);
            // ... affichage menu
        }
        
        // Gestion boutons
        if (BP_B_GetValue() == 0 && level < 9) level++;
        if (BP_D_GetValue() == 0 && level > 1) level--;
        if (BP_C_GetValue() == 0) {
            paletteIndex = (paletteIndex + 1) % 5;
            currentPalette = (PaletteType)paletteIndex;
        }
        if (BP_A_GetValue() == 0) confirmed = true;
    }
}
```

**📸 Photo recommandée :** Menu interactif avec boutons et sélections

**💡 Explication :**
- Menu de configuration complet avec boutons physiques
- Système de navigation intuitive
- Personnalisation du gameplay (niveau, palette)

**🎯 Lien compétences :**
- **Communication & PPP** : Interface utilisateur ergonomique
- **Automatisme & Informatique industrielle** : Gestion des entrées, configuration système

---

## 🔄 Section 11: Boucle principale et états de jeu

```c
void main(void) {
    // Initialisation système
    SYSTEM_Initialize();
    SPI1_Open(SPI1_DEFAULT);
    tft_begin();
    
    // Séquence de démarrage
    showIntroScreen();
    showMenu();
    
    // Boucle principale
    while (1) {
        // Gestion pause
        if (BP_E_GetValue() == 0) {
            isPaused = !isPaused;
            // ...
        }
        
        if (!isPaused) {
            updatePaddle();
            updateBall();
            
            // Conditions de victoire/défaite
            if (allDestroyed) {
                playVictoryMelody();
                // Reset niveau suivant
            }
            if (lives == 0) {
                playGameOverMelody();
                // Retour menu
            }
        }
        
        __delay_ms(16); // ~60 FPS
    }
}
```

**📸 Photo recommandée :** Jeu en cours d'exécution montrant tous les éléments

**💡 Explication :**
- Architecture en machine à états (intro→menu→jeu→fin)
- Boucle de jeu optimisée à ~60 FPS
- Gestion complète du cycle de vie du jeu

**🎯 Lien compétences :**
- **Automatisme & Informatique industrielle** : Architecture logicielle, temps réel
- **Communication & PPP** : Expérience utilisateur fluide

---

## 🏆 Synthèse des compétences développées

### 📐 **Mathématiques & Physique appliquée**
- ✅ Calculs de positions et collisions rectangulaires
- ✅ Génération de fréquences audio (NCO)
- ✅ Algorithmes de motifs géométriques
- ✅ Gestion des vecteurs vitesse/direction

### ⚡ **Automatisme & Informatique industrielle**
- ✅ Programmation microcontrôleur PIC en C
- ✅ Gestion temps réel (boucle 60 FPS)
- ✅ Interface avec périphériques (ADC, SPI, GPIO)
- ✅ Architecture logicielle modulaire

### 🔌 **Électronique & Systèmes embarqués**
- ✅ Interface écran TFT via SPI
- ✅ Lecture capteurs analogiques (joystick)
- ✅ Génération audio par NCO
- ✅ Gestion des entrées numériques (boutons pull-up)

### 💬 **Communication & PPP**
- ✅ Code documenté et structuré
- ✅ Interface utilisateur intuitive
- ✅ Menu de configuration ergonomique
- ✅ Expérience de jeu engageante

---

## 🎯 Points forts du projet

1. **Intégration complète** : Audio, vidéo, contrôles, tout fonctionne ensemble
2. **Code modulaire** : Fonctions bien séparées, réutilisables
3. **Interface riche** : Menus, palettes, niveaux progressifs
4. **Optimisation** : Gestion efficace de l'affichage et des ressources
5. **Gameplay varié** : Différents patterns de briques, difficulté croissante

---

## 📝 Apprentissage critique démontré

✅ **Transformation cahier des charges → code fonctionnel**
- Analyse des besoins du jeu Arkanoid
- Implémentation de toutes les fonctionnalités demandées

✅ **Débogage et correction**
- Gestion des collisions complexes
- Optimisation de l'affichage pour éviter les scintillements
- Calibrage des seuils du joystick analogique

✅ **Intégration matériel/logiciel**
- Maîtrise de l'écosystème MPLAB X / MCC
- Interface avec multiples périphériques simultanément





#### 💻 Programmation (MPLAB X)
- Programmation en langage C du jeu Arkanoid (affichage des briques, déplacement via boutons poussoirs).
- Intégration des boutons configurés en pull-up.
- Génération de positions aléatoires pour les briques (fonction rand).





**Apprentissage critique :**
- Transformer un cahier des charges en code fonctionnel.
- Déboguer des erreurs de compilation et corriger les bugs.

**Lien avec les matières :**
- **Automatisme & Informatique industrielle** : gestion des entrées/sorties, programmation microcontrôleur.
- **Mathématiques** : positionnement aléatoire des briques.

---

### 🔎 Problèmes rencontrés et solutions
- Ajustement des dimensions du boîtier après la première impression 3D.
- Mauvais câblage initial du PCB : correction après analyse du schéma.
- Problème de brasage du PCB (surchauffe, détérioration) : recommencer le brasage.

---

### 🏆 Compétences développées
| Matière | Compétence développée |
|---------|------------------------|
| Automatisme & Informatique industrielle | Organisation de projet, programmation microcontrôleur |
| Électronique & Systèmes embarqués | Schéma, routage, conception PCB |
| Mathématiques & Physique appliquée | Calculs dimensionnels, ajustements de mesures |
| Communication & PPP | Argumentation, justification technique |
