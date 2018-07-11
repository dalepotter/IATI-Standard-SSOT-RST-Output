transaction-type
================

``iati-activities/iati-activity/transaction/transaction-type``

This is the reference page for the XML element ``transaction-type``. See also the relevant overview page: :doc:`/activity-standard/overview/transactions` 

.. index::
  single: transaction-type

Definition
~~~~~~~~~~


The type of the transaction (e.g. commitment,
disbursement, expenditure, etc.).


Rules
~~~~~








This element must occur once and only once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/transaction-type/.code:

@code
  A code from the specified vocabulary.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`TransactionType codelist </codelists/TransactionType>`.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``transaction-type`` of ``transaction`` for an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*1*) from the *TransactionType* codelist.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--transaction starts-->
	:end-before: <!--transaction ends-->

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is `no longer allowed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#freetext-amended-elements>`__  within this element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L963>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/transaction/transaction-type.rst>`_

