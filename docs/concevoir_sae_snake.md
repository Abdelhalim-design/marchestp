# 📚 Portfolio SAE Arkanoid – BUT GEII 1ère Année

## 🔹 Compétence : Concevoir

### 🔸 Contexte
Initialement, notre projet consistait à réaliser une borne d’arcade miniature, mais après analyse des contraintes (transport, esthétique et complexité), nous avons pivoté vers une console portable inspirée de la Game Boy.

### 🔸 Activités réalisées

#### 📋 Cahier des charges et planification
- Analyse des besoins réels et adaptation du projet : abandon de la borne d’arcade pour une console portable.
- Rédaction d’un cahier des charges incluant les composants (PIC16F18877, écran TFT), contraintes techniques (taille, budget) et moyens disponibles à l’IUT.
- Utilisation d’un **diagramme de Gantt** pour organiser les tâches et planifier le projet.

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

**Apprentissage critique :**
- Adapter la conception au fur et à mesure des tests et impressions.
- Utiliser les itérations d’impression 3D pour corriger les défauts.

**Lien avec les matières :**
- **Électronique & Systèmes embarqués** : intégration mécanique du PCB.
- **Mathématiques & Physique appliquée** : calculs de dimensions, utilisation du pied à coulisse.

---

#### 🧩 Conception électronique (KiCad)
- Réalisation du schéma électrique complet de la carte son.
- Création des fichiers Gerber et validation auprès du constructeur.
- Résolution d’erreurs de routage (erreurs de fils, problèmes de perçage).

**Apprentissage critique :**
- Comprendre la chaîne de conception et de validation d’un PCB.
- Apprendre à gérer les erreurs et les contraintes du fabricant.

**Lien avec les matières :**
- **Électronique & Systèmes embarqués** : schéma électrique, routage, validation des fichiers Gerber.
- **Automatisme & Informatique industrielle** : interactions entre le PCB et le microcontrôleur.

---

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
