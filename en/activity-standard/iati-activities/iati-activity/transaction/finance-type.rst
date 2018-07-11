finance-type
============

``iati-activities/iati-activity/transaction/finance-type``

This is the reference page for the XML element ``finance-type``. See also the relevant overview page: :doc:`/activity-standard/overview/transactions` 

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



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``finance-type`` of a ``transaction`` in an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*111*) from the *FinanceType* codelist.

| Note: The ``finance-type`` element can override the ``default-finance-type`` value set in ``iati-activity``:

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

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1254>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/transaction/finance-type.rst>`_

