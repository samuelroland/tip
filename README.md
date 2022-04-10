# Site de sensibilisation après une attaque fictive de phishing

## Déployer en production
Prendre `index.html`, `background.jpg` et `output.css`, les poser sur un serveur web (via SFTP par exemple), puis le site s'affiche tel quel ça fonctionne.

## Modifier la page
En modifiant le contenu du fichier `index.html` on peut modifier le texte et son design si besoin. Le design est fait avec [TailwindCSS](https://tailwindcss.com/) (framework CSS) afin de rendre responsive le site. Si on utilises des classes fournies par TailwindCSS, il faut faire tourner un processus de compilation en temps réel du CSS pour voir les modifications.

Pour cela il suffit d'avoir NPM installé, d'avoir lancé `npm install` et de lancer `npm run watch` et d'ouvrir le fichier `index.html` dans son navigateur. Le CSS généré entre les classes utilisées de TailwindCSS et le `style.css`, se trouvera dans `output.css`.

## Builder une page modifiée pour la production
Il suffit de lancer `npm run prod` (après le `npm install` bien sûr) (seul le `output.css` sera modifié), puis de déployer la page comme défini dans la première section. L'avantage est d'avoir ce fichier `output.css` plus léger que durant le développement.