recipient-country
=================

``iati-activities/iati-activity/transaction/recipient-country``

This is the reference page for the XML element ``recipient-country``. 

.. index::
  single: recipient-country

Definition
~~~~~~~~~~


A country that will benefit from this transaction.
If a specific country is not known the recipient-region element should be used instead.

If transaction/recipient-country AND/OR transaction/recipient-region are used THEN ALL transaction elements MUST contain a recipient-country or recipient-region element AND (iati-activity/recipient-country AND iati-activity/recipient-region MUST NOT be used)


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/recipient-country/.code:

@code
  ISO 3166-1 alpha-2 code for the country.

  This attribute is required.



  This value must be of type xsd:string.


  This value should be on the :doc:`Country codelist </codelists/Country>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1173>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/transaction/recipient-country.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   recipient-country/narrative

