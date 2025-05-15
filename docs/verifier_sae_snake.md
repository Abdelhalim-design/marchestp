## 🔹 Compétence : Vérifier

### 🔌 Câblage et premiers tests

**Étapes réalisées :**
- Câblage entre le PIC16F18877 et l’écran TFT basé sur la datasheet.
- Test de base pour vérifier l'affichage de l’écran.

📷 Exemple de câblage :
> (À insérer : image câblage et datasheet)

---

### 🧪 Tests fonctionnels initiaux

#### 🔴 Premier test : affichage écran rouge



Objectif : Vérifier que l'écran est correctement câblé et fonctionnel.

🧱 Affichage de formes et briques
🧪 Test de dessin de briques

// Code pour afficher une image (brique) aléatoirement sur l'écran
void main(void) 
{
    while (1) {
        pos_x = rand() % (240-33);
        pos_y = rand() % (320-32);
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