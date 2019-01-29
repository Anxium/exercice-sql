# Les requêtes préparées

Exemple :

```PHP
try
{
    //Commence la transaction
    $bdd->beginTransaction();

    // Prépare la requête
    $push = $bdd->prepare("
        INSERT INTO team 
            (promo, firstname, lastname, gender, birthdate, age, github) 
        VALUES 
            (:promo, :firstname, :lastname, :gender, :birthdate, :age, :github)
    ");

    //Execute la requête
    $push->execute(array('test','test','test','M','test','20','test'));

	// Ferme la transaction
    $push->closeCursor();

    // Commit les données
    $bdd->commit();

} catch(Exception $e) {
    
    $bdd->rollback();
    echo 'Erreur : ' . $e->getMessage();

}
```

## Exercice

- Créer une requête préparée pour ajouter des données qui s'effectue simplement quand on charge la page dans un premier temps, avec un message de succès. (Et Vérifier dans sa bdd si c'est ajouté)

- Créer une requête préparée pour UPDATE les données ajoutée précédemment, avec un message de succès. (Et Vérifier)

- Créer une requête préparée pour DELETE les données ajoutée précédemment, avec un message de succès. (Et Vérifier)

### Doc

PDO::beginTransaction -> http://php.net/manual/fr/pdo.begintransaction.php

PDO::prepare -> http://php.net/manual/fr/pdo.prepare.php

PDO::execute -> http://php.net/manual/fr/pdostatement.execute.php

PDO::exec -> http://php.net/manual/fr/pdo.exec.php

PDO::closeCursor -> http://php.net/manual/fr/pdostatement.closecursor.php

PDO::commit -> http://php.net/manual/fr/pdo.commit.php

PDO::rollback -> http://php.net/manual/fr/pdo.rollback.php