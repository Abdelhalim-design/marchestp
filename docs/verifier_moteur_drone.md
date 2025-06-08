# ✅ VÉRIFICATION FINALE DU MOTEUR

## 🔌 Test des bobines – Résistance

🎓 **Compétence : C2a**  
🧠 *Apprentissage critique* : Mesurer et interpréter des résultats physiques  
📚 *Matières* : Électronique, Physique

- **Multimètre utilisé** pour mesurer :
  - Résistance des fils test : **0,30 Ω**
  - Résistance des bobines : **0,12 – 0,13 Ω**
- Contrôle qualité par validation ohmique

### 🔍 Premier test de continuité (avant assemblage)

> Multimètre branché sur chaque bobine

![Test de continuité](images/sae%20robot/sae%20motorisation%20de%20drone/test%20de%20continuiter.jpg)

| Bobine | Résistance mesurée | Résistance fil test | Résistance réelle |
|--------|---------------------|----------------------|--------------------|
| B1     | 0,42 Ω              | 0,30 Ω               | 0,12 Ω             |
| B2     | 0,43 Ω              | 0,30 Ω               | 0,13 Ω             |
| B3     | 0,41 Ω              | 0,30 Ω               | 0,11 Ω             |
| B4     | 0,42 Ω              | 0,30 Ω               | 0,12 Ω             |
| B5     | 0,43 Ω              | 0,30 Ω               | 0,13 Ω             |
| B6     | 0,42 Ω              | 0,30 Ω               | 0,12 Ω             |

---

### 🔍 Deuxième test de continuité (après assemblage)

![Test de continuité assemblé](images/sae%20robot/sae%20motorisation%20de%20drone/test_continuiter.png)

| Test réalisé         | Points de mesure | Résultat     | Interprétation        | Statut    |
|----------------------|------------------|--------------|------------------------|-----------|
| Continuité phase U   | U1 – U2          | Bip continu  | Bobinage intact        | ✅ Conforme  |
| Continuité phase V   | V1 – V2          | Bip continu  | Bobinage intact        | ✅ Conforme  |
| Continuité phase W   | W1 – W2          | Bip continu  | Bobinage intact        | ✅ Conforme  |
| Isolation U-V        | U1 – V1          | Silence      | Pas de court-circuit   | ✅ Conforme  |
| Isolation V-W        | V1 – W1          | Silence      | Pas de court-circuit   | ✅ Conforme  |
| Isolation U-W        | U1 – W1          | Silence      | Pas de court-circuit   | ✅ Conforme  |

📝 **Commentaire** :  
Tests concluants – les bobinages sont homogènes et utilisables.

---

## 📉 Test de fréquence de coupure – Filtre RL

🎓 **Compétence : C2b**  
🧠 *Apprentissage critique* : Déterminer la fréquence de coupure réelle  
📚 *Domaines* : Électricité, Physique appliquée

⚠️ **Erreur initiale** : Filtre **passe-haut** au lieu de **passe-bas**.

![Erreur filtre](images/sae%20robot/sae%20motorisation%20de%20drone/Circuit%20Rl.png)

### ⚙️ Paramètres de test

- Signal d’entrée : **1,0 V crête**
- Critère de coupure : \( V_{\text{out}} = 0{,}707 \times V_{\text{in}} \)
- Fréquence mesurée : **477 kHz** (après correction du montage)

📸 *Image à insérer* : Affichage de l’oscilloscope

📝 **Commentaire** :  
La courbe observée confirme une atténuation de 3 dB à 477 kHz. Résultat conforme à la théorie avec **R = 23,5 Ω** et **L estimée ≈ 7,8 μH**.

---

## 🧪 Mesure de l’inductance & du déphasage

🎓 **Compétences : C2a, C2b**  
🧠 *Apprentissage critique* : Comparaison réel vs théorique  
📚 *Domaines* : Électricité, Électronique

### ⚠️ Montage incorrect corrigé

- Filtre passe-haut remplacé par filtre passe-bas
- Inductance calculée après correction

📷 *Machine de mesure utilisée* :  
![LCR-mètre](images/sae%20robot/sae%20motorisation%20de%20drone/machine%20Induction.jpg)

| Bobine | Inductance Théorique (µH) | Inductance Mesurée (µH) | Écart (%) |
|--------|----------------------------|---------------------------|-----------|
| L1     | 7,8                        | 8,3                       | +6,4      |
| L2     | 7,8                        | 7,5                       | -3,8      |
| L3     | 7,8                        | 8,1                       | +3,8      |
| L4     | 7,8                        | 7,6                       | -2,6      |
| L5     | 7,8                        | 7,6                       | -2,6      |
| L6     | 7,8                        | 7,6                       | -2,6      |

---

### 🔄 Analyse du déphasage triphasé

🎯 Objectif : Vérifier **120° de déphasage**

![Déphasage mesuré](images/sae%20robot/sae%20motorisation%20de%20drone/dephasage%20120%20degraos.png)

| Mesure        | Théorique (°) | Mesuré (°) | Écart (°) |
|---------------|----------------|------------|-----------|
| Phase U → V   | 120            | 118,5      | -1,5      |
| Phase V → W   | 120            | 121,2      | +1,2      |
| Phase W → U   | 120            | 120,3      | +0,3      |

📝 **Commentaire** :  
Mesures corrigées conformes. Fonctionnement triphasé validé.

---

## 💻 Simulation PSIM – PWM

🎓 **Compétence : C2c**  
🧠 *Apprentissage critique* : Anticiper erreurs via simulation  
📚 *Matière* : Informatique industrielle, Simulation

- Ondulateur simulé sous PSIM
- Étude du rapport cyclique
- Analyse des signaux d'entrée/sortie

![Montage PSIM](images/sae%20motorisation%20de%20drone/IMG_0426.jpg)  
![Signaux PSIM](images/sae%20motorisation%20de%20drone/aop%20champs.jpg)

📝 **Commentaire** :  
Simulation utile pour corriger un signal déformé **avant** tests réels.

---

## 🔧 Brasure & câblage final

🎓 **Compétence : C2c**  
🧠 *Apprentissage critique* : S’adapter à un environnement contraint  
📚 *Méthodologie*, *Électronique*

- Brasure sur connecteur **DB15**
- Espace restreint : fil d’étain utilisé pour précision

![Brasure](images/sae%20robot/sae%20motorisation%20de%20drone/Disfonctionnement_brasage.png)

📝 **Commentaire** :  
Exercice de précision important en phase finale.

---

## ✅ Vérification finale – Montage étoile

- Test de continuité avec multimètre

![Test final](images/sae%20robot/sae%20motorisation%20de%20drone/test_continuiter.png)

| Phase | Points mesurés | Résultat | Interprétation         |
|-------|-----------------|----------|------------------------|
| U     | U1 – U2         | Bip      | OK                     |
| V     | V1 – V2         | Bip      | OK                     |
| W     | W1 – W2         | Bip      | OK                     |
| U-V   | U1 – V1         | Silence  | Pas de court-circuit   |

![Montage étoile](images/sae%20robot/sae%20motorisation%20de%20drone/montage_etoile.png)

🎓 **Compétence : C2a – Vérification électrique**  
📚 *Méthodologie*, *TP Électronique*

✔️ *Moteur prêt à l’alimentation sécurisée.*

---

## 🎓 Bilan personnel

> Ce projet m’a permis de développer une approche complète du **prototypage moteur** : modélisation, fabrication, test et amélioration.  
> J’ai renforcé ma capacité à travailler avec **précision**, à analyser les écarts, et à résoudre des **problèmes techniques réels**.

---

## 📎 Ressources utilisées

- **SolidWorks** – Modélisation CAO  
- **Multimètre / Oscilloscope** – Tests et mesures  
- **PSIM** – Simulation PWM  
- **Datasheets aimants & fils** – Caractéristiques techniques  

