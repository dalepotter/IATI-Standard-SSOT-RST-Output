forecast
========

``iati-activities/iati-activity/fss/forecast``

This is the reference page for the XML element ``forecast``. See also the relevant overview page: :doc:`/activity-standard/overview/crs-fss` 

.. index::
  single: forecast

Definition
~~~~~~~~~~


A container to hold separate forecasts for each of the years specified Text() holds the forecast value for each year.


Rules
~~~~~

The text in this element must be of type xsd:decimal.








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/fss/forecast/.year:

@year
  The calendar year that the forward spend covers

  This attribute is required.



  This value must be of type xsd:decimal.



  
.. _iati-activities/iati-activity/fss/forecast/.currency:

@currency
  The ISO 4217 alphabetic currency code of the value reported.
  This is required unless the iati-activity/\@default-currency is present and applies.


  This value must be of type xsd:string.


  This value must be on the :doc:`Currency codelist </codelists/Currency>`.



  
.. _iati-activities/iati-activity/fss/forecast/.value-date:

@value-date
  The date to be used for determining the exchange rate for
  currency conversions.


  This value must be of type xsd:date.



  



Example Usage
~~~~~~~~~~~~~
Example of ``forecast`` for the ``fss`` of an ``iati-activity``.

| An example date is declared in the ``@value-date`` attribute.
| This example date format conform to the *xsd:date* standard - for most cases *YYYY-MM-DD* is sufficient.

| This example declares the attribute ``@year`` as *2014*.

| This example declares a *Currency* code *GBP*, using the ``@currency`` attribute.
| Note: A *Currency* code should only be declared if different to ``@default-currency`` in the ``iati-activity`` element.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--fss starts-->
	:end-before: <!--fss ends-->

| Note: multiple forecasts are expressed by repeating the ``forecast`` element.

Changelog
~~~~~~~~~

1.03
^^^^
| New in 1.03
| Added the optional ``fss`` element and its child elements


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2413>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/fss/forecast.rst>`_

