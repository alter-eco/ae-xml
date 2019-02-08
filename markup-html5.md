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

- embeds
- notes de bas de page
- marginalia

## Embeds

On a le concept de pouvoir imbriquer (embed) de contenus dans d'autres. Par exemple, un graphique dans un article, ou bien un article dans un article dans le cadre d'un dossier. Nous utilisons la balise native HTML5 `<span>` dans ces cas, avec l'attribut data-embed-id-id. 

#### Exemple :
```xml
<?xml version="1.0" encoding="utf-8"?>
<NewsItem>
  <rightsInfo>...</rightsInfo>
  <itemMeta>...</itemMeta>
  <contentMeta>...</contentMeta>
  <contentSet>
    <HTML5><![CDATA[
        <p>Un peu de texte</p>
        <span data-embed-id="K4-XXXXX"></span>
        <p>Un peu plus de texte</p>
      ]]></HTML5>
  </contentSet>
</NewsItem>
```

## Notes de bas de page

Pour les notes de bas de page, nous avons retenu les propositions du W3C en matière de notes de bas de page. Plus précisement, [l'exemple numéro 14](https://www.w3.org/TR/html53/common-idioms-without-dedicated-elements.html#footnotes).

#### Exemple :
```xml
<?xml version="1.0" encoding="utf-8"?>
<NewsItem>
  <rightsInfo>...</rightsInfo>
  <itemMeta>...</itemMeta>
  <contentMeta>...</contentMeta>
  <contentSet>
    <HTML5><![CDATA[
        <p>Un peu de texte <a id="ref-1" href="#footnote-1">1</a></p>
        <p>Et un peu plus de texte <a id="ref-2" href="#footnote-2">2</a></p>
        <section id="footnotes">
          <p id="footnote-1"><a href="#ref-1">1</a> Le texte de la première note de bas de page</p>
          <p id="footnote-2"><a href="#ref-2">2</a> Le texte de la deuxième note de bas de page, <a href="#">elle peuvent contenir de liens</a></p>
        </section>
      ]]></HTML5>
  </contentSet>
</NewsItem>
```
## Marginalia

On reprend globalement le principe des notes de bas de page, mais avec des astériques, pour distinguer, et l'utilisation des balises `<dl>`.


#### Exemple :
```xml
<?xml version="1.0" encoding="utf-8"?>
<NewsItem>
  <rightsInfo>...</rightsInfo>
  <itemMeta>...</itemMeta>
  <contentMeta>...</contentMeta>
  <contentSet>
    <HTML5><![CDATA[
        <p>Texte du contenu, avec un marginalia<sup><a id="ref-*" href="#marginalia-*">*</a></sup></p>
        <p>Ensuite un deuxième marginalia<sup><a id="ref-**" href="#marginalia-**">**</a></sup></p>
        <dl>
          <div id="marginalia-*">
            <dt><a href="#ref-*">*</a> Titre du premier marginalia</dt>
            <dd><p>Texte du marginalia</p></dd>
          </div>
          <div id="marginalia-**">
            <dt><a href="#ref-**">**</a> Titre du deuxième marginalia</dt>
            <dd><p>Texte du marginalia</p></dd>
          </div>
        </dl>
      ]]></HTML5>
  </contentSet>
</NewsItem>
```