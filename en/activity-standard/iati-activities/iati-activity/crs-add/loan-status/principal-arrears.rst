principal-arrears
=================

``iati-activities/iati-activity/crs-add/loan-status/principal-arrears``

This is the reference page for the XML element ``principal-arrears``. See also the relevant overview page: :doc:`/activity-standard/overview/crs-fss` 

.. index::
  single: principal-arrears

Definition
~~~~~~~~~~


Arrears of principal at the end of the year. Included in principal-outstanding


Rules
~~~~~


The text in this element must be of type xsd:decimal.






This element must occur no more than once (within each parent element).








Example Usage
~~~~~~~~~~~~~
Example usage of ``principle-arrears`` within ``loan-status`` in context of ``crs-add`` element.

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

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2364>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/crs-add/loan-status/principal-arrears.rst>`_

