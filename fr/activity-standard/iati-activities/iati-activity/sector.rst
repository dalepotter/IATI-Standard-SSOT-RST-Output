sector
======

``iati-activities/iati-activity/sector``

This is the reference page for the XML element ``sector``. 

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



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L571>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/sector.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   sector/narrative

