# 🔍 SAE S1 – Robot Suiveur de Ligne : Partie VÉRIFIER

## 🎯 Objectif de cette page

Cette page décrit toutes les actions de **vérification, test, correction et amélioration** réalisées sur le robot HC-LineBoT. Elle correspond à la validation de la **compétence C2** du BUT GEII.

---

## 🧪 Tests matériels après soudure

Une fois la carte fabriquée, nous avons réalisé une série de vérifications :
![alt text](<images/sae robot/test_tableau.png>)

- **Tests de continuité et tension** avec un multimètre

- Contrôle de la polarité des LEDs, de la tension d’alimentation
- Vérification de la présence de court-circuit

> 🔧 Nous avons détecté un **court-circuit causé par une soudure trop épaisse**, et l’avons corrigé manuellement.

![alt text](<images/sae robot/soudure_lier.png>)

🎓 **Compétence C2a :** Identifier un dysfonctionnement  
📚 **Matières :** Électronique, Physique appliquée

---

## ⚠️ Diagnostic de pannes spécifiques

Plusieurs problèmes ont été identifiés :

- **Potentiomètre mal choisi** (20kΩ au lieu de 10kΩ)
- **Capteur IR trop haut** : ne détectait pas la ligne
- Résistance mal dimensionnée → LEDs trop faibles

![alt text](<images/sae robot/probleme_capteur.jpg>)

Chaque défaut a été corrigé avec un raisonnement basé sur les mesures et les données techniques.

🎓 **Compétence C2c :** Corriger une solution technique  
📚 **Matières :** Mathématiques, Physique, Anglais technique (datasheets)

---

## 🧠 Vérification du programme embarqué

En testant le robot :

- Les capteurs IR étaient mal calibrés → mauvaise détection
- Les LEDs ne réagissaient pas correctement
- Le robot tournait trop au lieu de 360°

Nous avons modifié les seuils, ajusté les temporisations, et corrigé les routines.

🎓 **Compétence C2b :** Tester une solution logicielle  
📚 **Matières :** Informatique, Automatisme

---

## 🚀 Optimisation des performances

Nous avons mesuré et comparé plusieurs essais :

- Ajustement de l’écartement entre capteurs : **1,8 cm** (égale à la largeur de ligne)
- Réduction de l’oscillation du robot
- Calibration précise du temps de rotation pour obtenir un **360° fluide**

🎓 **Compétence C2b / C2c** : Vérifier la conformité et ajuster les performances  
📚 **Matières :** Mathématiques, Informatique, Automatisme

---

## ✅ Résultats obtenus

| Critère | Résultat |
|--------|----------|
| Temps de course | ✅ 13,62 secondes |
| Bonus 360° | ✅ Réalisé avec précision |
| Stabilité du robot | ✅ Trajectoire fluide |
| Objectifs du cahier des charges | ✅ Tous atteints |

---
