# ✅ COMPÉTENCE C2 – VÉRIFIER

## 🔹 C2a – Vérifier le fonctionnement d’un système automatisé

Cette compétence consiste à **valider le bon fonctionnement d’un système réel** à l’aide d’outils de mesure, de tests, et de protocoles structurés.

---

### 🧪 Mise en situation

Après avoir terminé le câblage et la programmation de la station de pompage, j'ai effectué des **tests fonctionnels** pour vérifier que le comportement du système correspondait au GRAFCET prévu.

| 📸 Photo de la platine                        | ✅ Tests réalisés                                                                                     |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
|![alt text](<images/sae pompe/La_PLATINE_legende.png>) | ![alt text](<images/sae pompe/sequence_de_test.png>) |  
- **Vérification des tensions** avec multimètre *(24V DC aux bornes du transformateur)*  
- **Contrôle des capteurs TOR** simulant les niveaux d’eau  
- **Alternance automatique des pompes** selon la logique du programme  
- **Test d'arrêt d'urgence** via bouton poussoir  
- **Identification et correction d’un court-circuit** (fil mal dénudé) |

---

### 🧰 Automate utilisé

![alt text](<images/sae pompe/automate utiliser.png>)

Utilisation d’un **automate programmable industriel (API)** pour exécuter et valider la séquence automatisée.

---

### 🧩 Lien avec la compétence C2a

Chaque test visait à **valider le fonctionnement réel du système par rapport aux attentes**. Cela fait pleinement partie de la compétence :

- Vérification de **l'alimentation et des tensions**
- Validation des **entrées/sorties (capteurs, actionneurs)**
- **Comparaison entre comportement attendu et comportement observé**

---

### 📚 Lien avec les matières

- **Physique appliquée** : mesure des tensions, alimentation du circuit
- **Électronique** : détection et résolution de court-circuits
- **Automatisme** : exécution de scénarios définis dans le GRAFCET

---

## 🔹 C2b – Mettre en œuvre une stratégie d’amélioration

Cette compétence vise à **proposer et intégrer des améliorations concrètes** pour rendre le système plus fiable, plus sûr ou plus performant.

---

### 🔧 Améliorations apportées

| ⚙️ Élément modifié | 🖼️ Illustration | 📌 Objectif |
|--------------------|------------------|-------------|
| Commutateur 3 positions | ![Commutateur](<images/sae pompe/Photoaveclecomu.png>) | Ajout d’un **mode test / arrêt / automatique** |
| Capteur de niveau d'eau | ![Capteur](<images/sae pompe/ameloiratio avec le capteur.png>) | **Sécurité anti-débordement** physique |
| Alternance des pompes | ![alt text](<images/sae pompe/alternace_des_pompes.png>)| Évite l’usure prématurée d’une pompe |
| Voyant lumineux | ![alt text](<images/sae pompe/ajout_du voyant.png>)| **Diagnostic visuel** immédiat |
| Relais de surveillance de phase | ![Relais](<images/sae pompe/Bilan_amelioration.png>) | Protection contre **inversion de phase** |
| Analyse de datasheet relais | ![Datasheet](<images/sae pompe/datasheet.png>) | Compréhension technique du composant |

---

### 📘 Lien avec la compétence C2b

Ces modifications relèvent directement de la compétence C2b car elles :

- **Améliorent la sécurité** (voyant, capteur, relais)
- **Optimisent la durabilité** (alternance des pompes)
- **Facilitent la maintenance** (commutateur, visualisation)

Elles ont été validées par :
- la **mise à jour du programme automate**
- des **tests fonctionnels complémentaires**
- des **ajustements du câblage**

---

### 🛠️ Partie programmation (Ladder)

| Fonction Ladder                           | Capture |
|------------------------------------------|---------|
| Maintenance des pompes                   | ![alt text](<images/sae pompe/Ladder.png>) |
| Programmation du relais                  | ![alt text](<images/sae pompe/Programtion_relais.png>) |
| Gestion du capteur                       | ![Capteur](<images/sae pompe/Program_du_capteur.png>) |
| Alternance pompe / mode manuel           | ![Pompe](<images/sae pompe/Maintenant_Pompe.png>) |

---
![alt text](<images/sae pompe/Maintenant_Pompe.png>)
### 📚 Lien avec les matières

- **Automatisme** : adaptation du GRAFCET et du programme
- **Électronique** : choix et intégration des composants (capteur, relais, voyant…)
- **Informatique industrielle** : reprogrammation via **Machine Expert**

---

### 🧠 Synthèse – Partie "Vérifier"

Cette activité m’a permis de :

- **Valider le fonctionnement réel** d’un système automatisé
- **Appliquer une logique de test industrielle**
- **Mettre en œuvre des améliorations ciblées**
- **Travailler de manière interdisciplinaire** (électronique, automatisme, programmation)

> ✅ Ces compétences sont essentielles dans les métiers liés à la maintenance, au développement et à l’optimisation des systèmes industriels automatisés.
