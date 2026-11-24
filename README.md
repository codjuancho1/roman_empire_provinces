#Roman-Empire-Datasets

• roman_provinces_l and roman_provinces_p:

Roman provincial divisions (represented as lines and polygons), spanning from the early Republic to the conquest of Mesopotamia under Septimius Severus. Both the “roman_provinces_l” (lines) and “roman_provinces_p” (polygons) files follow the same format, with chronological divisions covering both the Republic and the Principate. Each stage is further subdivided into shorter periods (for the Republic) or dynasties (for the Principate). The design allows corresponding periods in both layers to be activated simultaneously, ensuring chronological alignment. For certain provinces—such as the Alpes Graiae and the Alpes Poeninae—the dates of their creation are a subject of debate. In cases of significant discrepancy, a specific date has been selected, as it is necessary to establish a precise moment for the province to appear in at least one of the sub-periods. To define the boundaries of each province, mountain ranges, drainage basins, and river courses were used as references. The layers employed for this delimitation include Esri’s “World Hillshade” (accessible directly from QGIS) and the Copernicus dataset titled “EU-Hydro River Network Database 2006-2012 (vector), Europe” (easily found via an online search). Furthermore, the locations of Roman cities from the period have been individually verified to ensure they fall within their respective provinces—a step particularly important for cities situated near borders. Given that it is sometimes impossible to determine the exact path of a provincial boundary, the priority has been to ensure that Roman cities are included within their correct, corresponding province. The attribute table for the “roman_provinces_p” polygon layer contains several columns:

▪ “fid”: A column containing a unique identification number for each spatial feature, automatically assigned by QGIS. 

▪ “latin”: The Latin name of the province in question. 

▪ “castellano”: The Spanish name of the province in question. 

▪ “creation”: A text field indicating the years during which the province was created. This serves solely as a reference; as it is a text-string field, it cannot be used for calculations. 

▪ “creation_start”: The year in which the creation of the province began. In most cases, this coincides with the year shown in the following field. 

▪ “creation_end”: The year in which the creation of the province was completed, or the year from which definitive evidence of its existence dates. 

For example, for the province of “Epirus,” the “creation_start” field indicates the year 103 (103 AD) and the “creation_end” field the year 114 (114 AD); although the exact date of its creation is unknown, it is understood to have occurred within this time frame. 

The visualization style is structured such that provinces created through the division of earlier ones—for instance, Pannonia Inferior and Pannonia Superior, formed by splitting the territory of the province of Pannonia (where the combined boundaries of the two new provinces match those of the original province prior to its division)—overlap with the preceding provinces. This avoids the unnecessary duplication of spatial features while preserving the specific creation dates for each province. 

The file named “roman_provinces_l” follows the same logic. However, in this case, the names do not refer to a single province, but rather to two provinces separated by a specific linear segment (for example, Gallia Lugdunensis/Gallia Narbonensis). Finally, it is worth noting that it is highly recommended to combine these provincial boundaries with the city layers provided by the Ancient World Mapping Center (AWMC) at the University of North Carolina, as well as with the extraordinary mapping of Roman roads carried out by the Itiner-e.org project. Both sources provide their data openly and free of charge via their respective websites. In particular, we have used the “coastline” layer provided by the AWMC to establish the coastal boundaries of the provincial polygons. Likewise, the excellent mapping of Roman roads and settlements produced by the Digital Britannia project—which also offers open access to its data—is particularly noteworthy. 

To the best of our knowledge, this is the most accurate provincial division currently available for this period; however, any corrections would be welcome. We are, of course, deeply grateful for the immense collective effort of the cartographers, historians, and enthusiasts of Roman history who have made it possible to define these provincial boundaries with such a high level of detail. As time permits, we plan to gradually develop a separate file—in the form of a guide or information note—containing the complete bibliography used in the creation of these datasets. 
• “rhine_danube_limes”:
A point layer showing legionary bases, *civitas* capitals, various cities (*coloniae* and *municipia*), auxiliary forts, and naval forts along the Roman *limes*—from the mouth of the Danube to the mouth of the Rhine. The spatial features are categorized by several attributes: settlement type (“settlement,” “legionary base,” “*civitas* capital,” “city (*colonia*/*municipium*),” “auxiliary fort,” and “naval fort”) and chronological period (ranging from the Augustan-Tiberian era to Late Antiquity). The layer includes a pre-configured style that classifies auxiliary forts, legionary bases, and naval forts according to their period. While cities and *civitas* capitals are not included in this specific style, they can easily be displayed by adding a few rules. There are also fields for the Latin name (“Romano”/“Roman”) and the modern name (“Actual”/“Modern”).

• “pannonia_wetlands”: A vector representation of the flood-prone and predominantly inundated areas of the Pannonian Plain, as they existed prior to the hydrological engineering projects of the 20th century. The source for this layer is provided in the bibliography file. 

• “germania_wetlands”: A vector representation of the heathlands and marshy areas in northwestern Germany, as well as the region surrounding the mouths of the Rhine and Meuse rivers. The source for this layer is provided in the bibliography file. 

• “litus_saxonicum”: A layer representing the various locations and forts that comprised the coastal defensive system known as the *Litus Saxonicum*.

We intend to periodically update this GeoPackage, incorporating an increasing number of historical features. Changes and updates will be documented in a log, which will be updated as new elements are added.
