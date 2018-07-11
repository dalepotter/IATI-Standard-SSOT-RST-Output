reference
=========

``iati-activities/iati-activity/result/indicator/reference``

This is the reference page for the XML element ``reference``. 

.. index::
  single: reference

Definition
~~~~~~~~~~


A standardised means of identifying the indicator from a code in a recognised vocabulary. Multiple vocabularies may be specified, but each vocabulary may be specified only once for each indicator.


Rules
~~~~~








This element may occur any number of times.







There must be no more than one element or attribute matched at ``reference[1]`` or ``../reference[1]``.




Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/indicator/reference/.vocabulary:

@vocabulary
  A code for a recognised vocabulary of indicators. The value for this field should appear in the IndicatorVocabulary codelist.

  This attribute is required.



  This value must be of type xsd:string.


  This value should be on the :doc:`IndicatorVocabulary codelist </codelists/IndicatorVocabulary>`.



  
.. _iati-activities/iati-activity/result/indicator/reference/.code:

@code
  A code for an indicator defined in the specified vocabulary specified.

  This attribute is required.



  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/result/indicator/reference/.indicator-uri:

@indicator-uri
  The URI where this vocabulary is defined. If the vocabulary is 99 or 98 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.


  This value must be of type xsd:anyURI.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1741>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/result/indicator/reference.rst>`_

