recipient-org-budget
====================

``iati-organisations/iati-organisation/recipient-org-budget``

This is the reference page for the XML element ``recipient-org-budget``. 

.. index::
  single: recipient-org-budget

Definition
~~~~~~~~~~


The recipient-org-budget element allows for the reporting of
forward looking budgets for each institution which receives
core funding from the reporting organisation. The
recommendation is that, where and when possible, annual
planned budgets for each recipient institution for each of the
next three financial years are reported. This is primarily
applicable to donors but any provider of core funding is
expected to use it. Earmarked budgets should be reported at
activity-level through the Activity Standard. The status
explains whether the budget being reported is indicative or
has been formally committed. The value should appear within
the BudgetStatus codelist. If the @status attribute is not
present, the budget is assumed to be indicative.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/recipient-org-budget/.status:

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

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L235>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/organisation-standard/iati-organisations/iati-organisation/recipient-org-budget.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   recipient-org-budget/recipient-org
   recipient-org-budget/period-start
   recipient-org-budget/period-end
   recipient-org-budget/value
   recipient-org-budget/budget-line

