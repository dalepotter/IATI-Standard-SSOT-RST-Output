country-budget-items
====================

``iati-activities/iati-activity/country-budget-items``

This is the reference page for the XML element ``country-budget-items``. See also the relevant overview page: :doc:`/activity-standard/overview/budgets` 

.. index::
  single: country-budget-items

Definition
~~~~~~~~~~


This item encodes the alignment of activities with both the functional and administrative classifications used in the recipient country's Chart of Accounts. This applies to both on- and off-budget activities.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/country-budget-items/.vocabulary:

@vocabulary
  An IATI code for the common functional classification or country system (This allows for common codes, country-specific, or any other classification agreed between countries and donors).

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`BudgetIdentifierVocabulary codelist </codelists/BudgetIdentifierVocabulary>`.



  



Example Usage
~~~~~~~~~~~~~
Example ``country-budget-items`` for an ``iati-activity``.

| This element is a parent for other child elements.

| The ``@vocabulary`` attribute declares a valid code (*2*) from the *BudgetIdentifierVocabulary* codelist.

.. code-block:: xml

    <country-budget-items vocabulary="2">
	...
    </country-budget-items>

Full example with all child elements:

.. code-block:: xml

	<country-budget-items vocabulary="2">
		<budget-item code="1.1.1">
			<description>
				<narrative>Description text</narrative>
			</description>
		</budget-item>
	</country-budget-items>


Changelog
~~~~~~~~~

1.03
^^^^
This is a new element, introduced in version 1.03 of the standard.



Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1569>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/country-budget-items.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   country-budget-items/budget-item

