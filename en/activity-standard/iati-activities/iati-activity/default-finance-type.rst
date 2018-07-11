default-finance-type
====================

``iati-activities/iati-activity/default-finance-type``

This is the reference page for the XML element ``default-finance-type``. See also the relevant overview page: :doc:`/activity-standard/overview/classifications` 

.. index::
  single: default-finance-type

Definition
~~~~~~~~~~


The type of finance (e.g. grant, loan, debt relief, etc). This
the default value for all transactions in the activity report;
it can be overridden by individual transactions.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/default-finance-type/.code:

@code
  A code from the OECD DAC CRS "Type of finance" codelist

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`FinanceType codelist </codelists/FinanceType>`.



  



Example Usage
~~~~~~~~~~~~~
Example ``default-finance-type``  for an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*110*) from the *FinanceType* codelist.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--default-finance-type starts-->
	:end-before: <!--default-finance-type ends-->
	
Changelog
~~~~~~~~~

2.01
^^^^
Freetext is `no longer allowed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#freetext-amended-elements>`__  within this element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L485>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/default-finance-type.rst>`_

