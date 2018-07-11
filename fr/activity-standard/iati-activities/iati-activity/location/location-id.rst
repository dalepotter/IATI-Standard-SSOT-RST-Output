location-id
===========

``iati-activities/iati-activity/location/location-id``

This is the reference page for the XML element ``location-id``. 

.. index::
  single: location-id

Definition
~~~~~~~~~~


A unique code describing the location according to a recognised gazetteer or administrative boundary repository. Administrative areas should only be reported here if the location being defined is the administrative area itself. For describing the administrative area/s within which a more specific location falls the location/administrative element should be used.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/location/location-id/.code:

@code
  A code from the gazetteer or administrative boundary repository specified by the vocabulary

  This attribute is required.



  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/location/location-id/.vocabulary:

@vocabulary
  An IATI code for a recognised gazetteer or administrative boundary repository.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`GeographicVocabulary codelist </codelists/GeographicVocabulary>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1349>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/location/location-id.rst>`_

