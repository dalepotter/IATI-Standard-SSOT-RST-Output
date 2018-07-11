total-budget
============

``iati-organisations/iati-organisation/total-budget``

This is the reference page for the XML element ``total-budget``. 

.. index::
  single: total-budget

Definition
~~~~~~~~~~


The total-budget element allows for the reporting of the organisation's
own budget. The recommendation is that, where and when possible, the
organisation's total annual planned budget for each of the next three
years is reported. The status explains whether the budget being reported
is indicative or has been formally committed. The value should appear
within the BudgetStatus codelist. If the @status attribute is not present,
the budget is assumed to be indicative.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/total-budget/.status:

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

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L132>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/organisation-standard/iati-organisations/iati-organisation/total-budget.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   total-budget/period-start
   total-budget/period-end
   total-budget/value
   total-budget/budget-line

