# Proposal

## Executive summary

For better interoperability of invasive species information, we propose adding a new term to the Darwin Core (DwC) standard: `origin`, to express information on the indigenousness of taxa. We also propose vocabularies for the existing terms `occurrenceStatus`  and `establishmentMeans` to make their meaning more clear and the data they contain more useful.

## Context

To improve the management and reduce the spread of invasive alien species (IAS) horizon scanning and impact assessments should be conducted regularly as part of a routine monitoring. However, these assessments are difficult to automate because the source data lack common formats and standards. Improved interoperability would allow the creation of repeatable workflows for rapid processing. A similar situation exists for the assessment of conservation statuses for Red Lists. Again, the lack of machine readable resources and inadequate standards prevents automation of the process. Ideally, such assessments could be run regularly or as soon as new data becomes available.

Basic pieces of information required for horizon scanning, impact assessment and red listing are whether the species is native to the area in question and does it currently live there. This information is frequently collected in species checklists and observations, but currently it is difficult to communicate these concepts in DwC, either due to a lack of fields or to the lack of clear advice on suitable controlled vocabularies. Furthermore, information on how an organism came to live in a location is needed for these assessment and can additionally be used to provide useful information for import controls.

DwC contains the term [establishmentMeans](http://rs.tdwg.org/dwc/terms/index.htm#establishmentMeans) with the following definition:

> The process by which the biological individual(s) represented in the Occurrence became established at the location. Recommended best practice is to use a controlled vocabulary.

The examples listed in the comment are:

```
native
introduced
naturalised
invasive
managed
```

The term’s name and definition suggest that it refers to the introduction pathway, however some examples relate to the impact and longevity of the species and none of the examples actually define a pathway as such. A similar situation exists for the term [occurrenceStatus](http://rs.tdwg.org/dwc/terms/index.htm#occurrenceStatus), although the field exists in DwC it can be interpreted in different ways and clearer guidance to users would help distinguish this term from other similar terms, such as [individualCount](http://rs.tdwg.org/dwc/terms/index.htm#individualCount).

Some suggested vocabularies exist for the required terms and we suggest formalizing these in DwC and building on them, rather than defining new vocabularies.

Sponsers:
Quentin Groom - Botanic Garden Meise, Belgium

## origin (new term)

### Justification

We value a region’s indigenous organisms because they give a unique character to different areas and habitats. Therefore we need information on the native status of an organism to make conservation assessments and direct policy towards IAS. This requires a new term in DwC and we also suggest a suitable controlled vocabulary for this term.

We propose adopting the term `origin` and suggested vocabulary from the [IUCN definitions](http://www.iucnredlist.org/technical-documents/red-list-training/iucnspatialresources) (accessed 24 Apr 2016). The only change was to add the distinction of introduction before and after ~~1500~~ the beginning of the modern era, because this is widely used in Europe to distinguish ancient and modern introductions. In Europe 1500 is usually used as the date for the beginning of the modern era, however, it is noted that the beginning of the modern era from a biogeographical standpoint started later in some places, such as New Zealand.

### Definition

To express the concept that a taxon has either been introduced by human activity or occurs naturally in a location and has done so before the impact of modern humans.

### Suggested controlled vocabulary

[origin vocabulary](vocabulary/origin.tsv)

### Comment

### Term group

Occurrence
 
## occurrenceStatus

### Justification

Many species checklists express whether a taxon occurs in a region at the time of publication or whether it has become extinct. The most obvious field for this information is `occurrenceStatus`, but currently the DwC documentation only suggests `present`, `absent`, `common`, `irregular`, `rare` and `doubtful` as example field entries. However, presence, absence and rarity can equally be expressed using the field `individualCount` or `organismQuantity` and `organismQuantityType` terms. We suggest that `individualCount`, `organismQuantity` and `organismQuantityType` are best used to indicate the abundance of a taxon during a surveying event or observation. In contrast `occurrenceStatus` is best used in the context of a checklist where the assessment comes from a reasoned analysis of the evidence that leads to the assignment of presence or extinction. 

### Definition

Adapted from [http://rs.tdwg.org/dwc/terms/occurrenceStatus](http://rs.tdwg.org/dwc/terms/occurrenceStatus):

> A statement about the continued presence of a Taxon at a Location. Recommended best practice is to use the vocabulary of the IUCN term for Presence.

### Suggested controlled vocabulary

We suggest changing the documentation to suggest a controlled vocabulary in line with the [IUCN definitions](http://www.iucnredlist.org/technical-documents/red-list-training/iucnspatialresources) (accessed 24 Apr 2016). However, we have retained the term absent from the original terms for back compatibility.

[presence vocabulary](vocabulary/presence.tsv)

### Comment

### Term group

Occurrence

## establishmentMeans

### Justification

Invasive species use many pathways to colonize new areas. Information on these pathways can be used for management, prevention and control purposes. The proposal is to create a standard vocabulary that matches the definition of `establishmentMeans` so that it can be more effectively used. The definition of `establishmentMeans` will remain the same.

### Definition

From [http://rs.tdwg.org/dwc/terms/establishmentMeans](http://rs.tdwg.org/dwc/terms/establishmentMeans):

> The process by which the biological individual(s) represented in the Occurrence became established at the location. Recommended best practice is to use a controlled vocabulary of the Convention on Biological Diversity.

### Suggested controlled vocabulary

Taken from, Convention on Biological Diversity (2014a) Pathways of Introduction of Invasive Species, their Prioritization and Management. UNEP/CBD/SBSTTA/18/9/Add.1. Secretariat of the Convention on Biological Diversity, Montreal. Which is an adaption of the hierarchical scheme proposed by Hulme et al. (2008) Grasping at the routes of biological invasions: a framework for integrating pathways into policy, *Journal of Applied Ecology*, **45**: 403–414;

Also see: Scalera, R., Genovesi, P., Booy, O., Essl, F., Jeschke, J., Hulme, P., McGeoch, M., Pagad S., Roy, H., Wolf-Christian S. & Wilson J. (2016) Progress toward pathways prioritization in compliance to Aichi target 9. Convention of Biological Diversity, subsidiary body on scientific technical and technological advice, twentieth meeting, UNEP/CBD/SBSTTA/20/INF/5

[pathways vocabulary](vocabulary/pathway.tsv)

### Comment

### Term group

Occurrence
