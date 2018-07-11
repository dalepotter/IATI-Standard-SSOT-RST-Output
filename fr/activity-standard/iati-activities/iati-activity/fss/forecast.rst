forecast
========

``iati-activities/iati-activity/fss/forecast``

This is the reference page for the XML element ``forecast``. 

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



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2413>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/fss/forecast.rst>`_

