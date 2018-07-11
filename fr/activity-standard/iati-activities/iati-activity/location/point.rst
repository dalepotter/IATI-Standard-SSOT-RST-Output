point
=====

``iati-activities/iati-activity/location/point``

This is the reference page for the XML element ``point``. 

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



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1431>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/location/point.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   point/pos

