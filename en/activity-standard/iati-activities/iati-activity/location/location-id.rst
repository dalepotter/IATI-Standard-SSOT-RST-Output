location-id
===========

``iati-activities/iati-activity/location/location-id``

This is the reference page for the XML element ``location-id``. See also the relevant overview page: :doc:`/activity-standard/overview/geography` 

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



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``location-id`` within a ``location`` of an ``iati-activity``..

| The ``@vocabulary`` attribute declares a valid code (*G1*) from the *GeographicVocabulary* codelist.
| An example value of *1453782* from that vocabulary is declared in the ``@code`` attribute.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--location-single starts-->
	:end-before: <!--location-single ends-->

Note: If the *GeographicVocabulary* *G2* (*Open Street Map*) is used, then the ``@code`` value should be of the form <OSM element>/<OSM identifier>

The OSM element will be a node, way or relation.

| Examples:

* node/1234567
* way/1234567
* relation/1234567

.. code-block:: xml

    <location-id vocabulary="G2" code="node/25524229" />


Changelog
~~~~~~~~~

2.01
^^^^
Freetext is `no longer allowed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#freetext-amended-elements>`__  within this element.

1.04
^^^^

| New in 1.04
| The location-id element was introduced in 1.04 to replace the gazetteer-entry element which was deprecated in 1.04


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1349>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/location/location-id.rst>`_

