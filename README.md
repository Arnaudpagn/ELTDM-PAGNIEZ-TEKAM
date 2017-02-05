# ELTDM-PAGNIEZ-TEKAM
Projet d'Eléments logiciels pour le traitement des données massives réalisé par Arnaud PAGNIEZ et Yann TEKAM.

Ce répertoire GitHub contient les données utilisées et le code produit dans le cadre de ce projet qui porte sur l'algorithme d'Affinity Propagation

L'étude que nous avons faite se base sur l'article écrit par Wei-Chih Hung, Chun-Yen Chu, and Yi-Leh Wu de la National Taiwan University of Science and Technology et par Cheng-Yuan Tang de la Huafan University à Taiwan. L'article s'intitule "Map/Reduce Affinity Propagation Clustering Algorithm" et porte sur l'implémentation de la méthode AP pour répartir de larges bases de données en groupes dits clusters. 

Cet algorithme présente plusieurs particularités très appréciables pour une démarche de clusterisation: 

- Le nombre de clusters ne doit pas être fixé à l'avance 
- La démarche mathématique est relativement simple et converge assez rapidement
- L'algorithme s'applique à tout types de données du moment qu'elles sont numériques
- Son implémentation est relativement rapide (certaines bibliothèques existent déjà)

Le principal défaut de l'algorithme AP est son coût en mémoire. En effet, pour exécuter l'algorithme AP sur une base de données de X lignes, il faut générer une matrice de taille X² afin de stocker toutes les valeurs à mettre à jour. Cela en fait un algorithme qui atteint vite ses limites sur de larges bases de données car une machine seule n'est pas capable de gérer facilement des tableaux d'une telle taille. 

Le but de ce code est donc: 

- Dans un premier temps de présenter les données à traiter et de les mettre en forme
- Appliquer l'algorithme AP sur une fraction des données sans utiliser Map/Reduce et critiquer le résultat
- Appliquer l'algorithme AP à l'ensemble des données grâce au langage PIG et critiquer les résultats.
- Comparer les résultats à l'algorithme K-means

L'article sur lequel est basé ce code est disponible à l'adresse suivante:

http://www.ijeee.net/uploadfile/2014/0807/20140807114023665.pdf
