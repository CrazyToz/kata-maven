# TIPS

## Générer un nouveau projet avec l'invité de commande

```shell
mvn archetype:generate -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4
```

## Centraliser la gestion des dépendances existantes

```xml
<dependencyManagement>
    <dependencies>
        <dependency>
            ...
        </dependency>
    </dependencies>
</dependencyManagement>
``` 

## Créer un projet war

Un fichier **web.xml** doit être présent, en général dans le dossier **/srv/webapp/WEB-INF**

```xml
<?xml version="1.0" encoding="ISO-8859-1"?>
<!DOCTYPE web-app
        PUBLIC "-//Sun Microsystems, Inc.//DTD Web Application 2.5//EN"
        "http://java.sun.com/dtd/web-app_2_5.dtd">

<web-app>

</web-app>
```

## Filtrer une resource

```xml
<project>
  ...
  <build>
    ...
    <resources>
      <resource>
        <directory>src/main/resources-filtered</directory>
        <filtering>true</filtering>
      </resource>
      ...
    </resources>
    ...
  </build>
  ...
</project>
```

# Ressources

[Maven Lifecycle](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html)
[Maven resources](https://maven.apache.org/plugins/maven-resources-plugin/examples/filter.html)

