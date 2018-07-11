reference
=========

``iati-activities/iati-activity/result/reference``

This is the reference page for the XML element ``reference``. 

.. index::
  single: reference

Definition
~~~~~~~~~~


A reference element to allow for the coded identification of a results framework.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/reference/.code:

@code
  A code from the codelist identified in vocabulary that identifies a results framework.

  This attribute is required.



  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/result/reference/.vocabulary:

@vocabulary
  A code for the results framework vocabulary. The code must be a valid value in the ResultVocabulary codelist.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`ResultVocabulary codelist </codelists/ResultVocabulary>`.



  
.. _iati-activities/iati-activity/result/reference/.vocabulary-uri:

@vocabulary-uri
  The URI where this vocabulary is defined. If the vocabulary is 99 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.


  This value must be of type xsd:anyURI.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1696>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/result/reference.rst>`_

