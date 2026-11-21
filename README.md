# PCA_CA_MCA_Analysis_base_CM

### Dataset : 

Relevés de base clients Club Med, 89 varibales dont NUMCLI pour les ID clients, et cluster pour leur classification effectué via K-means et DB-scan.
Certaines variables ont été catégorisées (modalités divisées en booléens) pour lesquels l'AFC et l'ACM seront inutiles. 
D'autres variables ont été discrétisées, leurs modalités ont été divisées en classes, le plus souvent via K-means.

Pour les analyses quantitatives, les clusters risquent de biaiser les données, soir vous pouvez supprimer la colonne, soit, pour l'AFC/ACM, comparer des variables explicatives à cette variables cible.

### Lecture et chargement du dataset

il est lourd, 174213 individus sur 89 variables, si c'est compliqué pour les machines on réfléchira à le limiter, en attendant voici comment charger et push le dataset, il faut rajouter : 

git config http.postBuffer 524288000
git push

Cela permet d'augmenter la taille des documents admise lors des push github.

### Bonnes pratiques de collaboration

Chaque personne doit créer sa propre branche pour ses modifications et récupérer les dernières mises à jour de `main` avant de commencer. Ne push que les fichiers nécessaires à votre travail sur votre branche, puis ouvrez une pull request afin que les changements puissent être examinés et fusionnés dans `main`. Évitez de modifier ou de supprimer des notebooks sans lien avec votre tâche.

Python .venv chargé avec VS code - pour vos besoins, veillez à utiliser votre propre environnement, et charger un .gitignore pour éviter les confusions de chargement.

Prévenir par whatsapp des changements pour une mise à jour plus fluide du repo.

### Bonnes pratiques de code

Bien commenter son code, rajouter des parties Markdown pour que les collaborateurs comprennent efficacement la réflexion derrière, si on comprend tous toute la réflexion ce sera décisif pour savoir tout expliquer le jour de l'examen.

### Pour charger les données :

""Base_CM = pd.read_csv("FILE/base_all_inclusive.csv", index_col="NUMCLI")

print(Base_CM.shape)
Base_CM.head()""



