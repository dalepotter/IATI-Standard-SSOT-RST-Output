period-start
============

``iati-activities/iati-activity/result/indicator/period/period-start``

This is the reference page for the XML element ``period-start``. See also the relevant overview page: :doc:`/activity-standard/overview/result` 

.. index::
  single: period-start

Definition
~~~~~~~~~~


The start of the reporting period.


Rules
~~~~~








This element must occur once and only once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/indicator/period/period-start/.iso-date:

@iso-date
  

  This attribute is required.



  This value must be of type xsd:date.



  ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``



Example Usage
~~~~~~~~~~~~~
Example usage of ``period-start`` within ``period``, in context of an ``indicator`` in a ``result`` element.

| An example date is declared in the ``@iso-date`` attribute.
| This example date format conform to the *xsd:date* standard - for most cases *YYYY-MM-DD* is sufficient.

.. literalinclude:: ../../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-period starts-->
	:end-before: <!--result-period ends-->


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1817>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/indicator/period/period-start.rst>`_

