planned-disbursement
====================

``iati-activities/iati-activity/planned-disbursement``

This is the reference page for the XML element ``planned-disbursement``. 

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



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2051>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/planned-disbursement.rst>`_


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

