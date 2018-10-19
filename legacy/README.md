# Correspondance

## Balises

Ancien format | AE-XML | Situation |  HTML5 
-|-|-|-
`<AppelNote>`|obsolète|N/A|
`<AppelDef>`|obsolète|N/A| 
`<AppelUrl>`|`<a>`|Toute balise `<inlineXML>` avec `contenttype="text/html"`|[Oui](https://developer.mozilla.org/fr/docs/Web/HTML/Element/a)
`<Auteur>`|`<author>`|/NewsItem/contentMeta/author|Non
`<BiblioItem>`|`<relatedInfoItem>`|/NewsItem/contentMeta/relatedInfo/relatedInfoItem|Non
`<Chapeau>`|`<lead>`|/NewsItem/contentMeta/lead|Non
`<Code>`|N/A|N/A|Non
`<CodePère>`|`<parentItem>`|/NewsItem/itemMeta/parentItem|Non
`<DateRevue>`|`<created>`|/NewsItem/contentMeta/created|Non
`<Document>`|`<NewsItem>`|/NewsItem|Non
`<Emphasis>`|`<em>`|Toute balise `<inlineXML>` avec `contenttype="text/html"`|[Oui](https://developer.mozilla.org/fr/docs/Web/HTML/Element/em)
`<EnSavoirPlus>`|`<relatedInfo>`|/NewsItem/contentMeta/relatedInfo|Non
`<EntretienAvec>`|`<interviewee>`|/NewsItem/contentMeta/interviewee|Non
`<Exp>`|`<sup>`|Toute balise `<inlineXML>` avec `contenttype="text/html"`|[Oui](https://developer.mozilla.org/fr/docs/Web/HTML/Element/sup)
`<Fonction>`|`<description>`|/NewsItem/contentMeta/author/description ou /NewsItem/contentMeta/interviewee/description|Non
`<Image>`|`<figure>`|/NewsItem/contentMeta/figure|Non
`<Ind>`|`<sub>`|Toute balise `<inlineXML>` avec `contenttype="text/html"`|[Oui](https://developer.mozilla.org/fr/docs/Web/HTML/Element/sub)
`<Inter1>`|`<h2>`|Toute balise `<inlineXML>` avec `contenttype="text/html"`|[Oui](https://developer.mozilla.org/fr/docs/Web/HTML/Element/Heading_Elements)
`<Inter2>`|`<h3>`|Toute balise `<inlineXML>` avec `contenttype="text/html"`|[Oui](https://developer.mozilla.org/fr/docs/Web/HTML/Element/Heading_Elements)
`<Legende>`|`<caption>`|/NewsItem/contentMeta/figure/caption|Non
`<LienExt>`|`<embedded-content>`|Toute balise `<inlineXML>` avec `contenttype="text/html"`|Non
`<Marginalia>`|`<marginalia>`|/NewsItem/contentMeta/marginalia|Non
`<MotCle>`|obsolète||
`<Nom>`|`<surname>`|/NewsItem/contentMeta/author/surname|Non
`<Note>`|`<section id="footnotes">`|Toute balise `<inlineXML>` avec `contenttype="text/html"`|Oui
`<NoticeBiblio>`|`<>`||Non
`<Ouvrage>`|`<>`||
`<Para>`|`<p>`|Toute balise `<inlineXML>` avec `contenttype="text/html"`|[Oui](https://developer.mozilla.org/fr/docs/Web/HTML/Element/p)
`<Prenom>`|`<firstname>`|/NewsItem/contentMeta/author/firstname|Non
`<Rub>`|`<section>`|/NewsItem/contentMeta/section|Non
`<Sect1>`|obsolète||Non
`<Sect2>`|obsolète||Non
`<Sect3>`|obsolète||Non
`<Sect4>`|obsolète||Non
`<Source>`|`<source>`|/NewsItem/contentMeta/source|Non
`<SousRub>`|`<subject>`|/NewsItem/contentMeta/subject|Non
`<Strong>`|`<strong>`|Toute balise `<inlineXML>` avec `contenttype="text/html"`|[Oui](https://developer.mozilla.org/fr/docs/Web/HTML/Element/strong)
`<Sujet>`|`<>`||Non
`<Tete>`|`<>`||Non
`<Texte>`|`<inlineXML>`|/NewsItem/contentSet/inlineXML|Non
`<Titre>`|`<title>`|/NewsItem/contentMeta/title|Non
`<TitreCdrom>`|obsolète||Non
`<TitreRevue>`|obsolète||Non
`<TitreWeb>`|obsolète||Non
`<Unite>`|`<unit>`|/NewsItem/contentMeta/unit|Non


