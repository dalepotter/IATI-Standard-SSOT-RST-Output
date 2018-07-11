loan-status
===========

``iati-activities/iati-activity/crs-add/loan-status``

This is the reference page for the XML element ``loan-status``. See also the relevant overview page: :doc:`/activity-standard/overview/crs-fss` 

.. index::
  single: loan-status

Definition
~~~~~~~~~~


The status of loan and interest repayments for the most recently reported financial year


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/crs-add/loan-status/.year:

@year
  CRS Reporting Year (CRS++ Column 1)

  This attribute is required.



  This value must be of type xsd:decimal.



  
.. _iati-activities/iati-activity/crs-add/loan-status/.currency:

@currency
  The ISO 4217 alphabetic currency code of the value reported.
  This is required unless the iati-activity/\@default-currency is present and applies.


  This value must be of type xsd:string.


  This value must be on the :doc:`Currency codelist </codelists/Currency>`.



  
.. _iati-activities/iati-activity/crs-add/loan-status/.value-date:

@value-date
  The date to be used for determining the exchange rate for
  currency conversions.


  This value must be of type xsd:date.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``loan-status`` in context of ``crs-add`` element.

| This element is a parent for other child elements.

| This example declares the attribute ``@year`` as *2014*.

| An example date is declared in the ``@iso-date`` attribute.
| This example date format conform to the *xsd:date* standard - for most cases *YYYY-MM-DD* is sufficient.

| This example declares a *Currency* code *GBP*, using the ``@currency`` attribute.
| Note: A ``Currency`` code should only be declared if different to ``@default-currency`` in the ``iati-activity`` element.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--crs-add starts-->
	:end-before: <!--crs-add ends-->


Changelog
~~~~~~~~~

1.03
^^^^
| New in 1.03
| Added the optional ``crs-add`` element and its child elements


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2342>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/crs-add/loan-status.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   loan-status/interest-received
   loan-status/principal-outstanding
   loan-status/principal-arrears
   loan-status/interest-arrears

