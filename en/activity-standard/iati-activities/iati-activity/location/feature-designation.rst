feature-designation
===================

``iati-activities/iati-activity/location/feature-designation``

This is the reference page for the XML element ``feature-designation``. See also the relevant overview page: :doc:`/activity-standard/overview/geography` 

.. index::
  single: feature-designation

Definition
~~~~~~~~~~


A more refined coded classification of the type of feature referred to by this location.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/location/feature-designation/.code:

@code
  A feature designation code form the authorised list (maintained by the US National Geospatial-Intelligence Agency)

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`LocationType codelist </codelists/LocationType>`.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``feature-designation`` within a ``location`` of an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*ADMF*) from the *LocationType* codelist.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--location-single starts-->
	:end-before: <!--location-single ends-->



Changelog
~~~~~~~~~

1.04
^^^^

| New in 1.04


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1500>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/location/feature-designation.rst>`_

