---
marp: true
title: Test Tailwind CSS
paginate: true
style: |
  @import url('https://unpkg.com/tailwindcss@^2/dist/utilities.min.css');
  
  /* Astuce : Forcer Marp à respecter la taille de texte de Tailwind */
  section p, section div, section h1, section h2, section h3 {
    font-size: inherit;
  }
---

# 🚀 Démonstration Tailwind & Marp

Voici une grille native en Tailwind CSS :

<div class="grid grid-cols-2 gap-6 mt-8">
  
  <!-- Correction ici : 'coolGray' au lieu de 'slate' pour la version 2 -->
  <div class="bg-coolGray-700 p-6 rounded-lg text-white shadow-lg">
    <h3 class="text-xl font-bold text-blue-400 mb-2">Bloc Gauche</h3>
    <p class="text-sm text-coolGray-300">Ce bloc utilise désormais une couleur de fond reconnue, le texte blanc devient donc parfaitement visible !</p>
  </div>

  <div class="bg-indigo-900 p-6 rounded-lg text-white shadow-lg">
    <h3 class="text-xl font-bold text-pink-400 mb-2">Bloc Droite</h3>
    <p class="text-sm text-indigo-200">Les couleurs s'appliquent immédiatement sans avoir besoin d'écrire une seule ligne de CSS classique.</p>
  </div>

</div>

---

# 🎨 Autres tests graphiques

🎯 Un texte <span class="text-red-500 font-extrabold uppercase">rouge, en gras et en majuscules</span>.
🎯 Un badge stylisé : <span class="bg-green-100 text-green-800 text-xs font-semibold px-2.5 py-0.5 rounded-full">Validé</span>

<div class="flex justify-around items-center h-32 mt-6 bg-gray-100 rounded">
  <div class="w-12 h-12 bg-blue-500 animate-pulse rounded-full"></div>
  <div class="w-12 h-12 bg-amber-500 animate-bounce rounded"></div>
</div>
