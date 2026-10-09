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
  .box-pdf-indigo { background-color: #312e81 !important; -webkit-print-color-adjust: exact !important; print-color-adjust: exact !important; }
  .box-pdf-slate { background-color: #334155 !important; -webkit-print-color-adjust: exact !important; print-color-adjust: exact !important; }
  .box-pdf-emerald { background-color: #064e3b !important; -webkit-print-color-adjust: exact !important; print-color-adjust: exact !important; }
  .box-pdf-light { background-color: #f8fafc !important; -webkit-print-color-adjust: exact !important; print-color-adjust: exact !important; }

  .grille-3-cols { display: grid !important; grid-template-columns: repeat(3, 1fr) !important; width: 100% !important; }
  .grille-2-cols { display: grid !important; grid-template-columns: 1fr 1fr !important; width: 100% !important; }

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

# 🎨 Autres tests graphiques de Tailwind

🎯 Un texte <span class="text-red-500 font-extrabold uppercase">rouge, en gras et en majuscules</span>.
🎯 Un badge stylisé : <span class="bg-green-100 text-green-800 text-xs font-semibold px-2.5 py-0.5 rounded-full">Validé</span>

<div class="flex justify-around items-center h-32 mt-6 bg-gray-100 rounded">
  <div class="w-12 h-12 bg-blue-500 animate-pulse rounded-full"></div>
  <div class="w-12 h-12 bg-amber-500 animate-bounce rounded"></div>
</div>

---

## 🚀 Exemple 1 : Cartes de Tarifs / Options (Grille à 3 colonnes)

Idéal pour présenter trois solutions, trois offres ou trois scénarios sur une seule slide :

<div class="grille-3-cols gap-4 mt-6 mx-auto">
  
  <!-- Option 1 -->
  <div class="p-5 rounded-lg text-white box-pdf-slate border border-slate-600 shadow-md">
    <div class="text-xs font-bold uppercase tracking-wider text-slate-400 mb-1">Scénario A</div>
    <h3 class="text-lg font-extrabold text-white mb-2">Statut Quo</h3>
    <div class="text-2xl font-black text-blue-400 mb-3">0 € <span class="text-xs font-normal text-slate-400">/ investissement</span></div>
    <p class="text-xs text-slate-300 leading-relaxed mb-4">Maintien de l'infrastructure existante. Risques techniques modérés à long terme.</p>
    <div class="text-xs font-semibold text-red-400"><i class="bi bi-x-circle"></i> Évolution limitée</div>
  </div>

  <!-- Option 2 (Mise en avant "Pop") -->
  <div class="p-5 rounded-lg text-white box-pdf-indigo border-2 border-indigo-500 shadow-xl relative transform scale-105">
    <div class="absolute -top-3 right-3 bg-pink-500 text-white text-xxs font-black px-2 py-0.5 rounded-full uppercase tracking-tight">Recommandé</div>
    <div class="text-xs font-bold uppercase tracking-wider text-indigo-300 mb-1">Scénario B</div>
    <h3 class="text-lg font-extrabold text-white mb-2">Migration Cloud</h3>
    <div class="text-2xl font-black text-pink-400 mb-3">12 K€ <span class="text-xs font-normal text-indigo-300">/ budget</span></div>
    <p class="text-xs text-indigo-100 leading-relaxed mb-4">Automatisation via GitHub Actions et hébergement centralisé sécurisé.</p>
    <div class="text-xs font-semibold text-green-400"><i class="bi bi-check-circle-fill"></i> Performance ++</div>
  </div>

  <!-- Option 3 -->
  <div class="p-5 rounded-lg text-white box-pdf-emerald border border-emerald-800 shadow-md">
    <div class="text-xs font-bold uppercase tracking-wider text-emerald-400 mb-1">Scénario C</div>
    <h3 class="text-lg font-extrabold text-white mb-2">Sur Mesure</h3>
    <div class="text-2xl font-black text-green-400 mb-3">Sur Devis</div>
    <p class="text-xs text-emerald-200 leading-relaxed mb-4">Développement d'outils internes dédiés sans dépendance externe.</p>
    <div class="text-xs font-semibold text-green-400"><i class="bi bi-shield-check"></i> Sécurité maximale</div>
  </div>

</div>

---

## 📅 Exemple 2 : Une Frise Chronologique (Timeline) Épurée

Parfait pour illustrer les étapes d'un projet ou une feuille de route (Roadmap) :

<div class="flex flex-col space-y-4 mt-6 w-full max-w-2xl mx-auto">

  <!-- Étape 1 -->
  <div class="flex items-center space-x-4">
    <div class="flex-none w-10 h-10 rounded-full bg-blue-500 text-white flex items-center justify-center font-bold text-sm shadow">1</div>
    <div class="flex-grow p-3 rounded-lg box-pdf-light border border-gray-200 shadow-sm">
      <h4 class="text-sm font-bold text-gray-800">Cadrage & Spécifications</h4>
      <p class="text-xs text-gray-600">Définition des besoins, choix de la structure Markdown et configuration du dépôt.</p>
    </div>
  </div>

  <!-- Fil de liaison -->
  <div class="w-0.5 h-4 bg-gray-300 ml-5"></div>

  <!-- Étape 2 -->
  <div class="flex items-center space-x-4">
    <div class="flex-none w-10 h-10 rounded-full bg-indigo-500 text-white flex items-center justify-center font-bold text-sm shadow">2</div>
    <div class="flex-grow p-3 rounded-lg box-pdf-light border border-gray-200 shadow-sm">
      <h4 class="text-sm font-bold text-gray-800">Automatisation CI/CD</h4>
      <p class="text-xs text-gray-600">Mise en place du workflow GitHub Actions et résolution des configurations de rendu PDF.</p>
    </div>
  </div>

  <!-- Fil de liaison -->
  <div class="w-0.5 h-4 bg-gray-300 ml-5"></div>

  <!-- Étape 3 -->
  <div class="flex items-center space-x-4">
    <div class="flex-none w-10 h-10 rounded-full bg-green-500 text-white flex items-center justify-center font-bold text-sm shadow"><i class="bi bi-flag-fill"></i></div>
    <div class="flex-grow p-3 rounded-lg box-pdf-light border border-gray-200 shadow-sm">
      <h4 class="text-sm font-bold text-gray-800">Déploiement en Production</h4>
      <p class="text-xs text-gray-600">Publication finale des diaporamas web et génération automatique des versions PDF.</p>
    </div>
  </div>

</div>

---

## 📊 Exemple 3 : Tableau Comparatif de Données Avancé

Tailwind permet de s'affranchir des tableaux Markdown basiques en créant des structures très graphiques :

<div class="w-full mt-6 overflow-hidden rounded-lg border border-gray-200 shadow-md box-pdf-light">
  <table class="w-full border-collapse text-left text-xs text-gray-500">
    <thead class="bg-gray-100 text-gray-700 font-bold uppercase text-xxs tracking-wider border-b border-gray-200">
      <tr>
        <th class="px-4 py-3">Fonctionnalité</th>
        <th class="px-4 py-3">Version Standard</th>
        <th class="px-4 py-3">Version Avancée (Tailwind)</th>
        <th class="px-4 py-3 text-center">Impact PDF</th>
      </tr>
    </thead>
    <tbody class="divide-y divide-gray-200 text-gray-700">
      <tr class="hover:bg-gray-50">
        <td class="px-4 py-3 font-semibold text-gray-900">Mise en page</td>
        <td class="px-4 py-3">Linéaire et verticale</td>
        <td class="px-4 py-3 text-indigo-600 font-semibold">Grilles multi-colonnes fluides</td>
        <td class="px-4 py-3 text-center"><span class="bg-green-100 text-green-800 px-2 py-0.5 rounded-full font-bold">Parfait</span></td>
      </tr>
      <tr class="hover:bg-gray-50">
        <td class="px-4 py-3 font-semibold text-gray-900">Gestion des icônes</td>
        <td class="px-4 py-3">Images lourdes (.png)</td>
        <td class="px-4 py-3 text-indigo-600 font-semibold">Bootstrap Icons vectorielles</td>
        <td class="px-4 py-3 text-center"><span class="bg-green-100 text-green-800 px-2 py-0.5 rounded-full font-bold">Parfait</span></td>
      </tr>
      <tr class="hover:bg-gray-50">
        <td class="px-4 py-3 font-semibold text-gray-900">Couleurs de fond</td>
        <td class="px-4 py-3">Unie par diapositive</td>
        <td class="px-4 py-3 text-indigo-600 font-semibold">Blocs imbriqués contrastés</td>
        <td class="px-4 py-3 text-center"><span class="bg-amber-100 text-amber-800 px-2 py-0.5 rounded-full font-bold">Fix Requis</span></td>
      </tr>
    </tbody>
  </table>
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
