transaction
===========

``iati-activities/iati-activity/transaction``

This is the reference page for the XML element ``transaction``. See also the relevant overview page: :doc:`/activity-standard/overview/transactions` 

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



  



Example Usage
~~~~~~~~~~~~~
Example ``transaction`` in an ``iati-activity``.

| This element is a parent for other child elements.

| An example ``@ref`` of *1234* is declared.

.. code-block:: xml

        <transaction ref="1234">
        ....
        </transaction>

| An example which would denote this as a humanitarian transaction i.e. with the ``@humanitarian`` element set to '1'.

.. code-block:: xml

        <transaction ref="1234">
        ....
        </transaction>

| Full example with all child elements:

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--transaction starts-->
	:end-before: <!--transaction ends-->

| The ``transaction`` element can be repeated in any ``iati-activity``.


Changelog
~~~~~~~~~

2.02
^^^^
| The ``humanitarian`` attribute was `added <http://support.iatistandard.org/entries/106937796-Humanitarian-Flag>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L954>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/transaction.rst>`_


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

