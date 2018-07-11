iati-organisation
=================

``iati-organisations/iati-organisation``

This is the reference page for the XML element ``iati-organisation``. 

.. index::
  single: iati-organisation

Definition
~~~~~~~~~~


Top-level element for a single IATI organisation report.


Rules
~~~~~








This element must occur at least once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/.last-updated-datetime:

@last-updated-datetime
  The last date/time that the data for this specific
  organisation was updated.  This date must change whenever
  the value of any field changes.


  This value must be of type xsd:dateTime.



  
.. _iati-organisations/iati-organisation/.xml:lang:

@xml:lang
  A code specifying the default language of text in this organisation. It is recommended that wherever possible only codes from ISO 639-1 are used.

  This value must be on the :doc:`Language codelist </codelists/Language>`.



  
.. _iati-organisations/iati-organisation/.default-currency:

@default-currency
  Default ISO 4217 currency code for all financial values in
  this activity report. If this is not declared then the
  currency attribute MUST be specified for all monetary
  values.


  This value must be of type xsd:string.


  This value must be on the :doc:`Currency codelist </codelists/Currency>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L62>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/organisation-standard/iati-organisations/iati-organisation.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   iati-organisation/organisation-identifier
   iati-organisation/name
   iati-organisation/reporting-org
   iati-organisation/total-budget
   iati-organisation/recipient-org-budget
   iati-organisation/recipient-region-budget
   iati-organisation/recipient-country-budget
   iati-organisation/total-expenditure
   iati-organisation/document-link

