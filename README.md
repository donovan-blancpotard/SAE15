
## Tutoriel d'installation et utilisation de Gnuplot

**1er étape télécharger gnuplot**

Sur linux pour installer gnuplot il suffit d'aller sur le cmd et de taper :

`apt install gnuplot`

Pour windows, on doit aller sur le web et télécharger gnuplot pour windows.

Lorsqu'on la installé, on a une interface de terminale où on va taper les commandes que l'on veut exécuter.

**2eme étape déclarer le dossier dans lequel on va ouvrir les fichiers**

Pour cela on doit spécifier le répertoire à l'aide de la commande :
`cd` sur linux comme sur windows

Exemple :

`cd 'C:\Users\Téo\Desktop'`

**3eme étape mettre les paramètres**

Avant de  traçer la courbe, il va falloir mettre en place des paramètre pour avoir la courbe que l'on souhaite.

Pour ça on utliser la commande :

`set`

Par exemple :

`set xlabel "Temps en minutes"` xlabel permet d'annoter un axe dans ce cas l'axe x

`set ylabel "Pourcentage moyen d'occupation des parkings"` ici on annote l'axe y avec ce qui est entre ""

`set yrange[0:100]` Pour définir l'intervalle de l'axe y

`set xrange[0:120]` Pour défibir l'intervalle de l'axe x

`set title "titre de la courbe"` Pour mettre un titre

`set output nom.png` Pour que la courbe s'enregistre dans une fichier .png (utile pour pouvoir afficher la courbe sur une page HTML)

**4eme étape affichage de la courbe**

Une fois qu'on a bien mit tout les paramètres qu'on voulait il suffit d'utiliser la commande `plot` pour afficher la courbe.

Exemple :

`plot carre.txt' using 1:2 w l , 'carre.txt' using 3:4 w l title"titre"`

Dans cet exemple, on va faire une courbe avec les valeurs dans le fichier carre.txt, avec la 2eme colonne de valeurs en fonction de la 1ere, le "w l" signifie que l'on va relier les points entre eux pour avoir une courbe (parce que par défaut il va juste placer les points) et pour la 2eme courbe on va prendre la 4eme colonne de valeurs en fonction de la 3ème toujours dans le fichier carre.txt

Attention à l'ordre des paramètres dans la commande `plot` car si il n'est pas respecté, sa peut ne pas marcher.
