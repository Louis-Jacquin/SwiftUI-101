# 2-App-Basics
## Exercice 1
1) Il manque un id à l'élément pour qu'il puisse être identifié par rapport aux autres
2) J'ai donc ajouté id: \.self pour qu'il s'utilise lui même en tant qu'indentifiant

## Exercice 2 
On a ajouté un Bouton dans le Body pour pouvoir utiliser la fonction AddItem et on est passé d'une List à un ForEach   
Le ForEach est nécessaire car on à ajouté un Bouton dans la List afin de l'avoir dans la List et on ne peux pas mettre de List dans un List, donc on fait un ForEach afin d'ajouter chaque élément de la List.

## Exercice 3 
Ce code ne fonctionne pas car la liste "loot" est immutable et ne peut donc pas être mise à jour   
On utilise @State sur la variable pour lui permettre d'être modifié et qu'elle puisse se reconstruire quand on là modifie

# 4-Ajout-Item
## Exercice 1 
Quand on clique sur le bouton rien ne se passe car l'id de "Magie de feu" est déjà utilisé   
Le message d'erreur indique que dans le Tableau de loot l'id est utilisé plusieurs fois

## Exercice 2 
Cela fonctionne de nouveau car la classe est maintenant Observable et la liste loot de la classe est publié donc il est possible de le modifier depuis l'exterieur   
On utilise @StateObject plutôt que @ObservedObject ou @State car Inventory est un objet donc il ne faut plus utiliser @State et si on utilise @ObservedObject la vue ne sera pas 
forcement instanciée qu'une seule fois et lors de sa destruction, elle peut ne pas être détruite partout donc on utilise @StateObject

