commitment-date
===============

``iati-activities/iati-activity/crs-add/loan-terms/commitment-date``

This is the reference page for the XML element ``commitment-date``. See also the relevant overview page: :doc:`/activity-standard/overview/crs-fss` 

.. index::
  single: commitment-date

Definition
~~~~~~~~~~


The CRS++ reported commitment date


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/crs-add/loan-terms/commitment-date/.iso-date:

@iso-date
  

  This attribute is required.



  This value must be of type xsd:date.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``commitment-date`` within ``loan-terms`` in context of ``crs-add`` element.

| An example date is declared in the ``@value-date`` attribute.
| This example date format conform to the *xsd:date* standard - for most cases *YYYY-MM-DD* is sufficient.

.. literalinclude:: ../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--crs-add starts-->
	:end-before: <!--crs-add ends-->

Changelog
~~~~~~~~~

1.03
^^^^

| New in 1.03
| Added the optional ``crs-add`` element and its child elements


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2277>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/crs-add/loan-terms/commitment-date.rst>`_

