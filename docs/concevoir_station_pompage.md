# 💧 Portfolio SAE S1 – Station de Pompage Automatisée

## 👋 Introduction

Bienvenue dans mon portfolio portant sur la **SAE S1 : Station de Pompage Automatisée**, réalisée en BUT GEII à l’IUT de Nîmes, en binôme avec Clément Durand.

Ce projet consistait à **concevoir un système automatisé de gestion de niveau d’eau** avec deux pompes commandées par un automate, et à en assurer :
- La **programmation**
- La **mise en œuvre physique**
- Les **tests fonctionnels**
- Et les **améliorations de sécurité et de fiabilité**

Ce projet mobilise des compétences en **électrotechnique, automatisme, programmation et gestion de projet**.

![Station de pompage](<images/sae pompe/Station_de_pompe.png>)

---
<div style="display: flex; gap: 20px; justify-content: space-between;">

<div style="width: 49%;">

🎯 Objectifs pédagogiques

<table>
  <tr>
    <th>Compétence</th>
    <th>Description</th>
    <th>Apprentissage Critique</th>
  </tr>
  <tr>
    <td><b>C1a</b></td>
    <td>Analyser un système automatisé</td>
    <td>Identification rigoureuse des fonctions du système</td>
  </tr>
  <tr>
    <td><b>C1b</b></td>
    <td>Réaliser un prototype matériel et logiciel</td>
    <td>Construction de la platine et développement du programme</td>
  </tr>
  <tr>
    <td><b>C1c</b></td>
    <td>Rédiger un dossier technique</td>
    <td>Schémas, nomenclature, devis</td>
  </tr>
  <tr>
    <td><b>C2a</b></td>
    <td>Tester un système technique</td>
    <td>Tests unitaires et globaux</td>
  </tr>
  <tr>
    <td><b>C2b</b></td>
    <td>Vérifier la conformité au cahier des charges</td>
    <td>Validation fonctionnelle</td>
  </tr>
  <tr>
    <td><b>C2c</b></td>
    <td>Diagnostiquer un dysfonctionnement</td>
    <td>Dépannage et sécurisation</td>
  </tr>
</table>

</div>

<div style="width: 49%;">

 📚 Matières mobilisées

<table>
  <tr>
    <th>Matière</th>
    <th>Rôle dans le projet</th>
  </tr>
  <tr>
    <td><b>Électrotechnique</b></td>
    <td>Dimensionnement et sélection des composants</td>
  </tr>
  <tr>
    <td><b>Automatisme</b></td>
    <td>Conception du GRAFCET, logique séquentielle</td>
  </tr>
  <tr>
    <td><b>CAO (WinRelais)</b></td>
    <td>Réalisation des schémas électriques</td>
  </tr>
  <tr>
    <td><b>Informatique industrielle</b></td>
    <td>Programmation Ladder sous Machine Expert</td>
  </tr>
  <tr>
    <td><b>PPP</b></td>
    <td>Organisation du travail et gestion des ressources</td>
  </tr>
  <tr>
    <td><b>Sécurité électrique</b></td>
    <td>Ajout de dispositifs de protection (relais, arrêt urgence)</td>
  </tr>
</table>

</div>

</div>

---

## 🧩 CONCEVOIR

### 🔍 Analyse fonctionnelle (C1a)

Avant de concevoir le GRAFCET, il était essentiel d’**apprendre à se connecter à l’automate** pour ne pas risquer de le bloquer, ni perturber les autres utilisateurs.

---

### ⚙️ 🔌 Procédure de connexion à l’automate (développée)

#### 🛠 Étapes suivies :

![alt text](<images/sae pompe/_- visual selection.png>)
---

#### 🖼 Visuels associés :

| Automate utilisé | Configuration Machine Expert |
|------------------|------------------------------|
| ![Automate](<images/sae pompe/automate utiliser.png>) | ![Config réseau](<images/sae pompe/config_machin_expertpng.png>) |

---

### 🔄 GRAFCET final du projet

![GRAFCET final](<images/sae pompe/GTAFCET_FINAL.png>)

Ce GRAFCET reflète l'enchaînement logique des actions du système (niveau haut, alternance, arrêt d'urgence…).

---

### ⚙️ Réalisation Ladder

![Ladder](<images/sae pompe/Ladder.png>)

💬 **Commentaire** : Le Ladder permet d’implémenter directement le GRAFCET dans l'automate selon une logique séquentielle claire.

🎓 **Compétence mobilisée** : C1a  
🧠 **Apprentissage critique** : Respect des transitions, états et priorités logiques selon le cahier des charges.  
📚 **Matière liée** : Automatisme

---

### 🧮 Choix des composants (C1b)

Une fois l’analyse fonctionnelle réalisée, nous avons procédé au **choix des composants** nécessaires à la mise en œuvre physique de la station de pompage. Ce choix s’est appuyé sur des **calculs techniques** et sur la **consultation de datasheets**.

---

#### 🔢 Calculs techniques réalisés :

- Calcul de la **Hauteur Manométrique Totale (HMT)**
- Estimation des **pertes de charge** dans le circuit
- Détermination de la **puissance nécessaire au moteur**
- Vérification des **intensités admissibles** des composants

| 🔬 Calculs techniques | 📐 Critères de choix d’un moteur |
|----------------------|----------------------------------|
| ![Calculs](<images/sae pompe/calcul technique.png>) | ![Moteur](<images/sae pompe/moteur.png>) |

Ces calculs nous ont permis de sélectionner un **moteur adapté** à notre application (pompage d’eau) en fonction de la hauteur de relevage, du débit souhaité et du rendement.

---

#### 🧩 Critères de sélection des composants

Les composants ont été choisis pour répondre aux exigences techniques, de sécurité et de compatibilité avec l’automate Schneider M221.

| Composant                  | Illustration |
|---------------------------|--------------|
| 🔌 **Contacteur**          | ![Contacteur](<images/sae pompe/contacteur.png>) |
| ⚡ **Disjoncteur**         | ![Disjoncteur](<images/sae pompe/disjoncteur.png>) |
| 🔧 **Sectionneur**         | ![Sectionneur](<images/sae pompe/Interupteur sectioneur.png>) |


---

### 📚 Lien avec les matières

- **Physique appliquée** : calculs d’intensité, puissance, pertes de charge, loi d’Ohm, compatibilité entre composants.
- **Énergie** : choix des composants de protection (disjoncteurs, relais thermiques), respect des normes et sécurité.

---

### 🎯 Lien avec la compétence C1b – Concevoir

> _"Réaliser un prototype matériel et logiciel"_

✔️ J’ai appliqué une **démarche rigoureuse de sélection technique** en partant des **calculs** jusqu’aux **données constructeurs**, en veillant à la cohérence du système.

🧠 **Apprentissage critique** :  
> J’ai appris à croiser les résultats techniques avec les documents fabricants pour garantir **fiabilité, sécurité et conformité** de l’installation.

### 💵 Devis détaillé du projet

![Devis](<images/sae pompe/DEVIS.png>)

💬 **Commentaire** : Ce tableau montre la capacité à anticiper les coûts, vérifier les disponibilités et justifier chaque dépense.

🎓 **Compétence mobilisée** : C1b  
🧠 **Apprentissage critique** : Démarche de conception réaliste et orientée contraintes techniques.  
📚 **Matière liée** : Électrotechnique, Excel, Physique appliquée

---

### 📐 CAO et documentation technique (C1c)
| Élément             | Illustration                                |
|---------------------|--------------------------------------------|
| **Schéma de commande** |  ![alt text](<images/sae pompe/schema de comande.png>) |
| **Schéma de puissance** | ![Schéma de puissance](<images/sae pompe/schema de puissance.png>) |

💬 **Commentaire** : Ces schémas permettent de visualiser clairement la logique de commande et le circuit de puissance, essentiels pour la conception et la réalisation du système automatisé.

🎓 **Compétence mobilisée** : C1c – Rédiger un dossier technique  

🧠 **Apprentissage critique** : Respect rigoureux des normes de schématisation industrielle, garantissant la compréhension par tous les intervenants techniques et facilitant la maintenance future.

📚 **Matières liées** : CAO, Énergie, Physique appliquée, Automatisme

#### 📄 Nomenclature

![alt text](<images/sae pompe/nomenclature.jpg>)

💬 **Commentaire** : Elle permet de suivre les références, gérer le stock, et préparer l’assemblage.

🎓 **Compétence mobilisée** : C1c  
🧠 **Apprentissage critique** : Conformité avec les normes de schématisation industrielle.  
📚 **Matière liée** : CAO, Énergie, Automatisme
