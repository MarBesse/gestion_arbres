# gestion_arbres
Ceci est un sig pour la gestion d'un patrimoine arboré d'une commune.

# Préparation des dossiers
Le dossier QGis_gestion_arbres contient le Qgis et le fichier externe des images.
C'est ici que vous entrerez vos images. Laissez l'arborescence telle quelle.

Le dossier Base de données contient un backup de la base de données "gestion_arbres". 
Il faut la charger sur pgadmin (par ex.) en lui donnant ce nom.

Le dossier infoarbre est le dossier du plugin QGis InfoArbre. Il faut aller le placer dans les dossiers plugins de votre QGis.
Par exemple à l'emplacement: "C:\Users\Votre_UserName\AppData\Roaming\QGIS\QGIS3\profiles\default\python\plugins"
<br>Dans le fichier InfoArbre.py, il faut modifier plusieurs choses: 
<br>-A la ligne 37, indiquez le chemin du dossier QGis_gestion_arbres.
<br>-Aux lignes 43 et 52, indiquez vos user et mot de passe pour accéder à la base de données. 

# Utilisation du projet QGis - fonctionnalités:

## 1: Consulter les attributs et interventions liées à un arbre
-Sélectionner la couche Martigny_centre (couche qui contient les arbres)
-Sélectionner une entité arbre (1 seule) avec l'outil de sélection.
-Cliquez sur l'icone du plugin InfoArbre

-> Les attributs et interventions apparaissent. 
La boîte erreurs console est une aide à l'utilisateur et vous donne diverses informations utiles.

## 2: Editer et/ou ajouter une entité arbre
-Editer la couche martigny_centre
-Sélectionner l'entité à modifier avec l'outil "identifier" OU utiliser l'outil "ajouter une entité ponctuelle" pour créer une nouvelle entité
-Faire les modifications/créer notre entité
-Enregistrer les changements et quitter l'édition

Remarques pour les images: 
-Pour ajouter une image, déposez au préalable votre image dans le dossier QGis_gestion_arbres\Images
-Dans Qgis, utiliser le bouton avec les trois petits points pour aller chercher l'image dans le dossier.

## 3: Ajouter une nouvelle essence d'arbres
-Editer la table essence_arbres
-Outil "Ajouter un enregistrement"
-Remplir, enregistrer et fermer l'édition
-Pour mettre à jour la symbologie, aller dans propriétés de la couche martigny-centre - onglet symbologie
-Cliquez sur +, et remplir la colonne valeur avec l'identifiant donné à notre essence, et le nom de l'essence

## 4: Editer et ajouter des interventions
-Editer la table intervention
-Outil "Ajouter un enregistrement"
-Remplir, enregistrer et fermer l'édition

-Editer la table arbre_intervention
-Outil "ouvrir la table d'attributs"
-Ajouter une entité
-Remplir en sélectionnant les id de l'arbre et de l'intervention concernées
-Enregistrer et fermer l'édition


