# 🎓 Portfolio - Abdelhalim Zouggagh   

Bienvenue sur mon portfolio !  
Vous y découvrirez mon parcours, mes compétences et mes projets réalisés en **Génie Électrique et Informatique Industrielle (GEII)**.  
 

## 🏅 À Propos de Moi  

🎓 <strong>Abdelhalim Zouggagh</strong>  
📍 <em>Étudiant en Génie Électrique et Informatique Industrielle (GEII) - IUT de Nîmes</em>  

<h2>📍 Localisation de mon IUT</h2>
<div id="map" style="width: 100%; height: 200px;"></div>

<!-- Ajout de Leaflet.js -->
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

<script>
  var map = L.map('map').setView([43.807772, 4.360149], 15);
  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '© OpenStreetMap contributors'
  }).addTo(map);

  L.marker([43.807772, 4.360149]).addTo(map)
    .bindPopup('📍 IUT de Nîmes - 8 Rue Jules Raimu')
    .openPopup();
</script>

🔹 **Parcours scolaire** :  
- 🎓 **Baccalauréat Général** (*Mathématiques & SES*)  
- 🏗️ **GEII - IUT de Nîmes** (*Projets en électronique, programmation, systèmes embarqués...*)  

🔹 **Compétences principales** :  
✅ Programmation (Python, C, HTML/CSS, Arduino)  
✅ Systèmes embarqués & électronique  
✅ Automatisme & réseaux industriels  


🔹 **Objectifs professionnels** :  
- 📡 Travailler dans le domaine des **systèmes embarqués et de l'électronique industrielle**  
- 🤖 Développer des solutions **d'automatisation et d’intelligence artificielle embarquée**  
- 🚀 Continuer mes études en **ingénierie ou recherche appliquée**  















<button id="dark-mode-toggle">🌙 Mode Sombre</button>

<script>
  document.getElementById("dark-mode-toggle").addEventListener("click", function () {
    document.body.classList.toggle("dark-mode");
  });
</script>

<style>
  .skills-container {
    max-width: 600px;
    margin: auto;
    padding: 20px;
    font-family: Arial, sans-serif;
  }

  .skills-container h2 {
    text-align: center;
    color: #007BFF; /* Bleu */
  }

  .skill {
    margin-bottom: 15px;
  }

  label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
    color: #0056b3;
  }

  progress {
    width: 100%;
    height: 20px;
    -webkit-appearance: none;
    appearance: none;
  }

  progress::-webkit-progress-bar {
    background-color: #e0e0e0;
    border-radius: 10px;
  }

  progress::-webkit-progress-value {
    background-color: #007BFF; /* Bleu */
    border-radius: 10px;
  }

  progress::-moz-progress-bar {
    background-color: #007BFF; /* Bleu pour Firefox */
    border-radius: 10px;
  }
</style>

<div class="skills-container">
  <h2>Mes Compétences</h2>

  <div class="skill">
    <label for="html">Code C</label>
    <progress id="html" value="90" max="100"></progress>
  </div>

  <div class="skill">
    <label for="css">Ladder</label>
    <progress id="css" value="85" max="100"></progress>
  </div>

  <div class="skill">
    <label for="js">Arduino</label>
    <progress id="js" value="75" max="100"></progress>
  </div>

  <div class="skill">
    <label for="python">Python</label>
    <progress id="python" value="80" max="100"></progress>
  </div>
</div>

<style>
    .skills-container {
        padding: 20px;
    }
    .skill {
        margin-bottom: 15px;
    }
    label {
        display: block;
        margin-bottom: 5px;
    }
    progress {
        width: 100%;
        height: 20px;
    }
</style>

## 🛠️ Logiciels Utilisés

| MPLAB X | Control Expert | WinRelais | Machine Expert |
|---------|----------------|-----------|----------------|
| [![MPLAB X](images/mplabx.png)](#mplabx) | [![Control Expert](images/controlexpert.png)](#controlexpert) | [![WinRelais](images/winrelais.png)](#winrelais) | [![Machine Expert](images/machineexpert.png)](#machineexpert) |

| SolidWorks | KiCad | TIA Portal | Arduino IDE |
|------------|-------|------------|--------------|
| <a href="#solidworks"><img src="images/solidworks-logo.jpg" alt="SolidWorks" width="100"/></a> | <a href="#kicad"><img src="images/image-kikad.jpg" alt="KiCad" width="100"/></a> | <a href="#tiaportal"><img src="images/tiaportal.png" alt="TIA Portal" width="100"/></a> | <a href="#arduino"><img src="images/arduino.png" alt="Arduino IDE" width="100"/></a>

