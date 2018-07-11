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



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L83>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity.rst>`_


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

