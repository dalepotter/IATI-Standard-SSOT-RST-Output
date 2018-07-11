location-class
==============

``iati-activities/iati-activity/location/location-class``

This is the reference page for the XML element ``location-class``. See also the relevant overview page: :doc:`/activity-standard/overview/geography` 

.. index::
  single: location-class

Definition
~~~~~~~~~~


Whether the location refers to a structure, a populated place (e.g. city or village), an administrative division, or another topological feature (e.g. river, nature reserve).


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/location/location-class/.code:

@code
  A code from the Location Class codelist

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`GeographicLocationClass codelist </codelists/GeographicLocationClass>`.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``location-class`` within a ``location`` of an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*2*) from the *GeographicLocationClass* codelist.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--location-single starts-->
	:end-before: <!--location-single ends-->

Changelog
~~~~~~~~~

1.04
^^^^

| New in 1.04
| The location-class element was introduced in 1.04 and replaced the now deprecated location-type element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1480>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/location/location-class.rst>`_

