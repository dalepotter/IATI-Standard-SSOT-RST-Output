sector
======

``iati-activities/iati-activity/sector``

This is the reference page for the XML element ``sector``. See also the relevant overview page: :doc:`/activity-standard/overview/classifications` 

.. index::
  single: sector

Definition
~~~~~~~~~~


A recognised code, from a recognised vocabulary, classifying
the purpose of the activity. Sector MUST EITHER be reported
here OR at transaction level for ALL transactions


Rules
~~~~~








This element may occur any number of times.







Either ``sector`` or ``transaction/sector`` must be present.




Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/sector/.vocabulary:

@vocabulary
  An IATI code for the vocabulary (see codelist) used for sector classifications. If omitted, OECD DAC 5-digit Purpose Codes are assumed.
  
  It is recommended that OECD DAC 5-digit Purpose Codes are used wherever possible. It is also recommended that if a publisher has its own classification system or systems then the vocabularies 99 or 98 (Reporting Organisation's own vocabularies) should be used in addition to DAC codes.
  
  Publishers using 98 or 99 must also include a narrative in the narrative element.
  
  Note that if multiple sector codes are used in multiple vocabularies, then each vocabulary’s percentages should add up to 100.
  
  Sector can also be reported at the transaction level rather than the activity level. Sector must only be reported at EITHER transaction level OR activity level.


  This value must be of type xsd:string.


  This value must be on the :doc:`SectorVocabulary codelist </codelists/SectorVocabulary>`.



  
.. _iati-activities/iati-activity/sector/.vocabulary-uri:

@vocabulary-uri
  The URI where this vocabulary is defined. If the vocabulary is 99 or 98 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.


  This value must be of type xsd:anyURI.



  
.. _iati-activities/iati-activity/sector/.code:

@code
  The code for the sector.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`Sector codelist </codelists/Sector>`, if the relevant vocabulary is used.



  
.. _iati-activities/iati-activity/sector/.percentage:

@percentage
  The percentage of total commitments or total activity budget to this item. Content must be a decimal number between 0 and 100 inclusive, with no percentage sign. All reported sectors from the same vocabulary MUST add up to 100.


  This value must be of type xsd:decimal.



  



Example Usage
~~~~~~~~~~~~~
Example ``sector`` of an ``iati-activity``.

| The ``@vocabulary`` attribute declares a valid code (*2*) from the *SectorVocabulary* codelist.
| An example value *111* from this vocabulary is declared with the ``@code`` attribute.

.. code-block:: xml

	<sector vocabulary="2" code="111" />

| The ``sector`` element can be repeated in any ``iati-activity``.
| When multiple ``sector`` are declared, then the ``@percentage`` values should sum to 100% for the specific ``iati-activity``.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--sector starts-->
	:end-before: <!--sector ends-->

| The ``vocabulary`` is used to declare which ``SectorVocabulary`` classification list is in use. If this is omitted, then IATI assumes a *SectorVocabulary* of *1* (OECD DAC CRS Purpose Codes (5 digit)).

| If a vocabulary is not on the *SectorVocabulary* codelist, then the value of *99* or *98* (Reporting Organisation) should be declared.

| If a publisher uses a vocabulary of 98 or 99 (i.e. 'Reporting Organisation'), then the ``@vocabulary-uri`` attribute should also be used, for example:

.. code-block:: xml

    <sector vocabulary="99" vocabulary-uri="http://example.com/vocab.html" code="A1" />


Changelog
~~~~~~~~~

2.03
^^^^
The ``@vocabulary`` attribute definition was `updated <https://discuss.iatistandard.org/t/bug-fix-implementing-checks-on-percentage-attributes/983>`__ (to remove the % sign).

2.02
^^^^
The ``vocabulary-uri`` attribute was `added <http://support.iatistandard.org/entries/105713163-Add-URI-attribute-to-elements-where-Reporting-organisation-vocabularies-are-used>`__.

2.01
^^^^
Freetext is no longer allowed with this element.  It should `now be declared <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#narrative-new-elements>`__  with the new child ``narrative`` element, but only in particular use-cases.

1.03
^^^^
Where used, the @percentage attribute is now designated as a decimal
value and no longer as a positive Integer


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L571>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/sector.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   sector/narrative

