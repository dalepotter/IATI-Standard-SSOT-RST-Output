value
=====

``iati-organisations/iati-organisation/total-budget/budget-line/value``

This is the reference page for the XML element ``value``. See also the relevant overview page: :doc:`/organisation-standard/overview/budgets` 

.. index::
  single: value

Definition
~~~~~~~~~~


Data type for an element containing a currency value.


Rules
~~~~~








This element must occur once and only once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/total-budget/budget-line/value/.currency:

@currency
  A three letter ISO 4217 code for the original currency of the
  amount. This is required for all currency amounts unless
  the iati-organisation/\@default-currency attribute is
  specified.


  This value must be of type xsd:string.



  
.. _iati-organisations/iati-organisation/total-budget/budget-line/value/.value-date:

@value-date
  The date to be used for determining the exchange rate for
  currency conversions.


  This value must be of type xsd:date.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``value`` in context of ``budget-line`` element.

| An example date is declared in the ``@value-date`` attribute.
| This example date format conform to the *xsd:date* standard - for most cases *YYYY-MM-DD* is sufficient.

| This example declares a ``Currency`` code *USD*, using the ``@currency`` attribute.
| Note: A ``Currency`` code should only be declared if different to ``@default-currency`` in the ``iati-organisation`` element.

.. literalinclude:: ../../../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--total-budget starts-->
	:end-before: <!--total-budget ends-->

Changelog
~~~~~~~~~

2.01
^^^^
| The ``budget-line`` element was introduced in 2.01.



Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L195>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/total-budget/budget-line/value.rst>`_

