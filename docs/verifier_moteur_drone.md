## ✅ VÉRIFIER

### 🔌 Test des bobines – résistance  
🎓 Compétence : **C2a**  
🧠 Apprentissage critique : Mesurer et interpréter des résultats physiques.  
📚 Matières : **Électronique**, **Physique**

- Utilisation d’un multimètre pour mesurer :
  - Résistance fil test : **0,30 Ω**
  - Résistance bobine : **0,12–0,13 Ω**
- Contrôle qualité des bobines par validation ohmique.

📌 **Image à insérer** : Multimètre branché sur une bobine  
**Commentaire** : Confirme que le bobinage est homogène et exploitable pour la suite.

---

### 📈 Test fréquence de coupure – filtre RL  
🎓 Compétence : **C2b**  
🧠 Apprentissage critique : Déterminer une fréquence de coupure réelle.  
📚 Matières : **Électricité**, **Physique appliquée**

- Signal d’entrée : 1 V crête
- Fréquence à -3dB : **477 kHz**
- Comparaison des valeurs théoriques et mesurées

📌 **Image à insérer** : Oscilloscope affichant Vout = 0.707 Vin  
**Commentaire** : Valide que le filtre RL réalisé fonctionne conformément à la théorie.

---

### 🧪 Mesure inductance & déphasage  
🎓 Compétence : **C2a**, **C2b**  
🧠 Apprentissage critique : Analyser un comportement réel vs théorique  
📚 Matières : **Électricité**, **Électronique**

- Inductances mesurées proches des **8 μH** attendus.
- Test de **déphasage des phases** sur oscilloscope :
  - Résultat attendu : **120°**
  - Résultat mesuré : **~60°**, diagnostic engagé

📌 **Image à insérer** : Oscillogramme affichant 3 tensions déphasées  
**Commentaire** : Ce test permet de vérifier si les phases du moteur sont correctement alimentées pour assurer une rotation stable.

---

### 🧪 Simulation PWM (PSIM)  
🎓 Compétence : **C2c**  
🧠 Apprentissage critique : Identifier les écarts et simuler les corrections  
📚 Matière : **Informatique industrielle**, **Simulation**

- Simulation d’un **ondulateur** pour ajuster la **modulation de largeur d’impulsion (PWM)**
- Mesure du rapport cyclique
- Évaluation du comportement sous différents signaux d'entrée

📌 **Image à insérer** : Capture du montage PSIM avec sinus + PWM  
**Commentaire** : Permet de tester virtuellement les corrections avant mise en œuvre matérielle.

---

### 🔧 Brasure & fin de câblage stator  
🎓 Compétence : **C2c**  
🧠 Apprentissage critique : Corriger un problème de câblage en respectant les normes  
📚 Matières : **Méthodologie**, **Électronique**

- Brasure minutieuse de la **DB15** malgré espace réduit
- Tests sur fils plastiques avant soudure finale
- Solution apportée : souder un fil d'étain sur la bobine pour plus de précision

📌 **Image à insérer** : Photo du DB15 ou bobine brasée  
**Commentaire** : Illustre l'adaptabilité et la rigueur dans la phase finale de fabrication.

---

## 🎓 Bilan personnel

> Ce projet m’a permis de **développer une approche complète du prototypage d’un moteur électrique** : modélisation, fabrication, test et amélioration.  
> J’ai renforcé ma capacité à travailler **précisément**, à **analyser des écarts**, et à **résoudre des problèmes techniques**.  
> La phase de vérification, notamment les tests d’oscilloscope, m’a permis de mieux comprendre les effets physiques réels.

---

## 📎 Ressources utilisées

- **SolidWorks** – Modélisation CAO
- **Multimètre / Oscilloscope** – Tests bobines et signaux
- **PSIM** – Simulation PWM
- **Datasheets aimants & fils** – Spécifications matériaux