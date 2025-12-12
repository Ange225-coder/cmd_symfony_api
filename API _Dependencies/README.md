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

Installation du package pour gérer la validation des champs requis lors d'une requête avec POST et PUT
```
composer require symfony/validator doctrine/annotations
```

Installation de lexikJWT
```
composer require lexik/jwt-authentication-bundle
```

Installation de Hateoas et JMSSerializer
```
composer require willdurand/hateoas-bundle
```

Installation de Nelmio pour la documentation
```
composer require nelmio/api-doc-bundle
```

Installation du client HTTP pour interroger une API externe
```
composer require symfony/http-client
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

Génération de clé public et privé (JWT)
```
openssl genpkey -out config/jwt/private.pem -aes256 -algorithm rsa -pkeyopt rsa_keygen_bits:4096
openssl pkey -in config/jwt/private.pem -out config/jwt/public.pem -pubout
```