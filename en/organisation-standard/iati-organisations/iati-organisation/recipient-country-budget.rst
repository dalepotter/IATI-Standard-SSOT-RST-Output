recipient-country-budget
========================

``iati-organisations/iati-organisation/recipient-country-budget``

This is the reference page for the XML element ``recipient-country-budget``. See also the relevant overview page: :doc:`/organisation-standard/overview/budgets` 

.. index::
  single: recipient-country-budget

Definition
~~~~~~~~~~


The recipient-country-budget element allows for the reporting of
forward looking budgets for each country in which the organisation
operates. The recommendation is that, where and when possible, the
organisation's total annual planned budget for each of the next
three financial years is reported for each recipient country.
It is strongly recommended that the start and end of the reported
financial years match those of the recipient country's
budgetary/planning cycle. The status explains whether the budget
being reported is indicative or has been formally committed. The
value should appear within the BudgetStatus codelist. If the
@status attribute is not present, the budget is assumed to be
indicative.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/recipient-country-budget/.status:

@status
  The status explains whether the budget being reported is indicative or has
  been formally committed. The value should appear within the BudgetStatus
  codelist. If the @status attribute is not present, the budget is assumed
  to be indicative.


  This value must be of type xsd:string.


  This value must be on the :doc:`BudgetStatus codelist </codelists/BudgetStatus>`.



  



Example Usage
~~~~~~~~~~~~~
| Example of ``recipient-country-budget`` for an ``iati-organisation``.

| This element is a parent for other child elements.

.. code-block:: xml

	<recipient-country-budget status="1">
	...
	</recipient-country-budget>

| Full example with all child elements.

.. literalinclude:: ../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--recipient-country-budget starts-->
	:end-before: <!--recipient-country-budget ends-->

| The ``recipient-country-budget`` element can be repeated in any ``iati-organisation``.


Changelog
~~~~~~~~~

2.02
^^^^
The ``status`` attribute was `added <http://support.iatistandard.org/entries/21150501-Budgets-and-tentativeness>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L521>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/recipient-country-budget.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   recipient-country-budget/recipient-country
   recipient-country-budget/period-start
   recipient-country-budget/period-end
   recipient-country-budget/value
   recipient-country-budget/budget-line

