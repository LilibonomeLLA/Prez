---
marp: true
theme: gaia
title: 📊 Présentation de LLA
paginate: true
---
A tester dans le marp :
theme: uncover
_class: lead
paginate: false
backgroundColor: #1e293b
color: #f8fafc

# 🐯 Titre
Contenu...

---
# 🍔 Test des images
💡 Rappel des commandes magiques de Marp pour la mise en page :

• Changer la taille : ![w:50px](img/image1.png) (pour fixer la largeur à 200 pixels).
---
---
# Image en arrière plan
![bg](img/wallhaven-7jxelo.png) 
---
---
# Découpage de l'ecran en deux ?
• Couper l'écran en deux : ![bg right](img/1790360591299.jpeg) (l'image se place automatiquement sur la moitié droite de la slide)
* Image à droite :
![bg left](img/1790779337907.gif)

---

# Mise en page en grille

<div id="content">
  <div class="box">Bloc 1 (Gauche haut)</div>
  <div class="box">Bloc 2 (Droite haut)</div>
  <div class="box">Bloc 3 (Gauche bas)</div>
  <div class="box">Bloc 4 (Droite bas)</div>
</div>

<!-- Tout le CSS est masqué à la fin du document -->
<style>
@import url('https://googleapis.com');
section { font-family: 'Roboto'; font-size: 28px !important; }
h1, h2 { font-family: 'Oswald'; }
#content {
  display: flex;
  flex-wrap: wrap;
  gap: 20px; /* Ajoute un espace entre les blocs */
}

.box {
  box-sizing: border-box; /* Évite que le padding n'agrandisse le bloc */
  width: calc(50% - 10px); /* Ajustement précis avec le gap pour deux colonnes parfaites */
  background: #334155; /* Fond ardoise sombre */
  padding: 20px;
  border-radius: 8px; /* Optionnel : adoucit les angles des blocs */
  
  /* --- AMÉLIORATION DE LA LISIBILITÉ --- */
  color: #f8fafc; /* Force le texte principal en blanc épuré */
}

/* Optionnel : Si vous avez des titres ou des liens dans vos blocs */
.box h1, .box h2, .box h3 {
  color: #ffffff; /* Blanc pur pour les titres */
  margin-top: 0; /* Aligne le titre en haut du bloc */
}

.box a {
  color: #38bdf8; /* Bleu ciel lumineux pour que les liens restent visibles */
}

/* --- OPTIMISATION MOBILE (Responsive) --- */
@media (max-width: 768px) {
  .box {
    width: 100%; /* Sur mobile, les blocs passent les uns sous les autres */
  }
}
</style>
