schematronReference
===================
schematronReference is a reference for the Schematron ISO standard ISO/IEC 19757 - Document Schema Definition Languages (DSDL) - Part 3: Rule-based validation - Schematron.
Its intention is to provide a valuable information resource for those interested in learning Schematron as well as a guide to work with in an everyday development practice.

Use the Reference
===================
Please download the latest built in your favorite file format to read the reference, or visit http://www.schematron.de/

Contribute
===================
Please help to translate the schematronReference in other languages:
* Create a copy of the DITA reference file you want to translate (for example "iso-schematron-title-element-en.dita" to translate the description of the &lt;sch:title&gt; element)
* Change the filename to {ORIGINAL FILENAME}-{COUNTY CODE OF YOUR TRANSLATION}.dita (for example to "iso-schematron-title-element-ru.dita", if you want to translate the original document into russian)
* Change the @xml:language attribute value at the reference element to your country code (for example &lt;rence id="iso-schematron-title-element" xml:language="ru">&g; if you want to translate the original document into russian)
* Replace the existing text with your translation of this text
* When your translation is finished, open the type-chapter.ditamap, element-chapter.ditamap or attribute-chapter.ditamap document where the original document you have translated is referenced
* Insert a new &lt;topicref&gt; Element in this ditamap document after the &lt;topicref&gt; element of the original document you have translated
* Add the @href attribute on the new &lt;reference&gt; element and insert your documents name as the attribute value
* Commit your changes

Repo Organisation
===================
* schematronReference > The repo root directory 
 * built > The built directory: All version of the schematronReference
  * [schematronReference-{VERSION}.zip]+ > A Version of the schematronReference
 * src > The source directory: Take a look and contribute to the workingdraft of the next schematronReference version
  * dita > The working directory: contribute by helping to translate the reference in other languages
   * schematronReferernce.ditamap > DITA Bookmap to reference the DITA map documents
   * attribute-chapter.ditamap > DITA map to reference the DITA topic documents for the attribute descriptions
   * element-chapter.ditamap > DITA map to reference the DITA topic documents for the element descriptions
   * type-chapter.ditamap > DITA map to reference the DITA topic documents for the type descriptions
   * [iso-schematron-{NAME}-{(attribute|element|type)}-{COUNTRY CODE}.dita]+
  * schema > The schema sources for the reference
   * relaxng > The folder of the schema for schematron as a Relax NG document
    * ISO-IEC-19757-3-schematron.rnc > The original schema for schematron as defined in Annex A of the ISO-IEC 19757-3 standard (WARNING: This document is NOT valid)
    * ISO-IEC-19757-3-schematron-fixed.rnc > The fixed version of the original schema for schematron.
   * xsd > The folder of the schema for schematron as a W3C XML Schema document
    * schematron-base.xsd > Result of the Trang conversion of "ISO-IEC-19757-3-schematron-fixed.rnc" with resolved &lt;xs:group&gt; and &lt;xs:attributeGroup&gt; elements and with global definitions of all structures for easier annotation and transformation
  * oxygen-documentation > The documentation sources for the reference created with the &lt;oXygen/&gt; XML Editor Version 15.0 
   * img > The image directory 
    * [schematron-base_xsd_{(Simple_Type|Element)}_sch_{NAME}.jpeg]+ > diagramms of the contentmodels for a schematron structure
   * schematron-base.html > The HTML index file of the oXygen documentation
   * comp.html > Not very interesting file
   * comp.html > Not very interesting file
   * docHtml.css > Not very interesting file
 * schematronReference-{VERSION}.zip > Download: The latest Version of the schematronReference published on http://www.schematron.de/
