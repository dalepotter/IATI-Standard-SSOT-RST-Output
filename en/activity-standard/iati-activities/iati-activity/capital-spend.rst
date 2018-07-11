capital-spend
=============

``iati-activities/iati-activity/capital-spend``

This is the reference page for the XML element ``capital-spend``. See also the relevant overview page: :doc:`/activity-standard/overview/budgets` 

.. index::
  single: capital-spend

Definition
~~~~~~~~~~


The percentage of the total commitment that is for capital
spending


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/capital-spend/.percentage:

@percentage
  The percentage of the total commitment allocated to or planned for capital expenditure. Content must be a decimal number between 0 and 100 inclusive, with no percentage sign.

  This attribute is required.



  This value must be of type xsd:decimal.



  



Example Usage
~~~~~~~~~~~~~
Example ``capital-spend`` of an ``iati-activity``.

| This example uses the ``@percentage`` attribute to state *88.8%* of the ``iati-activity`` budget is for capital expenditure.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--capital-spend starts-->
	:end-before: <!--capital-spend ends-->

Changelog
~~~~~~~~~

2.03
^^^^
Definition of ``@percentage`` attribute `updated <https://discuss.iatistandard.org/t/boundary-values-for-percentages-included-2-03/843>`__.

1.03
^^^^
This is a new element, introduced in version 1.03 of the standard


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L932>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/capital-spend.rst>`_

