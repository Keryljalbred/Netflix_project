# README

## Projet d'Analyse des Titres Netflix

Ce projet a pour objectif d'analyser le dataset "Titres Netflix", qui contient des informations sur les films et séries disponibles sur la plateforme. Ce document fournit des instructions sur le nettoyage des données et sur l'analyse des tendances du contenu Netflix.

### Contenu du Dataset

Le dataset comprend les colonnes suivantes :

- **show_id** : Identifiant unique pour chaque titre.
- **type** : Catégorie du titre ('Film' ou 'Série télévisée').
- **title** : Nom du film ou de la série.
- **director** : Réalisateur(s) du titre.
- **cast** : Liste des acteurs principaux.
- **country** : Pays de production.
- **date_added** : Date d'ajout du titre sur Netflix.
- **release_year** : Année de sortie originale.
- **rating** : Classification par âge.
- **duration** : Durée en minutes pour les films et en saisons pour les séries.
- **listed_in** : Genres auxquels appartient le titre.
- **description** : Résumé du titre.

### Étapes de Nettoyage et de Modélisation des Données

1. **Importation du fichier** : Importez le fichier `netflix_titles.csv` en résolvant les problèmes d'encodage si nécessaire.
   
2. **Création d'une copie du DataFrame** : Conservez les données originales en créant une copie du DataFrame.

3. **Suppression des colonnes inutiles** : Identifiez et supprimez les colonnes "Unnamed:..." qui ne contiennent pas de données.

4. **Définition d'un nouvel index** : Vérifiez que la colonne "show_id" est unique et sans valeur nulle, puis définissez-la comme index.

5. **Correction du type de colonne** : Assurez-vous que la colonne "date_added" est du type approprié.

6. **Gestion de la colonne "Duration"** :
   - Vérifiez que "type" contient uniquement 'Movie' et 'TV Show'.
   - Examinez les valeurs de la colonne "duration".
   - Créez des colonnes pour isoler la durée des films et le nombre de saisons des séries, tout en s'assurant que ces colonnes sont de type "float".
   - Supprimez la colonne "duration".

7. **Création de DataFrames annexes** : Transformez les colonnes contenant des valeurs séparées par des virgules (comme 'country', 'cast', et 'listed_in') en DataFrames distincts.

8. **Suppression des colonnes transformées** : Retirez les colonnes originales qui ont été transformées.

9. **Création de colonnes temporelles** : Ajoutez des colonnes pour l'année, le mois et le jour de la semaine d'ajout à partir de "date_added".

### Analyse des Données

Après le nettoyage, répondez aux questions suivantes :

1. Combien de "shows" sont présents dans le dataset ?
2. Quelle est la répartition entre les types 'Movie' et 'TV Show' ?
3. Quelle est la répartition des ajouts en fonction de l'année ?
4. Quel est le top 5 des catégories de shows les plus ajoutées ?
5. Quel est le top 5 des acteurs les plus plébiscités aux États-Unis ?
6. Quelle est la répartition des ajouts en fonction du jour de la semaine ?
7. Dans quel pays sont produits le plus de documentaires ?
8. En moyenne, combien de saisons ont les séries ?
9. Quelle est la distribution des films en fonction de leur durée (quartiles) ?
10. Combien de shows ont pour thématique la drogue (présence du mot "drug" dans la description) ?

### Installation

Assurez-vous d'avoir Python et les bibliothèques nécessaires installées :

```bash
pip install pandas
```

### Contribution

Les contributions sont les bienvenues ! N'hésitez pas à soumettre des issues ou des pull requests.

### License

Ce projet est sous licence MIT. Pour plus de détails, consultez le fichier LICENSE.
