# L'anatomie d'un fichier AE-XML

Ce document détaille et complémente en langage humain ce que les fichiers `short.xsd`, `long.xsd`, et `publication.xsd` détaillent en langage informatique.

---

## `<NewsItem>`

La balise racine. Nous ne détaillons pas les propriétés de base de [l'XML Schema](https://www.w3.org/TR/xml-names/)

#### `@standard` - obligatoire



#### `@id` - obligatoire

L'identifiant unique du document, identique au nom du fichier. Pour un contenu `publication`, se construit de la manière suivante :

```
CodePublicationNuméroEdition
```

Pour un contenu `long` ou `short`, se construit de la manière suivante :

```
CodePublicationNuméroEdition-NuméroPage-LettrePositionPage
```

Donc, le deuxième article sur la page 54 dans le numéro 368 d'Alternatives Economiques serait `A368-054-B`, pendant que le premier article sur la page 32 dans le numéro 44 de l'Economie Politique serait `EP44-032-A`.

Les codes publication sont les suivants : 
* `A` - Alternatives Economiques
* `HS` - Alternatives Economiques Hors Series
* `EP` - L'Economie Politique
* `ST` - Santé et Travail

#### `@version` - obligatoire

La version du document. Commence à `1`, et incrémente avec chaque nouvelle version.

#### Exemple : 
```xml
<NewsItem 
  xmlns="https://www.alternatives-economiques.fr/"
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="https://www.alternatives-economiques.fr/ ../../../xsd/long.xsd"

  standard="AE-XML"
  id="A382-007-A"
  version="1"
  >
  <rightsInfo>...</rightsInfo>
  <itemMeta>...</itemMeta>
  <contentMeta>...</contentMeta>
  <contentSet>...</contentSet>
</NewsItem>
```
## `<rightsInfo>`

Contient des informations sur les droits du contenu. Contient les balises `<copyrightHolder>` et `<copyrightNotice>`.

### `<copyrightHolder>`

Le nom de l'entité qui detient le copyright.

### `<copyrightNotice>`

L'avertissement relatif aux droits.

#### Exemple : 
```xml
  <rightsInfo>
    <copyrightHolder>
      Alternatives Economiques
    </copyrightHolder>
    <copyrightNotice>
      Copyright 2018 Alternatives Economiques - Toute reproduction, même partielle, des textes, infographies et documents parus est soumis à l'autorisation préalable de l'éditeur.
    </copyrightNotice>
  </rightsInfo>
 ```

## `<itemMeta>`

Données rélatives à l'entité. Contient des informations sur le type de l'entité, l'état de publication de l'entité, s'il est sous embargo, s'il est lié à une autre entité.

## `<contentMeta>`

Données relatives au contenu de l'entité. Contient le gros du contenu en dehors du corps du texte, par exemple le titre, chapô, auteur, rubrique, date de création/modification, image associée etc.

## `<contentSet>`

Contenu de l'entité. Le contenu brut du texte, normalement mise en forme avec un balisage conforme HTML5.

