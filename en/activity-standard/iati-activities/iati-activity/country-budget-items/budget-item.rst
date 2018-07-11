budget-item
===========

``iati-activities/iati-activity/country-budget-items/budget-item``

This is the reference page for the XML element ``budget-item``. See also the relevant overview page: :doc:`/activity-standard/overview/budgets` 

.. index::
  single: budget-item

Definition
~~~~~~~~~~


Identifier for a single item in the recipient-country budget. If more than one identifier is reported the percentage share must be reported and all percentages should add up to 100 percent.


Rules
~~~~~








This element must occur at least once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/country-budget-items/budget-item/.code:

@code
  A code for the budget-item from the vocabulary specified.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`BudgetIdentifier codelist </codelists/BudgetIdentifier>`, if the relevant vocabulary is used.



  
.. _iati-activities/iati-activity/country-budget-items/budget-item/.percentage:

@percentage
  When multiple budget-item elements are declared within a single country-budget-items element, then, for each vocabulary used, the percentage values should sum 100%.


  This value must be of type xsd:decimal.



  



Example Usage
~~~~~~~~~~~~~
Example ``budget-item`` within ``country-budget-items`` of an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*1.1.1*) from the *BudgetIdentifier* codelist.

.. code-block:: xml

	<country-budget-items vocabulary="2">
		<budget-item code="1.1.1">
			<description>
				<narrative>Description text</narrative>
			</description>
		</budget-item>
	</country-budget-items>

| The ``budget-item`` element can be repeated in any ``country-budget-items`` of the same ``vocabulary``.
| When multiple ``budget-item`` elements are declared within a single ``country-budget-items`` element, then, for each ``vocabulary`` used, the ``percentage`` values should sum 100%:

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--country-budget-items starts-->
	:end-before: <!--country-budget-items ends-->


Changelog
~~~~~~~~~

1.04
^^^^
The @percentage attribute had been erroneously set to be required in the schema on it's introduction in 1.03. This has now been set to 'optional' in the schema.

1.03
^^^^
Added the optional country-budget-item element


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1577>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/country-budget-items/budget-item.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   budget-item/description

