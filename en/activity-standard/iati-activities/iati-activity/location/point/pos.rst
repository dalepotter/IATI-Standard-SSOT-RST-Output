pos
===

``iati-activities/iati-activity/location/point/pos``

This is the reference page for the XML element ``pos``. See also the relevant overview page: :doc:`/activity-standard/overview/geography` 

.. index::
  single: pos

Definition
~~~~~~~~~~


The latitude and longitude coordinates in the format "lat lng"


Rules
~~~~~


The text in this element must be of type xsd:string.






This element must occur once and only once (within each parent element).








Example Usage
~~~~~~~~~~~~~
Example usage of ``pos``, a child element of the ``point`` element of ``location``.

.. literalinclude:: ../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--location-single starts-->
	:end-before: <!--location-single ends-->

Changelog
~~~~~~~~~

1.04
^^^^

| Introduced in 1.04 to align the geocoding standard with Geographic Markup Language (GML)



Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1439>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/location/point/pos.rst>`_

