location
========

``iati-activities/iati-activity/location``

This is the reference page for the XML element ``location``. See also the relevant overview page: :doc:`/activity-standard/overview/geography` 

.. index::
  single: location

Definition
~~~~~~~~~~


The sub-national geographical identification of the target locations of an activity. These can be described by gazetteer reference, coordinates, administrative areas or a textual description. Any number of locations may be reported.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/location/.ref:

@ref
  An internal reference that describes the location in the reporting organisation’s own system.


  This value must be of type xsd:string.



  



Example Usage
~~~~~~~~~~~~~
Example ``location`` for an ``iati-activity``.

| This element is a parent for other child elements.

| An example organisation ``@ref`` of *AF-KAN* is declared.

.. code-block:: xml

	<location ref="AF-KAN">
	...
	</location>

| Full example with all child elements:

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--location-single starts-->
	:end-before: <!--location-single ends-->

| The ``location`` element can be repeated in any ``iati-activity``:

.. code-block:: xml

	<location ref="AF-KAN">
	...
	</location>
	<location ref="KH-PNH">
	...
	</location>

Changelog
~~~~~~~~~
2.01
^^^^
The following child elements were removed: `coordinates; gazetteer-entry; location-type <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#location-removed-elements>`__.

The @percentage attribute was `removed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#location-removed-attributes>`__.

1.04
^^^^
Note that major changes were made to the subelements of ``location`` in version 1.04.

| For more information refer to:

* the :doc:`1.04 location changes overview guidance </upgrades/decimal-upgrade-to-1-04/location-summary/>`
* the :ref:`Activities Schema Changelog <1_04_activities_schema_changes>` (or the individual subemelement pages)

| The @ref attribute was introduced to provide a cross reference that a publisher can use to link back to their own internal system.
| The @percentage attribute was deemed unworkable and deprecated in 1.04


1.03
^^^^
Where used, the @percentage attribute is now designated as a decimal
value and no longer as a positive Integer


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1321>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/location.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   location/location-reach
   location/location-id
   location/name
   location/description
   location/activity-description
   location/administrative
   location/point
   location/exactness
   location/location-class
   location/feature-designation

