transaction-date
================

``iati-activities/iati-activity/transaction/transaction-date``

This is the reference page for the XML element ``transaction-date``. See also the relevant overview pages: :doc:`/activity-standard/overview/dates`,  :doc:`/activity-standard/overview/transactions` 

.. index::
  single: transaction-date

Definition
~~~~~~~~~~


The date on which the transaction was made or (in the
case of commitments) agreed. The narrative content may
contain text (e.g. 2011Q1) for accurately recording less
specific dates such as month, quarter, or year.


Rules
~~~~~








This element must occur once and only once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/transaction-date/.iso-date:

@iso-date
  

  This attribute is required.



  This value must be of type xsd:date.



  ``transaction-date/@iso-date`` must not be in the future.



Example Usage
~~~~~~~~~~~~~
Example usage of ``transaction-date`` of a ``transaction`` in an ``iati-activity``.

| An example date is declared in the ``@iso-date`` attribute.
| This example date format conform to the *xsd:date* standard - for most cases *YYYY-MM-DD* is sufficient.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--transaction starts-->
	:end-before: <!--transaction ends-->



Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L984>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/transaction/transaction-date.rst>`_

