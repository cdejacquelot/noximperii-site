# Restauration de noximperii.com

Le site de présentation de Nox Imperii — le fork de Naev, à ne pas confondre avec
la refonte JavaScript servie sur `nox.millenaire.org` — a cessé de répondre en
**décembre 2020**. Sa dernière capture vivante date du **12 août 2020**, et il
n'en existait plus aucune copie : ni sur l'ancienne VM Millénaire (éteinte, et de
toute façon le domaine pointait déjà ailleurs), ni dans `legacy-archive/`, dont le
rapatriement de juillet 2026 ne visait que `longnight` et `gloriamundi`.

Le contenu de ce dossier a donc été reconstitué depuis la Wayback Machine le
**16 août 2026**, fichier par fichier, en mode `id_` (contenu d'origine, sans les
scripts que l'Internet Archive injecte pour sa visionneuse). 54 fichiers, 19 Mo.

## Provenance

Chaque fichier vient de la capture 200 la plus récente de son adresse, pas d'une
date unique : la page a été archivée en août 2020, mais la plupart des images
n'ont plus été revisitées après septembre 2019. Prendre un horodatage global
aurait rendu neuf images introuvables.

`res/main.js` est vide — ce n'est pas une perte à la restauration : le fichier
d'origine faisait déjà zéro octet, ce que confirment ses deux captures.

## Écarts assumés avec l'original

Le parti pris est la fidélité, à trois exceptions près, toutes signalées par un
commentaire dans `index.html` :

| ce qui a changé | pourquoi |
|---|---|
| Traceur Google Analytics retiré | `ga.js` « classic » est arrêté depuis juillet 2023 |
| `blog.naev.org` → `naev.org` (2 liens), `wiki.naev.org/wiki/Compiling_Nix` → README du dépôt Naev | les deux sous-domaines ne résolvent plus (NXDOMAIN) |
| `forum.naev.org/viewforum.php?f=13` → racine du forum | le sous-forum Nox Imperii a disparu du phpBB ; la racine, elle, répond |

Le lien du **binaire Windows 0.5.1** passait par `goo.gl/FU41qg`, qui redirige
encore vers un Dropbox aujourd'hui éteint. L'archive n'a été retrouvée nulle part
— ni Wayback, ni disque local. Le lien a été remplacé par une mention honnête. Si
le `.7z` refait surface, en faire une release GitHub et rétablir le lien : le
commentaire qui marque l'endroit est dans la section *Download*.

Le code source, lui, n'a jamais été menacé : `github.com/Kinniken/NoxImperii`,
tag `naev-0.5.1`.

## Point de vigilance : `robots.txt`

Il a été conservé tel quel, et il porte `Disallow: /` — le réglage d'époque. Le
site restauré restera donc hors des moteurs de recherche tant que ce fichier n'est
pas modifié. À trancher au moment de la publication.
