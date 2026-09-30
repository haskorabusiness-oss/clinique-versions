# Versions du poste de la clinique

Ce dépôt public porte ce que le poste de la clinique lit sur internet pour se
mettre à jour. Il ne contient aucun code et aucune donnée de clinique.

- `canaux/<canal>.json` : le manifeste de chaque canal (`pilote`, `general`),
  signé par la clé de mise à jour de l'éditeur. Le poste refuse tout manifeste
  dont la signature ne correspond pas à la clé publique qu'il embarque.
- Releases `poste-v<version>` : l'installeur du poste désigné par un manifeste.
  Le poste vérifie sa taille et son SHA-256 avant de l'installer.
- Releases `telechargement-v<version>` : l'installeur proposé sur la page
  publique de téléchargement. Aucun manifeste ne les désigne ; elles
  n'entraînent aucune mise à jour automatique.

Ce dépôt n'est modifié que par `scripts/poste/publier.mjs` et
`scripts/poste/promouvoir.mjs` du dépôt de l'application, à la main pour les
Releases de téléchargement.
