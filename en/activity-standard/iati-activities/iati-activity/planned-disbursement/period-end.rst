period-end
==========

``iati-activities/iati-activity/planned-disbursement/period-end``

This is the reference page for the XML element ``period-end``. See also the relevant overview page: :doc:`/activity-standard/overview/budgets` 

.. index::
  single: period-end

Definition
~~~~~~~~~~


The ending date for the period in which this specific disbursement will be made.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/planned-disbursement/period-end/.iso-date:

@iso-date
  

  This attribute is required.



  This value must be of type xsd:date.



  ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``



Usage in practice
~~~~~~~~~~~~~~~~~
The ``period start`` should define when the actual transfer of funds will take place, if a specific date is known. If the specific payment date is not known, the period in which the transfer is due to take place should be described by using both ``period-start`` and ``period-end`` dates.

The timeframe between ``period-start`` and ``period-end`` should not normally exceed 3 calendar months.

Example Usage
~~~~~~~~~~~~~
Example usage of ``period-end`` of ``planned-disbursement`` for an ``iati-activity``.

| An example date is declared in the ``@iso-date`` attribute.
| This example date format conform to the *xsd:date* standard - for most cases *YYYY-MM-DD* is sufficient.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--planned-disbursement starts-->
	:end-before: <!--planned-disbursement ends-->

| In some instances, it may not be feasible to declare an ``period-end`` date.  In such cases, the element is not included:

.. code-block:: xml

	<planned-disbursement type="1">
		<period-start iso-date="2014-01-01" />
		<value currency="EUR" value-date="2014-01-01">3000</value>
	</planned-disbursement>


Changelog
~~~~~~~~~

2.02
^^^^
The definition of this element was amended for clarity.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2073>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/planned-disbursement/period-end.rst>`_

