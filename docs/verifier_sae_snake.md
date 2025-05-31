## 🔹 Compétence : Vérifier

### 🔸 Contexte
Une fois la conception terminée, il a fallu tester et valider le fonctionnement du projet pour garantir la conformité aux attentes et aux contraintes techniques du cahier des charges.

### 🔸 Activités réalisées

#### 🧪 Tests du PCB et du câblage
- Réalisation du test de continuité entre les composants après le brasage.
- Vérification de l’alimentation correcte de chaque composant.
- Correction des erreurs (ex. inversion de connecteurs) par débrasure et ressoudage.

**Apprentissage critique :**
- Savoir vérifier la conformité électrique et mécanique d’un circuit.
- Identifier et corriger les erreurs de brasage ou de câblage.

**Lien avec les matières :**
- **Physique appliquée** : tests de continuité, validation des circuits.
- **Électronique & Systèmes embarqués** : vérification du routage et du câblage.

---

#### 🖥️ Tests fonctionnels du jeu
- Vérification de l’affichage (écran rouge, test des formes et des briques).
- Tests des boutons poussoirs (déplacement du carré, réactivité des entrées).
- Test final du jeu Arkanoid avec les contrôles intégrés.

**Apprentissage critique :**
- Vérifier le respect des fonctionnalités définies dans le cahier des charges.
- Tester le code et ajuster la programmation en fonction des résultats.

**Lien avec les matières :**
- **Automatisme & Informatique industrielle** : tests fonctionnels, débogage du code.
- **Mathématiques** : validation des coordonnées et des mouvements du jeu.

---

#### 🧩 Intégration finale
- Assemblage du PCB et des composants dans le boîtier imprimé.
- Vérification de la bonne fixation mécanique et de la fermeture vissée.
- Tests d’utilisation complète (fonctionnement du jeu, commandes, alimentation).

**Apprentissage critique :**
- Importance de l’intégration mécanique et de l’ergonomie du produit fini.
- Validation finale de la conformité entre le prototype et les attentes.

**Lien avec les matières :**
- **Vie d’entreprise** : rigueur dans l’assemblage, respect des délais.
- **Communication & PPP** : présentation du produit final, démonstration orale.

---

### 🏆 Compétences développées
| Matière | Compétence développée |
|---------|------------------------|
| Physique appliquée | Validation des circuits électriques |
| Électronique & Systèmes embarqués | Tests de continuité, validation des fonctionnalités |
| Automatisme & Informatique industrielle | Tests fonctionnels, vérification du code |
| Communication & PPP | Présentation orale des résultats, argumentation technique |


### 🧪 Tests fonctionnels initiaux

#### 🔴 Premier test : affichage écran rouge



Objectif : Vérifier que l'écran est correctement câblé et fonctionnel.

🧱 Affichage de formes et briques
🧪 Test de dessin de briques

<pre><code class="language-c">
// Code pour afficher une image (brique) aléatoirement sur l'écran
void main(void) 
{
    while (1) {
        pos_x = rand() % (240-33);
        pos_y = rand() % (320-32);

    </code></pre>
        for (x = 0; x < 33<h2>Programmation de l'écran TFT</h2>



<p>Voici le premier test d'affichage d'un écran rouge :</p>


<pre><code class="language-c">
#include "mcc_generated_files/mcc.h"
#include "ILI9341.h"
#include "GFX_Library.h"
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;
#include &lt;time.h&gt;

void main(void)
{
    int n=0, button;
    time_t toc;
    SYSTEM_Initialize();
    SPI1_Open(SPI1_DEFAULT);
    tft_begin();
    time(&toc);
    srand((int)toc);
    fillScreen(ILI9341_RED);
    while(1) { }
}
</code></pre>

            for (y = 0; y < 32; y++) {
                drawPixel(x + pos_x, y + pos_y, (uint16_t)(TEST_IMAGE[x * 32 + y]));
            }
        }
    }
}

🎮 Mise en place des contrôles : Boutons poussoirs
Test du déplacement d’un carré avec boutons :


<h2>Test des boutons poussoirs</h2>
<p>Ce code permet de déplacer un carré à l'écran selon l'entrée des boutons configurés en numérique avec résistances pull-up.</p>

<pre><code class="language-c">
#include "mcc_generated_files/mcc.h"
#include "ILI9341.h"
#include "GFX_Library.h"

#define SQUARE_SIZE 10

uint16_t squareX = 100;
uint16_t squareY = 100;

void drawSquare(uint16_t x, uint16_t y, uint16_t color) {
    fillRect(x, y, SQUARE_SIZE, SQUARE_SIZE, color);
}

void main(void) {
    SYSTEM_Initialize();
    SPI1_Open(SPI1_DEFAULT);
    tft_begin();
    setRotation(1);
    fillScreen(ILI9341_BLACK);

    // Configuration des boutons
    BP_A_SetDigitalInput();
    BP_B_SetDigitalInput();
    BP_C_SetDigitalInput();
    BP_D_SetDigitalInput();
    BP_A_SetPullup();
    BP_B_SetPullup();
    BP_C_SetPullup();
    BP_D_SetPullup();

    drawSquare(squareX, squareY, ILI9341_WHITE);

    while (1) {
        drawSquare(squareX, squareY, ILI9341_BLACK);

        if (BP_A_GetValue() == 0 && squareY &gt; 0) {
            squareY -= 5;
        }
        if (BP_B_GetValue() == 0 && squareX &lt; 240 - SQUARE_SIZE) {
            squareX += 5;
        }
        if (BP_C_GetValue() == 0 && squareY &lt; 320 - SQUARE_SIZE) {
            squareY += 5;
        }
        if (BP_D_GetValue() == 0 && squareX &gt; 0) {
            squareX -= 5;
        }

        drawSquare(squareX, squareY, ILI9341_WHITE);
        __delay_ms(100);
    }
}
</code></pre>
 
l'Objectif etais de tester le fonctionnement des bouton a l'aide de code.


<h2>Intégration des boutons dans le jeu</h2>
<p>Ce code permet de déplacer le carré dans le jeu à l'aide des boutons, maintenant bien configurés.</p>

<pre><code class="language-c">
#include "mcc_generated_files/mcc.h"
#include "ILI9341.h"
#include "GFX_Library.h"

#define SQUARE_SIZE 10

uint16_t squareX = 100;
uint16_t squareY = 100;

void drawSquare(uint16_t x, uint16_t y, uint16_t color) {
    fillRect(x, y, SQUARE_SIZE, SQUARE_SIZE, color);
}

void main(void) {
    SYSTEM_Initialize();
    SPI1_Open(SPI1_DEFAULT);
    tft_begin();
    setRotation(1);
    fillScreen(ILI9341_BLACK);

    BP_A_SetDigitalInput();
    BP_B_SetDigitalInput();
    BP_C_SetDigitalInput();
    BP_D_SetDigitalInput();
    BP_A_SetPullup();
    BP_B_SetPullup();
    BP_C_SetPullup();
    BP_D_SetPullup();

    drawSquare(squareX, squareY, ILI9341_WHITE);

    while (1) {
        drawSquare(squareX, squareY, ILI9341_BLACK);

        if (BP_A_GetValue() == 0 && squareY &gt; 0) {
            squareY -= 5;
        }
        if (BP_B_GetValue() == 0 && squareX &lt; 240 - SQUARE_SIZE) {
            squareX += 5;
        }
        if (BP_C_GetValue() == 0 && squareY &lt; 320 - SQUARE_SIZE) {
            squareY += 5;
        }
        if (BP_D_GetValue() == 0 && squareX &gt; 0) {
            squareX -= 5;
        }

        drawSquare(squareX, squareY, ILI9341_WHITE);
        __delay_ms(100);
    }
}
</code></pre>


**Compétences développées :**

Conception électronique et mécanique (KiCad / SolidWorks)

Programmation microcontrôleur (PIC / MPLAB X)

Tests et validation (protocole de tests, débogage)