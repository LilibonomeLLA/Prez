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
    width: 45%; /* Chaque bloc prend un peu moins de la moitié de la largeur */
    background: #334155;
    padding: 15px;
  }
</style>

---
# 🍔 Test des images
💡 Rappel des commandes magiques de Marp pour la mise en page :

• Changer la taille : ![w:200px](img/image1.png) (pour fixer la largeur à 200 pixels).
• Mettre en arrière-plan : ![bg](img/decor.jpg) (l'image occupera toute la diapositive).
• Couper l'écran en deux : ![bg right](img/wallhaven-7jxelo.png) (l'image se place automatiquement sur la moitié droite de la slide, et votre texte reste à gauche).

---

# Mise en page en grille

<div id="content">
  <div class="box">Bloc 1 (Gauche haut)</div>
  <div class="box">Bloc 2 (Droite haut)</div>
  <div class="box">Bloc 3 (Gauche bas - car il n'y avait plus de place à droite !)</div>
</div>


