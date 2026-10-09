---
marp: true
title: Présentation Finale Validée
paginate: true
style: |
  /* Ajout de Tailwind */
  @import url('https://unpkg.com/tailwindcss@^2/dist/utilities.min.css');
  /* Ajout de Bootstrap-icons */
  @import url('https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css');
  
  /* Astuce : Forcer Marp à respecter la taille de texte de Tailwind */
  section p, section div, section h1, section h2, section h3, section i {
    font-size: inherit;
  }
  /* --- Forcer les couleurs de fond sur le PDF --- */
  .box-pdf {
    -webkit-print-color-adjust: exact !important;
    print-color-adjust: exact !important;
  }
  /* --- FIX pour le fond des grilles sur le PDF --- */
  .box-pdf-gauche {
    background-color: #334155 !important;
    -webkit-print-color-adjust: exact !important;
    print-color-adjust: exact !important;
  }
  
  .box-pdf-droite {
    background-color: #312e81 !important;
    -webkit-print-color-adjust: exact !important;
    print-color-adjust: exact !important;
  }

  .grille-fixe {
    display: grid !important;
    grid-template-columns: 1fr 1fr !important;
    width: 100% !important;
  .grille-fixe {
    display: grid !important;
    grid-template-columns: 1fr 1fr !important;
    width: 100% !important;
  }
---

# 🚀 Démonstration Tailwind & Marp

Voici une grille native en Tailwind CSS :

<div class="grille-fixe gap-6 mt-8 mx-auto">
  
  <!-- Les couleurs de fond sont maintenant gérées par les classes box-pdf -->
  <div class="p-6 rounded-lg text-white shadow-lg box-pdf-gauche">
    <h3 class="text-xl font-bold text-blue-400 mb-2">Bloc Gauche</h3>
    <p class="text-sm" style="color: #cbd5e1;">Ce bloc reste obligatoirement ancré à gauche. La structure ne peut plus se briser ni s'empiler verticalement.</p>
  </div>

  <div class="p-6 rounded-lg text-white shadow-lg box-pdf-droite">
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

<!-- Application de 'grille-fixe' et 'box-pdf' ici aussi pour éviter le bug Firefox et PDF -->
<div class="grille-fixe gap-6 mt-8 mx-auto">
  
  <div style="background-color: #334155;" class="p-6 rounded-lg text-white shadow-lg box-pdf flex items-start space-x-4">
    <div class="text-3xl text-sky-400 mt-1">
      <i class="bi bi-cpu"></i>
    </div>
    <div>
      <h3 class="text-xl font-bold text-sky-400 mb-1">Performances</h3>
      <p class="text-sm" style="color: #cbd5e1;">L'architecture serveur tourne à plein régime sans aucun ralentissement détecté.</p>
    </div>
  </div>

  <div style="background-color: #312e81;" class="p-6 rounded-lg text-white shadow-lg box-pdf flex items-start space-x-4">
    <div class="text-3xl text-pink-400 mt-1">
      <i class="bi bi-cloud-arrow-up"></i>
    </div>
    <div>
      <h3 class="text-xl font-bold text-pink-400 mb-1">Sauvegardes</h3>
      <p class="text-sm" style="color: #e0e7ff;">Les présentations et les images associées sont synchronisées sur la branche Cloud.</p>
    </div>
  </div>

</div>
