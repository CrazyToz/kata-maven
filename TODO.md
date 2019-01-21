# Objectif

Définir une architecture **n-tier** où le projet sera décomposé en trois couches : 
* core **(jar)**
* dao **(jar)**
* webapp **(war)**

En terme de dépendances, **webapp** dépend de **core** qui dépend lui de **dao**.

# TODO

1. Transformer le pom existant en pom dit **parent**
2. Créer 3 **sous-modules**, chacun correspondant à une couche de l'architecture applicative.
3. Packager le projet parent, les enfants doivent être buildés en même temps.
4. Centraliser la gestion des dépendances existantes