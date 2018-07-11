exactness
=========

``iati-activities/iati-activity/location/exactness``

This is the reference page for the XML element ``exactness``. See also the relevant overview page: :doc:`/activity-standard/overview/geography` 

.. index::
  single: exactness

Definition
~~~~~~~~~~


Defines whether the location represents the most distinct point reasonably possible for this type of activity or is an approximation due to lack of more detailed information.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/location/exactness/.code:

@code
  A code from the Geographic Exactness Codelist.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`GeographicExactness codelist </codelists/GeographicExactness>`.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``exactness`` within a ``location`` of an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*1*) from the *GeographicExactness* codelist.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--location-single starts-->
	:end-before: <!--location-single ends-->


Changelog
~~~~~~~~~

2.01
^^^^
Freetext is `no longer allowed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#freetext-amended-elements>`__  within this element.

1.04
^^^^

| New in 1.04
| This is used as a replacement for the deprecated location/coordinates/@precision attribute



Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1460>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/location/exactness.rst>`_

