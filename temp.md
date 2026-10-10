Bonjour ! Nous reprenons l'investigation sur ma configuration Marp + GitHub Pages (100% en ligne, sans installation locale).

Voici l'état actuel de notre projet pour mémoire :
1. L'environnement GitHub Actions et GitHub Pages (via la branche gh-pages) fonctionne parfaitement. Tout passe au VERT.
2. Le fichier README.md sert de portail d'accueil avec le thème Marp "uncover" en mode sombre, et les liens pointent vers les versions HTML et PDF.
3. Les diaporamas (dont Diaporama.md) intègrent avec succès Tailwind CSS, les Bootstrap Icons, ainsi que le correcteur d'impression pour conserver les fonds sombres sur le PDF (print-color-adjust). Tout s'affiche correctement sur Chrome et Firefox.

Le problème restant à résoudre :
Les schémas Mermaid (comme la mindmap et la timeline) ne s'affichent pas du tout. Ils apparaissent sous forme de blocs de code textuels bruts (sans rendu graphique), à la fois sur la version web HTML et sur le fichier PDF généré.

Voici mon fichier .github/workflows/main.yml actuel :
--------------------------------------------------
name: Deploy Marp Presentation
on:
  push:
    branches: [ main ]
permissions:
  contents: write
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Install Marp CLI
        run: npm install -g @marp-team/marp-cli

      - name: Create build folder
        run: mkdir -p build

      - name: Copy images folder (if it exists)
        run: |
          if [ -d img ]; then cp -r img build/img; fi
          if [ -d images ]; then cp -r images build/images; fi

      - name: Compile ALL Marp Presentations (HTML & PDF)
        run: |
          marp --html --mermaid --input-dir . --output build
          marp --pdf --allow-local-files --mermaid --input-dir . --output build

      - name: Rename README to index
        run: |
          if [ -f build/README.html ]; then mv build/README.html build/index.html; fi

      - name: Deploy to GitHub Pages Branch
        uses: JamesIves/github-pages-deploy-action@v4
        with:
          folder: build
          branch: gh-pages
--------------------------------------------------

Rappel : l'en-tête de mon fichier .md a été nettoyé de toutes les balises <script> expérimentales que nous avions testées.

Peux-tu m'expliquer pourquoi le drapeau `--mermaid` de Marp CLI ne déclenche pas le rendu des graphiques sur le serveur GitHub, et comment corriger cela ?
