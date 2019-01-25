# Introduction à MySQL
## Les bases

Prends d'abord quelques minutes pour lire la documentation

[MySQL et les bases de données](https://docs.google.com/presentation/d/1yXQz5dMMDkdSu5eBOG7YS2UH2uWyg5vJmU0kJt6YR6Q/edit#slide=id.g35f391192_00)

Pour manipuler les bases de données, tu effectueras essentiellement 4 types d'opérations : **CRUD**.

1. Create : ajouter une rangée à ta table.
1. Read : sélectionner une ou plusieurs rangées (pour les afficher par exemple).
1. Update : modifier l'information stockée sur une rangée.
1. Delete : effacer une rangée.

## Parcours SQL

1. Read : [**SELECT**](https://github.com/Anxium/exercice-sql/blob/dev/Parcours/select.md)
1. Create : [**INSERT INTO**](https://github.com/Anxium/exercice-sql/blob/dev/Parcours/insertinto.md)
1. Update : [**UPDATE**](https://github.com/Anxium/exercice-sql/blob/dev/Parcours/update.md)
1. Delete : [**DELETE FROM**](https://github.com/Anxium/exercice-sql/blob/dev/Parcours/delete.md)

## Introduction PDO

Un peu de [théorie](https://docs.google.com/presentation/d/14-5BGNJyuILB2kfYlxzsaFDRNA8zCrot9DbYVVNo3X4/edit#slide=id.g35f391192_00) sur la **PDO** pour commencer.

### Qu'est ce que PDO ?

PDO (**P**hp **D**ata **O**bject) est utilisé pour se connecter à une base de donnée.

Plus d'infos [ici](http://php.net/manual/fr/book.pdo.php)

### Syntaxe PDO

```PHP
<?php
try
{
	// On se connecte à MySQL
	$bdd = new PDO('mysql:host=localhost;dbname=becode;charset=utf8', 'root', 'MOTDEPASSE');
}
catch(Exception $e)
{
	// En cas d'erreur, on affiche un message et on arrête tout
    die('Erreur : '.$e->getMessage());
}
```

On utilise *Try* et *Catch* pour vérifier les erreurs.

### Parcours PDO