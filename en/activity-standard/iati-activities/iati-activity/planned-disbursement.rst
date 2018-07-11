planned-disbursement
====================

``iati-activities/iati-activity/planned-disbursement``

This is the reference page for the XML element ``planned-disbursement``. See also the relevant overview page: :doc:`/activity-standard/overview/budgets` 

.. index::
  single: planned-disbursement

Definition
~~~~~~~~~~


The planned disbursement element should only be used to report specific planned cash transfers. These should be reported for a specific date or a meaningfully predictable period. These transactions should be reported in addition to budgets - which are typically annual breakdowns of the total activity commitment.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/planned-disbursement/.type:

@type
  Whether this is an original plan (prepared when the original commitment was made) or has subsequently been revised.


  This value must be of type xsd:string.


  This value must be on the :doc:`BudgetType codelist </codelists/BudgetType>`.



  



Usage in practice
~~~~~~~~~~~~~~~~~

The purpose of planned-disbursement is to describe any predefined payment schedule.

Planned disbursements should relate to an actual transfer of funds.

Planned disbursements do not replace the activity-budget.


Example Usage
~~~~~~~~~~~~~
Example ``planned-disbursement`` for an ``iati-activity``.

| This element is a parent for other child elements.

| The ``@type`` attribute declares a valid code (*1*) from the *BudgetType* codelist.

.. code-block:: xml

	<planned-disbursement type="1">
	...
	</planned-disbursement>

| Note: If omitted, then *BudgetType* code *1* (Original) is assumed.

| Full example with all child elements:

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--planned-disbursement starts-->
	:end-before: <!--planned-disbursement ends-->

| Note: multiple planned disbursements are expressed by repeating the ``planned-disbursement`` element.

Changelog
~~~~~~~~~
2.01
^^^^
The attribute ``@last-updated`` was `removed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#planned-disbursement-removed-renamed-attributes>`__.

The attribute ``@type`` was `added <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#planned-disbursement-removed-renamed-attributes>`__.


1.05
^^^^
A description was added to this element


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2051>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/planned-disbursement.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   planned-disbursement/period-start
   planned-disbursement/period-end
   planned-disbursement/value
   planned-disbursement/provider-org
   planned-disbursement/receiver-org

