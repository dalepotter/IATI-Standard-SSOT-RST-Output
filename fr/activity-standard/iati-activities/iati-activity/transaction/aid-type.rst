aid-type
========

``iati-activities/iati-activity/transaction/aid-type``

This is the reference page for the XML element ``aid-type``. 

.. index::
  single: aid-type

Definition
~~~~~~~~~~


A code from the specified vocabulary.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/aid-type/.code:

@code
  A code from the specified vocabulary.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`AidType codelist </codelists/AidType>`.



  
.. _iati-activities/iati-activity/transaction/aid-type/.vocabulary:

@vocabulary
  A code for the vocabulary aid-type classifications. If omitted the AidType (OECD DAC) codelist is assumed. The code must be a valid value in the AidTypeVocabulary codelist.


  This value must be of type xsd:string.


  This value must be on the :doc:`AidTypeVocabulary codelist </codelists/AidTypeVocabulary>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1274>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/transaction/aid-type.rst>`_

