default-aid-type
================

``iati-activities/iati-activity/default-aid-type``

This is the reference page for the XML element ``default-aid-type``. 

.. index::
  single: default-aid-type

Definition
~~~~~~~~~~


The type of aid being supplied (project-type intervention,
budget support, debt relief, etc.). This element specifies a
default for all the activity's financial transactions; it can
be overridden at the individual transaction level.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/default-aid-type/.code:

@code
  A code from the specified vocabulary.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`AidType codelist </codelists/AidType>`.



  
.. _iati-activities/iati-activity/default-aid-type/.vocabulary:

@vocabulary
  A code for the vocabulary aid-type classifications. If omitted the AidType (OECD DAC) codelist is assumed. The code must be a valid value in the AidTypeVocabulary codelist.


  This value must be of type xsd:string.


  This value must be on the :doc:`AidTypeVocabulary codelist </codelists/AidTypeVocabulary>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L474>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/default-aid-type.rst>`_

