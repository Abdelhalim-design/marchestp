# 🎓 Portfolio - Abdelhalim Zouggagh   

Bienvenue sur mon portfolio !  
Vous y découvrirez mon parcours, mes compétences et mes projets réalisés en **Génie Électrique et Informatique Industrielle (GEII)**.  
 

## 🏅 À Propos de Moi  

🎓 **Abdelhalim Zouggagh**  
📍 *Étudiant en Génie Électrique et Informatique Industrielle (GEII) - IUT de Nîmes*  

<h2>📍 Localisation de mon IUT</h2>
<div id="map" style="width: 100%; height: 200px;"></div>

<!-- Ajout de Leaflet.js -->
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

<script>
  var map = L.map('map').setView([43.836209871068535, 4.351685276710129], 15);
  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '© OpenStreetMap contributors'
  }).addTo(map);

  L.marker([43.836209871068535, 4.351685276710129]).addTo(map)
    .bindPopup('📍 IUT de Nîmes')
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



<div class="skills-container">
    <h2>Mes Compétences</h2>
    <div class="skill">
        <label for="html">HTML</label>
        <progress id="html" value="90" max="100"></progress>
    </div>
    <div class="skill">
        <label for="css">CSS</label>
        <progress id="css" value="85" max="100"></progress>
    </div>
    <div class="skill">
        <label for="js">JavaScript</label>
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

