value
=====

``iati-activities/iati-activity/budget/value``

This is the reference page for the XML element ``value``. See also the relevant overview page: :doc:`/activity-standard/overview/budgets` 

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


.. _iati-activities/iati-activity/budget/value/.currency:

@currency
  The ISO 4217 alphabetic currency code of the value reported.
  This is required unless the iati-activity/\@default-currency is present and applies.


  This value must be of type xsd:string.


  This value must be on the :doc:`Currency codelist </codelists/Currency>`.



  
.. _iati-activities/iati-activity/budget/value/.value-date:

@value-date
  The date to be used for determining the exchange rate for
  currency conversions.


  This value must be of type xsd:date.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``value`` of ``budget`` for an ``iati-activity``.

| An example date is declared in the ``@value-date`` attribute.
| This example date format conform to the *xsd:date* standard - for most cases *YYYY-MM-DD* is sufficient.

| This example declares a *Currency* code *EUR*, using the ``@currency`` attribute.
| Note: A *Currency* code should only be declared if different to ``@default-currency`` in the ``iati-activity`` element.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--budget starts-->
	:end-before: <!--budget ends-->


Changelog
~~~~~~~~~

1.03
^^^^
Values are now allowed to be declared as decimals instead of integers.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2024>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/budget/value.rst>`_

