# Markup HTML5

Les balises qui peuvent apparaître dans les fichiers AE-XML sont globalement définis dans les fichiers XSD, mais la nature de la balise HTML5 nécessite plus d'informations que nous apportons ici. La balise HTML5 peut apparaître à plusieurs endroits. Il contient obligatoirement une balise `<![CDATA[]]>` avec du markup qui respecte la spécification HTML5 dedans. 

#### Exemple : 
```xml
<NewsItem>
  <rightsInfo>...</rightsInfo>
  <itemMeta>...</itemMeta>
  <contentMeta>...</contentMeta>
  <contentSet>
    <HTML5><![CDATA[
        <p>On peut mettre du markup HTML5 à l'intérieur de cette balise</p>
        <p>Tout ce qui est valide selon la spécification HTML5 vaut</p>
    ]]></HTML5>
  </contentSet>
</NewsItem>
```
