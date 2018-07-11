period-start
============

``iati-organisations/iati-organisation/recipient-org-budget/period-start``

This is the reference page for the XML element ``period-start``. See also the relevant overview page: :doc:`/organisation-standard/overview/budgets` 

.. index::
  single: period-start

Definition
~~~~~~~~~~


The start of the budget period.


Rules
~~~~~








This element must occur once and only once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/recipient-org-budget/period-start/.iso-date:

@iso-date
  

  This attribute is required.



  This value must be of type xsd:date.



  ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``



Example Usage
~~~~~~~~~~~~~
Example ``period-start`` of ``recipient-org-budget`` for an ``iati-organisation``.

| An example date is declared in the ``@iso-date`` attribute.
| This example date format conform to the *xsd:date* standard - for most cases *YYYY-MM-DD* is sufficient.

.. literalinclude:: ../../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--recipient-org-budget starts-->
	:end-before: <!--recipient-org-budget ends-->



Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L281>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/recipient-org-budget/period-start.rst>`_

