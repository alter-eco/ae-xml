# AE-XML

### \[Travail en cours\]

### Description

##### De quoi s'agit-il ?

Un format structuré pour les contenus produits par [Alternatives Economiques](https://www.alternatives-economiques.fr), nouveau pour 2018. Il remplace l'ancien format, en place depuis le milieu des années 2000.

##### Où est-il utilisé ?

Il est utilisé en interne pour communiquer entre le logiciel de PAO (K4 de vjoon) et le site éditorial.

##### Sur quoi se base-t-il ?
Ce format est principalement basé sur celui de l'IPTC de [NewsML-G2](https://iptc.org/standards/newsml-g2/).

##### Pourquoi un format spécifique au lieu d'utiliser NewsML ? 

La simple mise en place de NewsML nous n'est pas intéressante parce que d'un côté ce format comprend un niveau de compléxité trop élévé quant aux [vocabulaires contrôlés](https://iptc.org/std/NewsML-G2/guidelines/#controlled-vocabularies-and-qcodes), et de l'autre son système d'imbrication de contenus les uns dans les autres est lourd et verbeux. AE-XML en résulte de cette réflexion en tant qu'un sous-ensemble ainsi qu'une bifurcation par rapport au format NewsML.

Pour résumer, nous ne respectons pas le format NewsML mais préservons sa logique de base.

### Structure

Il y a trois types d'entité ; `publication`, `long`, et `short`, mais comme avec le format NewsML, toute entité partage une structure de base.

`publication` - pour les numéros
`long` - pour les articles, entretiens, éditos, chroniques, recensions de livres, dossiers
`short` - pour les brèves, encadrés, graphiques

[test](/ae-xml/tree/master/xsd)

### Exemples 

Voir les [exemples](https://github.com/alter-eco/ae-xml/tree/master/examples) selon les types de contenus. Chaque exemple est accompagné d'un fichier du format XML précedent dont le nom termine en `.old.xml`
