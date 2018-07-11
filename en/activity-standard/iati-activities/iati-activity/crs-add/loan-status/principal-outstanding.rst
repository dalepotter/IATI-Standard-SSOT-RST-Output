principal-outstanding
=====================

``iati-activities/iati-activity/crs-add/loan-status/principal-outstanding``

This is the reference page for the XML element ``principal-outstanding``. See also the relevant overview page: :doc:`/activity-standard/overview/crs-fss` 

.. index::
  single: principal-outstanding

Definition
~~~~~~~~~~


The amount of principal owed on the loan at the end of the reporting year.


Rules
~~~~~


The text in this element must be of type xsd:decimal.






This element must occur no more than once (within each parent element).








Example Usage
~~~~~~~~~~~~~
Example usage of ``principle-outstanding`` within ``loan-status`` in context of ``crs-add`` element.

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

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2357>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/crs-add/loan-status/principal-outstanding.rst>`_

