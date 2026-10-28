# Parc de logement social et ségrégation résidentielle à Brest métropole
segregation-logement-social-brestStructure urbaine, parc de logements et dynamiques de gentrification à Brest Métropole

Cette étude analyse l'effet de la distribution spatiale du parc de logements sociaux sur la ségrégation résidentielle au sein de Brest Métropole.
Alors que les politiques urbaines (comme la loi SRU) visent à promouvoir la mixité sociale, la concentration des logements sociaux peut paradoxalement alimenter la ségrégation. L'objectif est de vérifier si le parc social atténue ou renforce la séparation entre différentes couches de la population, dans un contexte de renouvellement urbain et de potentielle gentrification.   

Objectifs
- Mesurer la ségrégation résidentielle de trois catégories socioprofessionnelles : cadres, employés et ouvriers.
- Calculer et comparer des indices d'égalité (indice de dissimilarité D) et d'exposition (indices d'isolement xPx et d'interaction xPy).
- Cartographier la sur-représentation et sous-représentation spatiale via le quotient de localisation (LQ) à l'échelle des IRIS.
- Détecter les clusters de ségrégation par l'autocorrélation spatiale locale (LISA).
- Comparer deux scénarios (avec et sans les locataires du parc social) pour isoler l'impact du logement social.
- Étendre l'approche comparative à d'autres métropoles (Marseille et Paris).

Données

Fichier détaillé "Individus localisés au canton-ou-ville" du recensement de la population de l'INSEE 2022.   

Couches géographiques de contours IRIS (BD TOPO / data.gouv.fr).   

Données locales complémentaires (ADEUPa) sur le logement à Brest.   

Méthodologie

1- Préparation et agrégation des données

Filtrage par IRIS de type "habitat", sélection des catégories (cadres, employés, ouvriers) et agrégation des pondérations (IPONDI) via des scripts automatisés en Python.   

2- Calcul des indices de ségrégation

Utilisation de la bibliothèque PySAL pour quantifier la dissimilarité, l'isolement et l'interaction des groupes avec et sans la prise en compte du logement social.   

3- Analyse spatiale (Quotient de localisation)

Calcul du quotient (LQ) pour chaque IRIS afin d'identifier les secteurs de sur-représentation ou de sous-représentation pour chaque groupe.

4-Analyse de l'autocorrélation (LISA)

Mesure de l'indice global de Moran (contiguïté Queen) et cartographie des clusters locaux (High-High, Low-Low, etc.) pour évaluer la concentration spatiale.   

5- Mise en perspective

Comparaison des variations d'indices entre les scénarios à Brest, puis application de la même méthode sur Paris et Marseille pour observer l'influence du contexte urbain.




L'étude montre qu'à Brest, les cadres et les ouvriers sont les catégories les plus séparées spatialement, avec une géographie opposant un pôle populaire (nord-ouest) à un pôle plus aisé (centre et façade est).
L'intégration des données du logement social ne réduit pas la ségrégation globale mais la reconfigure : elle accentue légèrement la dissimilarité et l'isolement des catégories populaires (ouvriers), tout en diffusant marginalement leur présence dans de nouveaux secteurs. Contrairement à Marseille ou Paris, où le parc social tend à consolider rigidement les groupes dans leurs espaces historiques, le parc brestois engendre une dynamique spatiale plus nuancée sans pour autant corriger les inégalités résidentielles.   

Outils

- Python (bibliothèques Pandas, GeoPandas, PySAL, ESDA, Matplotlib)
- QGIS

Le rapport PDF de l'étude est disponible dans les fichiers de ce dépôt.

Mémoire du Master 1 - Géomatique et Modélisation Spatiale, Aix-Marseille Université.

Cartes interactives

Pour une meilleure lisibilité, l'ensemble des cartes produites dans le cadre de cette étude (Quotients de Localisation, LISA, etc.) est consultable à cette adresse :
https://mo-soidridine.github.io/brest_metropole/ 
