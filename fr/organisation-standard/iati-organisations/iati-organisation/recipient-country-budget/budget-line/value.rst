value
=====

``iati-organisations/iati-organisation/recipient-country-budget/budget-line/value``

This is the reference page for the XML element ``value``. 

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


.. _iati-organisations/iati-organisation/recipient-country-budget/budget-line/value/.currency:

@currency
  A three letter ISO 4217 code for the original currency of the
  amount. This is required for all currency amounts unless
  the iati-organisation/\@default-currency attribute is
  specified.


  This value must be of type xsd:string.



  
.. _iati-organisations/iati-organisation/recipient-country-budget/budget-line/value/.value-date:

@value-date
  The date to be used for determining the exchange rate for
  currency conversions.


  This value must be of type xsd:date.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L612>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/organisation-standard/iati-organisations/iati-organisation/recipient-country-budget/budget-line/value.rst>`_

