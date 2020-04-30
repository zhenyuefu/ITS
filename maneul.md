# maneul d'utilisation
## genere des donnees
Le programme a généré au hasard une grille de 200 * 200 (sous forme de gaussiennes)
Ici je utilise `scipy.stats.multivariate_normal`
## boucle de RS
Ensuite c'est la boucle de RS
On répète `L=200` fois pour chaque température:
1.Générez de nouvelles coordonnées au hasard
2.Calculer la valeur $\Delta f$ après la perturbation, accepter la perturbation si elle est supérieure à 0 et l'accepter avec une probabilité de $p=e^{−\Delta f/T}$ si elle est inférieure à 0.
3.Meilleure mise à jour `(x_best, y_best)`
Ensuite on refroid par le facteur `K` jusqu'à la température la plus basse `T_min`

Le boucle trouve le minimum de founction.
Je fois le founction par -1 pour trouver le maximum.
## display
On utilise `matplotlib.pyplot` pour afficher les résultats graphiques.
Et on `print` les values `x_best` et `y_best` et le maximun de founction.