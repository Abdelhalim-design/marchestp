# 🚁 Portfolio SAE – Conception et Réalisation d’un Moteur de Drone

## 👋 Introduction

Cette SAÉ avait pour but de **concevoir, bobiner, modéliser et tester un moteur de drone** fonctionnant avec un stator bobiné et un rotor aimanté, tout en respectant une logique de fabrication artisanale et de validation expérimentale.

Projet réalisé en binôme avec **Clément Durand**, encadré par **M. Talierco**.

---

<div style="display: flex; gap: 40px; flex-wrap: wrap; justify-content: space-between;">

<!-- Objectifs pédagogiques -->
<div style="flex: 1; min-width: 300px;">
<h2>🎯 Objectifs pédagogiques</h2>

<table>
  <thead>
    <tr>
      <th>Compétence</th>
      <th>Description</th>
      <th>Apprentissage Critique</th>
    </tr>
  </thead>
  <tbody>
    <tr><td><strong>C1a</strong></td><td>Produire une analyse fonctionnelle</td><td>Identifier les écarts fabrication/théorie</td></tr>
    <tr><td><strong>C1b</strong></td><td>Réaliser un prototype</td><td>Bobinage, modélisation SolidWorks</td></tr>
    <tr><td><strong>C1c</strong></td><td>Documenter la fabrication</td><td>Estimations, relevés, modèles 3D</td></tr>
    <tr><td><strong>C2a</strong></td><td>Tester le fonctionnement</td><td>Test résistance, inductance, équilibrage</td></tr>
    <tr><td><strong>C2b</strong></td><td>Valider les performances</td><td>Vérification fréquence de coupure, phase</td></tr>
    <tr><td><strong>C2c</strong></td><td>Corriger un défaut</td><td>Résolution de problème sur brasage & déphasage</td></tr>
  </tbody>
</table>
</div>

<!-- Matières mobilisées -->
<div style="flex: 1; min-width: 300px;">
<h2>📚 Matières mobilisées</h2>

<table>
  <thead>
    <tr>
      <th>Matière</th>
      <th>Apport dans le projet</th>
    </tr>
  </thead>
  <tbody>
    <tr><td><strong>Électronique</strong></td><td>Bobinage, mesure résistance, inductance</td></tr>
    <tr><td><strong>CAO</strong></td><td>Modélisation 3D des pièces avec SolidWorks</td></tr>
    <tr><td><strong>Électricité</strong></td><td>Mesures sur oscilloscope, filtres RL</td></tr>
    <tr><td><strong>Physique appliquée</strong></td><td>Fréquence de coupure, modélisation</td></tr>
    <tr><td><strong>Méthodologie projet</strong></td><td>Planification, documentation, résolution de problèmes</td></tr>
    <tr><td><strong>Informatique / Simulation</strong></td><td>Simulation PWM avec PSIM</td></tr>
  </tbody>
</table>
</div>

</div>

---

## 🧩 Conception du moteur

### 🛠️ Modélisation 3D avec SolidWorks

🎓 Compétence : **C1b – Réaliser un prototype**  
🧠 Apprentissage critique : Reproduire avec précision les pièces du moteur selon les plans  
📚 Matières mobilisées : **CAO**, **Mécanique**

- Modélisation du **rotor**, du **stator**, et des pièces structurelles.
- Création de cotes exactes pour assurer **compatibilité et ajustement**.
- Assemblage global du moteur simulé dans SolidWorks.

| Mise en Plan Rotor | Mise en Plan Stator |
|--------------------|---------------------|
| ![Rotor](images/sae%20motorisation%20de%20drone/misen%20plan%20stator.png) | ![Stator](images/sae%20motorisation%20de%20drone/mise%20en%20plan%20statorpng.png) |

---

### 📐 Relevés mécaniques & ajustements

🎓 Compétence : **C1a – Analyse fonctionnelle**  
🧠 Apprentissage critique : Identifier les écarts entre conception et réalité  
📚 Matières mobilisées : **Physique appliquée**, **Fabrication**

- Comparaison entre dimensions **théoriques** issues de la CAO et **réelles** (après impression 3D).
- Identification d’écarts critiques sur les diamètres, cercles et supports d’aimants.
- Ajustements manuels réalisés (lime, repositionnements).

<div style="display: flex; gap: 40px; flex-wrap: wrap; justify-content: space-between;">

<!-- Tableau Rotor -->
<div style="flex: 1; min-width: 300px;">
<h3>🌀 Rotor – Valeurs théoriques vs réelles</h3>
<table>
<thead><tr><th>Caractéristique</th><th>Théorique</th><th>Pratique</th></tr></thead>
<tbody>
<tr><td>Épaisseur emplacement aimant</td><td>8 mm</td><td>7,5 mm</td></tr>
<tr><td>Épaisseur rotor</td><td>10 cm</td><td>10 cm</td></tr>
<tr><td>Support du rotor</td><td>10 mm</td><td>9,5 mm</td></tr>
<tr><td>Diamètre rotor</td><td>65 mm</td><td>64 mm</td></tr>
<tr><td>Trou central</td><td>—</td><td>15,1 mm</td></tr>
<tr><td>Distance cercle central → aimant</td><td>9,5 mm</td><td>—</td></tr>
<tr><td>Cercle intérieur (aimant)</td><td>3 mm</td><td>2,5 mm</td></tr>
<tr><td>Cercle central</td><td>6 mm</td><td>5,9 mm</td></tr>
</tbody>
</table>
</div>

<!-- Tableau Stator -->
<div style="flex: 1; min-width: 300px;">
<h3>⚙️ Stator – Valeurs théoriques vs réelles</h3>
<table>
<thead><tr><th>Caractéristique</th><th>Théorique</th><th>Pratique</th></tr></thead>
<tbody>
<tr><td>Épaisseur</td><td>10 mm</td><td>10 mm</td></tr>
<tr><td>Diamètre</td><td>84 mm</td><td>84 mm</td></tr>
<tr><td>Cercle central</td><td>7 mm</td><td>7 mm</td></tr>
<tr><td>Cercles sur pieds</td><td>3 mm</td><td>3 mm</td></tr>
<tr><td>Longueur pied stator</td><td>—</td><td>100 mm</td></tr>
<tr><td>Angle des spires</td><td>40°</td><td>40°</td></tr>
</tbody>
</table>
</div>
</div>

> 📝 *Les écarts proviennent de la tolérance d'impression 3D et de l’usinage manuel.*

---

### 🧲 Montage des aimants

🎓 Compétence : **C1b**  
🧠 Apprentissage critique : Respecter la polarité et assurer un bon équilibrage  
📚 Matières : **Électronique**, **Physique appliquée**

- Disposition en alternance Nord / Sud.
- Utilisation d’un aimant de référence pour les polarités.
- Outils spécifiques pour insérer et retirer sans dommage.

![Aimants](images/sae%20motorisation%20de%20drone/Aiment.png)

📌 Outils utilisés :

![Outillage](images/sae%20motorisation%20de%20drone/outillage.jpg)

> 🛠️ *Cette étape a nécessité de la minutie et de la rigueur manuelle pour éviter les erreurs de champ magnétique.*


---

## 🧮 Bobinage et Calculs Expérimentaux

### 🧵 Estimation de la longueur totale de fil

🎓 Compétence : **C1c – Documenter la fabrication**  
🧠 Apprentissage critique : Estimer, anticiper les besoins en matériaux  
📚 Matière : **Électronique**

- Objectif : estimer la longueur de fil nécessaire pour les bobines.
- Méthode : calcul du périmètre d'enroulement, nombre de tours, couches, et bobines.
- Résultat : **~12 mètres de fil** pour l’ensemble du moteur.

<details>
  <summary><strong>📐 Calcul estimatif de la longueur de fil (cliquer pour voir)</strong></summary>

  <p><strong>Formule utilisée :</strong> périmètre = 2 × π × rayon</p>

  <p><strong>Rayon moyen :</strong> 75 mm ÷ 2 = 37,5 mm</p>

  <ul>
    <li>Périmètre complet : 2 × π × 37,5 ≈ 235,62 mm</li>
    <li>Demi-périmètre (cas pratique) ≈ 117,81 mm</li>
    <li>Longueur additionnelle par couche : 24,24 + 21,06 + 12,51 + 21,06 = 78,87 mm</li>
    <li>Nombre de tours : 24</li>
    <li>Longueur d'une bobine : 117,81 + (78,87 × 24) ≈ 2010,68 mm</li>
    <li>Pour 6 bobines : 2010,68 × 6 = <strong>12 064 mm ≈ 12,06 m</strong></li>
  </ul>

</details>

> 📝 *Ce calcul a permis de mieux anticiper le besoin en fil avant bobinage réel.*

**Realisation du bobinage** 

![alt text](<images/sae motorisation de drone/bobinage.jpg>)

> cette etape a demander d'etre tres minutieux et concentrer pour eviter de faire des erreur dans le nombre de spire et donc avoir des ecart.
---

### 📏 Mesures réelles et vérifications

🎓 Compétences : **C2a – Tester**, **C2b – Valider**  
🧠 Apprentissage critique : Confronter résultats pratiques et attendus  
📚 Matières : **Électronique**, **Physique appliquée**

<details>
  <summary>📐 Autres calculs et résultats de mesures (cliquer pour voir)</summary>
  <div style="display: flex; gap: 30px; flex-wrap: wrap; align-items: flex-start; margin-top: 1em;">

    <!-- Colonne gauche -->
    <div style="flex: 1; min-width: 300px;">

      <h3>🔹 Calcul de l'inductance (filtre RL)</h3>
      <p>Formule : L = R / (2 × π × fc)</p>
      <p>Avec : R = 47 Ω, fc = 477 000 Hz</p>
      <p><strong>Résultat :</strong> L ≈ 15,7 µH</p>

      <h3>🔹 Résistance pratique mesurée</h3>
      <p>Mesure avec les fils : 0,42 Ω</p>
      <p>Fils seuls : 0,30 Ω</p>
      <p><strong>Résistance réelle :</strong> 0,12 Ω</p>

      <h3>🔹 Résistance pour LED</h3>
      <p>R = (3,7 - 1,7) / 0,005 = <strong>400 Ω</strong></p>
      <p>Valeur utilisée : <strong>470 Ω</strong></p>
    </div>

    <!-- Colonne droite -->
    <div style="flex: 1; min-width: 300px;">

      <h3>🔹 Déphasage entre phases (objectif : 120°)</h3>
      <p>Formule : Déphasage = (Δt × 360) / T</p>
      <p>Exemple : Δt = 8,7 ms ; T = 26 ms</p>
      <p><strong>Déphasage mesuré ≈ 120°</strong></p>

      <h3>🔹 Comparaison inductance : théorique vs mesurée</h3>
      <p><strong>Théorique :</strong> 7,98 µH</p>
      <ul>
        <li>L1 : 8,34 µH</li>
        <li>L2 : 7,50 µH</li>
        <li>L3 : 8,13 µH</li>
        <li>L4 : 7,57 µH</li>
        <li>L5 : 7,57 µH</li>
        <li>L6 : 7,57 µH</li>
      </ul>
      <p><strong>Conclusion :</strong> Écarts acceptables pour un montage manuel.</p>
    </div>

  </div>
</details>

---

> 🧪 *Ces résultats expérimentaux valident globalement la qualité du bobinage, avec quelques ajustements nécessaires pour optimiser les performances.*


## 🧩 Conception du moteur

### 🛠️ Modélisation 3D avec SolidWorks

Avant toute fabrication, j’ai commencé par **modéliser en 3D les pièces du moteur**. Cette étape permet d’avoir une vue globale du système, de détecter les problèmes d’assemblage et de préparer l’impression 3D.

🎓 **Compétence C1b – Réaliser un prototype**  
🧠 *Reproduire avec précision les pièces du moteur selon les plans*  
📚 **CAO, Mécanique**

![Rotor](images/sae%20motorisation%20de%20drone/misen%20plan%20stator.png)  
*Plan de la pièce du rotor modélisée sous SolidWorks*

![Stator](images/sae%20motorisation%20de%20drone/mise%20en%20plan%20statorpng.png)  
*Plan du stator, servant de base au bobinage*

---

### 📐 Relevés mécaniques & ajustements

Après impression 3D, j’ai effectué **des relevés réels et comparé aux plans CAO**. Cela m’a permis de voir si les pièces étaient conformes, et de comprendre les écarts de fabrication.

🎓 **Compétence C1a – Analyse fonctionnelle**  
🧠 *Identifier les écarts entre conception et réalité*  
📚 **Physique appliquée, Fabrication**

> 📝 *Cela m’a appris à anticiper les tolérances de fabrication et à ajuster mes choix en conséquence.*

---

### 🧲 Montage des aimants et bobinage

Une fois les pièces ajustées, j’ai procédé au **montage des aimants selon leur polarité** et au **bobinage du stator**. Ces deux étapes sont cruciales car elles conditionnent le bon fonctionnement magnétique et électrique du moteur.

🎓 **Compétence C1b**  
🧠 *Respecter les contraintes physiques et logiques d’un moteur réel*  
📚 **Électronique, Physique appliquée**

![Aimants](images/sae%20motorisation%20de%20drone/Aiment.png)  
*Montage des aimants avec respect des polarités*

![Outillage](images/sae%20motorisation%20de%20drone/outillage.jpg)  
*Outils utilisés pour le montage et la fixation des bobines*

> 📏 *Le bobinage m’a appris à travailler avec rigueur et méthode pour garantir l’équilibre des phases.*

---

## 🧮 Mesures expérimentales

### 🔌 Mesure de la résistance des bobines

Après le bobinage, j’ai mesuré la **résistance des bobines à l’aide d’un multimètre**. Cela permet de vérifier que les spires sont bien en contact et qu’il n’y a pas de court-circuit.

🎓 **Compétence C2a – Tester**  
🧠 *Valider la qualité du bobinage*  
📚 **Électronique, TP de mesures**

![Mesure résistance](images/sae%20motorisation%20de%20drone/test%20de%20continuiter.jpg)  
*Contrôle des bobines avec multimètre*

---

### 📈 Test de fréquence de coupure – filtre RL

J’ai ensuite utilisé un montage RL pour **déterminer la fréquence de coupure réelle** de ma bobine. L’objectif était de comparer le comportement théorique et pratique.





🎓 **Compétence C2b – Valider**  
🧠 *Comparer les valeurs pratiques et théoriques*  
📚 **Électricité, Physique appliquée**

Filtre passe bas  : *Test de fréquence de coupure sur circuit RL*

![alt text](<images/sae robot/sae motorisation de drone/filtre_passe_bas.jpg>)



| Bobine | Fréquence de coupure (kHz) | VS à fc (V) |
|--------|-----------------------------|-------------|
| L1     | 475                         | 0,71        |
| L2     | 485                         | 0,70        |
| L3     | 470                         | 0,71        |
| L4     | 480                         | 0,70        |
| L5     | 480                         | 0,71        |
| L6     | 478                         | 0,70        |




> 🎯 *J’ai appris ici à interpréter un signal mesuré sur oscilloscope et à en tirer des valeurs critiques.*

---

### 🔄 Déphasage & triphasé

Pour valider que le moteur fonctionne bien en triphasé, j’ai observé les **signaux des trois phases à l’oscilloscope**. Cela m’a permis de vérifier le déphasage entre U, V et W.

🎓 **Compétence C2b – Mesurer**  
🧠 *Analyser les signaux triphasés sur oscilloscope*  
📚 **Oscilloscope, Électricité**

| Mesure        | Déphasage Théorique (°) | Déphasage Mesuré (°) | Écart (°) |
|---------------|--------------------------|------------------------|-----------|
| Phase U → V   | 120                      | 118,5                  | -1,5      |
| Phase V → W   | 120                      | 121,2                  | +1,2      |
| Phase W → U   | 120                      | 120,3                  | +0,3      |


Visualisation a l'ossilloscope : 


![alt text](<images/sae robot/sae motorisation de drone/dephasage 120 degraos.png>)


---

### 💻 Simulation PSIM

Avant de mettre le moteur sous tension, j’ai simulé un **ondulateur PWM sous PSIM**. Cela m’a permis de prévoir le comportement de l’alimentation triphasée et d’identifier les erreurs possibles.

🎓 **Compétence C2c – Corriger**  
🧠 *Valider virtuellement avant mise en œuvre*  
📚 **Simulation, Informatique industrielle**



| Montage AOP                                                                                     | Visualisation des signaux                                                                 |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| ![Montage AOP](images/sae%20robot/sae%20motorisation%20de%20drone/IMG_0426.jpg)                 | ![Visualisation signaux](images/sae%20robot/sae%20motorisation%20de%20drone/aop%20champs.jpg) |




> 🧠 *Cette simulation m’a permis de corriger un signal déformé avant de le tester en vrai.*

---

### 🔧 Brasure finale et DB15

Dernière étape : connecter le moteur à l’alimentation via une **brasure fine sur un connecteur DB15**. Cet exercice m’a demandé beaucoup de précision en espace réduit.

![Brasure du db15](<images/sae robot/sae motorisation de drone/Brasure.jpg>)


🎓 **Compétence C2c – Corriger un défaut**  
🧠 *Travailler en espace contraint avec précision*  
📚 **Électronique, Méthodologie projet**

> 🔩 *J’ai appris à m’adapter aux contraintes physiques de montage et à garantir des connexions fiables.*

---

## ✅ Vérification finale

### 🔎 Montage en étoile validé

Pour finir, j’ai vérifié le **montage des bobines en étoile** et testé les continuités. Cela permet d’assurer que les phases sont bien reliées et équilibrées.

Utilisation du multimettre pour relever la continuiter : 

![alt text](<images/sae robot/sae motorisation de drone/test_continuiter.png>)


| Phase | Mesure  | Résultat | Interprétation       |
|-------|---------|----------|---------------------|
| U     | U1 – U2 | Bip      | OK                  |
| V     | V1 – V2 | Bip      | OK                  |
| W     | W1 – W2 | Bip      | OK                  |
| U-V   | U1 – V1 | Silence  | Pas de court-circuit|


Realisation du montage etoile : 


![Montage etoile](<images/sae robot/sae motorisation de drone/montage_etoile.png>)


🎓 **Compétence C2a – Vérification électrique**  
📚 **Méthodologie, TP Élen**

> ✔️ *Le moteur est prêt à être alimenté de manière sécurisée et stable.*

---

## 🧠 Bilan personnel

> Ce projet m’a permis de **concevoir, simuler, fabriquer et tester un moteur électrique fonctionnel**.  
> J’ai renforcé ma capacité à **travailler avec précision**, à **corriger mes erreurs** et à **mener un projet jusqu’à sa validation finale**.  
> La partie vérification m’a appris à analyser les signaux réels et à comprendre les écarts possibles entre simulation et expérimentation.

---
