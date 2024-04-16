# Studies Survivor (Durée 1h30)

Ce projet contient des fragments de jeu mais vous devrez développer certaines parties pour rendre le projet jouable.

## Récupération du projet (2 points)

1. Faire un fork de ce dépôt.
2. Cloner votre fork sur votre machine.
3. Ouvrir le projet.

## Interaction avec les objets (4 points)

1. Détecter si le joueur entre en contact avec un objet.
2. Appeler la fonction **Pickup()** de l’objet si les conditions sont remplies.
    - Si c’est un consommable l’objet devra faire son effet immédiatement.
    - Si c’est un équipement, afficher l’UI proposant d’équiper ou non l’objet.
3. Détruire l’objet dans la scène.

## Patterns (10 points)

Les patterns demandés n’auront pas d’inter-dépendances afin de vous permettre de commencer par celui que vous souhaitez.

### Observer (4 points)

1. L’inventaire du joueur devra notifier les **Observers** des objets ramassés par ce dernier. (équipement **ET** consommable)
3. Rendre les ennemis attentifs aux objets ramassés par le joueur.
4. Si l’objet ramassé est une **Bombe**, alors détruire tous les ennemis.
    - *Bonus [2 points]* : Détruire seulement les ennemis à l’écran

### Objects pooling (6 points)

Les files n'étant pas implémentables en blueprint, vous utiliserez un tableau afin de mettre en place la pool.

1. Mettre en réserve en fin de tableau les projectiles devant être détruits.
2. Au moment de spawn un projectile
    - Si des projectiles sont en réserve, recycler le premier du tableau.
    - Si aucun projectile n’est disponible, spawn un nouveau projectile.

## Localization Dashboard (2 points)

1. Ajouter la culture en-US au jeu.
2. Modifier le menu principal afin de pouvoir changer la langue du jeu.

## Optimisation (2 points)

1. Utiliser les itérateurs de manière réfléchie.
2. Eviter les traitements superflus.
3. Améliorer la fonction **Execute()** du **Pistolet**.
