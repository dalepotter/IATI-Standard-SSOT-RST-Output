finance-type
============

``iati-activities/iati-activity/transaction/finance-type``

This is the reference page for the XML element ``finance-type``. 

.. index::
  single: finance-type

Definition
~~~~~~~~~~


Optional element to override the top-level default-finance-type element on a transaction-by-transaction basis, if needed.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/finance-type/.code:

@code
  A code from the OECD DAC CRS "Type of finance" codelist

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`FinanceType codelist </codelists/FinanceType>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1254>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/transaction/finance-type.rst>`_

