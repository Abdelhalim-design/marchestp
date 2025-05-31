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
