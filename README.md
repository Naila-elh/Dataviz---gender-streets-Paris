# Dataviz---gender-streets-Paris

Projet réalisé pour le cours de Data Storytelling dans le cadre de ma troisième année à l'ENSAE, avec Zoé Fontier, Laure-Hélène Genuyt et Colombe Saillard.
L'objectif de ce cours était de créer un site web afin de présenter de façon attractive, à partir de jeux de données, une thématique de notre choix.

Nous avons choisi de nous intéresser aux inégalités de genre dans l'espace urbain, dans la ville de Paris. Pour cela, nous avons travaillé à partir des données de la ville de Paris, disponible à partir de [ce lien](https://www.data.gouv.fr/fr/datasets/nomenclature-des-voies-actuelles-prs/), ainsi que de la [page Wikipédia](https://fr.wikipedia.org/wiki/Liste_des_voies_de_Paris_se_r%C3%A9f%C3%A9rant_%C3%A0_un_nom_de_femme) référençant la liste des voies de Paris se référant à un nom de femme. Notons que cette page inclut également des noms de rues se référant à des groupes de femmes, ainsi que les rues se référençant à des couples (soit une femme et un homme), ce qui peut expliquer pourquoi nos chiffres sont légèrement différents que ceux avancés par certaines associations.

## Présentation du repo
Ce repo contient le code nous ayant permis de construire une base de données, pour labelliser les rues selon leur genre. 
Après avoir procédé à un nettoyage basique des données (1_Cleaning_dataset.ipynb), nous avons utilisé un modèle de Name entity recognition pour reconnaître, dans la variable "historique" de chaque rue, le nom de l'individu, sa profession, et ses dates (2_NER.ipynb). Pour cela, nous avons au préalable labellisé à la main 200 rues, car les modèles classiques de NER ne permettent pas de reconnaître, en français, la profession des individus. Puis, nous avons incorporé les données Wikipédia (3_Wikipedia.ipynb), afin de distinguer les noms de femmes et les noms d'hommes. 
Enfin, le notebook 4_Graphs.ipynb contient le code ayant permis d'exporter des tables pour construire par la suite certains graphes via l'interface [datawrapper](datawrapper.de), ainsi que des wordclouds.

## Accès au site web
Le site web produit est disponible sur la page [https://a-qui-appartient-la-rue.github.io/](https://a-qui-appartient-la-rue.github.io/).
