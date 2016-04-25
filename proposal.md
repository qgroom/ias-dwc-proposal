We propose adding an additional term to the Darwin Core (DwC) standard to express information on the indigenousness of taxa. We also propose vocabularies for pre-existing terms in DwC to make their meaning more clear and the data they contain more useful.

To improve the management and reduce the spread of invasive alien species (IAS) horizon scanning and impact assessments should be conducted regularly as part of a routine monitoring. However, these assessments are difficult to automate because the source data lacks common formats and standards. Improved interoperability would allow the creation of repeatable workflows for rapid processing. A similar situation exists for the assessment of conservation statuses for Red Lists. Again, the lack of machine readable resources and inadequate standards prevents automation of the process. Ideally, such assessments could be run regularly or as soon as new data becomes available.

Basic pieces of information required for horizon scanning, impact assessment and red listing are whether the species is native to the area in question and does it currently lives there. This information is frequently collected in species checklists and observations, but currently it is difficult to communicate these concepts in DwC, either due to a lack of fields or to the lack of clear advice on suitable controlled vocabularies. Furthermore, information on how an organism came to live in a location is needed for these assessment and can additionally be used to provide useful information for import controls.

DwC contains the term **establishmentMeans** with the definition of *“The process by which the biological individual(s) represented in the Occurrence became established at the location”*. In the DwC documentation it is suggested to use a controlled vocabulary and it gives the following terms as examples, *"native", "introduced", "naturalised", "invasive"* and *“managed"*. The term’s name and definition suggest that it refers to the introduction pathway, however some examples relate to the impact and longevity of the species and none of the examples actually define a pathway as such. A similar situation exists for the term **occurrenceStatus**, although the field exists in DwC it can be interpreted in different ways and clearer guidance to users would help distinguish this term from other similar terms, such as **individualCount**.

Some suggested vocabularies exist for the required terms and we suggest formalizing these in DwC and building on them, rather than defining new vocabularies.

#Origin

##Justification

We value a region’s indigenous organisms because they give a unique character to different areas and habitats. Therefore we need information on the native status of an organism to make conservation assessments and direct policy towards IAS. This requires a new term in DwC and we also suggest a suitable controlled vocabulary for this term.

The term and suggested vocabulary has been adapted from the IUCN definitions ([http://www.iucnredlist.org/technical-documents/red-list-training/iucnspatialresources](http://www.iucnredlist.org/technical-documents/red-list-training/iucnspatialresources) accessed 24 Apr 2016). The only change was to add the distinction of introduction before and after 1500, because this is widely used in Europe to distinguish ancient and modern introductions.

##Definition

To express the concept that a taxon has either been introduced by human activity or occurs naturally in a location and has done so before the impact of modern humans.

##Suggested controlled vocabulary

* Native – The species either is or was native to the area
* Reintroduced – The species either is or was reintroduced through human activity, either on purpose or accidentally. It is implied that the species was originally native at the location. 
* Introduced – The species either is or was introduced outside of its historical distribution range through either through direct or indirect human activity.
  * Introduced on or before 1500 – synonym of archaeophyte. A subcategory of introduced to acknowledge the importance of modern long distance transport in the introduction of species.
  * Introduced after 1500 – synonym of neophyte. A subcategory of introduced. An Organism introduced from the beginning of the Modern Era.
* Vagrant – Synonymous with casual. The species has lived or occurs sporadically at the location but is not considered native
* Origin Uncertain – The species’ origin in an area is not known, it may be native, reintroduced or introduced.

##Comment

##Term group

Occurrence
 
#occurrenceStatus 

##Justification

Many species checklists express whether a taxon occurs in a region at the time of publication or whether it has become extinct. The most obvious field for this information is **occurrenceStatus**, but currently the DwC documentation only suggests “present” and “absent” as example field entries. However, presence and absence can equally be expressed using the field **individualCount** or **organismQuantity** and **organismQuantityType** terms. We suggest that **individualCount**, **organismQuantity** and **organismQuantityType** are best used to indicate the presence or absence of a taxon during a surveying event. In contrast **occurrenceStatus** is best used in the context of a checklist where the assessment comes from a reasoned analysis of the evidence that leads to the assignment of presence or extinction. 

##Definition

From [http://rs.tdwg.org/dwc/terms/Occurrence](http://rs.tdwg.org/dwc/terms/Occurrence)

*“A statement about the presence or absence of a Taxon at a Location. Recommended best practice is to use a controlled vocabulary.”*

##Suggested controlled vocabulary

We suggest changing the documentation to suggest a controlled vocabulary in line with the IUCN definitions ([http://www.iucnredlist.org/technical-documents/red-list-training/iucnspatialresources](http://www.iucnredlist.org/technical-documents/red-list-training/iucnspatialresources) accessed 24 Apr 2016).

* Extant
* Possibly Extant
* Possibly Extinct
* Extinct
* Extinct (post 1500)
* Present
* Presence Uncertain

##Comment

##Term group

Occurrence

#establishmentMeans

##Justification

Invasive species use many pathways to colonize new areas. Information on these pathways can be used for management, prevention and control purposes. The proposal is to create a standard vocabulary that matches the definition of **establishmentMeans** so that it can be more effectively used. The definition of **establishmentMeans** will remain the same.

##Definition

From [http://rs.tdwg.org/dwc/terms/establishmentMeans](http://rs.tdwg.org/dwc/terms/establishmentMeans)

*“The process by which the biological individual(s) represented in the Occurrence became established at the location. Recommended best practice is to use a controlled vocabulary.”*

##Suggested controlled vocabulary

Taken from, Convention on Biological Diversity (2014a) Pathways of Introduction of Invasive Species, their Prioritization and Management. UNEP/CBD/SBSTTA/18/9/Add.1. Secretariat of the Convention on Biological Diversity, Montreal. Which is an adaption of the hierarchical scheme proposed by Hulme et al. (2008) Grasping at the routes of biological invasions: a framework for integrating pathways into policy, *Journal of Applied Ecology*, **45**: 403–414;

  * Release
  * Biological control
  * Erosion control/ dune stabilization
  * Fishery in the wild
  * Hunting
  * Landscape/flora/fauna “improvement” in the wild
  * Introduction for conservation purposes or wildlife management
  * Release in nature for use
  * Other intentional release
* Escape
  * Agriculture
  * Aquaculture / mariculture
  * Botanical garden/zoo/aquaria
  * Pet/aquarium/terrarium species
  * Farmed animals
  * Forestry
  * Fur farms
  * Horticulture
  * Ornamental purpose other than horticulture
  * Research and ex-situ breeding
  * Live food and live bait
  * Other escape from confinement
* Contaminant
  * Contaminant nursery material
  * Contaminated bait
  * Food contaminant
  * Contaminant on animals
  * Parasites on animals
  * Contaminant on plants
  * Parasites on plants
  * Seed contaminant
  * Timber trade
  * Transportation of habitat material
* Stowaway
  * Angling/fishing equipment
  * Container/bulk
  * Hitchhikers in or on airplane
  * Hitchhikers on ship/boat
  * Machinery/equipment
  * People and their luggage/equipment
  * Organic packing material
  * Ship/boat ballast water
  * Ship/boat hull fouling
  * Vehicles
  * Other means of transport
* Corridor
  * Interconnected waterways/basins/seas
  * Tunnels and land bridges
* Unaided

##Comment

##Term group

Occurrence
