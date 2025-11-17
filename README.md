# Commandes utilitaires pour la création d'une API REST avec Symfony

## 🚀 Exécution des commandes pour les installations de dépendances

Installation du maker-bundle pour pouvoir générer certains éléments via la ligne de commande :
```bash
composer require symfony/maker-bundle --dev
```

Installation de Doctrine
```
composer require orm
```

Installation des fixtures
```
composer require orm-fixtures --dev
```

Installation du serializer
```
composer require symfony/serializer-pack
```

Installation du package pour gérer la validation des champs requis lors d'une requête avec POST
```
composer require symfony/validator doctrine/annotations
```









## 🚀 Exécution des commandes pour la générations des éléments avec php bin/console


Création d'une entité
```
php bin/console make:entity
```

Création de la base de données après configuration du fichier .env.local
```
php bin/console doctrine:database:create
```

Mise à jour de la base de données après une modification importante dans les entités
```
php bin/console doctrine:schema:update --force
```

Lancer une fixture
```
php bin/console doctrine:fixtures:load
php bin/console doctrine:fixtures:load --group={{fixture_group}} --append
```

Génération d'un controller
```
php bin/console make:controller
```

Génération d'un evenement pour éviter que les erreurs s'affichent en HTML mais plutot en JSON
```
php bin/console make:subscriber
```