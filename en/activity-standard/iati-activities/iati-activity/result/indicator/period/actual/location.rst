location
========

``iati-activities/iati-activity/result/indicator/period/actual/location``

This is the reference page for the XML element ``location``. See also the relevant overview page: :doc:`/activity-standard/overview/result` 

.. index::
  single: location

Definition
~~~~~~~~~~


A location already defined and described in the iati-activity/location element.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/indicator/period/actual/location/.ref:

@ref
  A cross-reference to the internal reference assigned to a defined location: iati-activity/location/\@ref.


  This value must be of type xsd:string.



  



Example Usage
~~~~~~~~~~~~~
Example of ``location`` in context of an ``actual`` element (as part of a parent ``result``/``indicator`` element).

| This example declares ``@ref`` as *AF-KAN*, which matches the ``@ref`` value for a location already referenced in iati-activity/location:

.. code-block:: xml

    <location ref="AF-KAN" />


| The ``location`` element can be repeated within any ``actual`` element:

.. literalinclude:: ../../../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-period starts-->
	:end-before: <!--result-period ends-->

Changelog
~~~~~~~~~

2.02
^^^^
The optional ``location`` element was `added <http://support.iatistandard.org/entries/79499149-Support-disaggregation-of-performance-data>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1878>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/indicator/period/actual/location.rst>`_

