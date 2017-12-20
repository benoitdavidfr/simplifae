# Simplifae - Simplification d'ADMIN EXPRESS

ADMIN-EXPRESS est une base de données de l'IGN qui décrit le découpage administratif français,
notamment celui des communes.
Elle est mise à jour chaque mois.
Voir http://professionnels.ign.fr/adminexpress.    

La géométrie d'ADMIN EXPRESS correspond à une résolution de l'ordre de 10 m ce qui conduit à des fichiers
relativement volumineux pour décrire la France entière.

L'objectif de Simplifae est de générer des fichiers SVG et GeoJSON les plus légers possibles tout en conservant :
- au moins un polygone de surface non nulle par commune,
- une partition de l'espace par les communes (cad que l'intérieur des communes ne s'intersectent pas).

Le process enchaine plusieurs scripts utilisant un stockage intermédiaire dans MongoDB.
Ces scripts sont dans le [répertoire scripts](https://github.com/benoitdavidfr/simplifae2/tree/master/scripts).  

Le [répertoire output](https://github.com/benoitdavidfr/simplifae2/tree/master/output) contient le résultat de la simplification sous la forme de défifférents fichiers:
- un fichier SVG restreint aux communes de métropole pesant moins de 3 Mo non compressé et moins de 700 Ko compressé.
- un fichier GeoJSON contenant toutes les communes de métropole et des DOM pesant moins de 7 Mo compressé
  et moins de 900 Ko compressé.
- des fichiers GeoJSON par région (+ 1 pour les 5 DOM) directement affichable dans GitHub.    

Ces fichiers ont été générés entre le 18/12/2017 et le 20/12/2017 à partir de la version d'ADMIN EXPRESS du 15/11/2017.

Des imperfections existent encore dans ce jeu de données expérimental.  
Je suis intéressé à connaitre les utilisations de ce fichier.  
