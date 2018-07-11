transaction
===========

``iati-activities/iati-activity/transaction``

This is the reference page for the XML element ``transaction``. 

.. index::
  single: transaction

Definition
~~~~~~~~~~


Transactions recording committed or actual funds flowing in or
out of an aid activity.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/.ref:

@ref
  An internal reference linking this transaction back to the publisher's financial management system.


  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/transaction/.humanitarian:

@humanitarian
  A process flag to indicate that this transaction relates entirely or partially to humanitarian aid. If the entire activity relates to humanitarian aid this should be reported using iati-activity/\@humanitarian, rather than for each transaction.


  This value must be of type xsd:boolean.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L954>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/transaction.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   transaction/transaction-type
   transaction/transaction-date
   transaction/value
   transaction/description
   transaction/provider-org
   transaction/receiver-org
   transaction/disbursement-channel
   transaction/sector
   transaction/recipient-country
   transaction/recipient-region
   transaction/flow-type
   transaction/finance-type
   transaction/aid-type
   transaction/tied-status

