point
=====

``iati-activities/iati-activity/location/point``

This is the reference page for the XML element ``point``. See also the relevant overview page: :doc:`/activity-standard/overview/geography` 

.. index::
  single: point

Definition
~~~~~~~~~~


The point element is based on a subset of the GML 3.3 Point element.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/location/point/.srsName:

@srsName
  The name of the spatial reference system used by the coordinates.
  
  Always: http://www.opengis.net/def/crs/EPSG/0/4326

  This attribute is required.



  This value must be of type xsd:string.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``point`` within a ``location`` of an ``iati-activity``.

| Note: The ``@srsName`` attribute should always be populated with *http://www.opengis.net/def/crs/EPSG/0/4326*.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
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

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1431>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/location/point.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   point/pos

