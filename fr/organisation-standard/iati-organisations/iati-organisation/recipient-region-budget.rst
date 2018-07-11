recipient-region-budget
=======================

``iati-organisations/iati-organisation/recipient-region-budget``

This is the reference page for the XML element ``recipient-region-budget``. 

.. index::
  single: recipient-region-budget

Definition
~~~~~~~~~~


The recipient-region-budget element allows for the reporting of forward
looking budgets where the organisation maintains region-wide, rather than
or in addition to country-specific budgets. The recommendation is that,
where and when possible, the organisation’s total annual planned budget
for each of the next three financial years is reported for each recipient
region. This must NOT include an aggregation of budgets reported in the
recipient-country-budget element. It is strongly recommended that
publishers report to existing defined regions wherever possible. The
status explains whether the budget being reported is indicative or has
been formally committed. The value should appear within the BudgetStatus
codelist. If the @status attribute is not present, the budget is assumed
to be indicative.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/recipient-region-budget/.status:

@status
  The status explains whether the budget being reported is indicative or has
  been formally committed. The value should appear within the BudgetStatus
  codelist. If the @status attribute is not present, the budget is assumed
  to be indicative.


  This value must be of type xsd:string.


  This value must be on the :doc:`BudgetStatus codelist </codelists/BudgetStatus>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L372>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/organisation-standard/iati-organisations/iati-organisation/recipient-region-budget.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   recipient-region-budget/recipient-region
   recipient-region-budget/period-start
   recipient-region-budget/period-end
   recipient-region-budget/value
   recipient-region-budget/budget-line

