iati-activity
=============

``iati-activities/iati-activity``

This is the reference page for the XML element ``iati-activity``. 

.. index::
  single: iati-activity

Definition
~~~~~~~~~~


Top-level element for a single IATI activity report.


Rules
~~~~~








This element must occur at least once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/.last-updated-datetime:

@last-updated-datetime
  The last date/time that the data for this specific
  activity was updated.  This date must change whenever the
  value of any field changes.


  This value must be of type xsd:dateTime.



  
.. _iati-activities/iati-activity/.xml:lang:

@xml:lang
  A code specifying the default language of text in this activity. It is recommended that wherever possible only codes from ISO 639-1 are used.

  This value must be on the :doc:`Language codelist </codelists/Language>`.



  
.. _iati-activities/iati-activity/.default-currency:

@default-currency
  Default ISO 4217 alphabetic currency code for all
  financial values in this activity report. If this is not
  declared then the currency attribute MUST be specified for
  all monetary values.


  This value must be of type xsd:string.


  This value must be on the :doc:`Currency codelist </codelists/Currency>`.



  
.. _iati-activities/iati-activity/.humanitarian:

@humanitarian
  A process flag to indicate that this activity relates entirely
  or partially to humanitarian aid.


  This value must be of type xsd:boolean.



  
.. _iati-activities/iati-activity/.hierarchy:

@hierarchy
  The hierarchical level within the reporting organisation's
  subdivision of its units of aid. (eg activity = 1;
  sub-activity = 2; sub-sub-activity = 3). If hierarchy is
  not reported then 1 is assumed. If multiple levels are
  reported then, to avoid double counting, financial
  transactions should only be reported at the lowest
  hierarchical level.


  This value must be of type xsd:int.



  
.. _iati-activities/iati-activity/.linked-data-uri:

@linked-data-uri
  A Linked Data URI for a given activity (overrides
  iati-activities/\@linked-data-default if set)


  This value must be of type xsd:anyURI.



  
.. _iati-activities/iati-activity/.budget-not-provided:

@budget-not-provided
  A code indicating the reason why this activity does not contain any iati-activity/budget elements. The value must exist in the BudgetNotProvided codelist.


  This value must be of type xsd:string.


  This value must be on the :doc:`BudgetNotProvided codelist </codelists/BudgetNotProvided>`.



  



Example Usage
~~~~~~~~~~~~~
Example of ``iati-activity``.

| This element is a parent for other child elements.

| This example provides a dateTime of *2014-09-10T07:15:37Z*  for the ``@last-updated-datetime`` attribute.
| A dateTime in UTC time is indicated by adding a *Z* behind the time
| This example date time format conforms to the *xsd:dateTime* standard.

| The ``@xml:lang`` attribute declares a valid code (*en*) from the *Language* codelist.
| The ``@default-currency`` attribute declares a valid code (*USD*) from the *Currency* codelist.

| The optional ``@humanitarian`` attribute is set as *1*
| The optional ``@hierarchy`` attribute is set as *1*
| The optional ``@linked-data-uri`` attribute is also included.
| The optional ``@budget-not-provided`` attribute is also included.

.. literalinclude:: ../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--iati-activity starts-->
	:end-before: <!--iati-identifier starts-->

The ``iati-activity`` element acts as a container for other sub-elements.  It is closed as follows:

.. literalinclude:: ../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--fss ends-->
	:end-before: <!--iati-activity ends-->

Changelog
~~~~~~~~~

2.03
^^^^
| The ``@budget-not-provided`` attribute was `added <https://discuss.iatistandard.org/t/add-budget-exempt-attribute-and-codelist-included-2-03/845>`__.

2.02
^^^^
| The ``@humanitarian`` attribute was `added <http://support.iatistandard.org/entries/106937796-Humanitarian-Flag>`__.

2.01
^^^^
| The ``@version`` attribute was `removed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#iati-activity-removed-attribute>`__.

1.02
^^^^
| Introduced the ``@linked-data-uri`` attribute on iati-activity element


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L83>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   iati-activity/iati-identifier
   iati-activity/reporting-org
   iati-activity/title
   iati-activity/description
   iati-activity/participating-org
   iati-activity/other-identifier
   iati-activity/activity-status
   iati-activity/activity-date
   iati-activity/contact-info
   iati-activity/activity-scope
   iati-activity/recipient-country
   iati-activity/recipient-region
   iati-activity/location
   iati-activity/sector
   iati-activity/tag
   iati-activity/country-budget-items
   iati-activity/humanitarian-scope
   iati-activity/policy-marker
   iati-activity/collaboration-type
   iati-activity/default-flow-type
   iati-activity/default-finance-type
   iati-activity/default-aid-type
   iati-activity/default-tied-status
   iati-activity/budget
   iati-activity/planned-disbursement
   iati-activity/capital-spend
   iati-activity/transaction
   iati-activity/document-link
   iati-activity/related-activity
   iati-activity/legacy-data
   iati-activity/conditions
   iati-activity/result
   iati-activity/crs-add
   iati-activity/fss

