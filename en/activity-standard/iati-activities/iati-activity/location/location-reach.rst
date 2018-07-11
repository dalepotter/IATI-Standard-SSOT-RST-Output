location-reach
==============

``iati-activities/iati-activity/location/location-reach``

This is the reference page for the XML element ``location-reach``. See also the relevant overview page: :doc:`/activity-standard/overview/geography` 

.. index::
  single: location-reach

Definition
~~~~~~~~~~


Does this location describe where the activity takes place or where the intended beneficiaries reside?


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/location/location-reach/.code:

@code
  An IATI code for the geographic scope of the activity.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`GeographicLocationReach codelist </codelists/GeographicLocationReach>`.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``location-reach`` within a ``location`` of an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*1*) from the *GeographicLocationReach* codelist.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--location-single starts-->
	:end-before: <!--location-single ends-->



Changelog
~~~~~~~~~

1.04
^^^^

| Introduced in 1.04



Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1329>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/location/location-reach.rst>`_

