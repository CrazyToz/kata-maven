# Objectif

Définir une architecture **n-tier** où le projet sera décomposé en trois couches : 
* core **(jar)**
* dao **(jar)**
* webapp **(war)**

En terme de dépendances, **webapp** dépend de **core** qui dépend lui de **dao**.

# TODO

1. Ajouter la dépendance suivante au module **dao**, packager le projet puis inspecter le contenu du **war**. 
    
    ```xml
      <dependency>
        <groupId>com.oracle</groupId>
        <artifactId>ojdbc14</artifactId>
        <version>10.2.0.4.0</version>
      </dependency>
    ```
 
2. Ajouter la même dépendance dans le module **core**, et surchargeant la version de **dao** (9.0.2.0.0). Inspecter le contenu du war. Commenter la déclaration dans **dependencyManagement** puis inspecter le contenu du war.
    
3. Changer le scope de la dépendance en provided. Quel est l'impact à la compilation ? au déploiement ?
 
4. Creer un fichier **src/main/webapp/WEB-INF/application.properties** dans le module webapp, contenant la property **dummy.property=${dummy.property.value}**. Filtrer cette property afin d'obtenir, au packaging, un fichier contenant **dummy.property=some dummy value**.
 
