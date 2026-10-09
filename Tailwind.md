---
marp: true
title: Test Tailwind CSS
paginate: true
style: |
  /* Ajout de Tailwind */
  @import url('https://unpkg.com/tailwindcss@^2/dist/utilities.min.css');
  /* Ajout de Bootstrap-icons */
  @import url('https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css');
  
  /* Astuce : Forcer Marp à respecter la taille de texte de Tailwind */
  section p, section div, section h1, section h2, section h3 {
    font-size: inherit;
  }
    /* --- FORCER LES COULEURS DE FOND SUR LE PDF --- */
  .box-pdf {
    -webkit-print-color-adjust: exact !important;
    print-color-adjust: exact !important;

  /* --- VERROUILLAGE FORCE DE LA GRILLE POUR TOUS LES NAVIGATEURS --- */
  .grille-fixe {
    display: grid !important;
    grid-template-columns: 1fr 1fr !important; /* Force 2 colonnes égales quoi qu'il arrive */
    width: 100% !important;
  }
    
---

# 🚀 Démonstration Tailwind & Marp

Voici une grille native en Tailwind CSS :

<!-- Remplacement de grid-cols-2 par notre classe grille-fixe ultra-robuste -->
<div class="grille-fixe gap-6 mt-8 mx-auto">
  
  <div style="background-color: #334155;" class="p-6 rounded-lg text-white shadow-lg box-pdf">
    <h3 class="text-xl font-bold text-blue-400 mb-2">Bloc Gauche</h3>
    <p class="text-sm" style="color: #cbd5e1;">Ce bloc reste obligatoirement ancré à gauche. La structure ne peut plus se briser ni s'empiler verticalement.</p>
  </div>

  <div style="background-color: #312e81;" class="p-6 rounded-lg text-white shadow-lg box-pdf">
    <h3 class="text-xl font-bold text-pink-400 mb-2">Bloc Droite</h3>
    <p class="text-sm" style="color: #e0e7ff;">Ce bloc reste ancré à droite. L'affichage est désormais identique sur Chrome, Firefox et en PDF.</p>
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

---
# Test de Bootstrap Icons
Exemples d'icônes directement dans le texte :

 <i class="bi bi-check-circle-fill text-green-500"></i> Une tâche complétée (Vert)
 <i class="bi bi-exclamation-triangle-fill text-amber-500"></i> Une alerte importante (Orange)
 <i class="bi bi-shield-lock-fill text-indigo-500"></i> Connexion sécurisée (Bleu)

---

# 📊 Tableau de bord avec indicateurs

<div class="grid grid-cols-2 gap-6 mt-8">
  
  <div style="background: #334155;" class="p-6 rounded-lg text-white shadow-lg flex items-start space-x-4">
    <div class="text-3xl text-sky-400 mt-1">
      <i class="bi bi-cpu"></i>
    </div>
    <div>
      <h3 class="text-xl font-bold text-sky-400 mb-1">Performances</h3>
      <p class="text-sm">L'architecture serveur tourne à plein régime sans aucun ralentissement détecté.</p>
    </div>
  </div>

  <div style="background: #312e81;" class="p-6 rounded-lg text-white shadow-lg flex items-start space-x-4">
    <div class="text-3xl text-pink-400 mt-1">
      <i class="bi bi-cloud-arrow-up"></i>
    </div>
    <div>
      <h3 class="text-xl font-bold text-pink-400 mb-1">Sauvegardes</h3>
      <p class="text-sm">Les présentations et les images associées sont synchronisées sur la branche Cloud.</p>
    </div>
  </div>

</div>
