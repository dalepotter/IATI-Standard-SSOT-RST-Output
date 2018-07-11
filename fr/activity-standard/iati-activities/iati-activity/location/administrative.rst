administrative
==============

``iati-activities/iati-activity/location/administrative``

This is the reference page for the XML element ``administrative``. 

.. index::
  single: administrative

Definition
~~~~~~~~~~


Coded identification of national and sub-national divisions according to recognised administrative boundary repositories. Multiple levels may be reported.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/location/administrative/.code:

@code
  The code for the administrative area being reported from the vocabulary specified.

  This attribute is required.



  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/location/administrative/.vocabulary:

@vocabulary
  An IATI code for a recognised administrative boundary repository.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`GeographicVocabulary codelist </codelists/GeographicVocabulary>`.



  
.. _iati-activities/iati-activity/location/administrative/.level:

@level
  A number defining a subdivision within a hierarchical system of administrative areas. The precise system for defining the particular meaning of each @level value is determined by the @vocabulary being used.


  This value must be of type xsd:nonNegativeInteger.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1397>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/location/administrative.rst>`_

