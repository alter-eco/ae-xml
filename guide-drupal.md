## Guide de mise en place sur le site éditorial (Drupal 7)

### Types de contenu 

Par nom système

- `article`
- `media_content`
- `ouvrage`
- `issue`

### `article`

##### `title`

NewsItem.contentMeta.title

##### `field_subhead`

NewsItem.contentMeta.section

##### `field_doc_type`

NewsItem.contentMeta.genre

##### `field_user_reference`

NewsItem.contentMeta.author

##### `field_interview_with`

NewsItem.contentMeta.interviewee

##### `field_interviewer`

NewsItem.contentMeta.author

##### `field_has_chapo`

N/A

##### `field_chapo`

NewsItem.contentMeta.lead

##### `body`

NewsItem.contentSet.inlineXML

##### `field_press_review`

N/A

##### `field_image`

NewsItem.contentMeta.figure

##### `field_alternate_image_style`

N/A

##### `field_hide_image`

N/A

##### `field_thema`

NewsItem.contentMeta.subSection

##### `field_media_content_reference`

A supprimer

##### `field_reviewed_book_reference`

En attente

##### `field_marginalia`

NewsItem.contentMeta.marginalia.marginaliaItem

##### `field_similar_content_reference`

N/A

##### `field_more_content`

NewsItem.contentMeta.relatedInfo

##### `field_tags`

Champs à supprimer

##### `field_promoted`

N/A

##### `field_statut`

N/A

##### `field_sr`

N/A

##### `field_access`

N/A

##### `field_modification_date`

NewsItem.contentMeta.modified

##### `xmlsitemap`

N/A

##### `metatags`

N/A

##### `redirect`

N/A

##### `field_node_main_workflow`

N/A

##### `path`

N/A

##### `field_issue_relation`

NewsItem.itemMeta.parentPublication

##### `field_xml_code`

NewsItem.itemMeta.parentPublication

##### `field_xml_code_pere`

N/A

##### `field_cloned_content_source`

N/A

##### `field_authors_string`

N/A

##### `field_author_text`

NewsItem.contentMeta.author.description

##### `field_interview_with_text`

N/A

##### `field_interviewer_text`

NewsItem.contentMeta.interviewee.description

##### `field_translator_text`

N/A

##### `field_cacher_bloc_meme_sujet`

N/A

##### `field_cacher_bloc_a_lire`

N/A

##### `field_cacher_bloc_commentaires`

N/A

##### `field_medias`

En attente

### `media_content`

##### `title`

NewsItem.contentMeta.title

##### `exclude_node_title`

N/A

##### `field_subhead`

NewsItem.contentMeta.section

##### `field_technical_label`
##### `field_user_reference`

NewsItem.contentMeta.author

##### `field_doc_type`

NewsItem.contentMeta.genre

##### `field_media_type`
##### `field_file`

N/A

##### `field_image`

NewsItem.contentMeta.figure

##### `field_portfolio`

N/A

##### `field_link`

N/A

##### `field_comicstrip`

N/A

##### `field_table`

N/A

##### `field_iframe_height`

N/A

##### `field_fullscreen`

N/A

##### `field_alt_image`

N/A

##### `field_full_width_display`

N/A

##### `metatags`

N/A

##### `path`

N/A

##### `body`

NewsItem.contentSet.inlineXML

##### `field_media_source`

NewsItem.contentMeta.source

##### `field_thema`

N/A

##### `xmlsitemap`

N/A

##### `redirect`

N/A

##### `field_source_file`

N/A

##### `field_access`

N/A

##### `field_texte_pushmail`

N/A

##### `field_xml_code`

N/A

### `ouvrage`

##### `title`
##### `field_user_reference`
##### `field_reviewed_book_source`
##### `field_reviewed_book_author_line`
##### `field_reviewed_book_cover`
##### `xmlsitemap`
##### `path`
##### `redirect`
##### `metatags`

#### `issue`

##### `title`

NewsItem.contentMeta.title

##### `field_issue_type`

NewsItem.contentMeta.publicationId

##### `field_issue_pub_date_label`

NewsItem.contentMeta.issueDate

##### `field_issue_cover`

NewsItem.contentMeta.figure

##### `field_issue_numero`

NewsItem.contentMeta.issueNumber

##### `field_issue_price`

NewsItem.contentMeta.price

##### `field_issue_paragraphs`

NewsItem.contentMeta.itemSet

##### `field_issue_feat_content`

N/A

##### `field_issue_newsltr_feat_content`

N/A

##### `field_issue_nwsltr_feat_issues`

N/A

##### `field_promo_text_footer`

N/A

##### `field_issue_featured_articles`

N/A

##### `body`

NewsItem.contentSet.inlineXML

##### `path`

N/A

##### `redirect`

N/A

##### `xmlsitemap`

N/A

##### `field_xml_code`

N/A

##### `field_old_cms_id`

N/A

##### `metatags`

N/A

##### `field_numero_epuise`

N/A
