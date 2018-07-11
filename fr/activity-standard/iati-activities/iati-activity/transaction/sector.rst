sector
======

``iati-activities/iati-activity/transaction/sector``

This is the reference page for the XML element ``sector``. 

.. index::
  single: sector

Definition
~~~~~~~~~~


A recognised code, from a recognised vocabulary, classifying the purpose of this transaction.

If this element is used then ALL transaction elements should contain a transaction/sector element and iati-activity/sector should NOT be used.

This element can be used multiple times, but only one sector can be reported per vocabulary.


Rules
~~~~~








This element may occur any number of times.







Either ``transaction/sector`` or ``sector`` must be present.




Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/sector/.vocabulary:

@vocabulary
  An IATI code for the vocabulary (codelist) used for sector classifications. If omitted, OECD DAC 5-digit Purpose Codes are assumed.
  
  It is recommended that OECD DAC 5-digit Purpose Codes are used wherever possible. It is also recommended that if a publisher has its own classification system or systems, then the vocabularies 99 or 98 (Reporting Organisation's own vocabularies) should be used in addition to the DAC codes.
  
  Note that at transaction level, only one sector per vocabulary can be reported.


  This value must be of type xsd:string.


  This value must be on the :doc:`SectorVocabulary codelist </codelists/SectorVocabulary>`.



  
.. _iati-activities/iati-activity/transaction/sector/.vocabulary-uri:

@vocabulary-uri
  The URI where this vocabulary is defined. If the vocabulary is 99 or 98 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.


  This value must be of type xsd:anyURI.



  
.. _iati-activities/iati-activity/transaction/sector/.code:

@code
  The code for the sector.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`Sector codelist </codelists/Sector>`, if the relevant vocabulary is used.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1124>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/transaction/sector.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   sector/narrative

