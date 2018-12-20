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
        <p>Par exemple on peut avoir <a href="je-vais-nul-part.com">des liens</a></p>
        <h3>Des titres</h3>
        <blockquote>
          <p>Des citations !</p>
          <cite>Par Joe Tout-le-monde</cite>
        </blockquote>
        <p>On peut avoir des balises pour mettre le texte en <strong>gras</strong> ou en <em>italiques</em> ou en <sup>superscript</sup> ou bien <sub>subscript</sub></p>
        <p>Renseignez-vous sur <a href="https://www.w3.org/TR/html50/grouping-content.html#the-blockquote-element">https://www.w3.org/TR/html50/grouping-content.html#the-blockquote-element</a></p>
    ]]></HTML5>
  </contentSet>
</NewsItem>
```

Il y a néanmoins quelques règles de gestion spécifiques avec le format AE-XML. Elles gèrent les :

- marginalia
- embeds
- notes de bas de page