budget
======

``iati-activities/iati-activity/budget``

This is the reference page for the XML element ``budget``. 

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



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1988>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/budget.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   budget/period-start
   budget/period-end
   budget/value

