budget
======

``iati-activities/iati-activity/budget``

This is the reference page for the XML element ``budget``. See also the relevant overview page: :doc:`/activity-standard/overview/budgets` 

.. index::
  single: budget

Definition
~~~~~~~~~~


The value of the activity's budget for each financial quarter or year over the lifetime of the activity. The purpose of this element is to provide predictability for recipient planning on an annual basis. The status explains whether the budget being reported is indicative or has been formally committed. The value should appear within the BudgetStatus codelist. If the @status attribute is not present, the budget is assumed to be indicative. The sum of budgets may or may not match the sum of commitments, depending on a publisher’s business model and legal frameworks.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/budget/.type:

@type
  Whether this is the original budget (prepared when the original commitment was made) or has subsequently been revised


  This value must be of type xsd:string.


  This value must be on the :doc:`BudgetType codelist </codelists/BudgetType>`.



  
.. _iati-activities/iati-activity/budget/.status:

@status
  The status explains whether the budget being reported is indicative or has been formally committed. The value should appear within the BudgetStatus codelist. If the @status attribute is not present, the budget is assumed to be indicative.


  This value must be of type xsd:string.


  This value must be on the :doc:`BudgetStatus codelist </codelists/BudgetStatus>`.



  



Example Usage
~~~~~~~~~~~~~
Example ``budget`` for an ``iati-activity``.

| This element is a parent for other child elements.

| The ``@type`` attribute declares a valid code (*1*) from the *BudgetType* codelist.
| The ``@status`` attribute declares a valid code (*1*) from the *BudgetStatus* codelist.

.. code-block:: xml

	<budget type="1" status="1">
	...
	</budget>

| Note: If the @type attribute is omitted, then *BudgetType* code *1* (Original) is assumed.
| Similarly, if the @status attribute is omitted, then *BudgetStatus* code *1* (Indicative) is assumed.

| Full example with all child elements:

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--budget starts-->
	:end-before: <!--budget ends-->

| The ``budget`` element can be repeated in any ``iati-activity``.

Changelog
~~~~~~~~~
27/02/2018

The ``budget`` definition was updated as a `bug fix <https://discuss.iatistandard.org/t/proposal-update-of-budget-element-description-text-in-activity-standard/1216>`__. 

2.02
^^^^

The ``status`` attribute was `added <http://support.iatistandard.org/entries/21150501-Budgets-and-tentativeness>`__.




Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1988>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/budget.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   budget/period-start
   budget/period-end
   budget/value

